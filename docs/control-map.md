# Cellographic Bela UI — Control Map (DRAFT v0.4)

**v0.19 changes:** P1–P8 on the SONG page choose the active TRIG bank. Bank 1 defaults to drums; bank 8 defaults to loop tricks on TRIG1–TRIG3 (TRIG4 reserved for another loop effect). Bank-select conflict resolved.

**v0.18 changes:** Thumb pads T1–T3 renamed **P6–P8** (they work like P1–P5, so pads are now P1–P8). 8 TRIG banks = 32 trigger slots. SONG page P6–P8 default to loop tricks. Three ways to play any pad defined: live, recorded into the loop audio, or recorded as a sequence.

**v0.17 changes:** Standing rule: parts stay separate (loops vs sequences). Arrangement is built by playing TRIG pads in time. TRIG banks selected from the SONG page, bank number on the OLED. Pedal confirmations for store/delete approved.

**v0.16 changes:** Overdubs vs secondary loops defined. Secondary loops snap to LOOP by default, BAR as an option (shorter sections like a chorus or bridge). Saving: hold B3 saves everything; OK in Page Options saves just that page.

**v0.15 changes:** New design rules: (1) any "default" implies other options, normally in that function's Page Options; (2) **blinking = unconfirmed, solid = confirmed** everywhere. Song timing options are bars-per-loop and beats-per-bar (custom time signatures). Page 10 renamed **SONG**. Expression assignment flow defined. Loops snap to the first loop's length; samples trigger freely, quantization optional.

**v0.14 changes:** Double-tap B3 creates a new song. Song structure defined: the first loop sets the tempo (16 beats of 4/4); sequences run for one or more loop lengths; multiple loops per song, stored to TRIG pads; a song can arrange several loops. SENC far right = EXPRESSION OPTIONS (expression pedal, default master volume).

**v0.13 changes:** Pedal reworked around songs: B1 hold behaviour depends on whether you're starting or ending a take; B3/B4 tap navigate songs, hold B3 = store, hold B4 = delete; B2 hold clears the loop without saving. Song switch timing default = end of loop, with end-of-bar / immediate as a page option. Page 10 renamed Song/Loop/Record.

**v0.12 changes:** Unsaved-changes marker approved. Foot pedal = Hotone Ampero Control (4 switches): B1 record/overdub (hold = erase last layer), B2 stop (hold = erase), B3/B4 = song previous/next (cue), B1 accepts the cued song. Songs can be cued from any page.

**v0.11 changes:** SENC stops at both ends; the far right also lands on PAGE OPTIONS for now (reserved for a future universal endpoint). 8 toggle slots and OK = Store approved. CANCEL keeps changes live until the song changes, but they are not saved.

**v0.10 changes:** TRIG3 = hi-hat, TRIG4 = open hat by default. New **Page Options mode**: turning SENC all the way left reaches PAGE OPTIONS; press to enter; pads toggle page-specific preferences shown on the OLED; OK stores them to the song; CANCEL escapes. Displaced toggles (pre/post etc.) move here.

**v0.9 changes:** Record-arm on T1–T3 withdrawn. Drum and FM pages get SOUND / SEQUENCE modes chosen with OK/CANCEL (tap steps, hold OK enters). Sequences are stored into persistent triggers. Thumb pads T4/T5 become **TRIG3 / TRIG4**; page-specific thumb pads are now T1–T3 only. Displaced T4/T5 functions are parked below.

**v0.8 changes:** Assign mode details approved (record-arm on T1–T3 later withdrawn in v0.9).

**v0.7 changes:** Assignment moves to **Assign mode**, entered by holding OK (replaces hold-a-pad). Because pads no longer need hold detection, playable pads fire on press (no delay); OK/CANCEL fire on release. The word "arm" is now reserved for record-arming.

**v0.6 changes:** Hold-to-arm is the general pattern. Holding an assigned pad clears it and arms it to receive a new assignment. The OLED shows an armed marker (• or *). Taps fire on release so a hold never triggers — ❓ except possibly playable pads (see "Tap timing").

**v0.5 changes:** KICK and SNARE are renamed **TRIG1 / TRIG2 (persistent triggers)**. They play kick and snare on every page by default, and can be reassigned to a sample or a synth note that also plays on every page. All earlier page-specific KICK/SNARE ideas are removed (parked list in section 2).

