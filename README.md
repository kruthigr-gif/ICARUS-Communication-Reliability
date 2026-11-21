# 🚀 Project ICARUS – Communications Reliability 

## 📌 Overview

Project ICARUS focuses on improving the reliability of satellite communication systems by implementing digital signal processing, error correction, synchronization, and Doppler compensation techniques.

The project aims to recover transmitted data accurately under noisy channel conditions, frequency offsets, and satellite movement using various communication algorithms and decoding techniques.

## ⚙️ Algorithms and Methods Implemented

### 1. Digital Modulation and Demodulation (BPSK)
- Implemented Binary Phase Shift Keying (BPSK) modulation and demodulation.
- Used correlation with the carrier wave followed by threshold detection to recover the original bitstream.
- Implemented matched filtering with rectangular pulses.
- Applied hard-decision detection for bit recovery.
- Used energy-based timing recovery to identify optimal sampling points.

### 2. Noise Modeling and SNR Calibration
- Implemented statistical modeling of Signal-to-Noise Ratio (SNR).
- Used dataset metadata to obtain SNR values.
- Considered Additive White Gaussian Noise (AWGN) effects present in the received signal.
- Analyzed signal degradation under different noise conditions.

### 3. Error Correction Coding and Decoding
- Implemented Reed-Solomon decoding using an external library.
- Incorporated convolutional decoding using the Viterbi algorithm.
- Explored concatenated coding schemes combining Reed-Solomon outer codes with convolutional inner codes.
- Used selective decoder invocation to apply only the necessary decoding modules.

### 4. Synchronization and Doppler Compensation
- Implemented FFT-based frequency offset estimation using peak detection.
- Identified frequency shifts caused by satellite movement and oscillator inaccuracies.
- Applied frequency correction by multiplying received signal samples with a complex exponential.
- Improved receiver synchronization and signal integrity.

### 5. Engineering Problem-Solving
- Followed a systematic approach to identifying and analyzing communication challenges.
- Evaluated signal behavior using dataset analysis.
- Developed, tested, and refined signal-processing algorithms.
- Addressed dataset inconsistencies through automated processing techniques.

## 🛠️ Challenges Faced and Solutions

| Challenge | Solution |
|---|---|
| Doppler Shift | Characterized Doppler effects using satellite visibility time and implemented FFT-based peak detection for frequency offset estimation. |
| Communication Delay | Used Forward Error Correction (FEC) techniques to reduce dependency on retransmissions. |
| Transmission Errors | Explored concatenated Reed-Solomon and convolutional coding schemes for error correction. |
| Dataset Inconsistencies | Implemented automated handling of missing keys, inconsistent metadata, and varying file names. |
| Graph Visualization | Developed text-based ASCII graph visualization as an alternative when Matplotlib was unavailable. |

## 🧠 Implementation Details

### Design Decisions

- **BPSK Modulation/Demodulation:** Matched filtering with rectangular pulses and hard-threshold detection for bit decisions.
- **Timing Recovery:** Energy maximization to determine optimal sampling positions.
- **Noise Modeling:** Relied on dataset metadata for SNR values, considering AWGN implicitly present in the received data.
- **Error Correction:** Implemented Reed-Solomon decoding and a convolutional (Viterbi) decoder with selective module execution.
- **Doppler Compensation:** Used FFT peak detection to estimate frequency offsets and complex exponential multiplication to correct them.

### Assumptions

- Each dataset folder represents a constant channel condition.
- `meta.json` files provide accurate and reliable metadata.
- The decoder uses hard-decision detection instead of soft-decision probability calculations.

### Limitations

- Incomplete convolutional decoding implementation.
- No carrier phase tracking.
- Limited noise modeling capabilities.
- Simplistic timing recovery mechanism.
- No hardware integration or real-time processing support.

## 📊 Graphs and Visualizations

The project focuses on the following signal analysis visualizations:

1. **BER vs SNR Curves:** Comparison of uncoded and coded communication systems.
2. **Constellation Diagrams:** Visualization of signal behavior at representative SNR levels.
3. **Doppler Compensation Plots:** Comparison of received signals before and after frequency offset correction.
4. **ASCII Graph Visualization:** Text-based representation of signal analysis results when graphical plotting libraries are unavailable.

## 🎯 Key Outcomes

- Developed a BPSK-based communication recovery pipeline.
- Implemented frequency offset estimation and Doppler compensation.
- Incorporated Reed-Solomon error correction and convolutional decoding techniques.
- Addressed noisy channel conditions through SNR analysis.
- Improved dataset handling through automated metadata processing.
- Explored techniques for enhancing satellite communication reliability.

## 🔮 Future Improvements

- Complete convolutional encoder and decoder integration.
- Implement carrier phase synchronization and tracking.
- Improve timing recovery using advanced synchronization algorithms.
- Enhance noise modeling and channel estimation.
- Integrate real-time signal processing and hardware-based testing.

---

**Project:** ICARUS – Communications Reliability Challenge  
**Domain:** Satellite Communication | Digital Signal Processing | Error Correction Coding  
**Core Techniques:** BPSK, FFT, Reed-Solomon, Viterbi Decoding, Doppler Compensation, SNR Analysis
