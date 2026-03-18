# 🚗 Driver Drowsiness Detection System 😴

![Python](https://img.shields.io/badge/Python-3.x-blue?logo=python)
![OpenCV](https://img.shields.io/badge/OpenCV-Computer%20Vision-green?logo=opencv)
![dlib](https://img.shields.io/badge/dlib-Facial%20Landmarks-orange)
![Status](https://img.shields.io/badge/Project-Complete-brightgreen)
![Platform](https://img.shields.io/badge/Platform-Windows-lightgrey)
![License](https://img.shields.io/badge/License-MIT-yellow)

---

A real-time computer vision-based system that detects driver drowsiness using eye aspect ratio (EAR) and alerts the user with an alarm when signs of sleep are detected.

---

## 📌 Project Overview

This project uses **OpenCV**, **dlib**, and **facial landmark detection** to monitor a driver's eye movements through a webcam. It calculates the **Eye Aspect Ratio (EAR)** to determine whether the eyes are open, drowsy, or closed.

If the system detects that the driver is falling asleep, it triggers a **continuous alarm** to alert them and prevent accidents.

---

## 🎯 Features

* 👁️ Real-time eye detection using webcam
* 📐 EAR (Eye Aspect Ratio) based analysis
* 🔄 Three states detection:

  * Active 😄
  * Drowsy 😐
  * Sleeping 😴
* 🔔 Continuous alarm when sleeping is detected
* ⚡ Instant alarm stop when user becomes active
* 🎯 Frame-based smoothing to reduce false detection

---

## 🧠 How It Works

1. Detect face using **dlib frontal face detector**
2. Extract **68 facial landmarks**
3. Isolate eye regions
4. Compute **Eye Aspect Ratio (EAR)**
5. Classify state:

   * High EAR → Active
   * Medium EAR → Drowsy
   * Low EAR → Sleeping
6. Trigger alarm if sleep is detected

---

## 📐 EAR Formula

```
EAR = (||p2 - p6|| + ||p3 - p5||) / (2 * ||p1 - p4||)
```

---

## 🛠️ Tech Stack

* Python 🐍
* OpenCV 👁️
* dlib 🤖
* NumPy 🔢
* winsound 🔔

---

## 📁 Project Structure

```
Driver-Drowsiness-Detection/
│
├── driver_drowsiness.py
├── wakeupaudio.wav
├── shape_predictor_68_face_landmarks.dat
└── README.md
```

---

## ⚙️ Installation & Setup

### 1️⃣ Clone the repository

```bash
git clone https://github.com/your-username/driver-drowsiness-detection.git
cd driver-drowsiness-detection
```

### 2️⃣ Install dependencies

```bash
pip install opencv-python numpy dlib imutils
```

### 3️⃣ Download landmark file

Download from:
http://dlib.net/files/shape_predictor_68_face_landmarks.dat.bz2

* Extract it
* Place it in project folder

---

## ▶️ Run the Project

```bash
python driver_drowsiness.py
```

Press **ESC** to exit.

---

## 🔔 Alarm System

* Alarm plays continuously when **sleep is detected**
* Stops automatically when user becomes active
* Uses `winsound` for stable playback (Windows)

---

## ⚠️ Requirements

* Webcam 📷
* Windows OS (for winsound)
* Python 3.x

---

## 🎓 Use Cases

* Driver safety systems 🚗
* Monitoring fatigue in workplaces 🏢
* AI-based surveillance 👁️

---

## 🤝 Contributing

Feel free to fork this repository and improve the project!

---

## 📄 License

This project is open-source and available under the MIT License.

---

## 🙌 Author

**Vansh Sharma**
📍 India
💻 Computer Science Student

---

⭐ If you like this project, don’t forget to star the repository!
