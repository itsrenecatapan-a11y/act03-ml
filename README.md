# Activity: Python Streamlit + ML Model (RENE)

## Project Overview
This is **RENE's** real-time computer vision activity project using:
- Streamlit
- streamlit-webrtc
- Ultralytics YOLOv8
- OpenCV

The app detects and tracks objects from a webcam stream, shows live metrics, sends target-object alerts, and saves annotated frames.

## Fixed Model Configuration
This project is intentionally locked to **`yolov8n.pt` only**.

Reason:
- `yolov8n.pt` is the fastest YOLOv8 variant in this project.
- It is suitable for smoother realtime performance on typical student/laptop hardware.

## Main Features
- Real-time object detection with YOLOv8 (`yolov8n.pt`)
- Lightweight multi-frame object tracking
- Adjustable confidence, IoU, and inference size
- Processing interval control (`Infer Every N Frames`) for smoother performance
- Target-object alerting with cooldown and confidence threshold
- Auto-capture on alert and manual frame capture
- Live runtime stats (FPS, processed frames, saved captures)
- Downloadable session summary CSV
- Snapshot fallback mode when WebRTC is unavailable
- Recent captures gallery inside the app

## UI Improvements
- Fully redesigned dashboard and sidebar controls
- RENE-branded header and visual theme
- Cleaner metrics panel and status chips
- Faster access to common actions (reset stats, quick save)

## Folder Structure
```text
PythonStreamlit+MLModel - RENE/
|- app.py
|- README.md
|- requirements.txt
|- packages.txt
|- runtime.txt
|- yolov8n.pt
|- yolov8s.pt
|- yolov8l.pt
`- captures/                  (generated at runtime)
```

## Requirements
- Python 3.10+
- Webcam-enabled browser
- OS: Windows / macOS / Linux

## Setup
```powershell
python -m venv .venv
.venv\Scripts\Activate.ps1
pip install -r requirements.txt
```

## Run
```powershell
streamlit run app.py
```
Open: `http://localhost:8501`

Allow camera permission in your browser when prompted.

## How to Use
1. Start the realtime stream.
2. Adjust detection thresholds and performance controls.
3. Select alert target objects and configure alert behavior.
4. Save frames manually or enable auto-save on alerts.
5. Export the session summary CSV when needed.

## Performance Note
The app uses only `yolov8n.pt` to prioritize speed and responsiveness for realtime class demonstrations.

## Output Artifacts
- Saved frames are written to `captures/`
- Session summary can be downloaded as `rene_session_summary.csv`