**v0.4.1:** Long-press SENC returns the slider to the page's default target.

**v0.4 changes:** T4 moves up next to SNARE (now TRIG2), T5 directly under T4, SENC below that beside the Flex slider. SENC works like the page encoder: turn previews, press locks in. Slider is relative — no jumps.

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
| TRIG1 | Large pad (2.5" × 1.75") — persistent trigger 1 (was KICK) | Left rib, in front of pickers 2–4 | ✅ |
| ENC | Pressable notched endless encoder | Left rib, toward the cello's face | ✅ |
| P6–P8 | Thumb pads | Right corner piece, front to back along the corner block | ✅ |
| SLIDER | Trill Flex slider | Upper-right, near the face, from above P6–P8 to about mid upper bout | ✅ |
| TRIG3 | Persistent trigger 3 (was thumb pad T4, percussion size) | Right next to TRIG2 | ✅ |
| TRIG4 | Persistent trigger 4 (was thumb pad T5, percussion size) | Directly under TRIG3 | ✅ |
| TRIG2 | Large pad, like TRIG1 — persistent trigger 2 (was SNARE) | Upper-right, above the slider | ✅ |
| OLED | 0.96" 128×64 blue/yellow screen | Upper-right, back half of the rib | ✅ |
| OK / CANCEL | Confirm / cancel pads | Behind the OLED | ✅ |
| SENC | Second pressable encoder — slider target | Below TRIG4, next to the Flex slider | ✅ |
| PEDAL | External foot pedal | Floor | ✅ |

Total capacitive pads: 14 (P1–P5, P6–P8, TRIG1–TRIG4, OK, CANCEL), all on one Trill Craft (30 channels available). Slider is the Trill Flex.

---

## 2. The grammar (the same on every page)

### ✅ Design rules
1. **Defaults imply options.** Whenever a rule names a default, other choices exist, normally set in that function's Page Options.
2. **Blinking = unconfirmed, solid = confirmed.** In any preview or pending choice (page encoder, slider encoder, song cue, Assign mode, expression assignment, confirm prompts) the option name on the OLED **blinks** until confirmed, then goes **solid**. Turning back to the current option shows it blinking too, until you confirm or cancel.
3. **Three ways to play any pad.** (a) **Live** — heard, not recorded. (b) **Into the loop** — while the loop is recording or overdubbing, the pad's sound is recorded into that audio layer. (c) **Sequence record mode** — the triggered events are recorded as a sequence, kept separate from the audio layers.
4. **Parts stay separate.** Cello loops, drum sequences and synth sequences are stored independently. Clearing the recordings keeps all sequences, and sequences are never baked into the recording, so either can be changed or removed without touching the other.

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
| SENC long-press | Jump straight back to this page's default slider target (💡 hold time about 0.6 s, tunable) | ✅ |
| OK / CANCEL | Reserved for confirmations (store, clear) and CANCEL-during-preview — never used for slider targets | ✅ |
| P6–P8 | Page-specific switches and actions (on/off, tap, latch, trigger) | ✅ |
| TRIG1–TRIG4 | **Persistent triggers** — work on every page. Default: TRIG1 = kick, TRIG2 = snare, TRIG3 = hi-hat, TRIG4 = open hat. Each can hold a sample, a synth note, or a **stored sequence**, and works on every page. | ✅ |
| (rule) | TRIG1/TRIG2 are the deliberate exception to "manual triggering only on the current page" | ✅ |
| **Assign mode** step 1 | On an assignable page, **hold OK** → OLED shows **?** (waiting for a target pad) | ✅ |
| Assign mode step 2 | Touch the pad to assign → **?** becomes **>** (waiting for a source). The touch does **not** play the pad. | ✅ |
| Assign mode step 3 | The next sample / drum / sequence / synth note selected on this page is assigned to that pad. OLED briefly shows the result, e.g. "TRIG1 = Sample 3". | ✅ |
| Old assignment | Kept until the new one lands, so backing out loses nothing | ✅ |
| Backing out | CANCEL at ? or > exits Assign mode with no change; changing page also exits | ✅ |
| Clearing a pad to empty | At >, hold CANCEL = clear that pad | ✅ |
| Non-assignable pages | Holding OK shows "no assign here" | ✅ |
| Assignable targets | TRIG1/TRIG2 from any assignable page, plus that page's own pads | ✅ |
| Restore kick/snare to TRIG1/TRIG2 | 💡 a "reset triggers" option on the drum page | 💡 |
| **Drum & FM pages: mode select** | **Tap OK / CANCEL** steps between options — **SOUND** or **SEQUENCE** (shown on OLED). **Hold OK** enters the highlighted mode. | ✅ |
| SOUND mode | Choose individual drum sounds / synth notes and assign them to pads (the Assign mode ? → > flow) | ✅ |
| SEQUENCE mode | Play hits/notes in time to record a sequence, then store it in a persistent trigger (TRIG1–TRIG4) | ✅ |
| CANCEL in modes | Cancels arming; hold CANCEL erases (with the usual confirm) | ✅ |
| Prompt priority | When an "are you sure?" prompt is showing, OK/CANCEL answer it and never step modes | ✅ |
| (also) | "Only a deliberate action counts as choosing a source" (pad hit, note played, or encoder press on a list) | ✅ |
| OK / CANCEL | Confirm or cancel anything that destroys or overwrites (store, clear) | ✅ |
| PEDAL | Loop controls — record, navigate, retrieve, store, create — on every page | ✅ |
| (rule) | Pad assignments are unique per page; manual triggering only on the current page | ✅ |
| (rule) | Settings and running sequences (sample sequences, drum patterns) keep going when you change pages | ✅ |

