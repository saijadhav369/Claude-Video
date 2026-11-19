# RicksClips3000: how the Shorts are made

This guide covers the 20 most recent Shorts (uploaded 2026-10-14 to 2026-11-04) and how they were measured:

- Every frame of every video was processed at its native 30 fps: brightness, contrast, saturation, colour temperature, vignette, motion, optical-flow camera moves, and cut/dissolve detection.
- Narration was transcribed with word-level timestamps.
- Audio was analysed for loudness and for the music bed level.
- Each video was reviewed visually as a contact sheet at 2 fps, plus full-resolution stills and frame-by-frame strips around effects.

Numbers come from those measurements. Anything marked *(inference)* is interpretation.

- Per-video breakdowns: [analysis/reports/](analysis/reports/)
- Full transcripts: [analysis/transcripts_all.md](analysis/transcripts_all.md)
- Raw numbers: [analysis/channel_stats.json](analysis/channel_stats.json)

---

## 1. The format at a glance

| | Channel norm (20 videos) | Range |
|---|---|---|
| Length | 56 s | 31–78 s (older videos ran 31–45 s; recent ones run 56–78 s) |
| Words | 208 | 112–295 |
| Narration speed | **223 words/min** | 201–246 (excluding pauses: about 250) |
| Voice starts | **0.00 s, every video** | no intro, title card, or logo |
| Ending | voice stops 0.07–0.55 s before the last frame | no call to action, outro, or "follow for more" |
| Shots | 23 per video, **average 2.5 s** | 1.7–4.1 s |
| Transitions | about 90% cross-dissolves, **median 14 frames (0.47 s)** | 3–45 frames; about 2 hard cuts per video |
| Camera moving | **96% of shots** | static shots are rare and deliberate |
| Captions | 1–3 words per card, white heavy rounded font with black outline, centred at 70% of frame height | same in all 20 |
| Loudness | **−14 LUFS**, loudness range about 2 LU | heavily compressed; a music bed sits about 6–7 dB under the voice |
| Resolution | 1080×1920, 30 fps | |
| Upload rate | about one per day | 20 videos in 22 days |
| Video description | just the title | |

---

## 2. Scripts

### 2.1 The skeleton
Almost every script follows this order. Positions are percent of runtime, taken from word timestamps across all 20.

```
0%    HOOK         one flat declarative sentence about a strange, specific act (avg 14 words, ends ~3.9 s)
4–11% [You see,]   optional: immediate backstory hinge ("You see, memories are money here.")
      SETUP        present tense, concrete details, exact numbers, a skeptic who mocks the hero
      ESCALATION   "Then…" / "But…" ladders, rule-of-three lists, "so X that Y" hyperbole
55–62% [Wait, what? … Well,]   optional: narrator voices the viewer's confusion, answers it
45–90% TURN       "But / Until / Instead / Except…": the thing nobody expected
65–91% YOU SEE,   the real-world mechanism in 1–3 sentences, often through an everyday analogy
END   PAYOFF       the irony lands; the last word often calls back to the hook's key word; stop
```

**Measured "You see," positions:**
- Early (backstory): 02 at 5%, 07 at 4%, 09 at 5%, 13 at 11%, 15 at 9%.
- Late (reveal): 01 at 81%, 03 at 66%, 04 at 71%, 06 at 65%, 10 at 76%, 11 at 81%, 12 at 87%, 16 at 73%, 18 at 67%, 20 at 80%.
- Video 09 uses it in both places.
- Videos 05, 07 (as a reveal), 08, 14, 17 and 19 don't use it. They pivot with "Well, picture…", "So let's crack it open.", or let the visuals explain.

