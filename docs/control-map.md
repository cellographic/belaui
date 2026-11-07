# Cellographic Bela UI — Control Map (DRAFT v0.4)

**v0.4 changes:** T4 moves up next to SNARE, T5 directly under T4, SENC below that beside the Flex slider. SENC works like the page encoder: turn previews, press locks in. Slider is relative — no jumps.

**v0.3 changes:** Option B chosen — a second pressable encoder (SENC) switches the slider's target, and the OLED shows the selection as you turn.

**v0.2 changes:** CANCEL-during-preview approved. P1–P5 are no longer a universal "pick a setting" rule — they are page-specific (notes on some pages, presets on others). The slider now has a default target on every page plus alternate targets; how you switch targets is an open choice (OK/CANCEL vs a second encoder).

**Status:** first draft for Scott's review. Nothing here is final.

**How to read the marks**
- ✅ **Decided** — comes from decisions Scott has already made.
- 💡 **Proposed** — Claude's suggestion. Change, keep, or delete freely.
- ❓ **Open question** — needs Scott's answer before it becomes code.

---

## 1. The physical controls

| ID | Control | Where | Source |
|---|---|---|---|
| P1–P5 | Picker pads | Left rib, running back toward the rear panel | ✅ |
| KICK | Large pad (2.5" × 1.75") | Left rib, in front of pickers 2–4 | ✅ |
| ENC | Pressable notched endless encoder | Left rib, toward the cello's face | ✅ |
| T1–T3 | Thumb pads | Right corner piece, front to back along the corner block | ✅ |
| SLIDER | Trill Flex slider | Upper-right, near the face, from above T1–T3 to about mid upper bout | ✅ |
| T4 | Thumb pad (percussion size) | Right next to SNARE | ✅ |
| T5 | Thumb pad (percussion size) | Directly under T4 | ✅ |
| SNARE | Large pad, like KICK | Upper-right, above the slider | ✅ |
| OLED | 0.96" 128×64 blue/yellow screen | Upper-right, back half of the rib | ✅ |
| OK / CANCEL | Confirm / cancel pads | Behind the OLED | ✅ |
| SENC | Second pressable encoder — slider target | Below T5, next to the Flex slider | ✅ |
| PEDAL | External foot pedal | Floor | ✅ |

Total capacitive pads: 14 (P1–P5, KICK, T1–T5, SNARE, OK, CANCEL), all on one Trill Craft (30 channels available). Slider is the Trill Flex.

---

## 2. The grammar (the same on every page)

Having one consistent "grammar" means your hands learn the instrument once, and every page just changes *what* the controls point at.

