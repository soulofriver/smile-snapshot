# Smile Snapshot

A real-time smile detection app using OpenCV that automatically captures and saves photos whenever a smile is detected.

---

## Features
- Real-time face detection
- Smile detection using Haar Cascades
- Automatic photo capture on smile
- Smart delay system to avoid duplicate captures
- Saves images locally

---

## How It Works

This project uses Haar Cascade classifiers to detect faces and smiles from webcam input.

Workflow:
1. Capture video from webcam
2. Detect faces in each frame
3. Focus on lower face region (mouth area)
4. Detect smiles inside the face ROI
5. If a smile is detected:
   - Save the image automatically
   - Prevent rapid duplicate captures using a delay timer

---

## Model Files

These will be downloaded automatically if not present:

haarcascade_frontalface_default.xml
haarcascade_smile.xml

---

## Run

smile-snapshot.py

### Controls

Press ESC to exit

---

## Output

Captured images will be saved in:

smiles/

File format:

smile_1.jpg
smile_2.jpg
...

---

## Parameters

capture_delay = 2

Prevents multiple captures within 2 seconds

minNeighbors=30 (smile detection)

Higher value reduces false positives

---

## Technical Notes

Smile detection is applied only to the lower half of the face
Helps reduce false detection from eyes or noise
Uses grayscale conversion for faster processing
