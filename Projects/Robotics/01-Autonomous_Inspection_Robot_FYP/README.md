# Autonomous Inspection Robot for Real-Time Metal Crack Detection (Final Year Project)

**Bachelor of Mechatronic Engineering — Mehran University of Engineering & Technology, Jamshoro (December 2024)**
Team of three, supervised by Engr. Aamir Shaikh.

📄 [Read the full thesis (PDF)](Projects/Robotics/01-Autonomous_Inspection_Robot_FYP/FYP_Thesis_Final_Draft.pdf)

## Problem
Manual inspection of metal surfaces in hazardous environments such as reactor pressure vessels is slow, costly, and exposes workers to risk.

## Solution
An autonomous mobile inspection robot with an operator HMI and AI-based crack detection.

- **Mechanical design:** circular robot (18 in chassis) with a 4-DOF manipulator: tilt, rack-and-pinion extension, 360° rotation, and a 4-bar camera mechanism. CAD models of the robot and an inspection arena were developed.
- **Control:** Arduino Mega 2560 for on-board motion and sensors, with encoder feedback, controlled from a PC over serial.
- **HMI (C# / WPF):** login, manual control, simulation, and autonomous pages. Autonomous tasks are built as CSV command lists and tracked live (pending / executed).
- **Path planning:** MATLAB probabilistic roadmap (PRM) planning and Pure Pursuit simulation, launched from the HMI.
- **Crack detection:** custom-trained YOLOv11-seg model converted to ONNX and embedded in the HMI for image, video, and live-camera inspection.

## Results
| Metric | Value |
|---|---|
| Crack detection precision / recall (box) | 96.58% / 93.43% |
| Segmentation precision / recall | 94.69% / 91.61% |
| mAP50 (detection / segmentation) | 96.88% / 93.53% |
| Inference time | 12.71 ms per image (~37 FPS) |
| Navigation position error | about 1.2–1.7% |
| Command-to-execution lag | 570 ms |

## Stack
Arduino Mega 2560 · C# / WPF · MATLAB · Python · YOLOv11-seg · ONNX · CVAT · Google Colab (Tesla T4)

## Related paper
[Development of a Robotic System for Pressure Vessel Inspection](Research_Papers/DEVELOPMENT_OF_ROBOTIC_SYSTEM_FOR_PRESSURE_VESSEL_INSPECTION.pdf)

## Media
- [<img width="514" height="365" alt="image" src="https://github.com/user-attachments/assets/30afa7a5-839a-4cc9-b4af-0e859c64f92d" />
<img width="674" height="501" alt="image" src="https://github.com/user-attachments/assets/9674c36b-417d-4cec-a757-7b5c3282dc7e" />
<img width="682" height="452" alt="image" src="https://github.com/user-attachments/assets/cd555816-bb3c-4c57-bc72-3e45471f958d" />
] Robot photo
- [<img width="1030" height="535" alt="image" src="https://github.com/user-attachments/assets/983598c1-175b-4185-9c64-d89f18088690" />
<img width="604" height="482" alt="image" src="https://github.com/user-attachments/assets/083a7382-85c6-4749-aea0-724e5cc7be4c" />
<img width="1014" height="575" alt="image" src="https://github.com/user-attachments/assets/f06800df-22c2-4b18-a260-8efbc9d19a8d" />
<img width="633" height="360" alt="image" src="https://github.com/user-attachments/assets/790278e5-8a66-42ac-a686-a3f4913947e1" />
] HMI screenshots