| Control | Job on every page | Source |
|---|---|---|
| ENC turn | Preview another page on the OLED (sound doesn't change yet) | ✅ |
| ENC press | Lock in the previewed page | ✅ |
| CANCEL during preview | Abandon the preview, stay on the current page | ✅ |
| **P1–P5** | **Page-specific.** Note values on some pages, preset selection on others — no universal rule. | ✅ |
| **SLIDER** | **Has a default target on every page**, plus a list of alternate targets per page. | ✅ |
| SENC turn | Preview the slider's next/previous target for this page. The OLED shows the target name and current value, so you can confirm visually if notch counting fails. The slider keeps controlling the old target until you press. | ✅ |
| SENC press | Lock in the previewed target | ✅ |
| CANCEL during SENC preview | Abandon the preview, keep the current target (same as the page encoder) | 💡 |
| Back to default target | 💡 The default is always first in the list, so turning all the way back reaches it. ❓ Want a faster shortcut (e.g. long-press SENC)? | 💡 |
| OK / CANCEL | Reserved for confirmations (store, clear) and CANCEL-during-preview — never used for slider targets | ✅ |
| T1–T5 | Page-specific switches and actions (on/off, tap, latch, trigger) | 💡 |
| KICK / SNARE | Page-specific big "performance" hits (momentary throws, triggers) | 💡 |
| OK / CANCEL | Confirm or cancel anything that destroys or overwrites (store, clear) | 💡 |
| PEDAL | Loop controls — record, navigate, retrieve, store, create — on every page | ✅ |
| (rule) | Pad assignments are unique per page; manual triggering only on the current page | ✅ |
| (rule) | Settings and running sequences (sample sequences, drum patterns) keep going when you change pages | ✅ |

### ✅ How the slider switches targets — Option B chosen
| | A: OK / CANCEL step through targets | B: Second pressable encoder for the slider |
|---|---|---|
| Hardware | Nothing new | One more encoder + mount on the right rib (3 more digital pins) |
| How it plays | OK = next target, CANCEL = previous | Turn = choose target, press = back to page default |
| Conflict | OK/CANCEL also answer "are you sure?" prompts — a stray tap could confirm a clear/store | None — OK/CANCEL stay reserved for confirmations |
| Eyes-free | Need to count taps or glance at OLED | Notched detents can be counted by feel |

### ✅ Slider behaviour: relative, not absolute
Because one slider controls many settings, an absolute slider would make values **jump** when you touch it. Proposal: the slider works **relative to the current value**. Touch anywhere and slide up or down to nudge the value from where it already is, like a scroll wheel. No jumps, ever.
✅ Decided: every touch starts from the value's last setting.

### 💡 OLED layout
The Elegoo screen has a yellow top band and a blue lower area.
- **Yellow band:** page name · loop/clock status (recording / playing / bar count)
- **Blue area:** picked setting name + big value bar, with 5 short labels for P1–P5 along the bottom

---

## 3. The pages

Order follows Scott's priority list. ✅ marks the page itself and any decided feature; per-control assignments are 💡 unless marked.

**v0.2 note:** in the tables below, the five settings listed under P1–P5 are now read as the **slider's target list** for that page — the first one is the default, the rest are alternates. What the P1–P5 *pads* do on each page (notes, presets, etc.) is still to be assigned page by page.

### Page 1 — I/O LEVELS ✅
| Control | Does |
|---|---|
| P1 | Cello (piezo) input gain |
| P2 | Voice / second input gain ✅ second input exists |
| P3 | Main output level |
| P4 | EQ low ❓ (EQ was "maybe") |
| P5 | EQ high ❓ |
| T1 | Mute cello input |
| T2 | Mute voice input |
| T3 | EQ on/off ❓ |
| T4 | OLED shows input meters / output meters (toggle) |
| T5 | Tuner on OLED ❓ (not requested — useful?) |
| KICK / SNARE | — unassigned |

### Page 2 — DELAY ✅
| Control | Does |
|---|---|
| P1 | Time |
| P2 | Feedback |
| P3 | Mix |
| P4 | Tone (darkens repeats) |
| P5 | Send to shared reverb ✅ everything routes through one reverb |
| T1 | Delay on/off |
| T2 | Tap time |
| T3 | Sync time to the loop clock on/off |
| T4 | Hold (infinite repeats while held) |
| T5 | Recorder takes this pre/post delay ✅ pre/post setting per page |
| KICK | "Dub throw": sends cello into the delay only while held |
| SNARE | Clear the delay repeats |

### Page 3 — REVERB (shared) ✅
| Control | Does |
|---|---|
| P1 | Size / decay |
| P2 | Damping (brightness) |
| P3 | Return level |
| P4 | Pre-delay |
| P5 | Direct cello send into reverb |
| T1 | Reverb on/off |
| T2 | Ducking (reverb dips while you play) on/off |
| T3 | Hold tail (very long decay while held) |
| T4 | — unassigned |
| T5 | Recorder pre/post reverb ✅ |
| KICK | Reverb throw (momentary big send) |
| SNARE | Kill tail |

### Page 4 — HARMONIZER (delay-based) ✅
| Control | Does |
|---|---|
| P1 | Voice 1 interval |
| P2 | Voice 2 interval |
| P3 | Mix |
| P4 | Detune / stereo spread |
| P5 | Send to shared reverb |
| T1 | Harmonizer on/off |
| T2 | Voice 2 on/off |
| T3 | Snap intervals to a scale on/off ❓ which scales? |
| T4 | Octave-down voice on/off |
| T5 | Recorder pre/post harmonizer ✅ |
| KICK / SNARE | ❓ unassigned — ideas welcome |

### Page 5 — FREEZE (grain-based) ✅
| Control | Does |
|---|---|
| P1 | Grain size |
| P2 | Density |
| P3 | Spread (position jitter) |
| P4 | Pitch |
| P5 | Freeze level |
| T1 | Capture freeze (latch) |
| T2 | Add a layer on top of the current freeze |
| T3 | Clear freeze (asks OK/CANCEL) |
| T4 | Fade time in/out |
| T5 | Recorder pre/post freeze ✅ |
| KICK | Momentary freeze (only while held) |
| SNARE | Release / fade out freeze |

### Page 6 — FILTER ✅
| Control | Does |
|---|---|
| P1 | Cutoff |
| P2 | Resonance |
| P3 | Envelope follower amount ✅ |
| P4 | Envelope follower speed (attack/release) |
| P5 | Sweep rate ✅ filter sweep |
| T1 | Filter on/off |
| T2 | Filter type: low-pass → band-pass → high-pass (cycles) |
| T3 | Envelope follower on/off ✅ |
| T4 | Sweep on/off ✅ |
| T5 | Recorder pre/post filter ✅ |
| KICK | One-shot sweep trigger |
| SNARE | — unassigned |

### Page 7 — DRUM SYNTH ✅
Patterns are tapped in on pads ✅ and keep running on other pages ✅, synced to loops ✅.
| Control | Does |
|---|---|
| KICK | Kick drum |
| SNARE | Snare drum |
| T1–T3 | Hi-hat, open hat, percussion |
| T4 | Pattern record arm (taps get recorded into the loop-length pattern) |
| T5 | Clear pattern (asks OK/CANCEL) |
| P1 | Kick tune / decay |
| P2 | Snare tone |
| P3 | Hat decay |
| P4 | Swing |
| P5 | Drum level |
| OK | Store pattern to a slot ❓ how many slots? |

### Page 8 — FM SYNTH ✅
Sequenced in sync with loops ✅.
| Control | Does |
|---|---|
| T1–T5 | Play 5 notes of the chosen scale ❓ |
| KICK | Sequence record arm |
| SNARE | Clear sequence (asks OK/CANCEL) |
| P1 | Ratio (timbre) |
| P2 | Index (brightness) |
| P3 | Envelope length |
| P4 | Root note / scale |
| P5 | Level |
❓ Is the FM synth mainly a bass voice, a pad, or a lead? That changes which 5 settings matter most.

### Page 9 — LIGHTING (internal cello LEDs) ✅
| Control | Does |
|---|---|
| T1–T5 | Lighting scenes 1–5 |
| P1 | Brightness |
| P2 | Colour (hue) |
| P3 | Saturation |
| P4 | Speed |
| P5 | Audio reactivity (how much the cello drives the light) |
| KICK | Flash / strobe while held |
| SNARE | Blackout toggle |
Stage DMX: later ✅, not in this version.

### Page 10 — RECORDER / LOOPER / SAMPLER ✅
The pedal does record / navigate / retrieve / store / create everywhere ✅. This page holds the settings ✅ and loop tricks ✅.
| Control | Does |
|---|---|
| P1 | Loop level |
| P2 | Overdub decay (how fast old layers fade) |
| P3 | Playback speed |
| P4 | Sample start / trim |
| P5 | Crossfade time |
| T1 | Reverse ✅ loop trick |
| T2 | Half speed ✅ loop trick |
| T3 | Stutter / retrigger ✅ loop trick |
| T4 | Assign last recording to a pad (then touch the destination pad) ✅ record button records samples assigned to pads |
| T5 | Recorder default: pre or post effects (global) ✅ default is post |
| KICK / SNARE | ❓ Sample pads? |
❓ **Big one:** which pads play back samples, and on which page? Your rule says manual triggering happens only on the current page. Should this page turn its pads into sample pads, or should samples live on their own page?

### Page 11 — RESOLUME ✅
| Control | Does |
|---|---|
| T1–T5 | Trigger clips 1–5 in the current column |
| KICK | Next column |
| SNARE | Visual flash / strobe effect |
| P1–P5 | Five mapped Resolume parameters (opacity, effect amounts) ❓ which ones? |
❓ How does Bela talk to Resolume: MIDI or OSC over the network? (Bela Mini has no built-in Wi-Fi.)

### Page 12 — MIDI OUT (low priority) ✅
Channels 1–10 for flexibility ✅. Placeholder: P1 picks channel, slider sends a CC, T1–T5 send notes. Defined later.

---

## 4. Open questions — summary

0. ~~Slider target switching~~ — decided: second encoder (B), below T5 beside the slider.
0b. P1–P5 pad roles, page by page (notes / presets / other).
1. ~~Slider mode~~ — decided: relative, no jumps. New: shortcut back to the default slider target (long-press SENC?)
2. Page 1: EQ yes/no? Tuner wanted?
3. Harmonizer: which scales for interval snapping? KICK/SNARE ideas?
4. Drums: how many pattern slots?
5. FM synth: bass, pad, or lead?
6. **Samples: which pads play them, and on which page?**
7. Resolume: MIDI or OSC? Which 5 parameters?
8. Foot pedal: what model, and how does it connect (USB MIDI, or wired to Bela's digital inputs)?
9. Is 12 pages the right number, or should some pages merge?