### ❓ Tap timing — fire on press or on release
✅ Resolved by Assign mode (v0.7): **playable pads fire on press** (immediate). Only **OK / CANCEL** fire on release, because they distinguish tap from hold. Table below kept for the record.
Earlier (v0.6): taps fire on **release**, so a press-and-hold never triggers by accident.
⚠️ Trade-off: on *playable* pads (TRIG1/TRIG2, drum pads, note pads) a release-trigger delays every hit by however long your finger is down (often around 0.1 s; estimate, not measured). That will feel late for drums.

| | A: Release on every pad | B: Press for playable pads, release for function pads |
|---|---|---|
| Accidental triggers when holding | Never | Never on function pads; on playable pads the first hit sounds, then the hold arms |
| Feel for drums/notes | Late, by the length of the tap | Immediate |
| Consistency | One rule everywhere | Two rules, split by pad type |

### ✅ Page Options mode (v0.10)
| Step | What happens | Source |
|---|---|---|
| Reach it | Turn SENC all the way left, past the slider targets, to **PAGE OPTIONS** | ✅ |
| Enter | Press SENC | ✅ |
| Use | Pads toggle this page's preferences (behaviour switches, not performance). The OLED shows each toggle's on/off state. | ✅ |
| Store | OK saves **just this page's** options to the song (a quick save). Holding B3 on the pedal saves **everything**, including any unsaved page changes. | ✅ |
| Leave | CANCEL escapes Page Options mode | ✅ |
| Encoder ends | SENC stops at both ends (no wrap-around), so the ends are reliable landings | ✅ |
| Which pads toggle | P1–P8 = 8 toggle slots per page. TRIG1–TRIG4 stay live so you can keep playing. | ✅ |
| Unsaved changes on CANCEL | Stay active until the song changes, but are not saved — loading the song again restores its stored settings | ✅ |
| Unsaved marker | A small mark on the OLED while a page has unsaved option changes | ✅ |
| "Song" | ❓ New concept — how is a song chosen and loaded (pedal retrieve? a Songs page?) | ❓ |

**💡 Toggle candidates per page (from displaced items):**
- Delay, Reverb, Harmonizer, Freeze, Filter: **Recorder pre/post** ✅ feature
- Delay: sync to loop clock · Reverb: ducking · Harmonizer: octave-down voice, scale snap · Freeze: fade in/out · Filter: sweep on/off ✅ feature, envelope follower on/off
- I/O: meter view input/output · tuner · EQ on/off
- Sampler: global recorder pre/post default ✅ feature
- Momentary performance actions (delay hold, freeze capture) stay on P6–P8, not in options

