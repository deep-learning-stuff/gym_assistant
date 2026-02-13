# SquatForm AI: Real-Time Pose Estimation 🏋️

SquatForm AI is a computer vision tool designed to analyze and correct squat technique in real-time. By leveraging human pose estimation, the system tracks key body joints to count repetitions and provide immediate feedback on form quality to prevent injuries.

## 🚀 Project Overview
The goal of this project is to act as a "virtual coach." It monitors critical joint angles during physical exercise to ensure the user maintains a safe and effective posture.

### Key Features:
* **Real-Time Detection:** Uses a standard webcam to capture and process movement at high frame rates.
* **Repetition Counter:** Intelligent algorithm based on joint angles to register valid squats (Down/Up states).
* **Posture Correction:**
    * **Knee Tracking:** Detects if knees are correctly aligned or moving improperly.
    * **Back Alignment:** Analyzes torso inclination to prevent excessive leaning or rounding.
* **Dynamic Visual Feedback:** On-screen HUD (Heads-Up Display) showing squat count and real-time posture status (e.g., "Correct", "Inclined", "Knee Error").

## 🛠️ Technologies Used
* **Language:** Python
* **Computer Vision:** [MediaPipe](https://mediapipe.dev/) (Pose Landmark Detection)
* **Image Processing:** OpenCV
* **Numerical Computation:** NumPy
* **Mathematics:** Analytical geometry for calculating biomechanical angles between joints.

## 📈 How It Works
1.  **Landmark Extraction:** The model identifies 33 key body landmarks (shoulders, hips, knees, ankles) using MediaPipe Pose.
2.  **Angle Calculation:** The system calculates the internal angle of the knee and the torso's angle relative to the vertical axis.
3.  **State Logic:** * A squat is only counted if the user reaches sufficient depth and returns to a standing position.
    * Validation filters ensure that "half-reps" or bad form (excessive leaning) are flagged.

## 💻 Setup & Usage

1.  **Prerequisites:**
    Install the required libraries using pip:
    ```bash
    pip install opencv-python mediapipe numpy
    ```

2.  **Execution:**
    Simply run the main notebook or export the code to a script:
    ```bash
    python pose_detection.py
    ```
    * **Note:** The system uses your default camera (ID 0).
    * **Exit:** Press the **ESC** key to close the camera window and end the session.

## 👥 Authors
Developed as a project focused on the implementation of computer vision algorithms and biomechanical motion analysis.

---
*Disclaimer: This software is an educational tool and does not replace the advice of a professional fitness coach or medical expert.*
