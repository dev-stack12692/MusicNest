# On-Device Heuristic ML & Recommendation Engine

The queue system, Home page categorization, and song recommendations are handled by a highly optimized, dual-layer on-device heuristic machine learning and ranking model.

Instead of relying on heavy cloud servers that slow down the app, listening taste is analyzed locally on the device in real time.

---

## Architecture Overview

```
                      User Interactions
        (Likes, Plays, Skips, Search Clicks, Playlist Adds)
                               |
                               v
                +-------------------------------+
                |       MusicTasteEngine        |
                |  * Interaction Scoring        |
                |  * Vibe Cluster Mapping       |
                |  * Circadian / Context Rules  |
                +---------------+---------------+
                               |
                               v
                +-------------------------------+
                |   Recommendation Heuristics   |
                |  * Epsilon-Greedy Perturbation|
                |  * Track Fatigue Decay        |
                |  * Artist Cooling Multipliers |
                +---------------+---------------+
                               |
        +----------------------+----------------------+
        |                                             |
        v                                             v
+-------------------------------+   +-------------------------------+
|       MusicNestAIEngine       |   |      InbuiltHomeAIEngine      |
|  * Dynamic Auto Flow Queue    |   |  * Greedy Shelf Allocation    |
|  * Seed Trajectory Matching   |   |  * 100% Unique Home Feeds     |
+-------------------------------+   +-------------------------------+
```

---

## 1. Multi-Dimensional Taste Scoring Model (`MusicTasteEngine`)

At the core is an on-device preference ranking algorithm. It behaves similarly to a Linear Regression / Multi-Factor Collaborative Filter scoring model, tracking user interactions across several behavioral dimensions.

### Interaction Weight Matrix

* **Positive Reinforcement Signals:**
  * `+18.0f` * Explicit Like (very strong preference)
  * `+15.0f` * Manual Playlist Addition (high-intent preference)
  * `+4.0f`  * Standard Play Completion (passive retention per stream)
  * `+2.5f`  * Search Click / Scribe (active exploratory interest)

* **Negative Reinforcement Signals:**
  * `-5.5f`  * Early Skip (penalizes artists and genres actively skipped)

| Event Type | Trigger Action | Weight Score | Algorithmic Impact |
| :--- | :--- | :--- | :--- |
| `LIKE` | User likes a track | `+18.0f` | Primary positive signal for artist and genre affinities |
| `PLAYLIST_ADD` | Added to a personal playlist | `+15.0f` | Strong curatorial intent; boosts associated sub-genres |
| `COMPLETION` | Full track play completed | `+4.0f` | Incremental preference growth |
| `SEARCH_CLICK` | Track selected directly from search | `+2.5f` | Signals active curiosity and direct intent |
| `EARLY_SKIP` | Skipped within initial playback window | `-5.5f` | Applies negative score across genre and artist vector |

### Habit and Context Alignment

* **Vibe Affinity:** Learns which of the 9 custom vibe clusters are interacted with most:
  * `Lofi Chill`
  * `Sad Heartbreak`
  * `Desi Hip-Hop`
  * `Romance`
  * `Acoustic Unwind`
  * `Workout Energy`
  * `Electronic Synth`
  * `Indie Pop`
  * `Deep Focus`
* **Time-of-Day Alignment:** Tracks morning versus night listening habits (for example, boosting Acoustic and Focus tracks during daytime working hours).

---

## 2. Industry-Standard Recommendation Heuristics

To match the behavior of professional streaming services like Spotify, the model implements advanced heuristic rules.

### Epsilon-Greedy Serendipity (Exploration vs. Exploitation)

To prevent the algorithm from falling into a "local optimum" (the filter bubble), the model introduces controlled serendipity by injecting a calibrated noise factor into track ranking scores:

```text
Score_Adjustment = (Math.random() - 0.5) * 0.8f
```

* **Exploitation:** Recommends high-confidence songs matching proven historical tastes.
* **Exploration:** Elevates less-traveled tracks to surface fresh, serendipitous music.

### Anti-Fatigue Cooling Penalties

* **Song Fatigue Cooling Penalty (Diversification):**
  * Penalizes recently played songs: `-60.0f` for the absolute last track played.
  * Gradually scales down to `-5.0f` across the last 30 songs.
  * Prevents songs from re-appearing in continuous playback loops.
* **Artist Fatigue Cooling Penalty:**
  * Applies an immediate `-20.0f` penalty to other songs by the same artist just listened to.
  * Ensures variety and smooth artist transitions in the queue.

---

## 3. Dynamic Queue Generation (`MusicNestAIEngine`)

Whenever a song is played, the queue system avoids static lists and dynamically constructs an **Auto Flow Queue**:

* **Seed Analysis:** Evaluates the seed song's genre, artist, and album/movie tags.
* **Catalog Sourcing:** Queries both the local persistent database and similar online catalog streams.
* **Scoring & Deduplication:** Passes all candidate tracks through the Taste Model and strips out duplicates and fatigued items.
* **Trajectory Alignment:** Builds an intelligent, context-aware play queue tailored to the active listening session.

---

## 4. Globally Unique Home Page Categories (`InbuiltHomeAIEngine`)

Home screen categories (such as *Inspired by Your Top Artists*, *Your Soulful Romance Mix*, or *Acoustic Unwind*) adapt on a daily schedule:

* Every track in the local catalog pool is evaluated by the ML Taste Model.
* The engine filters tracks matching each specific category vibe and sorts them by preference score.
* The engine runs a **Greedy Single-Allocation Algorithm**:
  * A track assigned to one shelf cannot appear on any other shelf on the Home page.
  * Result: Guarantees **100% unique, non-overlapping rows** across the entire Home feed every single day.
