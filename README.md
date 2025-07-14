# Computer Vision Projects 🚀

This repository contains two main computer vision projects focused on real-time detection and augmentation using Python and popular libraries such as YOLOv8 and MediaPipe. Each project tackles a specific use case related to object detection or augmented reality.

---

## 📂 Project 1: Mobile Phone Detection with YOLOv8

### 📝 Overview
This project aims to detect when a person is using a mobile phone. The system identifies both a person and a phone within the same region of an image and sends an alert (via email) when both are detected simultaneously.

### ⚙️ Technologies
- **YOLOv8** (Ultralytics)
- **Python 3.x**
- **OpenCV**
- **SMTP (Email Alerts)**

### 🛑 Challenges Encountered
- False positives on phone detection.
- Detection of phones not associated with people (e.g., on tables).
- Repeated email alerts for the same event.
- Small or blurry object confusion.
- Overly sensitive detection thresholds.

### 🔧 Solutions Implemented
- Applied a higher confidence threshold (> 0.75).
- Verified minimum object size to exclude small artifacts.
- Computed spatial proximity between people and phones.
- Implemented a flag to avoid sending duplicate alerts for the same situation.

### 📊 Results
- Reliable detection of simultaneous person + phone usage.
- Automatic email alerts are sent only for relevant detections.
- Effective in scenarios like classrooms, workplaces, or surveillance.

### 📸 Example Outputs
Screenshots show detections in various situations where the system successfully triggered alerts when a phone was being used.

### 📌 Conclusion
The final system can serve as a base for smart monitoring tools and control systems to detect inappropriate phone usage.

---

## 📂 Project 2: Dynamic Face Filters with MediaPipe

### 📝 Overview
This project superimposes dynamic filters (hat and glasses) onto faces detected in real-time. It adjusts the position and rotation of these filters according to head movements (pitch and roll).

### ⚙️ Technologies
- **MediaPipe**
- **OpenCV**
- **Python 3.x**
- **Image Processing Libraries (e.g., PIL)**

### 🛑 Challenges Encountered
- Incorrect vertical alignment of the hat.
- Filters not following head rotations (roll).
- Overlapping filters (hat covering glasses).
- Unnatural horizontal displacement during lateral head movement.

### 🔧 Solutions Implemented
- Used eye center coordinates for better facial positioning.
- Calculated eye-to-chin distance to adjust hat height dynamically.
- Adjusted horizontal positioning based on head tilt.
- Applied inverse rotation to ensure natural tracking of head movements.

### 📊 Results
- Realistic placement of virtual accessories.
- Smooth tracking across significant head movements.
- Filters remain properly aligned during rotations and inclinations.

### 📸 Example Outputs
Screenshots demonstrate accurate filter placements during different head movements and inclinations.

### 📌 Conclusion
The project delivers a smooth and coherent augmented reality experience where virtual accessories follow the head naturally in real-time.

---

## 📁 Repository Structure
```
computer_vision_projects/
│
├── computer_vision_project.ipynb       # Notebook containing code examples for both projects
├── Ousmane_KA_Rapport_Detection_Telephone_YOLOv8.pdf    # Report for Phone Detection
├── Ousmane_KA_Rapport_Filtres_Visage_MediaPipe.pdf      # Report for Face Filters
├── /images                               # Screenshots from results (if provided)
└── /assets                               # Additional resources (if applicable)
```

---

## 🚀 How to Run
### Prerequisites
- Python 3.x
- OpenCV
- MediaPipe
- Ultralytics YOLOv8
- smtplib (for email alerts)

### Installation
```bash
pip install opencv-python mediapipe ultralytics
```

### Running the Projects
1. Open `computer_vision_project.ipynb` in Jupyter Notebook or VSCode.
2. Run the relevant sections (YOLOv8 or MediaPipe).
3. Ensure webcam access for MediaPipe; configure email settings for YOLOv8 alerts.

---

## 📜 License
This project is licensed under the MIT License.

---

## ✨ Acknowledgments
Thanks to the creators of YOLOv8, MediaPipe, and the open-source community for providing robust tools for computer vision.

---

## 👨‍💻 Author
**Ousmane KA**
