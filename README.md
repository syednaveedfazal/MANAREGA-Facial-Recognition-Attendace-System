# MANAREGA Facial Recognition Attendance System

**MANAREGA** is an automated attendance system designed for daily gig workers. It uses **computer vision** and **machine learning** (TensorFlow) to instantly recognize a worker’s face and mark their attendance — without any manual administrative intervention.

---

## 🧠 Key Features

- **Face Recognition**: Instantly identify gig workers using their face.
- **Automated Attendance**: Once recognized, attendance is marked automatically.
- **Self-Registration**: Workers can register by capturing their own face images.
- **Model Training**: Use Tkinter-based GUI to train the model with new images.
- **Robust ML Backend**: Built on TensorFlow for training and inference.
- **Offline First**: Does not depend on constant Internet connectivity.
- **Secure & Privacy-aware**: Only stored embeddings or minimal face data; designed with data privacy in mind.

---

## 📚 Why MANAREGA

In many gig-economy systems, daily workers often lack formal infrastructure for attendance tracking. Traditional attendance systems require supervisors or administrators, which can be inefficient, error-prone, or even corruptible. MANAREGA tackles this by:

1. **Automating attendance** — No need for a manager to manually mark who came in.
2. **Reducing proxy risk** — Face recognition makes it hard to fake attendance.
3. **Encouraging self-service** — Workers enroll themselves, reducing administrative burden.
4. **Providing scalable infrastructure** — Easily scalable for large workforces or multiple sites.

---

## 🏗️ Architecture & Components

Here’s how the system works:

1. **Data Collection**  
   - A Tkinter GUI allows workers to capture multiple face images.  
   - Images are stored in a structured way (e.g., `dataset/<worker-id>/…`) for training.

2. **Model Training**  
   - The captured images are used to train a TensorFlow-based face recognition model.  
   - Training can be triggered via the GUI, and the model saves embeddings/weights for each individual.

3. **Face Recognition / Inference**  
   - A live camera stream (e.g., from a webcam) captures worker faces.  
   - Each frame is processed and compared against stored embeddings.  
   - If matched with sufficient confidence, the system marks the worker present.

4. **Attendance Logging**  
   - Once recognized, attendance is recorded (e.g., in a CSV file, database, or local file).  
   - Optionally, timestamps and worker IDs are stored for audit.

---

## 💾 Requirements / Dependencies

- Python 3.x  
- TensorFlow  
- OpenCV  
- NumPy  
- Tkinter (for GUI)  
- (Optional) pandas — for attendance logs  
- [Any other libraries you use in your repo]

You can install dependencies via:

```bash
pip install -r requirements.txt
