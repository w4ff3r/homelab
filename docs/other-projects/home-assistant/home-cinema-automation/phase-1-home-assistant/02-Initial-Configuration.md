## Objective

Configure Home Assistant after the first boot and establish the foundation required for future automation and dashboard development.

---

## Setup Wizard

After accessing:

http://homeassistant.local:8123

complete the onboarding wizard.

---

## Administrator Account

(For documentation purposes; I used personal login details)

Create:

### Username

administrator

### Password

```html
<Secure Password>
```

---

## Home Location

Configure the home location.

This enables:

- Sunrise and sunset calculations
- Weather services
- Location-based automations
- Presence detection

---

## Time Zone

Configure:

Australia/Brisbane

---

## Units

Metric

Temperature:

Celsius

Distance:

Kilometres

Time:

24-hour

---

## Automatic Discovery

Home Assistant scans the local network for supported devices and services.

Detected devices may include:

- Smart TVs
- Streaming devices
- Network equipment
- Media servers
- Mobile devices

These integrations can be ignored during initial setup and configured later.

---

## Areas

Create logical areas for devices.

Planned areas:

### Hallway

Contains:

- Vertical display
- Hallway dashboard

---

### Cinema Room

Contains:

- Samsung Frame TV
- Bose speakers
- Future smart lighting

---

### Kitchen

Contains:

- Tablet dashboard

---

### Office

Contains:

- Tablet dashboard

---

### Living Room

Reserved for future expansion.

---

## Naming Convention

Entity names should follow a consistent structure.

Examples:

hallway_display

cinema_tv

cinema_speakers

kitchen_tablet

office_tablet

movie_night_button

---

## Project Goals

### Family Mode

Default display mode.

Features:

- Family photographs
- Clock
- Weather
- Date

---

### Cinema Mode

Activated during movie sessions.

Features:

- Movie poster
- Title
- Runtime
- Rating
- Genre
- "Now Showing" banner

---

### Movie Night Automation

Future automation sequence:

1. Turn on Samsung Frame TV.
2. Open Plex.
3. Turn on Bose speakers.
4. Switch hallway display into cinema mode.
5. Dim lights (future).

---

## Future Integrations

### Plex

Primary media source.

---

### Samsung TV

Playback control.

---

### Bose Speakers

Audio control.

---

### Smart Lighting

Future enhancement.

---

### Touchscreen Support

Future enhancement.

---

## Completion Criteria

Phase 1 is complete when:

- Home Assistant VM is operational.
- Administrator account has been created.
- Location and units are configured.
- Areas have been defined.
- Home Assistant is reachable from the network.

---

## Next Phase

Phase 2:

Plex Integration