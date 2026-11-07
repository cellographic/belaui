# Cellographic Bela UI — Control Map (DRAFT v0.4)

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
| T1–T3 | Thumb pads | Right corner piece, front to back along the corner block | ✅ |
| SLIDER | Trill Flex slider | Upper-right, near the face, from above T1–T3 to about mid upper bout | ✅ |
| TRIG3 | Persistent trigger 3 (was thumb pad T4, percussion size) | Right next to TRIG2 | ✅ |
| TRIG4 | Persistent trigger 4 (was thumb pad T5, percussion size) | Directly under TRIG3 | ✅ |
| TRIG2 | Large pad, like TRIG1 — persistent trigger 2 (was SNARE) | Upper-right, above the slider | ✅ |
| OLED | 0.96" 128×64 blue/yellow screen | Upper-right, back half of the rib | ✅ |
| OK / CANCEL | Confirm / cancel pads | Behind the OLED | ✅ |
| SENC | Second pressable encoder — slider target | Below TRIG4, next to the Flex slider | ✅ |
| PEDAL | External foot pedal | Floor | ✅ |

Total capacitive pads: 14 (P1–P5, T1–T3, TRIG1–TRIG4, OK, CANCEL), all on one Trill Craft (30 channels available). Slider is the Trill Flex.

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
| SENC long-press | Jump straight back to this page's default slider target (💡 hold time about 0.6 s, tunable) | ✅ |
| OK / CANCEL | Reserved for confirmations (store, clear) and CANCEL-during-preview — never used for slider targets | ✅ |
| T1–T3 | Page-specific switches and actions (on/off, tap, latch, trigger) | ✅ |
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
| Reach it | Turn SENC all the way left, past the slider targets, to **PAGE OPTIONS**. For now the far right end also lands on PAGE OPTIONS (reserved for a second universal endpoint later). | ✅ |
| Enter | Press SENC | ✅ |
| Use | Pads toggle this page's preferences (behaviour switches, not performance). The OLED shows each toggle's on/off state. | ✅ |
| Store | OK saves this page's options **to the song**, so the song loads behaving as you set it | ✅ |
| Leave | CANCEL escapes Page Options mode | ✅ |
| Encoder ends | SENC stops at both ends (no wrap-around), so the ends are reliable landings | ✅ |
| Which pads toggle | P1–P5 + T1–T3 = 8 toggle slots per page. TRIG1–TRIG4 stay live so you can keep playing. | ✅ |
| Unsaved changes on CANCEL | Stay active until the song changes, but are not saved — loading the song again restores its stored settings | ✅ |
| Unsaved marker | A small mark on the OLED while a page has unsaved option changes | ✅ |
| "Song" | ❓ New concept — how is a song chosen and loaded (pedal retrieve? a Songs page?) | ❓ |

**💡 Toggle candidates per page (from displaced items):**
- Delay, Reverb, Harmonizer, Freeze, Filter: **Recorder pre/post** ✅ feature
- Delay: sync to loop clock · Reverb: ducking · Harmonizer: octave-down voice, scale snap · Freeze: fade in/out · Filter: sweep on/off ✅ feature, envelope follower on/off
- I/O: meter view input/output · tuner · EQ on/off
- Sampler: global recorder pre/post default ✅ feature
- Momentary performance actions (delay hold, freeze capture) stay on T1–T3, not in options

### Foot pedal — Hotone Ampero Control (v0.13)
**Paradigm:** the **song** is the stored unit. A song holds its loop recordings, loop length, drum/synth sequences and page options (💡 and TRIG assignments + effect settings ❓). The pedal covers navigate, retrieve, store, create and delete for songs, plus record control, from any page.

| Switch | Tap | Hold | Source |
|---|---|---|---|
| B1 | Record / overdub (starts **on press**) | Depends on when you hold — see below | ✅ |
| B2 | Stop | Clear all recordings in the current loop. Keeps loop length, sequences, page options. **Not saved** — reloading the song restores them unless you store. | ✅ |
| B3 | Song: previous → enters song-selection mode | **Store** the song | ✅ |
| B4 | Song: next → enters song-selection mode | **Delete** the selected song from storage | ✅ |
| B1 in song-selection mode | Accept → load the cued song | — | ✅ |
| B2 in song-selection mode | Cancel the cue | — | ✅ |

