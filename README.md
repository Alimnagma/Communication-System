# Analog-to-Digital Communication System using BASK

This project implements a complete end-to-end digital communication system in Python, demonstrating the process of analog-to-digital conversion, digital modulation, and non-coherent demodulation using Binary Amplitude Shift Keying (BASK).

## Overview

The system begins by generating an analog cosine wave, which is then ideally sampled and uniformly quantized. The quantized samples are encoded into binary form and converted into an NRZ unipolar waveform. This NRZ signal is used to modulate a carrier using BASK. At the receiver, square-law detection followed by envelope detection is used to recover the transmitted NRZ signal. The recovered binary data is decoded back into quantized samples, and envelope detection is applied to reconstruct the signal. The original and demodulated signals are finally compared to evaluate system performance.

## Signal Processing Chain

- Analog signal generation (cosine wave)

- Ideal sampling

- Uniform quantization

- Binary encoding

- NRZ unipolar line coding

- BASK modulation

- Envelope detection

- Binary decoding

- Signal reconstruction and comparison

## Working of the System

The analog message signal is first generated as a cosine waveform and discretized in time using ideal sampling. These sampled values are then uniformly quantized to a finite set of amplitude levels and encoded into binary form. The binary data is converted into an NRZ unipolar waveform, where logic ‘1’ is represented by a positive voltage level and logic ‘0’ by zero voltage. This NRZ signal acts as the baseband data and modulates a high-frequency carrier using Binary Amplitude Shift Keying (BASK), where the carrier is transmitted only when the data bit is ‘1’.

At the receiver, non-coherent demodulation is performed by passing the received signal through a device, which produces a DC component proportional to the signal envelope along with a high-frequency term. Envelope detection (low-pass filtering) removes the high-frequency component to recover the NRZ waveform. The recovered NRZ signal is then converted back into binary data, decoded into quantized sample values, and envelope detection is applied to reconstruct the signal. Finally, the reconstructed signal is compared with the original analog signal to verify successful transmission and reception.
