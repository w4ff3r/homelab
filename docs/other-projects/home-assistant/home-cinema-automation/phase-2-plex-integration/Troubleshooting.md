## Plex Client Discovery

### Problem

Media player entities were not immediately available after integrating Plex.

### Explanation

Plex clients are only discovered when active playback sessions exist.

### Solution

Initiated playback and used the "Scan Clients" action to discover active Plex clients.

### Justification

Playback entities expose metadata required for the Cinema Mode dashboard, including title, runtime, synopsis and poster artwork.