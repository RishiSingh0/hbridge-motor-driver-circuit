# Oscilloscope Captures

Probe setup for measuring shoot-through on one half-bridge leg:

- **Low-side VGS (N-channel):** probe gate directly, source is GND.
- **High-side VGS (P-channel):** scope math channel `CH1 - CH2`, with CH1 on the PMOS gate and CH2 on the PMOS source (HV+).

If both VGS traces show the FETs in their ON region at the same time during a PWM edge, shoot-through is confirmed.

- [`before/shortthrough.jpg`](before/shortthrough.jpg): original board under PWM. Both VGS traces cross through the linear region at the same time on each edge; the X-shaped overlap is the shoot-through window.
- [`after/shortthroughfix.jpeg`](after/shortthroughfix.jpeg): same probe points after the rework. One VGS is fully off before the other turns on, with a clear non-overlap gap between edges. Verified on both rising and falling transitions of the switching cycle.
