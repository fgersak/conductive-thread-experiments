# Conductive Thread Experiments

## Goal

Investigate conductive thread behaviour after insulation with lacquer and evaluate its suitability for underwater communication.

---

# Baseline Characterization

Before performing any insulation or communication tests, the electrical resistance of the conductive thread was measured to establish a baseline.

**Resistance:** **30 Ω/m**

This value is used as the reference for comparison with all subsequent modifications, including lacquer-coated threads, individual fibers, and parallel fiber configurations.

# Experiment 1 – UART Communication over Conductive Thread (Dry Conditions)

## Objective

Evaluate whether reliable UART communication can be established over the conductive thread under dry conditions.

## Setup

- Two microcontrollers configured for UART communication
- Conductive thread used as the communication medium
- Common ground connection between devices

## Procedure

1. Connect the transmitter and receiver using the conductive thread.
2. Configure both devices with the same UART settings.
3. Transmit a sequence of test messages.
4. Verify that the received data matches the transmitted data.

## Results

Reliable UART communication was successfully established over the conductive thread in dry conditions. No communication errors were observed during testing, demonstrating that the thread can be used as a transmission medium before applying insulation or introducing water. However, in further experiments we will use I²C communication because we have multiple sensors that have to be able to communicate. This experiment serves as a baseline communication test and confirms the functionality of the system under ideal conditions.

# Experiment 2 – I²C Communication over Conductive Thread (Dry Conditions)

## Objective

Evaluate whether reliable I²C communication can be established over the conductive thread under dry conditions.

## Setup

- Two microcontrollers configured for I²C communication
- Conductive thread used as the communication medium
- Common ground connection between devices

## Procedure

1. Connect the I²C master and slave using the conductive thread.
2. Configure both devices with matching I²C settings.
3. Perform data transfers between the master and slave.
4. Verify that all transmitted data is received correctly.

## Results

I²C communication over the conductive thread was successfully demonstrated under dry conditions. The system was able to transfer data correctly in most tests, showing that the uncoated conductive thread can be used as an I²C transmission medium in air. Occasional communication failures were observed, which were attributed primarily to poor contact quality between the Arduino pins and the conductive thread rather than limitations of the thread itself.
## Notes

This experiment extends the baseline evaluation by demonstrating that both UART and I²C communication protocols operate reliably over the uncoated conductive thread under dry conditions.

# Experiment 3 – Coated Conductive Thread Evaluation

## Objective

Evaluate the effect of applying an insulating coating to the conductive thread and determine whether the coating provides electrical isolation while maintaining conductivity through the thread.

## Setup

- Conductive thread coated with insulating lacquer
- Multimeter for resistance measurements
- Water used for leakage testing
- Same thread length and measurement points as previous experiments

## Procedure

1. Apply a couple of layers of insulating coating to the conductive thread.
2. Allow the coating to fully dry.
3. Measure the resistance through the thread to verify that conductivity is maintained.
4. Submerge the coated thread in water and test communication.

## Results

The conductive thread remained electrically conductive after applying the coating. The resistance through the thread remained within the expected range, confirming that the coating process did not interrupt the conductive path.

The coated thread showed improved electrical isolation when submerged in water, with significantly reduced leakage compared to the uncoated thread. However, the communication couldn't be established. The quality and thickness of the coating layer could have had a significant impact on insulation performance. Areas with incomplete coating coverage could still allow leakage through direct contact with water.

# Experiment 4 – Individual Fibers

## Objective

Investigate the electrical properties of individual conductive fibers separated from the original bundled thread. The goal is to determine how the resistance changes when using a single fiber instead of the complete thread structure and to evaluate its suitability for future insulated and parallel configurations.

# Conclusions

...
