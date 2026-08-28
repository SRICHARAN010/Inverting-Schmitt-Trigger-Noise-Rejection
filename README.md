# Inverting Schmitt Trigger for Noise Rejection

An analog circuit project implementing an **LM741-based Inverting Schmitt Trigger** to provide stable switching in the presence of noisy input signals.

The circuit was designed to create a **hysteresis window between 1V and 3V**, preventing rapid output switching caused by small noise variations. The design was validated through **LTspice simulation**, followed by **hardware implementation and testing**.

---

## 📌 Features

- LM741 op-amp based Inverting Schmitt Trigger
- Hysteresis window from **1V to 3V**
- Noise-resistant switching operation
- Positive feedback for hysteresis generation
- LTspice simulation and waveform analysis
- Hardware implementation and testing
- Threshold voltage calculation
- Digital Storage Oscilloscope (DSO) verification
- PCB schematic and layout design

---

##  Objective

The objective of this project is to design and implement an **Inverting Schmitt Trigger circuit** that creates a hysteresis window between:

- **Upper Threshold Voltage (VUT): 3V**
- **Lower Threshold Voltage (VLT): 1V**

The hysteresis window prevents unwanted rapid switching when the input signal contains noise.

---

## System Architecture

```text
              Noisy Input Signal
                     │
                     ▼
             ┌───────────────┐
             │ Input Resistor│
             │    Network    │
             └───────┬───────┘
                     │
                     ▼
             ┌───────────────┐
             │     LM741     │
             │ Operational   │
             │ Amplifier     │
             └───────┬───────┘
                     │
          ┌──────────┴──────────┐
          │                     │
          ▼                     │
    Stable Output          Positive Feedback
          │                     │
          └─────────────────────┘
                     │
                     ▼
              Hysteresis
             1V ───── 3V
