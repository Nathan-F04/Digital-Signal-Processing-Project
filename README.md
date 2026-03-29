Digital Signal Processing Project
Overview

Note: you must download the .wav files and add them to your google drive to run the notebook via colab.
Link to colab: https://colab.research.google.com/drive/1_RhqAzOkZmZTM8qpDrICauHzm4Ya5eaA?usp=sharing 

This project explores digital signal processing (DSP) techniques applied to real-world audio recordings. 
Audio samples containing bird sounds, wind, traffic, speech, sirens, and other ambient noise were recorded and analyzed. 
The project involves:

Computing spectrograms of audio samples.
Applying filters of varying types, orders, and frequency bands.
Comparing audio before and after filtering.
Documenting the filtering process with supporting background theory.

Analysis of signals and reflections was performed after the initial processing:

Audio Recording
Recordings were captured primarily during a campus walk, with one sample recorded in a quiet suburban environment.
All recordings were made using a preinstalled phone app and converted to .wav format via Audacity.

Signal Processing
Spectrogram Computation
Parameters include: window type, segment length, overlap, FFT length, scaling, and detrending.
Windowing: Hanning window used to reduce spectral leakage for non-periodic signals.
Overlap: Set to 512 samples, less than FFT length of 1024, improving event detection in the time domain.
Spectrogram amplitude is converted to decibels (dB) for visualization.
Plotting Functions
plot_time_domain: Plots audio in the time domain.
plot_spec_scipy: Plots spectrograms with configurable zoom, axes, and titles.
bode: Plots Bode plots for filter frequency responses.
bandpass_plot & high_pass: Apply Butterworth bandpass and high-pass filters, showing input vs output signals.

Several functions were refactored and enhanced with argument flexibility for ease of reuse and analysis.

Audio Analysis & Background Theory
Filter Theory
Research into low-pass, high-pass, band-pass, and band-stop filters, both passive and active was performed for the project.
Key insights include:
Passive filters have no gain; active filters can amplify signals.
Cutoff frequency calculations and circuit diagrams.
Bode plots and frequency responses for each filter type.
Filter Types
Butterworth: No ripples, smooth frequency response (used in this project).
Chebyshev: Quick transition, passband ripples.
Inverse Chebyshev: Quick transition, stopband ripples.
Elliptic: Fastest transition, ripples in both bands.
Bessel: Slow transition, no stopband ripples.
Analysis of Filtered Audio
Time domain plots and spectrograms are compared before and after filtering.
Contrasts examined:
Different filter types applied to the same sample.
Different filter orders for the same filter type.
Differences between sampling rates and noise levels.

Sample Analysis

Each audio sample was analyzed through time domain plots, spectrograms, and Bode plots, highlighting both the raw and filtered signals. 
Filters were applied based on the frequency characteristics of specific sounds such as speech, sirens, or bird calls.

Over the course of the project:

Improved understanding of Fourier transforms, Hanning windows, and filter theory.
Developed skills in filter selection, adjusting cutoff frequencies, and comparing high-pass vs bandpass outcomes.
Gained experience in analyzing real-world audio, including varying noise conditions.
Improved technical documentation, structuring analysis and workflow for clarity and reproducibility.

Lessons Learned & Future Work:

Gather a broader set of audio samples across noise levels.
Test different recording devices for sensitivity and consistency.
Refine filter cutoffs for optimal frequency isolation.
Explore more advanced methods for automated audio analysis.
