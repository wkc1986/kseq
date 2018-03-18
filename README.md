# kseq: complex standalone sequencer for Pd

## Left column

1. position indicator
2. blue sliders: output value 1. Pitch when in note mode
3. scrub cursor
4. purple sliders: output value 2. Velocity when in note mode
5. position indicator
6. mute switches
7. skip switches
8. reverse switches

## Right column

`pd guts`
1. on/off
2. interval (ms)
3. activate reverse

`pd output`
1. toggle note mode (default CC)
2. MIDI channel for CC and notes
3. last sent values 1 and 2
4. set CC#s

`pd probs`
1. skip probability: if skip is on this step, jump to a random step that has skip on with this probability, otherwise continue
2. reverse probability: if reverse is on this step, reverse current directionality with this probability, otherwise continue

`pd noteset`
Settings related to note output.

**Very much TBD**

1. base note length
2. velocity toggle: when on, note length is (base note length) * (value 2 / 127)
