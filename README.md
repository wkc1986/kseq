# kseq: complex standalone sequencer for Pd

## Left column

1. position indicator
2. scrub cursor
3. blue sliders: output value 1. Pitch when in note mode
4. purple sliders: output value 2. Velocity when in note mode
5. start/end brackets
6. mute switches
7. skip switches
8. reverse switches

## Right column

`pd guts`
1. on/off
2. interval (ms)
3. reverse switch/status

`pd output`
1. toggle note mode (default CC)
2. MIDI channel for CC and notes
3. last sent values 1 and 2
4. set CC#s

`pd noteset`

1. note length + number box for display 
2. velocity toggle: when on, note length is (base note length) * (value 2 / 127)
3. root MIDI pitch
4. scale selection slider + symbol box for display
5. button to reload `scales.txt` (see below)
6. toggle to quantize pitch; if off, blue sequencer output is used directly as pitch

`pd probs`
1. skip probability: if skip is on this step, jump to a random step that has skip on with this probability, otherwise continue
2. reverse probability: if reverse is on this step, reverse current directionality with this probability, otherwise continue

## scales.txt howto
Add one scale per line in format `$name $pitch0 $pitch1 ...`.
`$pitch0` should probably always be `0`.
Break lines with `;`, e.g.
```
major 0 2 4 5 7 9 11 12 ;
minor 0 2 3 5 7 8 10 12
```
