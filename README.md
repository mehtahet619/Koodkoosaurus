# 🦕 Kudkoosaur the Jumping Dino

**Author:** Het Mehta

A revolutionary take on the classic Chrome Dinosaur game with **tongue detection controls**! Control your dinosaur by sticking your tongue out - detected in real-time using computer vision and machine learning.

## 🎮 Game Modes

### Single Player (`main.py`)
- Classic dinosaur runner with tongue controls
- Jump by sticking your tongue out
- Duck by keeping your tongue in
- Avoid cacti and birds to survive!

### Two Player (`main_2p.py`) 
- **Stacked lanes**: Player 1 (top) vs Player 2 (bottom)
- Simultaneous gameplay with dual webcam detection
- Round ends when either player dies
- Winner overlay shows the champion

### Flappy Bird Mode (`main2.py`)
- Tongue-controlled Flappy Bird variant
- Stick tongue out to flap and stay airborne
- Navigate through pipes

## 🚀 Features

- **Real-time Tongue Detection**: Uses MediaPipe and OpenCV for accurate facial landmark detection
- **Webcam Integration**: Live video feed with tongue detection overlay
- **Multiple Game Modes**: Classic runner, 2-player competitive, and Flappy Bird
- **Retro Pixel Art**: Authentic Chrome Dino aesthetic with custom sprites
- **Dual Control Support**: Fallback keyboard controls (Space/Up/Down for P1, W/S for P2)

## 🛠️ Installations:

### Prerequisites
- Python 3.7+
- Webcam (for tongue detection)

### Setup
1. Clone this repository:
   ```bash
   https://github.com/mehtahet619/Koodkoosaurus.git
   cd jumping-dino
   ```

2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

3. Run the game:
   ```bash
   # Single player
   python main.py
   
   # Two player
   python main_2p.py
   
   # Flappy Bird mode
   python main2.py
   ```

## 📋 Requirements

```
pygame==2.5.2
opencv-python==4.9.0.80
mediapipe==0.10.14
```

## 🎯 Controls

### Tongue Controls (Primary)
- **Tongue Out**: Jump/Flap
- **Tongue In**: Duck/Fall
- **Hold Tongue (5s)**: Reset game on game over

### Keyboard Fallback
#### Single Player
- `Space` or `↑`: Jump
- `↓`: Duck

#### Two Player
- **Player 1 (Top Lane)**: `Space`/`↑` jump, `↓` duck
- **Player 2 (Bottom Lane)**: `W` jump, `S` duck

## 🧠 How It Works

The tongue detection system uses:
1. **MediaPipe Face Mesh**: Detects 468 facial landmarks in real-time
2. **Lip Landmark Analysis**: Monitors specific inner-lip ring landmarks
3. **Mouth Opening Detection**: Calculates mouth aspect ratio to detect tongue protrusion
4. **Multi-Face Support**: Can track up to 2 faces simultaneously for 2-player mode

### Technical Details
- **Face Detection**: MediaPipe's ML model for robust face tracking
- **Landmark Processing**: Real-time analysis of lip/mouth geometry  
- **Calibration**: Automatic baseline establishment for tongue detection
- **Smoothing**: Temporal filtering to reduce false positives

## 📁 Project Structure

```
jumping-dino/
├── main.py              # Single player game
├── main_2p.py           # Two player game  
├── main2.py             # Flappy Bird mode
├── tongue_switch.py     # Single face tongue detection
├── tongue_switch_2p.py  # Multi-face tongue detection
├── requirements.txt     # Python dependencies
├── assets/             # Game sprites and images
│   ├── Dino/           # Dinosaur animations
│   ├── Cactus/         # Obstacle sprites
│   ├── Bird/           # Flying obstacle sprites
│   ├── Flap/           # Flappy Bird assets
│   └── Other/          # UI elements
└── README.md           # This file
```

## 🎨 Assets

All game sprites are included in the `assets/` directory:
- **Dinosaur**: Running, jumping, ducking, and death animations
- **Obstacles**: Various cacti sizes and bird sprites
- **Environment**: Ground track, clouds, and backgrounds
- **Flappy Bird**: Complete sprite set for bird mode

## 🐛 Troubleshooting

### Webcam Issues
- Ensure webcam permissions are granted
- Check if another application is using the camera
- Try different camera indices if multiple cameras are present

### Performance Issues
- Close other applications using the webcam
- Reduce window size if frame rate is low
- Ensure adequate lighting for face detection

### Tongue Detection Not Working
- Ensure good lighting conditions
- Position face clearly in webcam view
- Calibrate by keeping tongue in for a few seconds at start
- Mouth should be clearly visible to the camera

## 🤝 Contributing

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📄 License

This project is open source. Feel free to use, modify, and distribute as needed.

## 🙏 Acknowledgments

- **MediaPipe**: Google's ML framework for face detection
- **pygame**: Python game development library
- **Chrome Dino**: Inspiration for the original game mechanics
- **OpenCV**: Computer vision processing

---

**Made with 💖 by Het Mehta**

*Stick your tongue out and start playing!* 🦕👅
