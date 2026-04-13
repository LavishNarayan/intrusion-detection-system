🚨 Intrusion Detection System (Real-Time Human Detection & Alert System)
📌 Overview

This project is a real-time Intrusion Detection System that uses computer vision and pose detection to identify human presence through a webcam feed. Once a human is detected continuously beyond a threshold, the system triggers an SMS alert using Twilio API.

It is designed for security surveillance applications such as restricted area monitoring, home security, and smart alert systems.

⚙️ Features
🎥 Real-time video capture using OpenCV
🧍 Human detection using Pose Estimation (cvzone)
🚨 Automatic alert system via SMS (Twilio API)
🔁 Continuous monitoring loop
⚡ Lightweight and fast execution
🛠️ Tech Stack
Python
OpenCV
cvzone (Pose Module)
Twilio API
📂 Project Structure
intrusion-detection-system/
│
├── main.py        # Main detection logic
├── send.py        # SMS alert module (Twilio)
├── README.md
🚀 How It Works
Webcam starts capturing live video.
Pose detection model scans frames for human presence.
If a human is detected continuously:
A counter increases.
Once threshold is reached:
SMS alert is triggered via Twilio.
System continues monitoring in real-time.
🧠 Core Logic (Simplified)
if len(lmlist) > 0:
    print("Human Detect")
    l.append(1)

if len(l) > 50 and flag:
    flag = False
    send.sendSms()
📲 Twilio Setup
Create account on https://www.twilio.com
Get:
Account SID
Auth Token
Replace in send.py:
account_sid = 'your_account_sid'
auth_token = 'your_auth_token'
▶️ Installation & Run
Step 1: Install dependencies
pip install opencv-python
pip install cvzone
pip install twilio
Step 2: Run the project
python main.py
📸 Output
Live webcam feed opens
Detects human presence
Sends SMS alert when intrusion is confirmed
⚠️ Limitations
Depends on lighting conditions
False positives possible
Requires internet for SMS functionality
🔮 Future Improvements
Add face recognition
Email + push notifications
Cloud logging system
Multi-camera support
AI-based anomaly detection
👨‍💻 Author

Lavish Narayan
