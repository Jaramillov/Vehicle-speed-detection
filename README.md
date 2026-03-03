# SLOW — Vehicle Speed Detection System

A real-time vehicle speed detection system using computer vision. It analyzes traffic footage, tracks vehicles across road zones, calculates their speed, and flags speeding infractions.

---

## How it works

The system divides the road into zones. When a vehicle crosses from one zone to the next, it measures the elapsed time and calculates speed. Vehicles exceeding 60 km/h are marked as violators and a screenshot is saved.

```
Video input → Background subtraction → Object tracking → Speed calculation → Report
```

---

## Files

| File | Description |
|------|-------------|
| `Main.py` | Main logic: video processing, zone detection, speed calculation |
| `Localizador_ob.py` | Tracks objects across frames by assigning persistent IDs |
| `Graph.py` | Tkinter window with a speed chart and data table |

---

## Requirements

- Python 3.8+
- OpenCV, NumPy, Matplotlib, pyscreenshot

---

## Usage

A window will open. Click **"Abrir video a detectar"**, select a video file, and the system will start processing it in real time.

---

## Configuration

You can adjust these values in `Main.py` to match your camera setup:

- **Road zones** — edit the `area_1`, `area_2`, `area_3` polygon coordinates
- **Speed limit** — change `60` in `if vel > 60`
- **Zone distance** — change `24.5` (meters) to match the real distance in your scene

---

