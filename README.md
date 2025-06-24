## Efficient and Smart Parking Management System

An intelligent and optimized parking system that uses Computer Vision, C++, and algorithmic logic to manage vehicle entries, exits, and slot allocation with real-time number plate detection and shortest path guidance.

---

## Features

- Real-time number plate detection using OpenCV and PyTesseract  
- Slot allocation using C++ DAA algorithms (priority queue, hash map, Dijkstra)  
- Automatic user dashboard showing entry time, slot path, and bill  
- Exit system with OCR to free the slot  
- Simple and responsive UI using Flask and Jinja templates

---

## Technologies Used

| Category        | Tech Stack                                |
|----------------|--------------------------------------------|
| Frontend       | HTML5, CSS3, JS, Bootstrap, Jinja          |
| Backend        | Python (Flask), C++                        |
| Computer Vision| OpenCV, Haar Cascade, PyTesseract          |
| Algorithms     | Dijkstra’s Algorithm, Priority Queue, Map  |
| Data Exchange  | CSV, File-based communication              |

---

## Project Structure

```
SmartParkingSystem/
│
├── app.py                 # Flask main app
├── number_plate.py        # Vehicle detection logic
├── parking.cpp            # C++ slot allocation logic
├── templates/             # HTML templates
├── static/                # CSS, videos, layout image
├── plates/
│   └── plate_img/         # Saved captured images
├── slots.txt              # Slot data
├── vehicle_logs.csv       # Vehicle entry logs
└── requirements.txt       # Python dependencies
```

## How it Works

- Vehicle is detected at the entry gate  
- License plate is captured and recognized via OCR  
- Python writes data to a CSV log  
- C++ reads the data and applies DAA logic to allocate the nearest available slot  
- Dashboard is displayed automatically with all user info  
- At exit, plate is detected again, slot is freed, and bill is calculated

---

## How to Run Locally

1. Clone this repo:
   ```bash
   git clone https://github.com/AnushkaNegi27/SmartParkingSystem.git
   cd SmartParkingSystem
2. Install dependencies:
   ```bash
   pip install -r requirements.txt
4. Run the app:
   ```bash
   python app.py
