🚀 Facial Identification System with AI-Generated Face Detection
A real-time Face Recognition System with AI-generated face detection, built using:
OpenCV
face_recognition (dlib)
LBP Texture Analysis (scikit-image)
Python

This project detects faces in a live webcam feed, identifies known persons, and also flags AI-generated faces using texture-based heuristics.
Features
✔ Real-Time Face Recognition

Recognizes faces using stored encodings from the known_faces/ directory.

✔ AI-Generated Face Detection

Uses LBP (Local Binary Patterns) to analyze skin texture.
Smooth / uniform textures (common in AI-generated images) are flagged as AI Face.

✔ Save New Faces

Press S during detection to add new face data dynamically.

✔ Modern UI

Rounded rectangles

Color-coded labels

🟢 Real Face

🔴 AI Face

✔ Automatic Face Dataset Management

Automatically loads and updates known face encodings from folders.
Project Structure
📦 Facial-Identification-System
 ┣ 📂 known_faces
 ┃ ┣ 📂 person_name
 ┃ ┃ ┣ image1.jpg
 ┃ ┃ ┗ image2.jpg
 ┣ 📜 faceID.py
 ┣ 📜 README.md
 ┗ 📜 requirements.txt

🛠 Installation
1️⃣ Clone the Repository
git clone https://github.com/<your-username>/<repo-name>.git
cd <repo-name>

2️⃣ Install Dependencies

Make sure Python 3.7+ is installed.

pip install opencv-python
pip install numpy
pip install face_recognition
pip install scikit-image


Note:
face_recognition requires dlib.
If installation fails, install dlib manually as per OS requirements.

▶ Running the System

Run the main file:

python faceID.py


The webcam will open and start:

Detecting faces

Identifying known persons

Checking if the detected face is AI-generated

🎯 Controls
Key	Action
S	Save a new face with a name
Q	Quit the application

When saving a face, the system will ask:

Enter name for the new face:


A new folder will be created inside known_faces/ automatically.

🤖 AI Face Detection Logic

This system uses LBP (Local Binary Pattern) texture analysis:

AI-generated faces usually have very smooth / uniform textures

Natural human skin has rich micro-textures

If uniform LBP patterns exceed a threshold → AI Face

This is a heuristic method, effective for basic fake face spotting.
Future Enhancements

Deep-learning based deepfake detection

Dataset-based SVM classifier

Multi-camera support

Flask-based web interface

🧪 Technologies Used
Tech	Purpose
OpenCV	Video processing & drawing UI
face_recognition	Face encoding + matching
scikit-image	LBP texture feature extraction
NumPy	Array operations
Haar Cascade	Fallback face detection
📝 Author

Pradeep Sathapathi
Cybersecurity | AI | R&D Innovator
LinkedIn: https://www.linkedin.com/in/pradeep-sathapathi-123950232?utm_source=share&utm_campaign=share_via&utm_content=profile&utm_medium=android_app
