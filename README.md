# RENE's Real-Time Object Detection Studio

Hey there! Welcome to my real-time object detection project. This app uses your webcam to spot and track things live on screen. 

Built with:
- Streamlit for the user interface
- YOLOv8 for the smart object detection
- OpenCV & streamlit-webrtc to handle the live camera feed

## What it does
- Live Detection: Spots objects in real-time right from your webcam.
- Smart Tracking: Keeps an eye on things frame by frame.
- Custom Alerts: Pick specific objects (like a person or cell phone) and get alerted when they show up.
- Auto & Manual Snaps: Save pictures of the detections automatically or with the click of a button.
- Modern UI: I gave it a massive glow-up with a sleek, modern girly theme.

## How to set it up

Just want to run it locally? It's super easy.

1. Set up a virtual environment:
```powershell
python -m venv .venv
.venv\Scripts\Activate.ps1
```

2. Install the dependencies:
```powershell
pip install -r requirements.txt
```

## How to run it

Type this into your terminal:
```powershell
streamlit run app.py
```
Then, open `http://localhost:8501` in your browser. Make sure to allow camera permissions when it asks!

## How to use the studio
1. Start the stream: Click start and let the camera run.
2. Tweak settings: Play around with the confidence sliders if you want it to be more or less strict.
3. Set alerts: Tell the app what to look for, and it will let you know when it finds it.
4. Save memories: Hit the save button to keep any cool annotated frames, or let it auto-save during alerts.
5. Get the stats: Download your session summary CSV when you are done.

All your saved pictures will automatically go into the `captures/` folder!
