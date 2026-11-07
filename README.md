# belaui

Control-layer software for the Cellographic video cello's Bela Mini performance interface.

## Hardware
- Bela Mini
- Trill Craft (capacitive stainless-steel pads on the upper-bout ribs)
- Trill Flex (slider)
- Pressable notched endless encoder (page select)
- 0.96" 128×64 SSD1306 OLED readout

## Structure (planned)
- **C++ control layer** — reads pads, slider and encoder; runs the page system, clock and presets; drives the OLED; sends named parameters to the sound layer and MIDI/OSC out.
- **Pure Data sound layer** — one abstraction per control page (I/O levels, delay, reverb, harmonizer, freeze, filter, drum synth, FM synth, looper).

## How changes are made
All work after this first commit happens on branches and arrives as pull requests. The owner (Scott / Cellographic) merges.
