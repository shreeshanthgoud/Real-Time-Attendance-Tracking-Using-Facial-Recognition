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
- 🖥️ GUI-based control to start/stop camera via **Tkinter**.

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

## 📁 Project Structure

##📌 How to Use
Prepare Dataset

Organize person images in folders labeled with person IDs (e.g., 001, 002, etc.).

Each folder should contain 6–7 facial images with varied expressions.

Train and save the KNN model (knn_model.pkl) and label encoder (label_encoder.pkl) using FaceNet embeddings.

Update Attendance File

Ensure Attendance.csv has the following columns:

Person ID,Name,Roll No,Department

Control Camera

A simple GUI opens with a Stop Camera button to terminate the session.

View Reports

After stopping the camera, the script saves a file named Attendance_Report.csv with the following columns:
Name, Roll No, Department, Entry Time, Exit Time

Unknown Detection

Unknown individuals are logged with a red bounding box.

A snapshot is saved inside the unknown_snapshots/ folder with timestamp in filename.
##📷 Sample Output
Known Face Detection:

Green box around face

Name label displayed

Attendance marked automatically

Unknown Face Detection:

Red box around face

“Unknown” label

Snapshot saved to unknown_snapshots/unknown_YYYYMMDD_HHMMSS.jpg

#🧠 Future Enhancements
Train KNN model dynamically from the UI.

Add face re-registration module.

Integrate with databases (MySQL, Firebase).

Email alerts for unknown detections.

Support for multiple camera sources.

##📄 License
This project is open-source and free to use for educational and research purposes.

##🤝 Acknowledgements
FaceNet by Keras-Facenet

OpenCV for real-time video capture

Inspiration from practical AI applications in smart surveillance and biometric systems.

👤 Author
KOYYADA SHREESHANTH
