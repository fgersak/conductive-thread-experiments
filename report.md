# Conductive Thread Experiments

## Goal

Investigate conductive thread behaviour after insulation with lacquer and evaluate its suitability for underwater communication.

---

| Experiment | Description |
|------------|-------------|
| Baseline | Resistance measurement |
| 1 | UART communication |
| 2 | I²C communication |
| 3 | Spray lacquer coating |
| 4 | Individual fibers |
| 5 | Liquid lacquer coating |

# Baseline Characterization

Before performing any insulation or communication tests, the electrical resistance of the conductive thread was measured to establish a baseline.

The measured resistance of the original conductive thread was approximately 30 Ω/m. This value is used as the reference for all subsequent experiments.

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

Reliable UART communication was successfully established over the conductive thread in dry conditions. No communication errors were observed during testing, demonstrating that the thread can be used as a transmission medium before applying insulation or introducing water. Although UART communication proved reliable, subsequent experiments focuse on I²C communication, as the intended application requires multiple sensors to communicate over the same interface. This experiment serves as a baseline communication test and confirms the functionality of the system under ideal conditions.

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

The coated thread showed improved electrical isolation when submerged in water, indicating that the lacquer reduced direct electrical contact with the surrounding water. However, reliable communication could not be established. This suggests that, although the insulation improved, the applied coating was not sufficient to maintain reliable communication under submerged conditions. The quality and thickness of the coating layer could have had a significant impact on insulation performance. Areas with incomplete coating coverage could still allow leakage through direct contact with water.

# Experiment 4 – Individual Fibers

## Objective

Investigate the electrical properties of individual conductive fibers separated from the original bundled thread. The goal is to determine how the resistance changes when using a single fiber instead of the complete thread structure and to evaluate its suitability for future insulated and parallel configurations.

## Results

The original conductive thread was successfully separated into two individual fibers. As expected, the resistance of each individual fiber was approximately twice that of the original bundled thread.

However, it was observed that each fiber consists of numerous thin metallic filaments. During the separation process, these filaments became more susceptible to separating from one another, making the fibers mechanically fragile and significantly more difficult to coat uniformly with insulating lacquer.

As a result, the coating quality was inferior to that achieved with the original bundled thread, making the individual fibers less suitable for reliable insulation using the current coating method.

# Experiment 5 – Liquid Lacquer Coating

## Objective

Evaluate whether a liquid insulating lacquer provides a more uniform coating of the conductive fibers compared to the previously used spray lacquer.

## Setup

- Conductive threads
- Liquid insulating lacquer
- Multimeter
- Water for leakage testing

## Procedure

1. Apply the liquid lacquer to the individual fibers.
2. Allow the coating to fully cure.
3. Inspect the coating for uniformity.
4. Measure the electrical resistance of the coated fibers.
5. Perform leakage tests in water.

## Results

It was expected that the liquid lacquer would produce a more uniform coating than the spray lacquer by better penetrating and covering the surface of the fibers. However, the results did not show a noticeable improvement.

As observed in the previous experiment, each fiber consists of numerous thin metallic filaments. During handling and separation, these filaments tended to spread apart, making it difficult for the lacquer to form a continuous insulating layer. Consequently, the liquid lacquer did not provide sufficient insulation, and the overall coating quality remained unsatisfactory.

## Conclusion

Replacing the spray lacquer with a liquid insulating lacquer did not resolve the coating challenges. The primary limitation appears to be the multi-filament structure of the conductive fibers rather than the coating method itself. Alternative insulation techniques or different conductive thread constructions should be investigated in future work.

# Overall Conclusions

The experiments demonstrated that conductive thread can reliably support both UART and I²C communication in dry conditions. Applying an insulating coating preserved the electrical conductivity of the thread but did not result in reliable underwater communication. Further investigation revealed that the multi-filament structure of the thread makes it difficult to achieve a continuous insulating layer, even when using different coating methods.

Future work will focus on evaluating alternative insulation techniques and investigating whether multiple insulated fibers connected in parallel can provide improved electrical performance while maintaining adequate insulation.
...