### 2.2 Hooks: all 20, verbatim
| # | Views | Hook | Words | Device |
|---|---|---|---|---|
| 13 | 31.4M | He put a bronze ball in a dragon's mouth and told the emperor, if this ever falls out, run. | 19 | odd act + ominous quoted rule |
| 02 | 19.5M | He sawed gaps into a railroad every 39 feet. | 9 | apparent self-sabotage + exact number |
| 11 | 16.5M | It's impossible to get fired in Japan, but companies found something way worse. | 13 | claim + "but" escalation |
| 18 | 13.8M | Gambling is illegal in Japan, yet there's a gambling hall on almost every street. | 14 | legal contradiction |
| 03 | 12.9M | He poured cooking oil into the sea, with a pirate ship so close behind them he could hear the pirates laughing. | 21 | mundane act under mortal danger |
| 09 | 11.3M | They buried a man alive with a bell tied to his finger. | 12 | shocking historical image |
| 14 | 8.8M | If your ship got hit by a cannonball, you'd actually be one of the lucky ones. | 16 | second-person counterintuitive claim |
| 16 | 8.7M | A blacksmith sold a spear that could pierce anything to one king, and a shield that nothing could pierce to his worst enemy. | 23 | classic paradox as a fable |
| 12 | 8.1M | A man snuck into a family's house every night and moved every single thing one inch to the left. | 19 | absurd specific act |
| 06 | 8.0M | The fastest gun in the West had one rule. Never draw first. | 9+3 | superlative + contradicting rule |
| 10 | 7.3M | He scanned a customer's lottery ticket, saw it had won a million dollars, and said, sorry man, not a winner. | 20 | dramatic irony + dialogue punchline |
| 20 | 6.1M | A scientist dropped people off a tower just to find out what happens to time right before you die. | 19 | shock act + curiosity gap |
| 08 | 6.0M | Look at these two scratch cards. (One's a winner and one's garbage. Yet there's a way to tell…) | 6+6+11 | imperative to the viewer + promised secret |
| 04 | 5.0M | He bet his life savings on the slowest horse in the race. | 12 | irrational bet, two superlatives |
| 05 | 3.5M | There's a button in the middle of town, and nobody's allowed to press it. | 14 | forbidden object |
| 15 | 1.6M | A knight paid a priest to forgive a crime he hadn't committed yet. | 13 | paradox (inverted order) |
| 07 | 0.46M | He sold his happiest memory to a stranger behind a counter. | 11 | literalised idiom, invented world |
| 17 | 0.30M | How do painkillers know where the pain is? | 8 | question |
| 19 | 0.11M | You just watched two jackpot symbols land, and the third one stopped one click short. | 15 | in-the-moment second-person scenario |
| 01 | 0.07M | They painted the jail cell pink, and not just any pink. | 11 | *uploaded the day of analysis, so views aren't comparable* |

**What every strong hook does:**
- It states an **action**, not a topic.
- It's past tense and third person ("He…", "They…", "A man…").
- It includes **one exact detail**: 39 feet, one inch to the left, a bell on his finger, the slowest horse.
- It **withholds the reason**.

*(inference, n=20):* The weakest performers are the pure "how X works" explainers with question or scenario hooks (17, 19), plus the invented-world fable (07). Every top performer is a **real-world rule or mechanism exploited by a clever person, told as a story with a twist.**

### 2.3 Recurring writing devices (with examples)
- **The skeptic or mocker, and a quoted line about every 10–15 s.**
  - "You're wrecking my railroad!"
  - "We're about to get boarded, and you're making soup?"
  - "Hey, Mirror Man, maybe try wiping it."
  - "Pal, that horse lost a race to the milk cart, and it was pulling the milk cart."
  - "Sir, that's impossible."
  - The ending reverses the mockery. In 04, "the room is laughing at him" becomes "nobody's laughing anymore".
- **Ironic joy right before the reversal.**
  - "The guards are thrilled." / "And his boss is thrilled." / "…the pirates couldn't be happier." / "At first, it's paradise."
- **"So X that Y" hyperbole.**
  - "a canyon so deep you can't see the bottom"
  - "so far ahead its jockey is waving to his mom"
  - "a wall so tall nobody's ever seen over it"
- **Time ladders with concrete units.**
  - "At 15 minutes… At 20… by the time they open the door…"
  - "In May, you can fit a coin in them. By July, barely a sheet of paper."
  - "Five minutes go by, then ten, until finally…"
- **Rule of three, with the third item comic.**
  - "a boat, a mansion, and a whole new set of friends, at least in his head"
  - "cookies, chocolate, a bottle of shampoo, or a few tiny plastic tokens"
- **The narrator voices the viewer's confusion, then answers it.**
  - "Wait, what? Well, nobody can explain it." / "Wait, what's a mirror going to do? Well,…" / "Wait, practiced? Well, he was never dead."
- **Everyday analogy for the science.**
  - "Ever blown on a bowl of soup?" (which turns the captain's "making soup?" insult into the explanation)
  - Catching a falling phone (reflex vs decision).
  - Your body as a house full of smoke alarms.
- **Comic deflation by understatement.**
  - "statistically a little suspicious"
  - "He'd lose a race to the saloon against a guy carrying two beers."
- **Callbacks and repeated motifs.**
  - "15 minutes" ×5 (01)
  - "one click short" ×3 (19)
  - "find out" ×2 (16)
  - The last word echoes the hook: buried → buried, customer → customer's, gambles → Gambling.
- **Sentence rhythm.** Sentences average 15 words, but long 20–37-word run-ons chained with *and / but / so* alternate with 2–5-word punches: "Then nobody moved." "Rail touching rail." "So, he waits." "Attack and find out."
- **Tense pattern.** A past-tense hook, then the historical present for the story ("His captain grabs him…"), then past tense for the real-world explanation ("sailors really carried oil just for this").
- **Pauses.** There are almost none. The average gap between words is 0.02–0.04 s, and there are 1–10 pauses of 0.25 s or more per video, with a maximum of 0.56 s. The rare pauses go after the hook, around "Wait… Well,", and right before the twist or punchline.

### 2.4 Endings and loops
- Every video ends on the payoff or explanation sentence itself. The picture cuts within about 0.3 s of the last word.
- Four videos are built as **seamless loops**: the last line flows into the first.
  - **05:** "We'll build our town right here." → "There's a button in the middle of town…"
  - **10:** "…pretending to be regular customers." → "He scanned a customer's…". The last frame recreates frame 0, but the name tag now reads TRAINEE.
  - **18:** "…on paper, nobody gambles." → "Gambling is illegal…". Same alley, same grade.
  - **20:** "…it all happened in slow motion." → "A scientist dropped people off a tower…". A flipbook page matches frame 0.
- Most of the others are **bookends**: the same location or motif, but not a seamless loop.

### 2.5 Titles
- Short and plain, 4–8 words, with no capitals-for-hype or emoji.
- Patterns:
  - **Why…** "Why Perfect Railroads Don't Work", "Why Sailors Carried Storm Oil"
  - **How…** "How a Mirror Rigged a Horse Race"
  - **The X That/Who Y** "The Burglar Who Only Moved Furniture", "The Window That Breaks Japan's Gambling Law"
  - **Levels of…**
  - **This X Found Y**

---

## 3. Visual style

### 3.1 Art direction
- **Characters** are flat 2D cartoons:
  - big round heads, thick black outlines, stick limbs
  - simple faces: half-lidded "knowing" eyes, dot eyes, a grid-teeth grin, a blush dot
  - each wears one bold identifying costume item (boater hat, bicorne, red cap, KYLE name tag)
- **Environments** are toon-shaded 3D with black outlines. Texture is painterly, with hand-hatched rock and streaked walls.
- Because the world is 3D, camera moves produce **real parallax**, while the characters keep a flat look.
- **No film grain**, checked at 1:1 crops.
- **Set dressing does the writing's job.** Readable signs, labels, documents, counters, maps and UI carry jokes and information:
  - "PARKING 10¢", "THAT'S MY BOY! ♥", "BRAIN NOT INCLUDED", "PATROL LOG — GAMBLING: NONE ☑", "LABOR LAW 労働法" padlock
  - a ledger stamped SOLD for every year except one
  - a corkboard bar chart: "CLERKS vs EVERYONE ELSE"
  - a counter going 0047 → 0048
- Infographics are always **physical props in the set**, never flat overlays.
- Sets are often built from the script's idioms. Video 10's "bait" story happens in a bait-and-tackle shop, with tickets hung on fish hooks.
- **Plants and payoffs live in props.** The answer is often visible in the first frames:
  - the burglar's key on his belt at 0.6 s (12)
  - the token window in shot 1 (18)
  - the smirking "dead" man (09)
  - the glowing number row (08)

### 3.2 Lighting
- **Practical lights carry the key:** desk lamps, pendants, lanterns, candles, windows, neon, phone screens, glowing objects. They have visible light cones, **bloom and haze**, and pools of light on floors.
- **The warm/cool split is the base look.** Warm practicals sit against a **cool blue, indigo or violet ambient fill**.
- **Shadows are never neutral black.** The darkest colour cluster in every video is a violet or plum near-black (#151230, #1f182b, #2a193f, #2c1b31, #2f232d).
- **Characters take the colour of the key light**, with a thin rim highlight along the outline.
  - In 08, the winning card lights the face gold and the losing card lights it sickly green, timed to the words "winner" and "garbage".
  - The mirror flash in 04 throws a warm patch onto the hero's face.
- **Signature setups:**
  - god rays through barred or arched windows
  - hard, short sun shadows in daytime exteriors
  - a noir **bar of light across the eyes** (09)
  - venetian-blind shadows (10)
  - an emissive glowing ring in the night sky (05)
  - lightning flashes of 1–2 frames (03)

### 3.3 Colour and contrast (measured)
- **Saturation runs high:** 90–180 out of 255.
- **Contrast is moderate**, with a luma standard deviation around 45–60. The image is punchy but never crushed.
- **Brightness changes by story section,** from about 60 (night alley) to 175 (daylight theory).
- **Each story section gets its own colour temperature.** Warm/cool swings of ±60–130 within one video are normal.
  - **Blue or night = suspense or complication:** the storm in 03, the stakeout in 12, the alarm in 13, the night press in 05.
  - **Warm, gold or sunset = payoff, memory, reunion, or "inside the mechanism":** the galley in 03, the inside of the slot machine in 19, the red interior of the body in 17, the sunset ending in 15.
  - **A cold flip for a tragic twist:** in 07 the warm hospital reunion (+45) dissolves into a cold blue close-up (−38) at the line "Jerry has no idea who this kid is."
  - "The reveal goes darker" is **one option, not a rule**. In 03, 05, 08, 13 and 19 the reveal is brighter and warmer than the suspense before it.
- **Example palettes:**
  - Video 03: ultramarine #375ad3, deep cobalt #131c84, plum-black #291822, copper wood #80452a, amber #d78033.
  - Video 09: aubergine #2a193f, rust #784036, blush #e0b8b5, indigo #3e3787, ochre #a48843.

### 3.4 Effects
- **Shallow depth of field.** Foreground props are blurred, and backgrounds go soft in close-ups.
- **Bloom** on every emissive: lamps, neon, screens, the forge, LEDs.
- **Particles:** rain, snow, dust, sparks, smoke, debris, money rain, sparkle motes.
- **Cartoon effects:** sweat drops, steam from the ears, stink lines, speed lines, impact stars and shockwave rings, a red "rage aura" (darkened head, glowing eyes, vein-cracks over the set), and an anime power-up (06).
- **One-frame flashes** for explosions and lightning.
- **Masks:** an iris spotlight (10) and a telescope mask (04).
- **Time-lapse grade:** a day → sunset → night → day colour cycle in about 1.5 s, on the line "A whole week went by" (16).

---

## 4. Camera movement
- **The camera never stops.** 96% of shots have measurable motion. The default is a **slow push-in at 5–20%/s with a gentle roll of 2–10°/s**, a "drifting" camera. Push-ins outnumber pull-outs about 2:1 (271 vs 145 shots).
- **Punch-ins on the key word** run 40–210%/s:
  - a whip push-in to the stopwatch on "exactly 15 minutes"
  - a dive at 166%/s to the button
  - a 208%/s pull-out on "rip the bench"
- **Whip pans** reach 1.24 frame-widths per second with roll. Roll-whips circle a character (02).
- **Cranes** move between scales: up through a roof to a map ("all over the country"), from the pedestal up to an aerial view of the town ("built around it in perfect circles").
- **The longest take (6–11 s) holds the turn or the explanation,** nearly locked off, with action **staged in depth**. In 10, the undercover agent walks in at the back while the cashier cheers in the foreground.
- **The opening comes in two flavours:**
  - one continuous move that acts the hook out literally (spear into anvil, pill into mouth, cannonball ride); this is the most common;
  - a micro-burst of 0.2–0.4 s shots (02, 03, 11).
  - Video 05 opens on a static shot, a deliberate exception.
- **Static shots are rare and purposeful:** emotional dialogue, a reunion, a held beat before a payoff.

---

## 5. Editing
- **Pace:** about 25 transitions per minute, with an average shot length of 2.5 s.
- **Transitions are cross-dissolves by default.** About 90% are dissolves, with a median length of 14 frames.
  - **30–45-frame dissolves** mark jumps in time or memory: into a memory (07), night to sunrise (09).
  - **Hard cuts** (about 2 per video) are saved for gags, punchlines, number reveals and flash frames.
- **Transitions are silent.** Measured: there is no whoosh or impact energy at transitions.
- **Edits follow the sentence.**
  - A dissolve *starts* within 0.25 s of a new sentence 34% of the time, against 12% by chance. The median offset is +0.04 s.
  - Inside a sentence, the picture changes on the **noun being named** ("300", "stomach", "blood", "undercover").
  - Lists get one shot per item.
- **In-camera transitions hide the big jumps:**
  - pushing into a pupil that becomes a porthole (06) or a brain room (20)
  - pushing through a mirror's reflection (04), a photo, or a phone screen
  - a door opening in a man's face (20)
  - a foreground object or character wiping past
  - 2D smoke-cloud wipes
  - flipbook pages
- **Montage bursts** of 0.4–1 s shots for lists, journeys and time passing.
- **The detector's limits:** some fast camera moves or pose swaps were logged as cuts, and some 7–9-frame dissolves were missed. The agents corrected these by eye in the reports.

---

## 6. Captions
- **Font:** heavy, rounded geometric sans in white, with a black outline and a soft drop shadow. I couldn't identify the exact font. *(inference: something in the Nunito Black / Poppins ExtraBold family.)*
- **Position and size:** centred horizontally, at about **70% of frame height**. The text is small, roughly 4% of frame height.
- **Chunking:** 1–3 words per card ("to fire", "the building.", "The next morning,").
- **Timing:** each card appears about **one frame (0.03–0.04 s) before** its spoken word, measured on 3 videos.
- **No animation:** no pop, scale, fade, colour highlight or emoji. Cards switch instantly.
- **Formatting:** punctuation is kept, and spoken numbers become numerals and units ("300 pounds" is shown as "300 lbs"; "a thousand pounds" as "1000 lbs").

---

## 7. Character animation
- **Pose-to-pose:** expressions are instant face swaps, not tweens. In 01, calm → furrowed → gritted teeth → sinister grin happens in about 4 frames.
- **Lip-sync only on quoted dialogue:** mouth flaps switch between open, gritted and flat every 2–4 frames. The narration is never lip-synced.
- **The "knowing" hero face:** a deadpan, half-lidded smirk that holds steady while everyone else panics. It makes the twist feel earned.
- **Comic beats are full-body:** legs sticking out of a trash can, a face-plant into sand, a hat flying off, crowds bobbing and pumping arms.
- **Movement:** lanky walk cycles. Background crowds are copied figures standing still.

---

## 8. Audio
- **Loudness is −14 LUFS integrated** in every video (YouTube's normalisation target), with a loudness range of about 2 LU. The voice is heavily compressed and very even.
- **The voice-over starts on frame 0**, with no intro.
- **A music bed runs throughout.** The level between words is −22 to −28 dB, against about −17 dB for speech. The bed runs about 6–7 dB under the voice, and YouTube's auto-captions tag it `[music]`.
- **No sound effects at transitions** (measured). I didn't measure sound effects inside scenes.
- **Not determined:** whether the voice is human or synthetic. Nothing here measures that.

---

## 9. Making something in this style
This is the craft, distilled for building your **own** stories and characters.

1. **Topic:** a real-world rule, loophole or mechanism, exploited by one clever person and told as a story with a twist. Pure "how X works" explainers underperformed on this channel.
2. **Hook (≤4 s, about 14 words):** the strange act, past tense, one exact number or detail, no reason given.
3. **Script:**
   - about 210–235 words for 60 s, at about 225 wpm with almost no pauses
   - historical present for the story
   - a skeptic with one quoted line
   - an ironic-joy beat
   - an escalation ladder
   - "But / Until / Instead" for the turn at 70–90%
   - "You see," plus a one-to-three-sentence real mechanism with an everyday analogy
   - end on the payoff word; optionally write the last line to flow into the first
4. **Visual:**
   - flat outlined characters in outlined toon 3D sets
   - practical-light key with bloom, cool violet fill, violet shadows
   - shallow depth of field
   - one colour temperature per story section (blue for suspense, warm for payoff)
5. **Camera:** always drifting forward (5–20%/s, slight roll); punch in on key words; hold the longest take on the turn.
6. **Edit:**
   - 12–16-frame dissolves started on sentence starts
   - 30–45-frame dissolves for time jumps
   - hard cuts only for gags
   - hide big jumps in pushes through eyes, mirrors, screens or doors
7. **Captions:** 1–3-word cards, white heavy rounded font with black outline, at 70% height, appearing 1 frame early, no animation.
8. **Mix:** −14 LUFS, compressed voice, music bed about 6–7 dB under, silent transitions, cut within 0.3 s of the last word.

---

## 10. Files
| Path | What |
|---|---|
| `videos/` | the 20 source videos (1080×1920, 30 fps) and their YouTube metadata |
| `analysis/transcripts_all.md` | all 20 transcripts with timestamps (3 Whisper errors corrected by hand) |
| `analysis/transcripts/*.json` | word-level timings |
| `analysis/reports/videos_01-05.md` … `16-20.md` | per-video deep dives: full transcript, beat-by-beat script breakdown, section colour stats, shot-by-shot camera notes, effects, animation, loop check |
| `analysis/channel_stats.json` | per-video numbers (pace, hook, shots, colour arc, audio) |
| `analysis/frames/*_frames.csv` | per-frame stats for all 33,664 frames |
| `analysis/edit/*_edit.json`, `*_dense.jpg` | detected transitions and shot moves; 2 fps contact sheets |
| `analysis/stills/` | full-resolution stills and frame strips the analysis references |
