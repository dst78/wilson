# Wilson :: Sample and Hold

This is a relatively straight forward combined noise and sample & hold circuit, with a bunch of adjustment capabilities.

- External sample source and trigger inputs.
- White noise output, S&H output.
- Adjustment knobs for internal sampling rate, S&H range and transposition.

Note that the external trigger input needs *extremely* steep flanking signals. To be honest, I might have overdone this. Consider changing R3 and R4 to higher values if your trigger source doesn't trigger the sampling.

The internal clock is capable of ranges roughly between 0.2Hz and 20Hz.

The sample output can be adjusted in two ways:

- The R13 shift pot transposes the voltage range up and down.
- The R19 range pot increases / decreases the range of voltages.

Note that R13 and R19 are somewhat interdependent.

## Internal trimming abilities

- R12 noise amplification
- R14 noise transposition

Tweak these until the noise out is in the -5V to 5V range.

- R11 S&H amplification

Tweak this until the S&H out is in the -5V to 5V range when the output attenuator R19 is fully open and R13 is centered.


## External Connections

- Input jack for external triggers (normalled to internal clock)
- Input jack for external sampling source (normalled to noise)
- Output jack for noise
- Output jack for S&H signal

- Potentiometer for internal clock rate adjustment
- Potentiometer for S&H transposition (shifts possible voltage range up/down)
- Potentiometer for output attenuation (attenuates voltage range, not volume)

## What's in the name?

The module was named in honor of Nobel price laureates Robert Wilson and Arno Penzias for their discovery of cosmic microwave background radiation.

## Possible improvements

- replace R3/C3 and R4/C4 to allow slightly slower trigger flanks.
- clock LED is hardwired to the internal signals, could move it to flash with external triggers as well.
- change R13 to be less sensitive.
