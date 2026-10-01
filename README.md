# Real-Time Hand Gesture Tracking 🖐️

A real-time hand-tracking web application built using **HTML, CSS, JavaScript, MediaPipe Hands, and HTML5 Canvas**. The project uses the webcam to detect and visualize hand movements directly in the browser.

The application detects **21 landmarks on each hand**, supports up to **two hands**, and dynamically draws glowing connections between the landmarks as the hands move, rotate, and change position.

## ✨ Features

* Real-time hand tracking using the webcam
* Detects 21 landmarks for each hand
* Supports tracking up to two hands simultaneously
* Draws the hand skeleton using connected landmarks
* Connects corresponding fingertips when both hands are detected
* Uses distance calculations for dynamic connection effects
* Includes a mirror effect for natural hand movement
* Runs completely on the client side

## 🛠️ Tech Stack

* **HTML & CSS** – Structure and interface
* **JavaScript** – Application logic and landmark processing
* **MediaPipe Hands** – Real-time hand landmark detection
* **HTML5 Canvas** – Drawing landmarks and connections
* **WebRTC / getUserMedia()** – Webcam access

## ⚙️ How It Works

The webcam is accessed using the browser's `getUserMedia()` API. The live video is passed to **MediaPipe Hands**, which detects the hand and returns 21 landmark coordinates for each detected hand.

The landmark coordinates are converted from MediaPipe's normalized coordinate system into canvas coordinates. The coordinates are then mirrored horizontally to make the interaction feel like a mirror.

JavaScript uses the processed coordinates to draw points and connect related landmarks on the HTML5 Canvas. Distance calculations between selected landmarks are also used to create dynamic visual effects as the fingers move closer or farther apart.

### Processing Flow

```text
Webcam
   ↓
getUserMedia()
   ↓
Live Video
   ↓
MediaPipe Hands
   ↓
21 Hand Landmarks
   ↓
Coordinate Processing
   ↓
Distance Calculations
   ↓
Canvas Rendering
```

## 💡 What I Learned

Through this project, I explored how **computer vision can be integrated into a web application** and learned about hand landmark detection, real-time video processing, coordinate transformations, Canvas rendering, and distance-based gesture logic.

I also used AI during development to understand concepts, explore implementation approaches, debug issues, and improve the hand-tracking logic.

## 🔮 What's Next?

I plan to extend this project beyond basic hand tracking by adding:

* **Shape recognition**
* **Letter recognition**
* **Gesture-based UI control**
* **More interactive hand gestures**

The goal is to move from simply **tracking the hand** to understanding gestures and using them as a natural way to interact with a web interface.