### ✅ Expression Options mode (v0.14) — SENC far right
| Step | What happens | Source |
|---|---|---|
| Reach it | Turn SENC all the way right until **EXPRESSION** blinks | ✅ |
| Enter | Press SENC → the arming marker appears on the OLED | ✅ |
| Choose | Turn SENC left; each notch blinks the next control the pedal could take over | ✅ |
| Assign | Press SENC → that control is assigned to the expression pedal and goes solid | ✅ |
| Leave without changing | 💡 CANCEL | 💡 |
| Save to the song | 💡 Same as Page Options: unsaved marker until OK stores it | 💡 |
| Default target | Expression pedal = **master output volume** | ✅ |
| Other targets | Chosen here — anything the slider can control (the same "variable output" list) | ✅ |
| 💡 Scope | Expression assignment is global (works on every page) and saved with the song, so master volume never depends on which page you're on | 💡 ❓ |
| Hardware | An expression pedal plugged into one of the Ampero Control's 2 TRS jacks (max 10 kΩ pot); it reaches the Bela as MIDI | 💡 |
| 💡 Second jack | Room for a second expression pedal or extra footswitches later | 💡 |

### Foot pedal — Hotone Ampero Control (v0.13)
**Paradigm:** the **song** is the stored unit. A song holds its loop recordings, loop length, drum/synth sequences and page options (💡 and TRIG assignments + effect settings ❓). The pedal covers navigate, retrieve, store, create and delete for songs, plus record control, from any page.

| Switch | Tap | Hold | Source |
|---|---|---|---|
| B1 | Record / overdub (starts **on press**) | Depends on when you hold — see below | ✅ |
| B2 | Stop | Clear all recordings in the current loop. Keeps loop length, sequences, page options. **Not saved** — reloading the song restores them unless you store. | ✅ |
| B3 | Song: previous → enters song-selection mode. **Double-tap = create a new song** | **Store** the song | ✅ |
| B4 | Song: next → enters song-selection mode | **Delete** the selected song from storage | ✅ |
| B1 in song-selection mode | Accept → load the cued song | — | ✅ |
| B2 in song-selection mode | Cancel the cue | — | ✅ |

**B1 hold — two behaviours, decided by state:**
| You hold B1 when… | Result | Source |
|---|---|---|
| Starting a take (not currently recording) | Nothing new is recorded, and the previous layer is erased (step back). If this was the first recording, loop recording is cancelled. Repeat to step back further. | ✅ |
| Ending a take (currently recording) | The take you just made is erased; earlier layers stay | ✅ |

**Song switching:** default = at the end of the loop ✅. Alternatives "end of bar" and "immediate" are a Page Option on the SONG page ✅. 💡 If nothing is playing, the song loads immediately.

**💡 Proposals:**
- ✅ **Confirm destructive pedal holds.** Store-over-existing (hold B3) and delete (hold B4) show "Store over SONG 4?" / "Delete SONG 4?" on the OLED; **B1 = confirm, B2 = cancel**.
- ~~Create = store into an empty slot~~ — replaced by double-tap B3 ✅. Where the new song goes (next free slot vs right after the current song) is a SONG page option ✅.
- **Double-tap timing:** 💡 a single B3 tap waits ~0.3 s to make sure it isn't a double-tap before moving the cue. Navigation isn't timing-critical, so the small delay should be fine.
- **What hold B3 stores:** the current state into the *selected* slot. If you've cued a different song first, that's a "save as" — the confirm prompt names the target so you can't overwrite by accident.
- **Step-back depth:** keep every layer separately so B1 can step back through all of them. 💡 Memory estimate (not measured): ~11.5 MB per 30 s stereo layer, so roughly 20+ layers fits comfortably in the Bela Mini's RAM.
- **Saving audio during a show:** writing recordings to the SD card happens in the background so audio never glitches; the OLED shows "saving…" until done.
- **Pedal setup:** switches in *momentary* mode (sends press + release); Bela times holds itself.
- **Connection:** USB to start (most reliable); Bluetooth adapter optional later.

