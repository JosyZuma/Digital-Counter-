Digital Counter (555 + 74LS90)

A binary/decade counter built and simulated in Proteus. A 555 timer generates a clock pulse, which drives a 74LS90 decade counter through its binary states (Q0–Q3), decoded and displayed on a 7-segment output.

This kind of circuit is the basis for things like digital clocks, event counters, frequency dividers, and timing/sequencing circuits — anywhere you need to count pulses without a microcontroller.


How it works
Clock source: 555 timer set up to free-run and generate a continuous square wave, R1 (R7) = 3.3MΩ, R2 (R6) = 3.3MΩ, C1 = 100nF, C2 = 100nF (pin 5 decoupling)
f ≈ 1.44 / ((R1 + 2·R2)·C) ≈ 1.45 Hz (period ≈ 0.69s, duty cycle ≈ 67%)

Slow enough to visually watch the counter step through each digit

Counting: Clock feeds the 74LS90, which counts in binary/BCD and advances Q0→Q3 on each rising edge

Decoding & display: Counter output is decoded by a 74LS47 BCD-to-7-segment driver and shown on a common-anode 7-segment display; R2–R5 (330Ω) limit segment current

Build


Simulated first in Proteus to verify timing and logic transitions


Then built physically on breadboard to confirm real-world behaviour

Waveform captures included: 555 clock output, and 74LS90 output across Q0–Q3 showing the binary count sequence


https://github.com/user-attachments/assets/48efc315-cc7d-4907-adc2-dbe4ab78cf46

Files

Proteus simulation + physical build demo

<img width="333" height="221" alt="Screenshot 2026-07-27 223426" src="https://github.com/user-attachments/assets/deb08cc9-518d-46d9-85f0-8e6c2e04ab20" />




<img width="389" height="218" alt="Screenshot 2026-07-27 223405" src="https://github.com/user-attachments/assets/83febbe3-e2c2-403a-8978-94579996c626" />


<img width="640" height="336" alt="Board Photo" src="https://github.com/user-attachments/assets/84b35956-ec82-4228-8045-589d13549e1a" />




<img width="3024" height="4032" alt="IMG_1604" src="https://github.com/user-attachments/assets/e1046864-ec38-4e4e-b74e-29111af310c7" />




