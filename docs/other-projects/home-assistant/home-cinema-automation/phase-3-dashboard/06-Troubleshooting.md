## Plex Metadata Unavailable

### Problem

Movie metadata disappeared when Plex playback stopped.

---

### Explanation

The Plex playback entity changes to an `unavailable` state when no media is actively playing. As a result, attributes such as title, poster, runtime and synopsis are removed.

---

### Solution

Dashboard logic will detect unavailable states and transition to the Cinema Idle or Family Screensaver view instead of attempting to display missing metadata.

---

### Justification

Separating active playback from idle dashboard states improves reliability and provides a better user experience.

---

