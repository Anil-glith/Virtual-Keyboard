# 🖐️ Virtual Keyboard - Hand Gesture Typing

A real-time virtual keyboard application powered by computer vision and hand tracking. Type without touching your keyboard using intuitive hand gestures!

![Python](https://img.shields.io/badge/Python-3.7%2B-blue)
![OpenCV](https://img.shields.io/badge/OpenCV-4.x-green)
![License](https://img.shields.io/badge/License-MIT-yellow)

## ✨ Features

### Core Functionality
- **👋 Hand Tracking**: Real-time hand detection and tracking using MediaPipe
- **👆 Gesture Recognition**: Pinch gesture detection for key selection
- **⌨️ Virtual Typing**: Full QWERTY keyboard layout with special keys
- **📝 Live Text Display**: Real-time text output with scrolling capability
- **🎯 Hover Effects**: Visual feedback when hovering over keys
- **⏱️ Click Cooldown**: Prevents accidental double-clicks
- **🔤 Keyboard Output**: Types directly into any application

### Visual Features
- **🎨 Modern UI Design**: Sleek, transparent overlay design
- **💫 Smooth Animations**: Color transitions for key states (normal, hover, click)
- **📊 FPS Counter**: Real-time performance monitoring
- **🖼️ Custom Styling**: Professional color scheme with transparency effects
- **📱 Responsive Layout**: Optimized for 1280x720 resolution

### Special Keys
- **SPACE**: Add spaces between words
- **BACKSPACE**: Delete the last character
- **CLEAR**: Clear entire text field
- **Standard Keys**: Full A-Z alphabet and common punctuation

## 🚀 Installation

### Prerequisites
- Python 3.7 or higher
- Webcam
- Good lighting conditions

### Install Dependencies

```bash
# Install all required packages
pip install opencv-python cvzone mediapipe pynput numpy
```

Or use requirements.txt:

```bash
pip install -r requirements.txt
```

### Requirements.txt
```
opencv-python
cvzone
mediapipe
pynput
numpy
```

## 💻 Usage

### Running the Application

```bash
python virtual_keyboard.py
```

### Controls
1. **Show your hand** to the camera (palm facing forward)
2. **Point** with your index finger to hover over keys
3. **Pinch** (bring index finger and thumb together) to click/type
4. Press **'q'** on physical keyboard to quit

### Tips for Best Performance
- ✅ Ensure good lighting
- ✅ Keep hand within camera frame
- ✅ Maintain steady hand position
- ✅ Use clear pinch gestures
- ✅ Position yourself 1-2 feet from camera

## 🎯 How It Works

1. **Hand Detection**: Uses CVZone's HandTrackingModule (powered by MediaPipe) to detect hand landmarks
2. **Gesture Recognition**: Calculates distance between index finger tip and thumb tip
3. **Key Selection**: Tracks index finger position to determine key hover
4. **Click Detection**: Pinch gesture (distance < 40 pixels) triggers key press
5. **Output**: Sends keystrokes to active application using pynput

## ⚙️ Configuration

### Adjustable Parameters

```python
# Hand detection sensitivity
detectionCon=0.8  # Range: 0.0 to 1.0 (higher = more strict)

# Click threshold
l < 40  # Pinch distance in pixels

# Cooldown time
cooldownTime = 0.5  # Seconds between clicks

# Camera resolution
cap.set(3, 1280)  # Width
cap.set(4, 720)   # Height
```

### Color Customization

```python
KEY_COLOR = (102, 204, 204)         # Default key color
KEY_HOVER_COLOR = (41, 128, 185)    # Hover state color
KEY_CLICK_COLOR = (52, 152, 219)    # Click state color
TEXT_COLOR = (255, 255, 255)        # Text color
```

## 📋 System Requirements

- **OS**: Windows, macOS, or Linux
- **RAM**: 4GB minimum (8GB recommended)
- **Processor**: Intel i3 or equivalent
- **Camera**: Built-in or USB webcam (720p or higher)
- **Python**: 3.7+

## 🐛 Troubleshooting

### Camera Issues
```
Error: Camera not accessible
Solution: Close other apps using webcam, check camera permissions
```

### Hand Not Detected
```
Issue: Hand tracking not working
Solution: Improve lighting, ensure hand is clearly visible, adjust detectionCon value
```

### Import Errors
```
ModuleNotFoundError: No module named 'cvzone'
Solution: pip install cvzone mediapipe
```

### Performance Issues
```
Low FPS / Lag
Solution: Close other applications, reduce camera resolution, update graphics drivers
```

## 🔧 Technical Stack

- **OpenCV**: Video capture and image processing
- **CVZone**: Hand tracking wrapper for MediaPipe
- **MediaPipe**: Hand landmark detection
- **Pynput**: Keyboard control
- **NumPy**: Array operations

## 📝 Project Structure

```
virtual-keyboard/
│
├── virtual_keyboard.py    # Main application file
├── requirements.txt       # Python dependencies
└── README.md             # Project documentation
```

## 🎓 Use Cases

- **Accessibility**: Alternative input method for users with mobility challenges
- **Hygiene**: Touchless typing in public spaces
- **Education**: Learning tool for computer vision and gesture recognition
- **Presentations**: Interactive demonstrations
- **Gaming**: Novel input method for games

## 🤝 Contributing

Contributions are welcome! Feel free to:
- Report bugs
- Suggest new features
- Submit pull requests
- Improve documentation

## 📄 License

This project is open source and available under the MIT License.

## 👨‍💻 Author

Created with ❤️ using Python and Computer Vision

## 🙏 Acknowledgments

- **MediaPipe** by Google for hand tracking technology
- **CVZone** for simplified hand detection
- **OpenCV** community for computer vision tools

## 📞 Support

If you encounter any issues or have questions:
1. Check the Troubleshooting section
2. Review camera and lighting conditions
3. Ensure all dependencies are installed correctly

---

⭐ **Star this repository if you find it useful!**

🐛 **Report issues to help improve the project**

🔀 **Fork and create your own version**
