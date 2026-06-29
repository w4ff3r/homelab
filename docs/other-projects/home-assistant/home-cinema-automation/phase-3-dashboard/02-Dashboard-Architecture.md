## Display Flow

```text
Family Screensaver
        │
        ▼
Touch Screen
        │
        ▼
Home Dashboard
        │
 ┌──────┴──────┐
 ▼             ▼
Calendar   Movie Night
                │
                ▼
         Cinema Idle
                │
                ▼
          Now Showing
```

---

## Data Sources

| Source | Purpose |
|----------|---------|
| Plex | Movie metadata |
| Home Assistant | Dashboard logic |
| Weather | Current conditions |
| Calendar | Family events |
| Shopping List | Shared household lists |

---

## Primary Plex Entity

```
media_player.plex_client_service_plex_plex_web_opera_windows
```

The Plex media player entity provides all metadata required for the Now Showing dashboard.