### ✅ Song structure (v0.14)
| Rule | Source |
|---|---|
| A new song is defined by its **first loop** | ✅ |
| The first loop's length = **16 beats of 4/4** (default) → that sets the song's tempo, which drives all sequences | ✅ |
| Drum/synth sequences can last one loop length or several, for longer form | ✅ |
| A song can hold **several loops**. The **first loop** sets the song's length unit. Recordings on top of a loop are **overdubs** (layers of that same loop). **Secondary loops** are separate loops; any loop can be stored to a TRIG pad. | ✅ |
| A longer song = an arrangement of loops plus drum/synth sequences, all on the bar grid set by the first loop | ✅ |
| A song can also be as simple as one loop and nothing else | ✅ |
| **Secondary loop length** snaps to the **LOOP** (one or more full lengths of the first loop) by default. SONG page option: **BAR**, which snaps to whole bars, so a chorus or bridge can be shorter than the verse. Either way everything stays on the same beat grid. | ✅ |
| **Samples** are free recordings, triggered with or without quantization. **Default: FREE**; quantize options in SONG page options. | ✅ |
| **Bars per loop** and **beats per bar** are SONG page options, allowing custom time signatures (default 4 bars × 4 beats = 16) | ✅ |
| The **arrangement** is built by playing: loops are assigned to TRIG pads, then you play the pads in time and that sequence is recorded as the song's structure | ✅ |
| 💡 A song saves everything: loops, sequences, arrangement, TRIG assignments, page options and effect settings | 💡 ❓ |
| **TRIG banks.** On the SONG page, **P1–P8 choose the active bank** (1–8). The current bank number shows on the OLED (💡 in the yellow status band, e.g. "BK3"). | ✅ |
| **8 banks × 4 TRIG pads = 32 trigger slots** | ✅ |
| **Bank 8 defaults to loop tricks:** TRIG1 = reverse, TRIG2 = half speed, TRIG3 = stutter; TRIG4 reserved for another loop effect. They can be overwritten if the slots are needed. As triggers they work from any page and can be recorded as sequences. | ✅ |
| 💡 Switching banks changes what the pads trigger **next**; anything already playing keeps playing until stopped | 💡 |
| **Bank 1 defaults to drums** (kick, snare, hat, open hat). 💡 Banks 2–7 start empty. | ✅ |


### Displaced by T4/T5 → TRIG3/TRIG4 (v0.9) — need new homes or can be dropped
- **Recorder pre/post** on Delay, Reverb, Harmonizer, Freeze, Filter (✅ feature) — ✅ now a Page Options toggle
- Recorder global pre/post default (✅ feature, sampler page)
- Filter sweep on/off (✅ feature)
- Delay hold · Harmonizer octave-down · Freeze fade time · I/O meter view · Tuner
- Lighting scenes 4–5 · Resolume clips 4–5 · FM notes 4–5
- Sampler "assign last recording" — now covered by Assign mode ✅

### Parked ideas (removed from KICK/SNARE in v0.5 — could move to T pads if wanted)
Delay dub throw · delay clear · reverb throw · kill reverb tail · momentary freeze · release freeze · one-shot filter sweep · FM sequence record arm / clear (❓ needs a new home) · lighting flash / blackout · Resolume next column / flash.

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
| P6 | Mute cello input |
| P7 | Mute voice input |
| P8 | EQ on/off ❓ |

### Page 2 — DELAY ✅
| Control | Does |
|---|---|
| P1 | Time |
| P2 | Feedback |
| P3 | Mix |
| P4 | Tone (darkens repeats) |
| P5 | Send to shared reverb ✅ everything routes through one reverb |
| P6 | Delay on/off |
| P7 | Tap time |
| P8 | Sync time to the loop clock on/off |

### Page 3 — REVERB (shared) ✅
| Control | Does |
|---|---|
| P1 | Size / decay |
| P2 | Damping (brightness) |
| P3 | Return level |
| P4 | Pre-delay |
| P5 | Direct cello send into reverb |
| P6 | Reverb on/off |
| P7 | Ducking (reverb dips while you play) on/off |
| P8 | Hold tail (very long decay while held) |

### Page 4 — HARMONIZER (delay-based) ✅
| Control | Does |
|---|---|
| P1 | Voice 1 interval |
| P2 | Voice 2 interval |
| P3 | Mix |
| P4 | Detune / stereo spread |
| P5 | Send to shared reverb |
| P6 | Harmonizer on/off |
| P7 | Voice 2 on/off |
| P8 | Snap intervals to a scale on/off ❓ which scales? |

### Page 5 — FREEZE (grain-based) ✅
| Control | Does |
|---|---|
| P1 | Grain size |
| P2 | Density |
| P3 | Spread (position jitter) |
| P4 | Pitch |
| P5 | Freeze level |
| P6 | Capture freeze (latch) |
| P7 | Add a layer on top of the current freeze |
| P8 | Clear freeze (asks OK/CANCEL) |

