
# Gesture Controller

The Gesture Controller is a Python-based project that uses a webcam to capture hand gestures and perform various system control actions such as adjusting volume, brightness, scrolling, and mouse control. It leverages OpenCV for video capture, MediaPipe for hand tracking, and PyAutoGUI for automating GUI interactions.

## Features

- **Gesture Recognition**: Detects various hand gestures and maps them to specific actions.
- **System Control**: Adjust system brightness and volume, scroll horizontally and vertically, and control the mouse cursor.
- **Pinch Gestures**: Supports pinch gestures for finer control over system settings.

## Requirements

- Python 3.x
- OpenCV
- MediaPipe
- PyAutoGUI
- PyCaw
- Screen Brightness Control

## Installation

1. Clone the repository:
    ```bash
    git clone https://github.com/your-repo/gesture-controller.git
    cd gesture-controller
    ```

2. Install the required packages:
    ```bash
    pip install opencv-python mediapipe pyautogui comtypes screen-brightness-control
    ```

3. For volume control, you need to install `pycaw`:
    ```bash
    pip install pycaw
    ```

## Usage

Run the `gesture_controller.py` script to start the gesture controller.

```bash
python gesture_controller.py
```

## Gesture Mappings

- **FIST**: Click and drag.
- **V_GEST**: Move the mouse cursor.
- **MID**: Left-click.
- **INDEX**: Right-click.
- **TWO_FINGER_CLOSED**: Double-click.
- **PINCH_MAJOR**: Control system brightness (horizontal) or volume (vertical).
- **PINCH_MINOR**: Scroll horizontally or vertically.

## Code Overview

### Gesture Encodings

The `Gest` class enumerates the various gestures using binary encoding.

### Multi-handedness Labels

The `HLabel` class enumerates the hand labels for major and minor hands.

### HandRecog Class

The `HandRecog` class processes the hand landmarks provided by MediaPipe and converts them into recognizable gestures.

### Controller Class

The `Controller` class executes commands based on detected gestures.

### GestureController Class

The `GestureController` class handles video capture, processes frames to detect hand landmarks using MediaPipe, and manages the overall gesture control logic.

## License

This project is licensed under the MIT License.
