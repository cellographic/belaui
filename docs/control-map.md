# Cellographic Bela UI — Control Map (DRAFT v0.4)

**v0.24.1:** CTRL is sticky: once chosen it stays active across pages until changed with the slider encoder.

**v0.53 changes:** SLDR moves recorded into the current page's sequence (A). SAMPLE approved; SD-card sample library with a default set. DELAY drafted.

**v0.52.1:** FLTR noted in SAMPLE's SLDR list; proposal that SLDR moves are recorded into the current page's sequence.

**v0.52 changes:** FM page approved. SAMPLE page drafted.

**v0.51 changes:** FM always follows the song's scale (its own chromatic option dropped); Chromatic songs use Transpose on the slider. FM Page Options shifted: P5 = notes into loops, P6 = hold notes, P7–P8 free.

**v0.50 changes:** Standing rule 8: few choices = tap to step, many/numbers = slider. Song scales: Major, Minor, Harmonic Minor, Blues (+ Chromatic). FM notes follow the song's key and scale (no separate FM scale setting).
💡 8 pads beyond a 7-note scale: pads continue up the scale past the octave (Blues has 6 notes, so pads 7–8 reach above the octave).

**v0.49 changes:** FM page drafted: each sound played on 8 notes of the song scale; default sounds Bass1/2, Pads1/2, Lead1/2, Noise1/2.

**v0.48 changes:** DRUM page approved; Level is the default SLDR setting; a tuned kit is saved with the song, or to the library for reuse.

**v0.47 changes:** DRUM page drafted.

**v0.46 changes:** SLDR details approved: CANCEL backs out one layer, shared filter mode, FILTER 1/2 layer when two filters are on, MIDI CC/channel layer.

**v0.45 changes:** FLTR and MIDI folded into SLDR. SLDR browsing defined, with sub-layers for items that need more definition (FLTR: AutoWah, Hi/Lo/Band Pass, Notch). CENC list: PAGE OPTIONS · SEQUENCE · (COMPOSE) · BANK · EXPRESSION · SLDR.

**v0.44 changes:** Page slider-target lists removed from the Control Encoder; each page's default and alternatives live inside **SLDR** (unset = page default; clear = back to default). The bottom of the OLED always shows the slider's target name and a level bar.

**v0.43.1:** Full CENC order written in one place.

**v0.43 changes:** BANK added to every page's Control Encoder (bank select from anywhere). Loops are not put on triggers; hold OK on SONG only arms a new loop.

**v0.42 changes:** SLDR tap settings (tap the slider in rhythm). Loops can optionally go on triggers. Clear a sequence = hold CANCEL in SEQUENCE mode.

