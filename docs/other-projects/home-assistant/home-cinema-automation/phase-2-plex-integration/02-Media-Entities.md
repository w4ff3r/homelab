## Objective

Identify the entities required for the Cinema Mode dashboard.

---

## Library Sensors

### Movies Library

Entity:

sensor.library_hard_drive_movies

Purpose:

Provides movie library statistics.

---

### TV Shows Library

Entity:

sensor.library_hard_drive_tv_shows

Purpose:

Provides television library statistics.

---

### Plex Activity

Entity:

sensor.prestonplexserver

Purpose:

Reports the number of active viewers.

---

## Primary Playback Entity

Entity:

media_player.plex_client_service_plex_plex_web_opera_windows

State:

playing

Purpose:

Provides metadata for the currently playing movie.

---

## Key Attributes

|Attribute|Purpose|
|---|---|
|media_title|Movie title|
|media_duration|Runtime|
|media_content_rating|Classification|
|media_summary|Synopsis|
|entity_picture|Poster artwork|
|media_library_title|Source library|

---

## Selected Entity

The Plex Web client entity was selected as the primary metadata source for the Cinema Mode dashboard because it exposes all information required for the "Now Showing" display.

---
## Playback State Behaviour

The Plex playback entity retains metadata while media is playing or paused.

When playback is stopped, the entity changes to:

```
unavailable
```

That means Phase 3 needs two display states:

```text
Active Movie State
→ show poster, title, runtime, rating, synopsis

Cinema Idle State
→ show favourite movies, family photos, or "Ready for Movie Night"