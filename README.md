# ECE 145 Analog Function Generator

This is our ECE 145 Honors Project (Fall 2026) at UIUC. We are building a function generator out of analog parts that outputs square, triangle, and sine waves. It runs off a single 12 V supply. One knob sets the frequency, and each output has its own amplitude knob.

Team: Tommy Liu, Sean Fang, Dang Nguyen

## How it works

The circuit is split into four blocks:

- Block A makes a 6 V reference from the 12 V supply using a resistor divider and a TL074 op amp. The other blocks use this 6 V as their ground.
- Block B is an oscillator built with an LM13700. It makes the triangle and square waves.
- Block C turns the triangle into a sine wave using a matched transistor pair (SSM2212).
- Block D has three op amp stages that set the amplitude of each output.

## Folders

- `ltspice` has the LTspice schematics for each block.
- `kicad` has the KiCad schematic and PCB files.
- `docs` has our final proposal.

## Running the simulations

Open any of the `.asc` files in LTspice and run it. The Block B file needs `LM13700_sim.lib` and `LM13700_v2.asy` in the same folder, which they already are. We used our own simple LM13700 model because the one from TI would not run in LTspice.

## Status

- Block A: built and tested
- Block B: built and tested, tunes from about 300 Hz to 14 kHz
- Block C: being built
- Block D: simulated, not built yet