**B1 hold — two behaviours, decided by state:**
| You hold B1 when… | Result | Source |
|---|---|---|
| Starting a take (not currently recording) | Nothing new is recorded, and the previous layer is erased (step back). If this was the first recording, loop recording is cancelled. Repeat to step back further. | ✅ |
| Ending a take (currently recording) | The take you just made is erased; earlier layers stay | ✅ |

**Song switching:** default = at the end of the loop ✅. Alternatives "end of bar" and "immediate" are a Page Option on the Song/Loop/Record page ✅. 💡 If nothing is playing, the song loads immediately.

**💡 Proposals:**
- **Confirm destructive pedal holds.** Store-over-existing (hold B3) and delete (hold B4) show "Store over SONG 4?" / "Delete SONG 4?" on the OLED; **B1 = confirm, B2 = cancel** (the pedal's OK/CANCEL, matching the rule that destructive actions are confirmed).
- **Create = store into an empty slot.** Navigate past the last song to "NEW", hold B3 → creates a new song from the current state.
- **What hold B3 stores:** the current state into the *selected* slot. If you've cued a different song first, that's a "save as" — the confirm prompt names the target so you can't overwrite by accident.
- **Step-back depth:** keep every layer separately so B1 can step back through all of them. 💡 Memory estimate (not measured): ~11.5 MB per 30 s stereo layer, so roughly 20+ layers fits comfortably in the Bela Mini's RAM.
- **Saving audio during a show:** writing recordings to the SD card happens in the background so audio never glitches; the OLED shows "saving…" until done.
- **Pedal setup:** switches in *momentary* mode (sends press + release); Bela times holds itself.
- **Connection:** USB to start (most reliable); Bluetooth adapter optional later.

❓ One loop per song, or can a song hold several loops?
❓ Do TRIG assignments and effect settings belong to the song too?

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
| T1 | Mute cello input |
| T2 | Mute voice input |
| T3 | EQ on/off ❓ |

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

### Page 7 — DRUM SYNTH ✅
Patterns are tapped in on pads ✅ and keep running on other pages ✅, synced to loops ✅.
| Control | Does |
|---|---|
| TRIG1 | Kick drum (this is TRIG1's default on every page) |
| TRIG2 | Snare drum (this is TRIG2's default on every page) |
| T1–T3 | Hi-hat, open hat, percussion |
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
| T1–T3 | Play notes ❓ (T4/T5 are now TRIG3/TRIG4; notes may move to P1–P5) |
| P1 | Ratio (timbre) |
| P2 | Index (brightness) |
| P3 | Envelope length |
| P4 | Root note / scale |
| P5 | Level |
❓ Is the FM synth mainly a bass voice, a pad, or a lead? That changes which 5 settings matter most.

### Page 9 — LIGHTING (internal cello LEDs) ✅
| Control | Does |
|---|---|
| T1–T3 | Lighting scenes 1–3 (scenes 4–5 displaced) |
| P1 | Brightness |
| P2 | Colour (hue) |
| P3 | Saturation |
| P4 | Speed |
| P5 | Audio reactivity (how much the cello drives the light) |
Stage DMX: later ✅, not in this version.

### Page 10 — SONG / LOOP / RECORD (was Recorder/Looper/Sampler) ✅
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
❓ **Big one:** which pads play back samples, and on which page? Your rule says manual triggering happens only on the current page. Should this page turn its pads into sample pads, or should samples live on their own page?

### Page 11 — RESOLUME ✅
| Control | Does |
|---|---|
| T1–T3 | Trigger clips 1–3 in the current column (clips 4–5 displaced) |
| P1–P5 | Five mapped Resolume parameters (opacity, effect amounts) ❓ which ones? |
❓ How does Bela talk to Resolume: MIDI or OSC over the network? (Bela Mini has no built-in Wi-Fi.)

### Page 12 — MIDI OUT (low priority) ✅
Channels 1–10 for flexibility ✅. Placeholder: P1 picks channel, slider sends a CC, T1–T3 send notes. Defined later.

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
8. ~~Foot pedal~~ — mapped (v0.13). Still open: one loop or several per song; what else a song stores; confirm prompts for store/delete.
9. Is 12 pages the right number, or should some pages merge?
