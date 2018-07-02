# MadJacks2

## Act 1 (Ext)

### Detect Gun -> Close Door

- Consume camera feed from RTSP streams
- Apply motion detection
- If motion, then
  - Produce event to Gun image recognition

- Consume Gun image recognition events
- Apply Gun detection
- If gun detection threshold met, then
  - Produce event for recognized Gun In Image

- Consume recognized Gun In Image event
- Apply gun chronology verification of subsequent events (avoid false positives)
- If gun has been around for N image motion frames, then
  - Produce event for Close Door

- Consume Close Door event
- Check door state
- If door isn't already closed, or in the process of opening, push the button to close the door.

## Act 2 (Int)

### Detect Gun -> Dazzle with Lights

- Consume recognized Gun In Image event
- Apply gun chronology verification of subsequent events (avoid false positives)
- If gun has been around for N image motion frames, then
  - Produce event for Dazzle with Lights

- Consume Dazzle with Lights
- Check lights state
- If lights are not already dazzling, dazzle the attacker with lights.

## Act 3 (Sneak)

### Detect face -> Follow bad guy

- Consume recognized Gun In Image event
- Apply gun chronology verification of subsequent events (avoid false positives)
- If gun has been around for N image motion frames, then
  - Identify and process faces from motion stream nearest to Gun position
  - Train Memory Augmented Neural Net (MANN) with attacker's face
  - Send to quadcopter to hunt and orbit

