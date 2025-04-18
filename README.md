# 📸 Real-Time Face Recognition Attendance System

A real-time attendance tracking system using facial recognition, powered by **FaceNet embeddings**, **KNN classifier**, and **OpenCV**. The system identifies individuals through a live webcam feed and marks their entry and exit times with high accuracy. Unknown individuals are automatically detected and their images are saved with timestamps.

---

## 🚀 Features

- 🔍 **Real-time face detection** using webcam.
- 🤖 **Face recognition** using FaceNet + KNN classifier.
- ✅ **Automatic attendance marking** with entry and exit timestamps.
- 🔐 **Confidence threshold** to prevent false positives.
- 🧠 **Face stabilization logic** to avoid flickers.
- 🧾 **Attendance logging** in a structured CSV file.
- ❌ **Unknown face detection** with red bounding box and snapshot saving.
- 🖥️ **GUI-based control** to start/stop camera via **Tkinter**.

---

## 🛠️ Tech Stack

- **Python 3.x**
- [OpenCV](https://opencv.org/)
- [Keras-FaceNet](https://pypi.org/project/keras-facenet/)
- [NumPy](https://numpy.org/)
- [Pandas](https://pandas.pydata.org/)
- [Tkinter](https://docs.python.org/3/library/tkinter.html)
- **KNN Classifier** (trained model loaded via `pickle`)

---

## 📌 How to Use

### 1. Prepare Dataset
- Organize person images in folders labeled with person IDs (e.g., `001`, `002`, etc.).
- Each folder should contain **6–7 facial images** with varied expressions and angles.

### 2. Train Model
- Train and save the **KNN model** (`knn_model.pkl`) and **label encoder** (`label_encoder.pkl`) using **FaceNet embeddings**.

### 3. Update Attendance File
- Ensure `Attendance.csv` has the following columns:

### 4. Control Camera
- Run the script.
- A **simple GUI** opens with a **"Stop Camera"** button to terminate the session.

### 5. View Reports
- After stopping the camera, a file named `Attendance_Report.csv` is saved with:

### 6. Unknown Detection
- Unknown individuals:
- Are displayed with a **red bounding box**.
- Are labeled as **“Unknown”**.
- Have their snapshot saved to `unknown_snapshots/` with a timestamped filename.

---

## 📷 Sample Output

### ✅ Known Face Detection:
- Green bounding box
- Name label displayed
- Attendance marked automatically

### ❌ Unknown Face Detection:
- Red bounding box
- “Unknown” label
- Snapshot saved to `unknown_snapshots/unknown_YYYYMMDD_HHMMSS.jpg`

---

## 🧠 Future Enhancements

- Dynamic KNN training from the UI.
- Face re-registration module.
- Integration with databases (MySQL, Firebase).
- Email alerts for unknown detections.
- Multi-camera support.

---

## 📄 License

This project is **open-source** and free to use for **educational and research purposes**.

---

## 🤝 Acknowledgements

- [FaceNet](https://pypi.org/project/keras-facenet/) by Keras-Facenet
- [OpenCV](https://opencv.org/) for real-time video capture
- Inspiration from practical AI applications in **smart surveillance** and **biometric systems**

---

## 👤 Contributors

- [Koyyada Shreeshanth](https://www.linkedin.com/in/koyyada-shreeshanth-a17414285/)
- [Dogga Pavan Sekhar](https://www.linkedin.com/in/dogga-pavan-sekhar-006a83252/)
 
---

Feel free to contact `shreeshanthgoud@gmail.com`, `doggapavansekhar@gmail.com`
