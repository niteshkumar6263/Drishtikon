# Drishtikon

# 🧠 AI-Powered Blind Navigation System  
*"Empowering the visually impaired with real-time vision and voice."*

This project is a **wearable AI-powered assistive system** designed to help visually impaired individuals **navigate streets safely and independently**. It combines **YOLO(deep learning)** for object detection, **lane detection** using classical computer vision, and **real-time text-to-speech** feedback to describe obstacles and guide the user's direction.
This system acts as a **virtual assistant**, providing spoken instructions.

---

## 🎯 Problem Statement

Over **285 million people** worldwide live with visual impairments. Most rely on white canes or guide dogs, which offer **limited awareness of their surroundings**. In busy urban environments, these traditional tools fail to detect:
- Incoming vehicles
- Obstacles like benches or stop signs
- Lanes 

There is a need for **affordable, real-time, intelligent navigation systems** that can fill this gap — and this project is a step toward that.

---

## 💡 Solution Overview

This project brings together AI and assistive tech to deliver:
- **Visual sensing** using a chest-mounted
- **Object detection** (cars, people, traffic signs) using YOLOv8
- **Lane detection** for navigation guidance
- **Speech output** to notify the user of threats, objects, and directions
- **Distance estimation** to prioritize nearby obstacles

The user receives **spoken navigation cues** in real time, enabling them to:
- Avoid obstacles
- Understand direction
- Walk safely and confidently

---

## ✨ Key Features

| Feature | Description |
|--------|-------------|
| 🧍 Object Detection | Detects people, cars, buses, traffic lights, animals, etc. |
| 🛣️ Lane Detection |
| 🗣️ Audio Guidance | Speaks alerts like “Bus ahead”, “Turn left” |
| 🎥 Video Input | Works on live webcam |

---

## 🧪 Technology Stack

### 🔍 Vision & AI
- **YOLOv8 (Ultralytics)** – Object detection on video frames
- **OpenCV** – Lane detection using Canny + Hough Transform

### 🗣️ Audio & Speech
- **pyttsx3** – Offline, cross-platform text-to-speech engine
- **Threading + Queue** – Non-blocking speech processing

### 🧠 Logic & Control
- **NumPy** – Image and distance calculations
- **Custom logic** – For threat filtering, direction inference, and visual overlay

---

## 🔁 How It Works

1. **Video is captured** (via webcam)
2. **YOLOv8** detects all visible objects and estimates distance
3. **OpenCV** performs edge and line detection to identify lanes
4. **Position logic** decides what the user should do next (turn, stop, walk)
5. **pyttsx3** gives voice instructions to the user
