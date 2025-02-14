Deep Learning-Based Illegal Bowling Action Detection

Overview

This project introduces a deep learning-based approach for detecting illegal bowling actions in cricket using computer vision techniques. The system identifies illegal bowling actions by analyzing the arm's angle difference between two key frames in a bowler's delivery: the shoulder frame and the release frame. If the angle difference exceeds a predefined threshold (15 degrees), the action is flagged as illegal.

Features

Utilizes MediaPipe for pose estimation.

Employs YOLOv8 for release frame extraction.

Processes video footage from multiple angles (front, back, and side) for comprehensive analysis.

Achieves 91.96% accuracy and a 100% true positive rate on a controlled dataset.

Works in real-time and can be integrated into live cricket matches.

Dataset

A dataset of 62 videos featuring 11 male bowlers was collected and labeled for analysis.

Footage includes both legal and illegal bowling actions.

The dataset is used to train and validate the deep learning model.

Methodology

Dataset Collection & Preprocessing: Videos are collected and labeled based on ICC regulations.

Frame Extraction:

Shoulder Frame Extraction: Identifies the frame where the arm is closest to the shoulder level (270° angle).

Release Frame Extraction: Uses YOLOv8 to detect when the bowler releases the ball.

Bowling Action Analysis:

Measures the elbow flexion in both frames using MediaPipe.

If the angle difference exceeds 15°, the delivery is flagged as illegal.

Model Evaluation:

Tested with accuracy, precision, recall, and F1-score.

Compared different models (CNN, YOLOv7, YOLOv8) for optimal performance.
