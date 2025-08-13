# Setup Instructions

## Step 1: Connecting the Rayban Meta glasses

Connect the Rayban Meta glasses to your smartphone through the MetaAI App.

## Step 2: Setup WhatsApp Video Call

On Your Smartphone:

1. Open WhatsApp on your phone

2. Start a video call to a contact who has WhatsApp Desktop

3. Keep the call active throughout the detection session

## Step 3: Install Dependencies

1. For object detection: 

```
pip install ultralytics opencv-python mss pyttsx3 numpy torch
```

2. For Scene Analysis/OCR Script

```
pip install torch transformers opencv-python pillow openai pyttsx3 numpy
```

Step 4: Configure the Scripts

1. Object Detection Configuration:

In YOLO_Guide.py

```
monitor = {
    "top": 0,           # Adjust to cover WhatsApp video window
    "left": 960,        # Adjust horizontal position  
    "width": 960,       # Adjust width to match video window
    "height": 1080      # Adjust height to match video window
}
```

2. Scene Analysis Configuration:

In Scene_Analysis.py

```
API_KEY = "sk-your-openai-api-key-here"  # Replace with your OpenAI API key
CAPTURE_INTERVAL = 5  # Seconds between scene analyses
```

## Step 5: Position Your Setup

1. WhatsApp video call window should show the smartphone camera feed

2. Adjust screen capture area in the object detection script to cover the video window

## Controls:

1. for object detection script:

Q - Quit the application

S - Save current frame with detections

Ctrl+C - Emergency stop

2. for scene analysis script: 

Ctrl+C: Stop the analyzer

Check scene_analyzer.log for detailed logs

Adjust CAPTURE_INTERVAL for different timing
