# Virtual Keyboard

A hand gesture-controlled virtual keyboard using OpenCV and MediaPipe. Type by pinching your thumb and index finger together over the keys displayed on your screen.

## Features

- 🎯 **Hand Gesture Detection**: Uses MediaPipe for accurate hand tracking
- ⌨️ **Virtual Keyboard Interface**: Beautiful on-screen keyboard with hover and click effects
- 📝 **Text Input**: Type text by pinching over keys
- 🎨 **Modern UI**: Clean, colorful interface with visual feedback
- 🔄 **Special Keys**: Space, Backspace, and Clear functionality

## Requirements

- Python 3.8 - 3.11 (MediaPipe compatibility)
- Webcam
- Required Python packages (see Installation)

## Installation

1. Clone this repository:
```bash
git clone https://github.com/Anil-glith/Virtual-Keyboard.git
cd Virtual-Keyboard
```

2. Install the required dependencies:
```bash
pip install opencv-python cvzone numpy pynput mediapipe
```

**Note**: If you're using Python 3.13, you'll need to use Python 3.11 or earlier for MediaPipe compatibility. You can use:
```bash
py -3.11 -m pip install opencv-python cvzone numpy pynput mediapipe
```

## Usage

Run the application:
```bash
python main.py
```

Or if using Python 3.11:
```bash
py -3.11 main.py
```

### How to Use

1. **Start the application**: The virtual keyboard will appear on your screen
2. **Position your hand**: Make sure your hand is visible to the webcam
3. **Hover over keys**: Move your index finger over the keys you want to type
4. **Pinch to type**: Pinch your thumb and index finger together (distance < 40 pixels) to press a key
5. **View your text**: The typed text appears in the text field at the bottom
6. **Quit**: Press 'q' key to exit the application

### Keyboard Layout

- **Row 1**: Q, W, E, R, T, Y, U, I, O, P
- **Row 2**: A, S, D, F, G, H, J, K, L, ;
- **Row 3**: Z, X, C, V, B, N, M, ,, ., /
- **Row 4**: SPACE, BACKSPACE, CLEAR

## Controls

- **Pinch Gesture**: Bring thumb and index finger together to click a key
- **'q' Key**: Quit the application
- **SPACE**: Add a space to your text
- **BACKSPACE**: Delete the last character
- **CLEAR**: Clear all text

## Technical Details

- **Hand Detection**: MediaPipe Hand Tracking with 0.8 detection confidence
- **Click Detection**: Distance-based pinch detection (threshold: 40 pixels)
- **Cooldown**: 0.5 seconds between clicks to prevent accidental multiple presses
- **Resolution**: 1280x720 webcam feed
- **FPS Display**: Shows frames per second in the bottom right corner

## Dependencies

- `opencv-python`: Computer vision library
- `cvzone`: Simplified OpenCV wrapper
- `numpy`: Numerical computing
- `pynput`: Keyboard control
- `mediapipe`: Hand tracking and gesture recognition

## Troubleshooting

- **No hand detected**: Ensure good lighting and your hand is fully visible
- **MediaPipe not found**: Make sure you're using Python 3.8-3.11
- **Webcam not working**: Check if your webcam is connected and not being used by another application

## License

This project is open source and available for educational purposes.

## Author

Anil-glith

## Contributing

Contributions, issues, and feature requests are welcome!

