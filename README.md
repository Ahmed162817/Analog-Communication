# 🎧 Analog Modulation Communication System — Super-Heterodyne Receiver

This MATLAB project simulates the core components of an **Analog Communication System** including an **AM (Amplitude Modulation) Transmitter** and a **Super-Heterodyne Receiver**.  

![image alt](https://github.com/Ahmed162817/Analog-Communication/blob/c1180115b4629423cf72e454a2a4134e957622d2/Super_Heterodyne_Rx.jpg)

## 🧩 Project Overview

The objective of this project is to model a complete **AM transceiver** system, where an input audio message is modulated, multiplexed (using Frequency Division Multiplexing - FDM), and then demodulated using a **super-heterodyne receiver** architecture.

The simulation demonstrates how signals are processed through various stages such as modulation, mixing, filtering, and baseband recovery using **MATLAB**.

---

## ⚙️ System Architecture

### 1. **Transmitter (AM Modulator)**
- Implements **DSB-SC (Double Sideband Suppressed Carrier)** modulation.  
- Each baseband audio message is modulated with a distinct carrier frequency:  
  \[
  f_n = 100 + n\Delta F \text{ (kHz)}, \quad \Delta F = 55 \text{ kHz}
  \]
- Multiple AM signals are combined to form an **FDM signal**.

### 2. **Receiver (Super-Heterodyne Architecture)**
The receiver consists of the following stages:

| Stage | Description |
|--------|-------------|
| **RF Stage** | Band-Pass Filter (BPF) tuned to the desired station for interference rejection. |
| **Mixer + Oscillator** | Frequency conversion using an oscillator at \( \omega_c + \omega_{IF} \), where \( \omega_{IF} = 27.5 \text{ kHz} \). |
| **IF Stage** | Band-pass filtering around the intermediate frequency (IF). |
| **Baseband Detection** | Mixing and Low-Pass Filtering to retrieve the original message signal. |

---

## 🧠 Key Concepts

- **Amplitude Modulation (DSB-SC)**
- **Frequency Division Multiplexing (FDM)**
- **Super-Heterodyne Receiver**
- **Band-Pass and Low-Pass Filter Design**
- **MATLAB Signal Processing (`fft`, `filter`, `interp`)**

---

## 🧰 Tools & Environment

- **Software:** MATLAB (R2021a or newer recommended)  
- **Functions Used:**  
  - `audioread`, `fft`, `fftshift`, `interp`, `sound`, `filter`, `fdesign.lowpass`, `fdesign.bandpass`
- **Audio Inputs:** `.wav` stereo files (provided)

---


