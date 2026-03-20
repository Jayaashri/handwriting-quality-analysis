# Handwriting Quality Analysis System

A collaborative project that analyzes handwritten text images and estimates handwriting quality using a deep learning model and computer vision techniques.

---

## Overview

This project allows users to upload a handwritten paragraph image and receive:

- Character-level predictions using a trained neural network
- A handwriting quality score based on prediction confidence
- An overall grade (A, B, C)
- Practice worksheets for letters identified as weak

The system uses model confidence as a proxy for handwriting clarity and consistency.

---

## Key Features

- Handwritten character segmentation using OpenCV
- Character recognition using a CNN (TensorFlow/Keras)
- Confidence-based scoring for handwriting quality
- Grade assignment with feedback messages
- Worksheet generation by merging pre-existing letter PDFs
- Simple web interface for uploading and viewing results

---

## System Workflow

1. User uploads a handwritten image via the web interface  
2. Node.js (Express) server handles the request  
3. Python script:
   - Segments characters using OpenCV  
   - Runs inference using trained model (`htr.h5`)  
   - Computes confidence scores and identifies weak letters  
4. Results are returned to the server  
5. Server:
   - Assigns a grade and feedback  
   - Merges worksheet PDFs for weak letters  
6. Final results are displayed to the user  

---

## Tech Stack

**Backend / Web**
- Node.js
- Express.js
- EJS
- Multer

**Machine Learning / CV**
- Python
- TensorFlow / Keras
- OpenCV
- NumPy

---

## Project Structure


---

## My Contribution

- Worked on the handwriting analysis pipeline in Python
- Implemented character segmentation and preprocessing using OpenCV
- Integrated model inference and confidence-based scoring
- Contributed to connecting the ML pipeline with the web application

---

## Notes

- Developed as part of a team project  
- This is a prototype/demo system and not production-ready  
- Some components (frontend and server integration) were built collaboratively  

---

## Future Improvements

- Improve robustness of character segmentation
- Replace hard-coded paths with configurable inputs
- Improve scoring methodology beyond confidence-based proxy
- Deploy as a scalable backend service