### Page 6 — FILTER ✅
| Control | Does |
|---|---|
| P1 | Cutoff |
| P2 | Resonance |
| P3 | Envelope follower amount ✅ |
| P4 | Envelope follower speed (attack/release) |
| P5 | Sweep rate ✅ filter sweep |
| P6 | Filter on/off |
| P7 | Filter type: low-pass → band-pass → high-pass (cycles) |
| P8 | Envelope follower on/off ✅ |

### Page 7 — DRUM SYNTH ✅
Patterns are tapped in on pads ✅ and keep running on other pages ✅, synced to loops ✅.
| Control | Does |
|---|---|
| TRIG1 | Kick drum (this is TRIG1's default on every page) |
| TRIG2 | Snare drum (this is TRIG2's default on every page) |
| P6–P8 | Hi-hat, open hat, percussion |
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
| P6–P8 | Play notes ❓ (T4/T5 are now TRIG3/TRIG4; notes may move to P1–P5) |
| P1 | Ratio (timbre) |
| P2 | Index (brightness) |
| P3 | Envelope length |
| P4 | Root note / scale |
| P5 | Level |
❓ Is the FM synth mainly a bass voice, a pad, or a lead? That changes which 5 settings matter most.

### Page 9 — LIGHTING (internal cello LEDs) ✅
| Control | Does |
|---|---|
| P6–P8 | Lighting scenes 1–3 (scenes 4–5 displaced) |
| P1 | Brightness |
| P2 | Colour (hue) |
| P3 | Saturation |
| P4 | Speed |
| P5 | Audio reactivity (how much the cello drives the light) |
Stage DMX: later ✅, not in this version.

### Page 10 — SONG (loops, recording, samples; was Recorder/Looper/Sampler) ✅
The pedal does record / navigate / retrieve / store / create everywhere ✅. This page holds the settings ✅ and loop tricks ✅.
| Control | Does |
|---|---|
| P1 | Loop level |
| P2 | Overdub decay (how fast old layers fade) |
| P3 | Playback speed |
| P4 | Sample start / trim |
| P5 | Crossfade time |
| P1–P8 | Choose the active TRIG bank 1–8 (loop tricks moved to bank 8's TRIG pads) |
❓ **Big one:** which pads play back samples, and on which page? Your rule says manual triggering happens only on the current page. Should this page turn its pads into sample pads, or should samples live on their own page?

### Page 11 — RESOLUME ✅
| Control | Does |
|---|---|
| P6–P8 | Trigger clips 1–3 in the current column (clips 4–5 displaced) |
| P1–P5 | Five mapped Resolume parameters (opacity, effect amounts) ❓ which ones? |
❓ How does Bela talk to Resolume: MIDI or OSC over the network? (Bela Mini has no built-in Wi-Fi.)

### Page 12 — MIDI OUT (low priority) ✅
Channels 1–10 for flexibility ✅. Placeholder: P1 picks channel, slider sends a CC, P6–P8 send notes. Defined later.

---

## 4. Open questions — summary

0. ~~Slider target switching~~ — decided: second encoder (B), below TRIG4 beside the slider.
0b. P1–P5 pad roles, page by page (notes / presets / other).
1. ~~Slider mode~~ — decided: relative, no jumps. Long-press SENC = back to default target.
2. Page 1: EQ yes/no? Tuner wanted?
3. Harmonizer: which scales for interval snapping?
3b. ~~Reassigning~~ — decided: hold-to-arm + OK. Still open: which pad arms FM sequence recording?
3c. ~~Tap timing~~ — resolved: playable pads on press, OK/CANCEL on release.
3d. ~~Assign mode details~~ — approved.
4. Drums: how many pattern slots?
5. FM synth: bass, pad, or lead?
6. **Samples: which pads play them, and on which page?**
7. Resolume: MIDI or OSC? Which 5 parameters?
8. ~~Foot pedal~~ — mapped. ~~Loops per song~~ — several. Still open: does a song save everything (TRIGs, effect settings)? Is 4 TRIG pads enough? Confirm prompts for store/delete. Expression pedal global or per page?
9. Is 12 pages the right number, or should some pages merge?