**v0.41 changes:** Composition: TOUCH default / LATCH option (SONG P4); plays straight away when a song loads. Sequence overdubs additive by default. SLDR flow defined (browse the page's settings, press to hold, press-and-hold CENC to clear).

**v0.40 changes:** Composition overwrite clarified: only the specific setting you change is replaced, at the moment you change it.

**v0.39 changes:** SLDR added at the far right of CENC. Sequences: loop-aligned, a whole number of loops long, overdubbable; LOOP/SONG length choice removed. New **Composition** (one per song, recorded from the SONG page via COMPOSE). Glossary added.

**v0.38 changes:** CTRL scrapped. SONG P1–P8 = loop slots (first loop auto-saves to P1; hold OK arms a new loop, FS1 records it in sync). SEQUENCE redefined as recording each page's control events, LOOP or SONG length, unsaved until stored.

**v0.37 changes:** Samples move to their own **SAMPLE** page (page 4, after FM), handled like Drum/FM. SONG = song structure and loops. 12 pages: SONG · DRUM · FM · SAMPLE · DELAY · REVERB · HARPEGGIO · FLTR/FRZ · LIGHTING · RESOLUME · MIDI · SYSTEM.

**v0.36 changes:** SONG page sequences the song (via CENC). Loops vs samples defined: loops are grid-locked and linear; samples are free-length and overlay.

**v0.35 changes:** Slider encoder renamed **Control Encoder (CENC)**. SEQUENCE mode entered from CENC (Drum, FM, and 💡 SONG); OK/CANCEL tapping no longer switches modes. Preset library via press-and-hold page encoder; save tuned sounds as presets; SEQUENCE-mode note/drum pads defined.

**v0.34 changes:** Standing rule 5: slider-encoder lists are page-specific but shared items keep the same order. Drum/FM: P1–P8 = presets, Assign mode (hold OK) kept, triggers store a copy, last-touched sound is edited.

**v0.33 changes:** No separate SONGS page: on SONG, press-and-hold the page encoder opens the song list. SYSTEM stays immediately left of SONG.

**v0.32 changes:** Hand song browsing moves to the **page encoder** (on the SONG page, press-and-hold to open the list, browse, press to load at loop end); removed from the slider encoder. Page Options: slider auto-acts as CTRL. TRIG slots hold any type, 32 per song. New-song placement default = after current. SONG slider targets approved.

**v0.30 changes:** SONG page fully drafted: bank select, LOOP/SEQUENCE modes, slider targets, 8 Page Options.

**v0.29 changes:** FLTR/FRZ: one freeze; one filter by default with an optional second filter.

**v0.28 changes:** SENC right end: … MIDI · FLTR · EXPRESSION · CTRL. MIDI on SENC = slider sends a MIDI control value from any page.

**v0.27 changes:** Right end of SENC set: … MIDI · EXPRESSION · CTRL (CTRL at the far right for quick access).

**v0.26 changes:** CTRL simplified: the slider/expression pedal ignores page changes and page defaults, and supplies values for numerical settings. P1–P8 are unaffected. (Replaces the v0.25 edit-mode version.)

**v0.24 changes:** Page encoder **wraps** (SYSTEM one click left of SONG). Freeze + Filter merged into **FLTR/FRZ** (page 7) with selectable sources; freeze hold on a second footswitch. New global slider-encoder options **CTRL** (edit any setting) and **FLTR** (filter sweep from any page). 11 pages: 1 SONG · 2 DRUM · 3 FM · 4 DELAY · 5 REVERB · 6 HARPEGGIO · 7 FLTR/FRZ · 8 LIGHTING · 9 RESOLUME · 10 MIDI · 11 SYSTEM.

**v0.23 changes:** Page order set: 1 SONG · 2 DRUM · 3 FM · 4 DELAY · 5 REVERB · 6 HARPEGGIO · 7 FREEZE · 8 FILTER · 9 LIGHTING · 10 RESOLUME · 11 MIDI · 12 SYSTEM. MIDI device/port setup confirmed in SYSTEM. Freeze/Filter merge under discussion.

**v0.22 changes:** Foot buttons renamed **FS1–FS4**. A separate song-specific **MIDI** page returns (page 12) for controlling external devices; SYSTEM keeps rig-wide settings.

**v0.21 changes:** I/O and MIDI out merged into a **SYSTEM** page (rig-wide, never saved per song, saved with hand OK/CANCEL). Pedal saves are for live song management. Song scale set on the SONG page; HARPEGGIO uses named intervals, or half steps −12…+12 when the scale is Chromatic. Arpeggio spacing synced to tempo by default (approved).

**v0.20 changes:** Page 4 is now **HARPEGGIO** — harmonizer + arpeggiator: root plus up to 3 harmony notes (±1 octave), delay-based; separating the notes in time makes arpeggios.

**v0.19.1:** Loop tricks are tap on / tap off.

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
| CENC | Second pressable encoder — slider target | Below TRIG4, next to the Flex slider | ✅ |
| PEDAL | External foot pedal | Floor | ✅ |

Total capacitive pads: 14 (P1–P5, P6–P8, TRIG1–TRIG4, OK, CANCEL), all on one Trill Craft (30 channels available). Slider is the Trill Flex.

---

## 2. The grammar (the same on every page)

### ✅ Design rules
1. **Defaults imply options.** Whenever a rule names a default, other choices exist, normally set in that function's Page Options.
2. **Blinking = unconfirmed, solid = confirmed.** In any preview or pending choice (page encoder, slider encoder, song cue, Assign mode, expression assignment, confirm prompts) the option name on the OLED **blinks** until confirmed, then goes **solid**. Turning back to the current option shows it blinking too, until you confirm or cancel.
3. **Three ways to play any pad.** (a) **Live** — heard, not recorded. (b) **Into the loop** — while the loop is recording or overdubbing, the pad's sound is recorded into that audio layer. (c) **Sequence record mode** — the triggered events are recorded as a sequence, kept separate from the audio layers.
4. **Parts stay separate.** Cello loops, drum sequences and synth sequences are stored independently. Clearing the recordings keeps all sequences, and sequences are never baked into the recording, so either can be changed or removed without touching the other.
5. **Control encoder lists are page-specific, but shared items keep the same order.** Each page offers what it needs; when controls are common across pages they appear in the same order everywhere. Fixed frame: PAGE OPTIONS at the far left; … MIDI · FLTR · EXPRESSION at the far right.
6. **SEQUENCE mode records a page's control events.** Every page is a kind of control, so SEQUENCE on any page records *that page's* events. A sequence is a **section of the song** holding event triggers synced to the original loop.
   - **Start and end align with loop boundaries.** Stop recording before a full loop and the sequence still ends at the loop's end, so repeats stay in time. Keep recording past the loop and it continues into a second loop-length segment, and so on (e.g. a sequence 4 loops long).
   - Once the length is set, further passes **overdub** — secondary layers on top of the sequence, like audio overdubs.
   - The LOOP/SONG length choice is **removed**; long-form recording is the **Composition** (below).
   - Sequence data is **not permanent until saved**.
   - ✅ **SLDR moves are recorded too:** while SEQUENCE is on, slider moves through SLDR (e.g. FLTR) are recorded into the current page's sequence, even if the setting belongs to another page. SLDR stays held when you enter SEQUENCE (only press-and-hold CENC clears it).
   - **Sequence overdubs are additive by default** (no overwrite); overwrite can be set as an option (💡 in each page's Page Options, since sequences belong to pages). · **Clear a page's sequence:** hold CANCEL in SEQUENCE mode, with confirm ✅
7. **Composition = the longest form in a song.** One per song. Everything performed from the start of the song: which loops play when, which sequences run, and all other events.
   - **Record:** on the SONG page, turn CENC to **COMPOSE** and press to arm (arm before the song starts if needed). Recording starts at the top of the song and stops when you **CANCEL** it or the **song stops**.
   - **Playback:** you can **play live over** a composition.
   - **Re-recording overdubs by default:** only the **specific setting you change** is replaced, at the moment you change it — e.g. changing delay feedback replaces only the recorded delay feedback, not delay on/off or anything else. Everything you don't touch plays back as before.
   - **After you let go: TOUCH (default)** — the old recording of that setting resumes. **LATCH** (option) — your new value holds until the old recording next changes it. Set in SONG Page Options (P4).
   - **When a song loads, its composition plays straight away.** The composition is where time-critical performance data lives, keyed to the start of the song: after building loops and sequences, you organise them in the composition along with external MIDI, video and lighting changes timed to key moments.
8. **Choosing in Page Options.** A few fixed choices → **tap the pad to step through them**. Many choices or a number (e.g. song key, bars per loop) → **set with the slider**.

### Glossary
| Term | Meaning |
|---|---|
| **Song** | The master file: settings, time signature, loops, sequences, triggers, composition |
| **Loop** | Recorded audio. The first loop sets the song's timing; later loops are sections. Loops play one at a time. |
| **Overdub** | A layer recorded on top of a loop — or, for sequences/compositions, a further pass of events |
| **Sequence** | Recorded control events from one page; a whole number of loop lengths; repeats; can be overdubbed |
| **Sample** | A free-length recording that plays over loops |
| **Sound** | A drum or FM preset, copied onto a trigger |
| **Trigger / Bank** | 4 triggers × 8 banks = 32 slots per song |
| **Composition** | One per song: the long-form record of everything from the song's start |

Having one consistent "grammar" means your hands learn the instrument once, and every page just changes *what* the controls point at.

| Control | Job on every page | Source |
|---|---|---|
| ENC turn | Preview another page on the OLED (sound doesn't change yet) | ✅ |
| ENC press | Lock in the previewed page | ✅ |
| CANCEL during preview | Abandon the preview, stay on the current page | ✅ |
| **P1–P5** | **Page-specific.** Note values on some pages, preset selection on others — no universal rule. | ✅ |
| **SLIDER** | **Has a default target on every page**, plus a list of alternate targets per page. | ✅ |
| CENC turn | Move through the Control Encoder list (PAGE OPTIONS · SEQUENCE · … · SLDR); the item under the knob **blinks** | ✅ |
| CENC press | Enter / confirm the blinking item | ✅ |
| CANCEL during CENC preview | Abandon the preview, keep the current target (same as the page encoder) | 💡 |
| **Page encoder wraps around** (no end stops). Power-up and loading a song land on **SONG** (page 1); **SYSTEM** (last page) is one click to the left. Turning right is the normal performance direction. | ✅ |
| **Control encoder (CENC) list, left to right:** **PAGE OPTIONS** · **SEQUENCE** · (SONG only: **COMPOSE** 💡) · **BANK** · **EXPRESSION** · **SLDR**. CENC stops at both ends. There is **no separate list of slider targets**: each page's default and alternatives live inside **SLDR**. Positions of SEQUENCE, COMPOSE and BANK are 💡 proposals. | ✅ / 💡 |
| **BANK** (on every page's CENC) | Press → turn through TRIG banks 1–8 (each **blinking**) → press to select. Switch banks from any page mid-performance. 💡 Position: start of the global group, so the right end reads … BANK · MIDI · FLTR · EXPRESSION · SLDR | ✅ (💡 position) |
| **Global slider-encoder options** (on every page): **BANK**, **EXPRESSION**, **SLDR** (FLTR and MIDI are now inside SLDR). **MIDI** = the slider sends a MIDI control value to the external device from any page. | ✅ |
| ~~CTRL~~ | Scrapped (v0.38). | ✅ |
| **SLDR** (far right of CENC) | Holds the slider's assignment. **Unset = the current page's default.** Set it (SLDR flow) to put the slider on any setting from that page's SLDR list; it then stays there **on every page** until **cleared** (press-and-hold CENC), which returns the slider to each page's default. | ✅ |
| SLDR tap settings | For tap settings such as tap tempo, **tap the slider** in rhythm to set the new value. ❓ On Delay, does this set the delay's time only (💡), not the song tempo (which comes from the first loop)? | ✅ ❓ |
| SLDR flow | Turn CENC to **SLDR**, press → the **current SLDR selection flashes** (if unset, the current page's **default** flashes). Turn to browse that page's SLDR list. Press: if the item has **no further options**, it activates on the slider; if it **needs more definition**, you drop into the **next layer** with its first option flashing — turn to browse, press to activate. The slider then holds it on every page until cleared (press-and-hold CENC). | ✅ |
| **FLTR in SLDR** (every page) | Sub-layer: **AutoWah** (slider = wah range) · **Hi Pass** · **Lo Pass** · **Band Pass** · **Notch** (slider = sweep). Selecting one switches the filter to that mode and puts it on the slider. | ✅ |
| **MIDI in SLDR** (every page) | Slider sends a MIDI control value to the external device. Sub-layer: which control (CC) / channel, from the MIDI page's setup | ✅ |
| Backing out of a sub-layer | CANCEL goes up one layer (when CANCEL isn't already in use); at the top layer it leaves SLDR unchanged. To clear SLDR entirely: press-and-hold CENC. | ✅ |
| With two filters on | When a second filter is turned on (FLTR/FRZ page), FLTR's sub-layer first offers **FILTER 1 / FILTER 2**, then that filter's modes | ✅ |
| Filter mode is shared | Choosing a mode in SLDR sets the filter itself, so FLTR/FRZ always shows the same mode | ✅ |
| **FLTR** | The slider plays the filter sweep set up on the FLTR/FRZ page, from any page | ✅ |
| CENC long-press | **Clears SLDR** → the slider returns to the current page's default (💡 hold time about 0.6 s, tunable) | ✅ |
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
| **Drum & FM pages: SEQUENCE mode** | Entered from the **control encoder (CENC)**: turn to **SEQUENCE**, press. Outside SEQUENCE mode the page is in its normal sound state (P1–P8 = presets). | ✅ |
| Normal (sound) state | Audition presets on P1–P8, tune, and assign to triggers with Assign mode (hold OK) | ✅ |
| SEQUENCE mode | Play hits/notes in time to record a sequence, then store it in a persistent trigger (TRIG1–TRIG4). **FM:** P1–P8 play 8 notes of the song scale (root to octave), with an Octave target on CENC. **Drum:** P1–P8 play 8 drum sounds from the current preset bank. | ✅ |
| 💡 CENC position | Modes sit just inside the left end (SEQUENCE, and COMPOSE on SONG); global items sit at the right end (BANK · MIDI · FLTR · EXPRESSION · SLDR) | 💡 |
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
| Reach it | Turn CENC all the way left, past the slider targets, to **PAGE OPTIONS** | ✅ |
| Enter | Press CENC | ✅ |
| Use | Pads toggle this page's preferences (behaviour switches, not performance). The OLED shows each toggle's on/off state. | ✅ |
| Store | OK saves **just this page's** options to the song (a quick save). Holding FS3 on the pedal saves **everything**, including any unsaved page changes. | ✅ |
| Leave | CANCEL escapes Page Options mode | ✅ |
| Encoder ends | CENC stops at both ends (no wrap-around), so the ends are reliable landings | ✅ |
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

### ✅ Expression Options mode (v0.14) — second from the right end of CENC
| Step | What happens | Source |
|---|---|---|
| Reach it | Turn CENC right until **EXPRESSION** blinks (the far right end: … MIDI · FLTR · EXPRESSION) | ✅ |
| Enter | Press CENC → the arming marker appears on the OLED | ✅ |
| Choose | Turn CENC left; each notch blinks the next control the pedal could take over | ✅ |
| Assign | Press CENC → that control is assigned to the expression pedal and goes solid | ✅ |
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
| FS1 | Record / overdub (starts **on press**) | Depends on when you hold — see below | ✅ |
| FS2 | Stop | Clear all recordings in the current loop. Keeps loop length, sequences, page options. **Not saved** — reloading the song restores them unless you store. | ✅ |
| FS3 | Song: previous → enters song-selection mode. **Double-tap = create a new song** | **Store** the song | ✅ |
| FS4 | Song: next → enters song-selection mode | **Delete** the selected song from storage | ✅ |
| FS1 in song-selection mode | Accept → load the cued song | — | ✅ |
| FS2 in song-selection mode | Cancel the cue | — | ✅ |

**FS1 hold — two behaviours, decided by state:**
| You hold FS1 when… | Result | Source |
|---|---|---|
| Starting a take (not currently recording) | Nothing new is recorded, and the previous layer is erased (step back). If this was the first recording, loop recording is cancelled. Repeat to step back further. | ✅ |
| Ending a take (currently recording) | The take you just made is erased; earlier layers stay | ✅ |

**Song switching:** default = at the end of the loop ✅. Alternatives "end of bar" and "immediate" are a Page Option on the SONG page ✅. 💡 If nothing is playing, the song loads immediately.

**💡 Proposals:**
- ✅ **Confirm destructive pedal holds.** Store-over-existing (hold FS3) and delete (hold FS4) show "Store over SONG 4?" / "Delete SONG 4?" on the OLED; **FS1 = confirm, FS2 = cancel**.
- ~~Create = store into an empty slot~~ — replaced by double-tap FS3 ✅. Where the new song goes (next free slot vs right after the current song) is a SONG page option ✅.
- **Double-tap timing:** 💡 a single FS3 tap waits ~0.3 s to make sure it isn't a double-tap before moving the cue. Navigation isn't timing-critical, so the small delay should be fine.
- **What hold FS3 stores:** the current state into the *selected* slot. If you've cued a different song first, that's a "save as" — the confirm prompt names the target so you can't overwrite by accident.
- **Step-back depth:** keep every layer separately so FS1 can step back through all of them. 💡 Memory estimate (not measured): ~11.5 MB per 30 s stereo layer, so roughly 20+ layers fits comfortably in the Bela Mini's RAM.
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
| **Bank 8 defaults to loop tricks:** TRIG1 = reverse, TRIG2 = half speed, TRIG3 = stutter; TRIG4 reserved for another loop effect. Each trick is **tap on / tap off**. They can be overwritten if the slots are needed. As triggers they work from any page and can be recorded as sequences. | ✅ |
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
- **Yellow band:** page name · loop/clock status (recording / playing / bar count) · bank · markers (armed, unsaved)
- **Bottom of the screen (always):** the slider's current target **name** and a **level bar** showing its value ✅

---

## 3. The pages

Order follows Scott's priority list. ✅ marks the page itself and any decided feature; per-control assignments are 💡 unless marked.

**v0.2 note:** in the tables below, the five settings listed under P1–P5 are now read as the **slider's target list** for that page — the first one is the default, the rest are alternates. What the P1–P5 *pads* do on each page (notes, presets, etc.) is still to be assigned page by page.

### Page 1 — SONG (song structure and loops) ✅
The pedal handles record / stop / song navigate / store / create / delete from every page ✅. This page holds song structure, banks and song settings.

**Normal use**
| Control | Does | Source |
|---|---|---|
| P1–P8 | **Loop slots 1–8.** The first loop auto-saves to P1; each new loop saves to the next slot. | ✅ |
| TRIG1–TRIG4 | Play exactly as assigned. Any slot can hold a **loop, sequence, sample, drum sound or synth sound**. 8 banks × 4 = **32 triggers per song**. | ✅ |
| SEQUENCE (via CENC) | Turn CENC to **SEQUENCE**, press, to sequence the song: loops in order plus sample events | ✅ |

**Loops vs samples** ✅
| | Loop | Sample |
|---|---|---|
| Length | Locked to the first loop's length or derivations (LOOP / BAR snap) | Free — any length |
| Playback | **Linear**: loops play one after another; they never layer on each other (overdubs are layers *within* a loop) | **Overlays** loops; independent of them unless sequenced |
| In a sequence | Placed on the loop/bar grid | Placed with or without quantize (default FREE) |
| ❓ How you record one vs the other | see chat — 💡 arm a trigger first, then record = sample; record with nothing armed = loop | |
| ❓ Starting a **new secondary loop** vs overdubbing the current one | see chat | |
| **New loop** | **Hold OK** arms a new loop → **FS1** records it, in sync with the existing loop → on completion it saves to the next free P slot | ✅ |
| Loops on triggers | Not needed — loops live on SONG's P1–P8. With 32 trigger slots there's no need to put loops on triggers. Hold OK on SONG simply arms a new loop. | ✅ |
| SEQUENCE mode | Record the song **arrangement** by playing TRIG pads in time | ✅ arrangement-by-playing · 💡 placement here |
| Samples | Moved to their own **SAMPLE** page (page 4) | ✅ |

**SLDR list (default first)** — the slider follows the first item unless SLDR is set to another
| # | Target | Source |
|---|---|---|
| 1 (default) | Loop level | ✅ |
| 2 | Overdub decay (how fast old layers fade) | ✅ |
| 3 | Loop crossfade time | ✅ |
| then | MIDI · FLTR · EXPRESSION | ✅ |

**Browsing songs by hand — on the PAGE encoder (left)** ✅
| Step | Action | OLED |
|---|---|---|
| 1 | On the **SONG** page (or while previewing it), **press and hold** the page encoder | The song list appears, **blinking** |
| 2 | Turn the page encoder to browse | Each song name blinks |
| 3 | Press the page encoder again | Name stops blinking (loaded/cued); the new song begins when the current song's loop completes (per the song-switch timing option) |
| Back out | 💡 CANCEL | Current song keeps playing |
The pedal (FS3/FS4 browse, FS1 load, FS2 cancel) uses the same cue. There is no separate SONGS page — song browsing is part of SONG. A short press on SONG works as normal (locks in the page); press-and-hold opens the song list. Page ring unchanged: SYSTEM sits immediately left of SONG.

**Page Options (8 slots)**
| Pad | Option | Choices | Source |
|---|---|---|---|
| P1 | Song switch timing | END OF LOOP (default) · END OF BAR · IMMEDIATE | ✅ |
| P2 | New song placement | AFTER CURRENT (default) · NEXT FREE SLOT | ✅ |
| P3 | Secondary loop snap | LOOP (default) · BAR | ✅ |
| P4 | Composition overdub | TOUCH (default) · LATCH | ✅ |
| P5 | Bars per loop | number (default 4) | ✅ |
| P6 | Beats per bar | number (default 4) | ✅ |
| P7 | Song key | C · C♯ · D … B (12 choices — set with the slider) | ✅ |
| P8 | Song scale | **Major** · **Minor** · **Harmonic Minor** · **Blues** · Chromatic (tap to step through). 💡 Other modes (Dorian, Phrygian, Lydian, Mixolydian, Locrian) can be added later if wanted | ✅ |
| ✅ | Tapping a pad with fixed choices steps through them. **In Page Options the slider automatically supplies values**, so numerical options (P5–P7) take their value from it; it returns to normal on leaving. | ✅ |
| 💡 | Recorder pre/post **global default** moves to SYSTEM (it's a rig-wide setting), freeing a slot here | 💡 |

### Drum & FM pages — shared sound rules (v0.34) ✅
| Rule | Source |
|---|---|
| P1–P8 are **sound presets** to audition (tap to hear) | ✅ |
| Assigning uses **Assign mode** (hold OK → touch a TRIG → tap the preset), not hold-the-trigger | ✅ |
| Triggers store a **copy** of the sound — tuning one trigger never changes the preset or other triggers | ✅ |
| **Last touched sound is the one edited** — a preset on P1–P8 or a TRIG pad; works tune-then-assign or assign-then-tune | ✅ |
| 💡 Tuning uses the page's **SLDR list** (pitch, decay, tone…), shared in the same order on Drum and FM where they overlap | 💡 |
| **More presets:** press-and-hold the page encoder opens the preset library (banks of 8, blinking); press loads a bank onto P1–P8. General rule: *hold the page encoder = open this page's library*. | ✅ |
| **Save a tuned sound as a preset:** in the preset library, browse to an empty slot or NEW and press OK; overwriting asks for confirmation | ✅ |

### Page 2 — DRUM (drum synth) ✅ (approved v0.48)
Drum patterns keep running on other pages ✅ and stay in sync with the loops ✅. Shared Drum/FM rules above apply.

**Typical workflow:** dial in sounds one at a time (Level, then the tone-shaping settings), then assign them to triggers or keep the tuned P1–P8 kit for this song.
**Two levels of saving:** the tuned kit on P1–P8 is saved **with the song** (hold FS3); saving to the **preset library** (OK into an empty slot / NEW) makes a sound reusable in other songs.

**Normal use**
| Control | Does | Source |
|---|---|---|
| P1–P8 | **Drum sound presets** from the current preset bank — tap to hear; the last touched is edited | ✅ |
| Preset bank = a **kit** | Each bank of 8 is a kit, e.g. kick · snare · closed hat · open hat · clap · tom · rim · perc | ✅ |
| TRIG1–TRIG4 | Play the active trigger bank. **Bank 1 defaults** to kick · snare · hi-hat · open hat | ✅ |
| Hold OK | **Assign mode:** touch a TRIG → tap a preset → that TRIG gets a copy | ✅ |
| Hold page encoder | **Preset library:** browse kits (blinking), press to load onto P1–P8; save a tuned sound to an empty slot / NEW with OK | ✅ |

**SEQUENCE (via CENC)**
| Control | Does | Source |
|---|---|---|
| P1–P8 | Play the 8 drum sounds as drum pads while recording | ✅ |
| Recorded | This page's control events — hits plus any drum setting changes | ✅ |
| Length | Loop-aligned, a whole number of loops; further passes **add** by default | ✅ |
| Clear | Hold CANCEL in SEQUENCE mode, with confirm | ✅ |

**SLDR list (default first)** — shared order with FM: Level · Pitch · Decay · Tone, then drum-specific
| # | Setting | Source |
|---|---|---|
| 1 (default) | Level | ✅ |
| 2 | Pitch | ✅ |
| 3 | Decay | ✅ |
| 4 | Tone (dark ↔ bright) | ✅ |
| 5 | Snap / attack (click at the start of the hit) | ✅ |
| 6 | Noise (amount of noise, mainly snares/hats) | ✅ |
| 7 | Drive (grit) | ✅ |
| then | FLTR · MIDI (on every page) | ✅ |

**Page Options (8 slots)** — approved
| Pad | Option | Choices |
|---|---|---|
| P1 | Sequence overdub | **ADD** (default) · OVERWRITE ✅ |
| P2 | Swing | number (default 0) |
| P3 | Live-hit timing correction while recording | OFF · 1/8 · **1/16** (default) |
| P4 | Velocity | **FIXED** (default) · TOUCH (harder/larger touch = louder) |
| P5 | Choke: closed hat cuts the open hat | **ON** (default) · OFF |
| P6 | Drum hits go into loop recordings | **OFF** (default; keeps parts separate) · ON |
| P7 | Pad sensitivity | number |
| P8 | Drums follow song key (tuned drums like toms) | **OFF** (default) · ON |

### Page 3 — FM (FM synth) ✅ (approved v0.52)
**Each sound is played on 8 notes** (option A) ✅. FM is the exception to the shared "P1–P8 = presets" rule: here P1–P8 are always **notes**.

**Normal use**
| Control | Does | Source |
|---|---|---|

| P1–P8 | Play the current sound on **8 notes of the song's key and scale**, root to octave. FM always follows the song's scale; if the song's scale is **Chromatic**, the pads play 8 half steps up from the key and **Transpose** reaches the rest. Triggers are never taken over. | ✅ |
| Default sounds | **Bass1 · Bass2 · Pads1 · Pads2 · Lead1 · Lead2 · Noise1 · Noise2** | ✅ |
| Change sound | Hold the page encoder → sound library (blinking) → press to load | ✅ |
| Save a tuned sound | In the library, an empty slot / NEW → OK. Tuned sounds are also saved with the song (hold FS3) | ✅ |
| Hold OK | **Assign mode:** touch a TRIG → tap a note pad → the TRIG gets a copy of the sound **plus that note** | ✅ |
| TRIG1–TRIG4 | Play the active trigger bank | ✅ |
| Chords | Holding several note pads plays a chord, up to 4 notes at once (my estimate for the Bela Mini's processor, not measured) | ✅ |

**SEQUENCE (via CENC)**
| Control | Does | Source |
|---|---|---|
| P1–P8 | Play notes while recording; **how long you hold** each note is recorded too (matters for pads) | ✅ |
| Recorded | Notes plus any FM setting changes | ✅ |
| Length / overdub / clear | Loop-aligned · adds by default · hold CANCEL to clear | ✅ |

**SLDR list (default first)** — shared order with DRUM, then FM-specific
| # | Setting | Source |
|---|---|---|
| 1 (default) | Level | 💡 (matches DRUM) |
| 2 | Pitch (fine tune) | ✅ |
| 3 | Decay | ✅ |
| 4 | Tone (brightness — the FM "index") | ✅ |
| 5 | Ratio (changes the basic timbre) | ✅ |
| 6 | Attack | ✅ |
| 7 | Release | ✅ |
| 8 | Feedback (grit) | ✅ |
| 9 | Octave (shift the 8 notes up/down) | ✅ |
| 10 | Glide (slide between notes, for bass/leads) | ✅ |
| 11 | Transpose (half steps — with the song scale set to Chromatic, shifts the 8 pads to reach the other notes) | ✅ |
| then | FLTR · MIDI | ✅ |

**Page Options (8 slots)** — approved
| Pad | Option | Choices |
|---|---|---|
| P1 | Sequence overdub | **ADD** (default) · OVERWRITE ✅ |
| P2 | Voice mode | **POLY** (chords) · MONO (one note at a time, for bass/leads) |
| P3 | Live-note timing correction while recording | OFF · 1/8 · **1/16** (default) |
| P4 | Velocity | **FIXED** (default) · TOUCH |
| P5 | FM notes go into loop recordings | **OFF** (default) · ON |
| P6 | Hold notes (tap on / tap off, for drones) | **OFF** (default) · ON |
| P7 | free (future needs) | — |
| P8 | free (future needs) | — |

### Page 4 — SAMPLE (sample instrument) ✅ (approved v0.53)
Samples are a **custom instrument** for recording and triggering sounds on the fly. Free length, they **overlay loops** and are independent unless sequenced ✅. Like DRUM, each pad holds its own sound.

**Normal use**
| Control | Does | Source |
|---|---|---|
| P1–P8 | **Sample slots** from the current sample bank — tap to hear; last touched is edited | ✅ |
| Record into a slot | Hold OK → touch a **P slot** (**>**) → **FS1** starts / stops recording. OLED shows **REC SMPL**. FS1 with nothing armed still records a loop. | ✅ |
| Assign to a trigger | Hold OK → touch a **TRIG** → tap a sample → the TRIG gets a copy | ✅ |
| Record straight to a trigger | Hold OK → touch a **TRIG** → **FS1** instead of tapping a sample: records a new sample onto that trigger (and into the next free P slot) | ✅ |
| Library | Hold the page encoder → sample banks; save to an empty slot / NEW with OK; samples are also saved with the song (hold FS3) | ✅ |

**SEQUENCE (via CENC)**
| Control | Does | Source |
|---|---|---|
| P1–P8 | Play samples while recording, quantized or free (per P3 below) | ✅ |
| Length / overdub / clear | Loop-aligned · adds by default · hold CANCEL to clear | ✅ |

**SLDR list (default first)** — shared order, then sample-specific
| # | Setting |
|---|---|
| 1 (default) | Level |
| 2 | Pitch |
| 3 | Decay (fade-out) |
| 4 | Tone |
| 5 | Start |
| 6 | End |
| 7 | Fade-in |
| 8 | Play mode → sub-layer: **ONE-SHOT** (plays through) · **HOLD** (plays while held) · **LOOP** (tap on / tap off) — set per sample |
| 9 | Reverse → sub-layer: OFF · ON — per sample |
| then | **FLTR** (sweep samples live — the filter's source must include samples, set on FLTR/FRZ) · MIDI ✅ |

**Page Options (8 slots)** — approved
| Pad | Option | Choices |
|---|---|---|
| P1 | Sequence overdub | **ADD** (default) · OVERWRITE ✅ |
| P2 | Sample trigger timing (live) | **FREE** (default) ✅ · BEAT · BAR |
| P3 | Timing correction while recording a sequence | OFF · 1/8 · **1/16** (default) |
| P4 | Velocity | **FIXED** (default) · TOUCH |
| P5 | Samples go into loop recordings | **OFF** (default) · ON |
| P6 | Re-hitting a playing sample | **RESTART** (default) · LAYER (overlap) |
| P7 | Record source | **CELLO** (default) · VOICE · BOTH · FULL MIX |
| P8 | Record before / after effects | PRE · **POST** (default ✅ — recorder captures post-effects by default) |
💡 Length: my estimate is about 11.5 MB of memory per minute of mono sample (not measured); long samples are fine but are written to the SD card in the background.
**Sample library on the SD card** ✅: the card carries a sample library, including at least **one full default set** that preloads into new songs. 💡 Details: the default set is chosen in SYSTEM; songs **reference** library files (trim/pitch etc. saved as settings) and only newly recorded samples are saved as new audio; library files should match Bela's audio format (my understanding: 44.1 kHz WAV — to verify); large sets load in the background.

### Page 5 — DELAY ✅ — DRAFT v0.53
**Normal use** (all 💡)
| Control | Does |
|---|---|
| P1–P4 | **Delay presets** (e.g. slapback · dotted-1/8 dub · ping-pong · long ambient) — tap to load; hold the page encoder for the full library |
| P5 | **Hold** — infinite repeats while held |
| P6 | **Dub throw** — sends the input into the delay only while held |
| P7 | **Clear** the repeats |
| P8 | Delay **on / off** |
| SEQUENCE (CENC) | Records presets, holds, throws and setting changes, like any page |

**SLDR list (default first)** — shared effect order (Mix · main amount · Tone · Reverb send), then delay-specific; based on your list (mode, level, tempo, feedback, modulation, tap tempo)
| # | Setting | Source |
|---|---|---|
| 1 (default) | Mix (level) ❓ or Feedback as the default? | 💡 |
| 2 | Time | ✅ (your "tempo") |
| 3 | Tone | 💡 |
| 4 | Reverb send | 💡 |
| 5 | Feedback | ✅ |
| 6 | Modulation | ✅ |
| 7 | Tap tempo — tap the slider in rhythm; 💡 sets the **delay's** time only, not the song tempo | ✅ / ❓ |
| 8 | Mode → sub-layer: 💡 DIGITAL · TAPE · PING-PONG · REVERSE | ✅ |
| then | FLTR · MIDI | ✅ |

**Page Options (8 slots)** — 💡 unless marked
| Pad | Option | Choices |
|---|---|---|
| P1 | Sequence overdub | **ADD** (default) · OVERWRITE ✅ |
| P2 | Time follows song tempo | **SYNC** (default) · FREE |
| P3 | Sync division | 1/4 · **1/8** · dotted 1/8 · 1/8 triplet · 1/16 … (slider) |
| P4 | Source (what feeds the delay) | **CELLO** (default) · VOICE · SAMPLES · DRUMS · FM · MIX |
| P5 | Recorder takes this pre/post delay | PRE · **POST** (default) ✅ (decided per page) |
| P6 | Repeats when turned off | **SPILL OVER** (default — tails ring out) · CUT |
| P7 | Ducking (repeats dip while you play) | **OFF** (default) · ON |
| P8 | free | — |

### Page 6 — REVERB (shared) ✅
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

### Page 7 — HARPEGGIO (harmonizer + arpeggiator, delay-based) ✅
| Rule | Source |
|---|---|
| Plays the **root note** (the cello) plus **up to 3 settable harmony notes**, each from **1 octave below to 1 octave above** | ✅ |
| Sound comes from delay-speed adjustments (delay-based pitch shifting) | ✅ |
| When the harmony notes are **separated in time**, the harmony becomes an **arpeggio** | ✅ |
| Time separation follows the song tempo by default (e.g. 1/8 or 1/16 steps); free timing as an option | ✅ |
| The **song's scale** is set on the SONG page. With a named scale, harmony notes use **named intervals** (e.g. "+maj3"). With **Chromatic**, they use **half steps from −12 to +12** (0 = unison, e.g. "+4"). | ✅ |
| ❓ Named intervals: fixed sizes (+maj3 always = +4 half steps), or scale-aware harmony that changes interval size with the note you play (needs pitch detection) — see chat | ❓ |
| 💡 Note (my expectation, not tested): delay-based shifting gets more "warbly" toward ±1 octave; worth hearing early in the simulator stage | 💡 |

Previous per-pad draft (to be redone in the P1–P8 pass): voice intervals, mix, spread, reverb send, on/off, voice on/off, scale snap.

### Page 8 — FLTR/FRZ (filter + grain freeze) ✅
| Rule | Source |
|---|---|
| Freeze and Filter share one page | ✅ |
| **Sources are selectable for each effect** — e.g. cello only, mic only, loops/synths, the whole mix except drums, or the master output | ✅ |
| **Freeze hold** on an extra footswitch in the Ampero Control's second TRS jack (one jack = expression, one = freeze) | ✅ |
| Filter modes: auto-wah (envelope follower) or sweeps (low-pass, high-pass, band-pass, notch, others) — set up here | ✅ |
| **FLTR** is a global slider-encoder option, so filter sweeps can be played from any page | ✅ |
| **One freeze.** **Filters: 1 by default; a second filter can be assigned** (Page Options), each with its own source | ✅ |
| 💡 With two filters: FLTR on the slider encoder controls Filter 1 by default (option: Filter 2 or both); each filter processes its own source side by side (parallel) | 💡 |
| 💡 Extra options from chat to choose from: freeze grain size, density, spread, pitch/octave, drift, width, tone, latch vs hold, fade in/out, stack vs replace, decay, auto-freeze on new note; filter LFO sweep synced to tempo, step filter, formant/vowel, comb, drive, envelope sensitivity/attack/release, sweep range | 💡 |

Earlier per-pad drafts (to be redone in the P1–P8 pass):

**Freeze draft:**
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

**Filter draft:**
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

### Page 10 — RESOLUME ✅
| Control | Does |
|---|---|
| P6–P8 | Trigger clips 1–3 in the current column (clips 4–5 displaced) |
| P1–P5 | Five mapped Resolume parameters (opacity, effect amounts) ❓ which ones? |
❓ How does Bela talk to Resolume: MIDI or OSC over the network? (Bela Mini has no built-in Wi-Fi.)

### Page 11 — MIDI (song-specific) ✅
A dedicated page for controlling **external devices** thoroughly and intentionally. Settings are saved **per song**. Used most often for controlling external gear. Channels 1–10 ✅.
✅ Split: MIDI *device and port setup* stays in SYSTEM (rig-wide); *what this song sends and on which channels* lives here. Per-pad details in the P1–P8 pass.

### Page 12 — SYSTEM (I/O + MIDI; rig-wide, never saved per song) ✅
SYSTEM settings are set-and-forget, saved with the hand OK/CANCEL pads (not the pedal). Holds I/O levels and all rig-wide settings (incl. MIDI device/port setup ✅). 💡 Also a home for tuner, pedal setup, Resolume connection, screen brightness, new-song defaults. Song-specific MIDI lives on the MIDI page (page 12).

I/O draft:
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

---

## 4. Open questions — summary

0. ~~Slider target switching~~ — decided: second encoder (B), below TRIG4 beside the slider.
0b. P1–P5 pad roles, page by page (notes / presets / other).
1. ~~Slider mode~~ — decided: relative, no jumps. Long-press CENC = back to default target.
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
