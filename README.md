# QRS Complex Detection in ECG Signals: A Pan-Tompkins Algorithm Implementation

### Introduction
Electrocardiogram (ECG) signal analysis is a cornerstone of cardiac diagnostics, providing essential
information about heart function and potential abnormalities. One of the most critical features in ECG
interpretation is the accurate detection of QRS complexes, which represent ventricular depolarization in
the cardiac cycle. This project implements an enhanced version of the Pan-Tompkins algorithm—a widely
respected method for QRS detection—adapted specifically for the MIT-BIH Arrhythmia Database, one of the
most comprehensive ECG databases available for cardiac research.
The implemented system processes ECG signals through a series of digital signal processing (DSP) stages
to identify QRS complexes accurately, even in the presence of noise and signal variations common in
clinical settings. The project evaluates the algorithm's performance against expert annotations, providing
metrics such as sensitivity, positive predictivity, and F1 score to quantify detection accuracy.

# The Pan-Tompkins Algorithm

### Overview
Developed in 1985 by Jiapu Pan and Willis J. Tompkins, the Pan-Tompkins algorithm represents a
systematic approach to QRS detection that remains relevant despite its age. The algorithm processes an
ECG signal through multiple stages, each designed to enhance specific characteristics of the QRS complex
while suppressing noise and other ECG components like P and T waves.

The implementation in this project follows an enhanced version of the original algorithm with optimizations
for the MIT-BIH Arrhythmia Database's specific characteristics. The core processing stages include:
1. Bandpass Filtering - To isolate the QRS frequency components
2. Derivative Computation - To emphasize the steep slopes of the QRS complex
3. Squaring - To make all signal values positive and emphasize higher frequencies
4. Moving Window Integration - To extract waveform features in addition to slope information
5. Adaptive Thresholding - To distinguish QRS complexes from noise and adapt to signal variations
