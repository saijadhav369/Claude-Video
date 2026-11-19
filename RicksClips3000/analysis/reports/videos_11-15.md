# RicksClips3000: videos 11–15, visual and script breakdown

**Sources:** info.json, Whisper word timings, the edit json (transitions, shots and optical-flow moves), the per-frame CSV, the dense sheets, and stills and frame strips I extracted myself. The stills are in `analysis/stills/`. Composites are named `v11_key.jpg`, `v12_loop.jpg`, `v14_strip_17.4.jpg` and so on. Single frames are named `NN_<id>_<t>.jpg`.

**Metrics used:**
- **luma:** 0–255.
- **contrast:** luma standard deviation.
- **sat:** mean saturation, 0–255.
- **warm:** mean R−B. Positive means warm and negative means blue.
- **vignette:** centre luma minus edge luma.
- **WPM span:** words ÷ (end of the last word − start of the first word).
- **Articulation WPM:** words ÷ the summed durations of the words, so pauses are excluded.

"(inference)" marks interpretation. Everything else was measured or seen in frames.

---

## 0. Cross-video findings that refine the channel summary

1. **"Imagine you…" is not the template.** Only #11 uses second-person "Imagine".
   - #12, #13 and #15 are third-person stories that open with "A man…", "He…" and "A knight…".
   - #14 opens with a second-person conditional ("If your ship…") and then switches to third-person explanation.
   - What stays the same across all five: the hook is 13–19 words long and lasts 3.4–5.3 s. It states a paradox or a strange, specific act. The first word starts at 0.00 s, with no intro and no title card.
2. **"You see," is the house pivot phrase.** It appears in 4 of 5 videos, in two positions:
   - right before the reveal (#11 at 49.24 s, #12 at 50.94 s);
   - straight after the hook, to deliver backstory (#13 at 7.32 s, #15 at 3.50 s).
   - #14 does not use it.
3. **Ridicule, then vindication.** Someone dismisses the protagonist: the officer laughs in #12, and the court laughs three times in #13. Each video also has one quoted line of in-world dialogue mid-story:
   - #11: "wait, I'm getting paid for this?"
   - #12: "so someone broke in to move your furniture an inch?"
   - #13: "Hey, it's the toy guy. Did your frogs get hungry again?"
4. **Twist timing.** The twist lands at 70–91% of the runtime. The explanation that follows lasts 4–16 s, and the video ends on that explanation line: no call to action, no outro. The audio stops 0.12–0.28 s after the last word.
5. **None of the five loops seamlessly.** No last frame matches its first frame, and no last line runs grammatically into the first. Each video instead uses an abrupt end (a tail of 0.3 s or less) plus a thematic bookend (#11, #14 and #15; details in each section).
6. **A hook burst (shots of 0.2–0.4 s) appears only in #11.**
   - #12–#15 open on shots of 0.7–3.3 s. #15's hook is a single 3.27 s push-in, and #14's is one continuous camera ride on a cannonball.
   - When a fast montage appears, it comes right after the hook: #15 at 3.3–6.2 s, #12 at 4.1–5.5 s.
7. **"The reveal goes darker and bluer" holds only for #11.** A better rule across these five: the night or blue section carries the suspense, and the reveal is often brighter and warmer.
   - #13: the night alarm has warm −57.5 and luma 88. The rubble reveal has warm +73 and luma 164.
   - #12: the night stakeout has warm −10. The daytime sale reveal has warm +32.5.
   - #15 never cools down and ends at its warmest (+63.7, sunset, vignette 39).
8. **Transitions.**
   - 88–96% are cross-dissolves, with a median of 12–14 frames (range 3–32).
   - "Hidden" transitions also appear:
     - 2D smoke-cloud wipes (#14)
     - foreground-object wipes (#15)
     - pushes through a photo or phone screen (#11, #12)
     - a whip pan with speed lines (#13)
     - long continuous single-take camera moves (#14: 6.5–18.0 s and 37.1–47.0 s)
   - Edit rate is 23–30 transitions per minute. Average shot length (ASL) is 1.9–2.5 s.
9. **Transitions sit on clause boundaries.**
   - 32–54% of transitions fall within ±0.2 s of a clause start. Random times do so only 14–24% of the time.
   - 50–70% of sentence starts (7 of 14 up to 7 of 10) have a transition within 0.25 s.
10. **Planted props pay off later.**
    - #12: the burglar's gold key, on a red house-shaped keychain, is on his belt at 0.6 s, long before "kept one key" at 50.9 s. It is still on his belt in the last shot.
    - #11: the boss dangles a red "STORAGE" key tag at 3–4.5 s.
    - Gag text on props: "LANGRAGE" plaque slides down to reveal "GARBAGE" (#14); a price-of-sins tower topped by "Kicking the Bishop's Goat – 150" and a crowned "The Very Worst – 1000" (#15); a "LABOR LAW 労働法" padlock on a fire alarm (#11); a pardon signed "Fr. Tetzel" (#15).
11. **Reactions are shown in reflections.** The emperor appears in his wine bowl (#13, 20.5 s), and the priest appears in the knight's sword blade (#15, 21.3 s).
12. **Captions** have the same style in all five. Each caption card shows 1–3 words, for example "losing his mind." or "The next morning,". Spoken numbers become numerals and units: "a thousand pounds" is captioned "1000 lbs", and "1700s," also appears as numerals.
13. **Audio (inference, not checked by ear).** Inside narration pauses, the level sits at −15 to −38 dBFS against roughly −17 dBFS for speech. That suggests a continuous music or effects bed rather than silence.

| # | Title | Dur | Views (likes) | Words | WPM span / artic. | Sentences (mean words) | Transitions (dissolve/cut) | Per min | Median dissolve | ASL | Shots starting <2 s |
|---|---|---|---|---|---|---|---|---|---|---|---|
| 11 | The Job Nobody Wants in Japan | 60.5 s | 16,469,677 (612k, 3.7%) | 225 | 224 / 253 | 15 (15.0) | 23 (22/1) | 22.8 | 13 f | 2.52 s | 5 |
| 12 | The Burglar Who Only Moved Furniture | 58.4 s | 8,076,546 (204k, 2.5%) | 239 | 247 / 263 | 14 (17.1) | 25 (23/2) | 25.7 | 14 f | 2.34 s | 2 |
| 13 | The Ancient Jar That Warned an Empire | 64.9 s | 31,370,819 (886k, 2.8%) | 235 | 218 / 239 | 19 (12.4) | 26 (23/3) | 24.1 | 13 f | 2.40 s | 2 |
| 14 | Levels of Pirate Cannonballs | 63.5 s | 8,840,167 (211k, 2.4%) | 221 | 209 / 222 | 9 (24.6) | 27 (24/3) | 25.5 | 14 f | 2.27 s | 2 |
| 15 | This Knight Found the Ultimate Loophole | 40.6 s | 1,615,018 (41k, 2.5%) | 158 | 234 / 258 | 10 (15.8) | 20 (18/2) | 29.5 | 12 f | 1.94 s | 1 |

The description of every video is just its title. The uploads ran from 2026-10-18 (#15) to 2026-10-22 (#11).

---

## Video 11: "The Job Nobody Wants in Japan"

Runtime is 60.5 s (61 s in info.json), with 16.47M views. Uploaded 2026-10-22. It has the highest like rate of the five.

### Transcript
> It's impossible to get fired in Japan, but companies found something way worse. Imagine your boss walks you past your desk to a tiny room with no computer and no work. Just a ticking clock and a guy with his feet up, scrolling on his phone like he's on vacation. Your new job, your boss says, is nothing. Just sit here until six, and you're thinking, wait, I'm getting paid for this? At first, it's paradise. Then, your co-workers start staring when you walk past. The emails stop, and your old desk already has someone else's family photos on it. Every Friday, your boss pops his head in with a big smile to ask how you're enjoying your new role. Still, the guy in the corner has been doing this for three years and looks happier than anyone in the building. So, if they want to pay you to do nothing, fine, you kick your feet up right next to him. Then, one Monday, you walk in, and he's gone. His chair is pushed in, his desk is cleared, and nobody will tell you where he went. You see, Japanese law makes it almost impossible to fire someone, but there's no law against making them miserable. So, they take away your work and your friends and just wait, because nobody can do nothing forever.

### Script breakdown
- **Hook** (0.00–4.26 s, 13 words): "It's impossible to get fired in Japan, but companies found something way worse."
  - Device: an absolute claim, then "but", then a vague superlative. The open question is "what's worse?".
- **Setup** (4.52–19.72 s): "Imagine…" in the second person, present tense.
  - A concrete inventory of the room: "no computer and no work. Just a ticking clock and a guy with his feet up."
  - The inner-voice question "wait, I'm getting paid for this?" has a 0.34 s pause before "wait," for comic timing.
- **False high** (19.86–21.36 s): "At first, it's paradise." This is the shortest sentence (4 words) and the slowest segment (160 wpm).
- **Escalation** (21.68–33.0 s): a ladder of small social losses, linked by time markers ("Then," and "Every Friday").
  - co-workers stare
  - emails stop
  - the old desk has "someone else's family photos"
  - the boss asks "with a big smile" how you're enjoying your new role
- **Counterpoint** (33.22–42.22 s): "Still, the guy in the corner… looks happier than anyone in the building," followed by "So… fine, you kick your feet up right next to him."
- **Turn** (42.34–49.06 s, about 70% in): "Then, one Monday, you walk in, and he's gone."
  - It is followed by a tricolon: "His chair is pushed in, his desk is cleared, and nobody will tell you where he went."
- **Reveal** (49.24–54.88 s, about 81% in): "You see, Japanese law makes it almost impossible to fire someone, but there's no law against making them miserable."
  - This is a near word-for-word callback to the hook, built on a "but" contrast.
- **Ending** (54.88–60.28 s): "…because nobody can do nothing forever."
  - An aphorism that plays on "nothing": the job is nothing, you do nothing, nobody can do nothing forever.
- **Loop:** none in the sentence. Read straight on, it would be "…forever. It's impossible to get fired…", which does not run on grammatically. The bookend is thematic: hook and reveal share the same phrase.
- **Point of view and tense:** second person, present tense. "You" or "your" appears 20 times.
- **Devices:**
  - "but" contrast, twice
  - the tricolon above
  - callbacks: "impossible to fire", "feet up", "nothing"
  - one rhetorical question
  - a time ladder: At first → Then → Every Friday → three years → one Monday
- **Pace:**
  - 225 words; 224 wpm span, 253 wpm articulation.
  - Sentences average 15 words (range 4–21).
  - 14 pauses of 0.2 s or more, the longest 0.34 s.
  - Pauses come after discourse markers ("Then,", "Still,", "You see,", "Monday,") rather than at full stops.
  - Fastest segment: "So, if they want to pay you…" at 291 wpm.

### Visual
- **Settings:**
  - the boss's office: wood panelling, a 誠 ("sincerity") hanging scroll and a red FIRE EMPLOYEE button;
  - an open-plan office: white ceiling grid, cobalt carpet, desks with monitors;
  - the "Career Development Room" (キャリア開発室): mint-green tiled walls, a wall clock, two bare desks, a HAWAII suitcase;
  - the night exterior of a glass office tower;
  - a corridor.
- **Palette:** cobalt or royal blue (carpet and night); mint or sage green (tiles); white and pale grey (office); warm amber or yellow (sun shaft, lamp, lit window); signal red (button, ties, calendar header, fire alarm); orange-brown wood (boss's office).
- **Lighting:**
  - **Office:** high-key, with flat top light from the ceiling panels.
  - **Room:** a hard-edged diagonal yellow sun shaft falls across the green tiles (seen at 10.8 s and 35–36 s).
  - **Boss's office:** warm wood bounce light with a rim light on the boss's head.
  - **Night exterior** (37.0–39.5 s): blue ambient light and a pink-violet horizon. Only one window glows warm amber, the room with the happy idler, while every other floor is blue and dim with workers at desks.
  - **Reveal corridor:** the set is re-lit. The same door appears with a warm wall sconce (top right) throwing a radial pool of light onto blue walls.
- **Colour by section (CSV):**

  | Section | luma | contrast | sat | warm | vignette |
  |---|---|---|---|---|---|
  | Hook 0–4.5 | 88.9 | 50.4 | 147.8 | −7.7 | 27.6 |
  | Middle 4.5–33.2 | 155.7 | 58.4 | 86.7 | −16.1 | 6.8 |
  | Build 33.2–49.3 | 123.6 | 43.9 | 120.9 | −37.8 | 8.4 |
  | Reveal 49.3–54.9 | 106.0 | 57.2 | 127.1 | −36.2 | 18.1 |
  | End 54.9–60.5 | 87.1 | 52.5 | 147.4 | −66.6 | 31.0 |

  - The night exterior at 37.5–40 s reaches warm −98, the bluest moment.
  - The arc runs dark and saturated (hook) → bright and desaturated (the office's "paradise") → progressively darker and bluer, with heavier vignette.
- **Depth of field and blur:**
  - The hook push-in has a strongly blurred background (the worker behind the button) plus motion blur during the speed ramp.
  - The FIRE button frames carry a red glow and bloom.
- **Effects and gags:**
  1. **Speed-ramped push-in** onto the FIRE EMPLOYEE button (0–0.2 s). Optical flow drops from 209%/s to 17%/s. The edit json logs a "cut" at 0.17 s, but frame by frame the move is continuous.
  2. **Ejector-seat gag.** A stick-arm hand presses the button on "fired" (about 1.2 s). The worker shoots up through a ceiling hatch on puffs of smoke, then drops back into his chair on "Japan" (about 2.0 s): impossible to get fired.
  3. **The button lamp dies** on "companies" (2.42 s). A 28-frame dissolve takes the scene to the boss, who grins and holds up the STORAGE key; a sparkle glints on "worse" (about 3.9–4.2 s).
  4. **Tear-off calendar** (29.0–30.0 s). Pages physically fly off, NOV FRI 11 → 18 → 25, then the camera pans to the door where the boss pops in.
  5. **iOS-style Mail screen**: "Inbox (0) / No new mail / Checking for Mail…" with a pull-to-refresh spinner (24.3–25.7 s). The camera pushes into the phone, then through the empty-mailbox icon, which becomes the transition to "your old desk".
  6. **Lights-down re-light dissolve** at 49.4–49.9 s, on "You see". The same corridor and door go from bright white to dark blue with a warm sconce; luma falls 167 → 98 over 5 frames.
  7. **A "PULL DOWN" fire alarm** locked with a "LABOR LAW 労働法" padlock, on "almost impossible to fire" (51–52 s).
- **On-screen text:** FIRE EMPLOYEE, STORAGE, CAREER DEVELOPMENT ROOM / キャリア開発室, HAWAII, NOV FRI dates, Inbox (0), LABOR LAW.

### Camera and edit
- **Counts:** 24 shots, 23 transitions (22 dissolves of 3–28 frames, median 13; one false cut). ASL is 2.52 s, or 3.11 s after the first 4 s. The longest shot runs 7.77–16.03 s (8.27 s): the room introduction, a slow pull-out at 3.8%/s.
- **Hook burst:** 0.17, 0.17, 0.40, 0.43 and 0.97 s (5 shots before 2.13 s), then 2.37, 3.27 and 8.27 s. This is the only video of the five with a true burst.
- **Moves:** 14 push-ins, 8 pull-outs, nothing static. 13 of 24 shots include a slow roll of 2–11°/s. Moves tied to the script:
  - pan-left at 0.24 w/s, "boss walks you past your desk" (4.50 s);
  - push-in at 43.8%/s, "paradise → co-workers staring" (21.30 s);
  - pull-out at 31.7%/s with a 6.7°/s roll, past the desk with the photos (25.60 s);
  - pull-out at 23%/s from the lit window to the whole tower, "happier than anyone in the building" (36.33 s);
  - push-in at 43%/s, "nobody will tell you where he went" (47.47 s);
  - a slow 5.9%/s push toward the Career Development Room door under the final line (54.03 s).
- **Sync:** 8 of 15 sentences start within 0.25 s of a transition, for example "Imagine" (−0.02 s), "Still," (+0.01 s), "You see," (+0.09 s) and "Just" (−0.07 s). The action also hits individual words:
  - button press on "fired";
  - lamp off on "companies";
  - glint on "worse";
  - calendar pages on "Friday" and "your".

### Character animation
- Cut-out ("puppet") 2D characters in 3D sets, animated in limited steps.
- When a character speaks within the narration, mouths are swapped every 2–3 frames. For example, the boss at 31–33 s cycles through gritted teeth, a wide grin, an open "o" and a flat line while his eyes stay as closed happy arcs (^^).
- Lip-sync is generic flapping, not matched to phonemes (inference).
- Expressions: the boss's permanent fake grin (comic, sinister); the idler's smug feet-up pose and sunglasses (a Dutch-angle shot at 20.5–21 s); a nervous wide-eyed white face at the end (59–60 s).

### Loop check
- **First frame:** a blurred push toward the red button in the boss's office.
- **Last frame:** a blue door marked CAREER DEVELOPMENT ROOM, with the worker visible through its window.
- No visual match. Both ends are blue-dominant (warm −49 for 0–2.5 s, −66 at the end), but the cut back to the start is not a match cut.

---

## Video 12: "The Burglar Who Only Moved Furniture"

Runtime is 58.4 s, with 8.08M views. Uploaded 2026-10-21.

### Transcript
> A man snuck into a family's house every night and moved every single thing one inch to the left. The first night, nobody notices, because who measures their couch? But by the end of the week, the fridge is blocking the back door, and the dad is pretty sure he's losing his mind. So they call the police. The officer looks at the couch, then at the dad, and goes, "So someone broke in to move your furniture an inch?" He laughs all the way back to his car. They start locking every door and window at night, but every morning, everything has still crept a little further, until the bed is pressed up against the wall. At this point, their daughter swears she hears something sliding across the floor at 3 a.m. So the dad camps out on the couch with a baseball bat, ready to catch whoever's doing this. He wakes up the next morning, and the couch is one inch to the left, with him still on it. By the end of the month, the couch is halfway across the living room, and the family can't take it anymore. They sell the house for half what they paid, and the buyer is him. You see, he'd sold them that house a year earlier and kept one key. So all it took was a month of sliding furniture to buy it back at half the price.

### Script breakdown
- **Hook** (0.00–5.28 s, 19 words): "A man snuck into a family's house every night and moved every single thing one inch to the left."
  - Device: a bizarre, hyper-specific act ("one inch to the left") with the motive hidden. Repeating "every… every" adds weight.
- **Setup** (5.50–8.56 s): "The first night, nobody notices, because who measures their couch?" A rhetorical question used as a joke.
- **Escalation, run on a time ladder:** first night → end of the week → night/every morning → 3 a.m. → next morning → end of the month.
  - Physical stakes rise: the fridge blocks the back door, the bed is pressed against the wall, the couch ends up halfway across the room.
  - Authority dismisses it. "So they call the police" is a 5-word sentence. The officer's line follows a 0.56 s pause after "goes," (the longest pause in the video), then "He laughs all the way back to his car."
  - Comic peak (39.02–43.16 s): "the couch is one inch to the left, with him still on it." This calls back the hook's phrase.
- **Turn** (47.84–50.80 s, about 82% in): "They sell the house for half what they paid, and the buyer is him."
- **Reveal** (50.94–54.24 s): "You see, he'd sold them that house a year earlier and kept one key."
- **Ending** (54.24–58.18 s): "So all it took was a month of sliding furniture to buy it back at half the price." This summarises the scheme; "half" is a callback.
- **Loop:** none. "…at half the price. / A man snuck into…" is a restart, not a run-on.
- **Point of view and tense:** third person throughout. The tense shifts:
  - the hook is in the past ("snuck", "moved");
  - the story is in the historical present ("nobody notices", "they call", "goes");
  - the reveal is in the past perfect ("he'd sold").
- **Devices:**
  - "so" four times as a causal engine
  - "but" twice
  - "every" four times
  - callbacks: "one inch to the left", "half"
  - a dialogue quote
- **Pace:** the fastest read of the five, at 246.5 wpm span and 263 wpm articulation, with only 4 pauses of 0.2 s or more. Sentences are the second-longest (mean 17.1 words, up to 28). From 39 s onward most segments run at 255–286 wpm, which feels breathless.

### Visual
- **Settings:**
  - a suburban house at night: blue clapboard siding, an AC unit, pumpkins (autumn);
  - a daytime living room: red couch, yellow curtains, cream walls;
  - a kitchen: teal fridge, teal-and-white checker floor, yellow walls;
  - a child's bedroom at night;
  - the living room at night, for the stakeout;
  - the front yard by day: pale teal house no. 27, red door, FOR SALE sign;
  - the flashback photo.
- **Palette:** indigo or cobalt night blue, cyan moonlight, red couch, mustard yellow (curtains, walls), teal (fridge, floor), orange tabby cat, lawn green.
- **Lighting:**
  - **Hook:** blue moonlight rims the siding from the left. A circular pool of light on the lawn falls off into dark edges (vignette 42.4 for 0–2.5 s, the strongest hook vignette in this set).
  - **Daytime interiors:** high-key, warm and sunny.
  - **Bedroom:** a glowing cyan bunny night-light and star decals.
  - **Stakeout:** backlit by a full moon in the window, with a warm lantern on the side table as the practical light and a headlamp on the dad.
  - **3 a.m. shot:** a floor-level glide down a warm-lit hallway.
  - **Reveal:** flat, bright daylight.
  - **Final shot:** a blue night window behind a warm-lit couch.
- **Colour by section (CSV):**

  | Section | luma | contrast | sat | warm | vignette |
  |---|---|---|---|---|---|
  | Hook 0–5.4 | 87.4 | 49.9 | 154.7 | −59.0 | 32.9 |
  | Day escalation 5.4–30.5 | 160.8 | 62.0 | 90.5 | +11.8 | 7.6 |
  | Night escalation 30.5–47.8 | 125.7 | 58.2 | 135.3 | −10.1 | 7.1 |
  | Twist (sale, day) 47.8–50.9 | 158.2 | 52.4 | 94.5 | +32.5 | −9.1 |
  | Explanation / end 50.9–58.3 | 127.6 | 56.4 | 116.0 | −2.2 | −2.3 |

  - The last 2.5 s drop to luma 80.7 (night).
  - The arc is a night → day → night sandwich, and the twist is daylight.
- **Depth of field:** the key close-up at 54 s has a blurred background; most other shots are deep focus.
- **Effects and gags:**
  1. **Ruler under the couch foot**, with indentation marks on the carpet, on "inch… left" (4.5–5.5 s).
  2. **Door-peephole fisheye POV**, with a brass rim and fisheye distortion of the police car outside, on "all the way back to his car" (22.0–23.1 s).
  3. **Floor-level skim:** the camera dives to the floorboards and glides on "sliding across the floor at 3 a.m.", landing on the cat (34.0–35.0 s; push-in 59%/s plus pan 0.27 w/s).
  4. **Continuous crane-up** (42.9–46.2 s). It starts on the slippers, still on the rug where the dad left them, while the couch has moved, and rises to a high-angle wide on "halfway across the living room".
  5. **Polaroid zoom-through:** the buyer holds up a photo captioned "SOLD! Welcome home". The camera pushes into the photo until it fills the frame (push-in 88%/s), entering the flashback on "that house a year earlier" (52.0–52.9 s). In the flashback the burglar is the realtor and winks (53.3 s).
- **On-screen text:** FOR SALE / SOLD / 50% OFF, 555-0142, "SOLD! Welcome home", house number 27.

### Camera and edit
- **Counts:** 25 shots, 25 transitions (23 dissolves of 4–31 frames, median 14; 2 cuts). ASL is 2.34 s and the longest shot is 6.43 s (the officer).
- **Opening:** no burst. Shots run 1.63, 1.03 and 1.43 s, then a micro-burst on "one inch": 0.43 s (push-in 60%/s with a 13°/s roll), then 0.93 s.
- **Moves:** 16 push-ins, 5 pull-outs, 2 static shots. The static ones are the peephole and the bed, which lets the gag image read.
- **Sync:** 7 of 14 sentences start within 0.25 s of a transition, for example "The" (−0.03 s), "officer" (−0.04 s), "At" (+0.05 s), "He" (−0.02 s) and "sell" (−0.05 s). Within ±0.08 s, transitions also land on "house", "moved", "all" and "night,".

### Character animation
- **Burglar:**
  - a balaclava with eye-holes in the hook, where he turns from front to back as a two-drawing turnaround and climbs the AC unit with a bouncy stride;
  - a full dark beard and hair as "the buyer" (50 s), whose silhouette echoes the balaclava (inference);
  - a beanie in the flashback and ending, with a smug half-lidded face.
- **Officer** (18–21 s): skeptical half-lidded eyes. His mouth swaps every 3–6 frames (open "o", flat line, smirk) during his quoted line, then he laughs with squinted eyes.
- **Dad:** round glasses, a worried brow, a baseball bat and a headlamp.
- **Cat:** a recurring witness. Its smug half-lidded eyes in the last shot mirror the burglar's.

### Loop check
- **First frame:** the burglar in the night yard.
- **Last frame:** the burglar and the cat on the red couch, with the SOLD sign in the window at night.
- Same character, same night-blue mood, but not a match. The gold key on the house-shaped keychain appears in both (crop: `v12_belt.jpg`).

---

## Video 13: "The Ancient Jar That Warned an Empire"

Runtime is 64.9 s, with 31.37M views, the most-viewed of the five. Uploaded 2026-10-19.

### Transcript
> He put a bronze ball in a dragon's mouth and told the emperor, "If this ever falls out, run." The whole court burst out laughing. You see, there were eight dragons coiled around a giant bronze jar, each holding a ball over a frog's open mouth. But the emperor had the biggest army in the world, and he wasn't about to run from a jar. Weeks later, a ball fell, but nothing happened, not even a ripple in the emperor's wine. Now they laughed even harder. The emperor called it the world's most expensive toy and threw the inventor out of the city, jar and all. So he dragged it up a hill outside the walls and lived there alone. Then one night, a ball dropped, then another, then all eight at once. He ran to the city gates, screaming for everyone to get out. "Hey, it's the toy guy. Did your frogs get hungry again?" The guards laughed him all the way back up the hill. The next morning, the palace was a pile of rubble. Inside the jar hung a heavy pendulum with a rod pointing at each dragon. The slightest nudge and the pendulum swung into a rod. The rod snapped the dragon's jaw open and the ball dropped. One ball meant a nudge from far away. All eight meant the biggest earthquake the empire had ever seen was right underneath them.

### Script breakdown
- **Hook** (0.00–5.00 s, 19 words): "He put a bronze ball in a dragon's mouth and told the emperor, if this ever falls out, run."
  - Device: a quoted cryptic warning that ends on a one-word imperative ("run.", set off by 0.26 s and 0.30 s pauses). It starts in the middle of the action with an unnamed "He".
- **Ridicule:** "The whole court burst out laughing." (6 words).
- **Exposition** (7.32 s): "You see," explains the device (eight dragons, frogs).
- **Counter:** "But the emperor had the biggest army in the world…"
- **False alarm** (17.80 s): "a ball fell, but nothing happened, not even a ripple in the emperor's wine."
- **Escalated ridicule:** "Now they laughed even harder." (5 words). Then the inventor is banished ("jar and all").
- **Isolation:** "So he dragged it up a hill… and lived there alone."
- **Turn** (33.00 s): "Then one night, a ball dropped, then another, then all eight at once." A rule-of-three count-up.
- **Warning ignored:** the inventor screams at the gates; the guards mock him ("Hey, it's the toy guy. Did your frogs get hungry again?"). This is the third round of laughter.
- **Payoff** (45.84 s, about 71% in): "The next morning, the palace was a pile of rubble."
- **Explanation** (48.58–60.20 s): the mechanism in short declarative steps: pendulum → rod → jaw → ball.
- **Ending** (60.44–64.78 s): "All eight meant the biggest earthquake the empire had ever seen was right underneath them." It reframes the hook's "run".
- **Loop:** none. The ending answers the hook's "run" (inference).
- **Point of view and tense:** third person, past tense, with two lines of quoted dialogue. "Then" appears three times.
- **Devices:**
  - triple laughter as escalation (laughing → laughed even harder → laughed him all the way back)
  - rule of three (a ball, another, all eight)
  - "but" twice
  - a "one… / all eight…" parallel in the explanation
- **Pace:**
  - The most measured read: 217.7 wpm span, 239 wpm articulation.
  - The shortest sentences: mean 12.4 words, with several of 5–6 words ("Now they laughed even harder.", "Hey, it's the toy guy.").
  - 13 pauses of 0.2 s or more.

### Visual
- **Settings:**
  - an imperial throne room: red and gold canopy, a rose window, columns, gold dragon heads on a grey bronze jar, silver frog statues;
  - a symmetrical parade ground with a massive army and snowy peaks;
  - a banquet hall;
  - the city gate;
  - a hill at sunset;
  - the hilltop at night;
  - the walls and portcullis, with torches;
  - a morning view of the city in ruins;
  - a cutaway inside the jar;
  - a far mountain;
  - a geological cross-section.
- **Palette:** crimson and gold (throne); slate and stone grey (jar, walls); royal blue (robes); sunset pink, orange and magenta; night periwinkle and navy; final strata in orange, teal and violet with a white-hot fault line.
- **Lighting:**
  - **Throne room:** warm braziers (fire practicals) and candle chandeliers, with specular gold highlights. The extreme close-up of the dragon has foreground fire bokeh and shallow depth of field (1.0–2.5 s).
  - **Sunset hill** (30–31.5 s): backlit sun with god rays, silhouettes and lens bloom. This section has the highest contrast in the video (70.8).
  - **Night:** a cool blue moon key, with glinting gold eyes on the frogs and dragons. The gates add warm torches against blue.
  - **Rubble:** hazy, warm morning light with atmospheric perspective.
  - **Jar interior:** a top-down radial composition lit by a ring of point lights.
  - **Final shot:** an emissive fault line with heavy bloom.
- **Colour by section (CSV):**

  | Section | luma | contrast | sat | warm | vignette |
  |---|---|---|---|---|---|
  | Hook 0–5.3 | 109.1 | 47.8 | 76.3 | +19.6 | 22.5 |
  | Ridicule / setup 5.3–32.9 | 107.3 | 51.2 | 98.7 | +29.2 | 24.5 |
  | Night alarm 32.9–45.9 | 88.1 | 38.3 | 134.9 | −57.5 | 12.4 |
  | Rubble payoff 45.9–48.6 | 164.0 | 41.0 | 103.4 | +73.0 | 10.9 |
  | Mechanism 48.6–58.2 | 113.7 | 41.6 | 90.7 | +46.3 | 11.2 |
  | Ending 58.2–64.8 | 142.6 | 46.7 | 110.5 | +62.5 | 10.1 |

  - The suspense is the darkest and bluest part; the payoff is the brightest and warmest.
- **Effects:**
  1. **Speed lines and a sweat drop** on "run." (5.0–5.3 s): white anime-style lines and a sweat drop on the inventor, then a whip pan (motion 42) to the laughing court.
  2. **Wine-bowl reflection:** a fast push-in (80%/s) onto the bowl on "happened", showing the emperor's grumpy reflection in still wine, then a pull-out on "not even a ripple" (19.9–22.5 s).
  3. **Destruction:** a smoke column, flying debris and birds over the rubble (46.5–48.5 s).
  4. **A ball falling** past the open jaw (55.5–58 s).
  5. **A distant mountain** with a dust plume for "a nudge from far away" (58.5–60 s).
  6. **Into the ground:** a dissolve to a cracked street, then the camera tilts and cranes down into a cross-section of strata (with a fossil fish and a violet cave pocket) to a glowing fault directly under the city, on "right underneath them" (61.6–64.8 s).
- **On-screen elements:** captions only, plus the device itself, used like a diagram (top-down view of the pendulum and rods at 49–53 s).

### Camera and edit
- **Counts:** 27 shots, 26 transitions (23 dissolves of 3–29 frames, median 13; 3 "cuts" at 41.63–42.10 s). ASL is 2.40 s and the longest shot is 6.33 s (the jar interior).
- **The 41.6–42.1 s "cuts":** in the frame strip this is a fast reframe on the guards. A foreground guard slides out, and the background guard turns to camera and winks on "Did". Treat these as reframes rather than true cuts (inference).
- **Opening:** shots of 0.73, 2.40, 0.77 and 1.37 s. The second shot rolls at −9.5°/s and has the highest shake (jitter 4.72).
- **Moves:** 14 push-ins, 10 pull-outs, 2 static. Static is held for the army wide (13.4–17.8 s) and the guards' gag.
- **Moves tied to the script:**
  - pull-out at 15.6%/s, "Then one night" (32.97 s);
  - push-in with a −9.6°/s roll into the jar interior, "Inside the jar" (48.60 s);
  - pull-outs with pans of 0.23–0.26 w/s, moving the camera "away" on "from far away" (58.27–61.57 s);
  - the final tilt-down into the ground on "underneath".
- **Sync:** the tightest of the five. 13 of 19 sentences start within 0.25 s of a transition, and 54% of transitions sit within ±0.2 s of a sentence start (random: 11%).

### Character animation
- **Inventor:** eyes swap from skeptical half-lids to wide round eyes within the first 0.5 s. He has a sweat drop and points upward on "run". He screams behind the bars of the portcullis.
- **Emperor:** a permanent grumpy brow and a downturned mouth, played for comedy.
- **Courtiers:** laugh with closed eyes and open mouths.
- **Guards:** a smirk and a wink.
- **Frogs:** glowing eyes and mouths that open as the balls drop.
- **Animation style:** limited, with pose and face swaps.

### Loop check
- **First frame:** the inventor beside the jar in the throne room.
- **Last frame:** the glowing fault line in the cross-section.
- No visual or verbal loop.

---

## Video 14: "Levels of Pirate Cannonballs"

Runtime is 63.5 s, with 8.84M views. Uploaded 2026-10-19.

### Transcript
> If your ship got hit by a cannonball, you'd actually be one of the lucky ones. In the 1700s, the Navy's round shot would smash through a pirate ship's wall and turn it into a storm of splinters that tore through half the crew. The pirates couldn't afford proper ammo, so they fired back with langrage, which is a fancy word for literal garbage. But the Navy had a nastier idea called hot shot. They shoveled cannonballs into a furnace until they glowed red, carried them over with giant tongs and dropped them in behind a soaking wet plug so the gunpowder wouldn't go off early. The ball buried itself deep in the pirate ship's hull, and a few minutes later, the whole ship lit up from the inside like a giant lantern. Not to be outdone, the pirates fired back with the carcass, a hollow cannonball packed with burning tar and punched full of holes, so it spat fire the whole way over and turned the entire Navy ship into a torch. Eventually, ships advanced from wood to iron, and the fireballs just bounced off. So America built the Rodman gun, a cannon that fired a single ball weighing over a thousand pounds, made to punch a hole in an iron warship big enough to sink it in one shot.

### Script breakdown
This video uses a different format: a **"Levels of…" escalation ladder**, not a twist story.

- **Hook** (0.00–3.82 s, 16 words): "If your ship got hit by a cannonball, you'd actually be one of the lucky ones."
  - Device: a counter-intuitive second-person conditional ("actually", "lucky") that implies a ladder of worse options.
- **Level 1, round shot** (3.96 s): a splinter storm.
- **Level 2, langrage** (11.92 s): pirates' garbage ammo, with an appositive definition played as a joke ("which is a fancy word for literal garbage").
- **Level 3, hot shot** (17.86 s): introduced with "But the Navy had a nastier idea". The process is a 32-word chain of verbs (shoveled / carried / dropped). Payoff: "lit up from the inside like a giant lantern".
- **Level 4, carcass** (37.14 s): "Not to be outdone…". The longest sentence of the five videos (40 words), ending "into a torch".
- **Level 5, Rodman gun** (48.94 s): a technological reset ("ships advanced from wood to iron, and the fireballs just bounced off"), then "So America built…". The superlative lands at about 84%.
- **Ending:** "…big enough to sink it in one shot."
- **Structure:** tit-for-tat escalation, alternating sides (Navy → pirates → Navy → pirates → America). Each level is a new noun plus a vivid result.
- **Loop:** none in the sentence. Thematically the end ("sink it in one shot") sits next to the hook ("If your ship got hit by a cannonball") (inference).
- **Point of view and tense:** the hook is second person; the body is third-person past and past-habitual ("would smash").
- **Devices:**
  - similes: "like a giant lantern", "into a torch"
  - definitions given inline
  - comparatives: "nastier", "Not to be outdone"
  - numbers: 1700s, a thousand pounds
  - no rhetorical questions and no "You see"
- **Pace:**
  - 209 wpm span and 222 wpm articulation, the slowest of the five.
  - Only 9 sentences, mean 24.6 words: an explainer register.
  - 5 pauses of 0.2 s or more, all at commas.

### Visual
- **Settings:**
  - 18th-century wooden warships on turquoise water among tall sandstone sea stacks and natural arches with green tops (a fantasy Caribbean or Ha Long look);
  - a Navy ship with a US flag and a crew in blue uniforms;
  - pirates in striped shirts and bandanas;
  - a brick "HOT SHOT" furnace on shore;
  - the pirate deck at dusk;
  - an ironclad: dark riveted hull and a smokestack;
  - a coastal fort with the Rodman gun hung from a wooden tripod.
- **Palette:** turquoise and aqua sea, sandstone peach and tan, warm wood brown and red-orange hulls, white sails, red-hot orange, dusk violet and magenta, iron blue-grey.
- **Lighting:**
  - **Daylight:** high-key, with soft shadows.
  - **Furnace** (23–24 s): a one-point-perspective brick tunnel with emissive orange coals, glowing balls and floating embers.
  - **Hull interior** (31–32 s): dark, with the glowing ball as the only light, a cartoon starburst and sparks.
  - **Dusk "lantern" shot** (33.2–37.1 s): a purple-pink sky, with warm light leaking from the gunports.
  - **Burning Navy ship:** emissive fire against violet.
  - **Final section:** cooler daylight.
- **Colour by section (CSV):**

  | Section | luma | contrast | sat | warm | vignette |
  |---|---|---|---|---|---|
  | Hook 0–3.9 | 131.8 | 48.4 | 128.8 | +30.6 | 7.7 |
  | L1 round shot 3.9–11.9 | 141.2 | 46.7 | 118.5 | +7.8 | −5.3 |
  | L2 langrage 11.9–17.9 | 138.0 | 44.4 | 117.8 | +36.3 | −13.0 |
  | L3 hot shot 17.9–33.2 | 131.7 | 47.3 | 118.2 | +25.6 | 12.8 |
  | Lantern dusk 33.2–37.1 | 87.7 | 51.3 | 144.7 | +17.5 | 45.8 |
  | L4 carcass 37.1–48.9 | 90.0 | 37.9 | 136.7 | +53.0 | 14.6 |
  | L5 iron / Rodman 48.9–63.5 | 129.7 | 46.7 | 105.5 | −18.9 | 2.6 |

  - The dusk "lantern" shot is almost still (motion 1.9) with the heaviest vignette, a held "beauty shot".
  - The fire level is the warmest. The iron level goes cool.
- **Particles and effects:**
  1. **Flat 2D muzzle-flash bursts** (orange-yellow, outlined) and speed streaks on the water behind the flying ball (1.4–2.3 s).
  2. **Splinter-storm particles:** the camera passes through the hull with the ball (6.5–8.5 s).
  3. **Label swap:** the brass "LANGRAGE" plaque slides down to reveal "GARBAGE" stencilled underneath, between "literal" and "garbage" (17.0–17.4 s). The cannon then fires a smoke puff full of junk.
  4. **Smoke-cloud wipes:** a 2D cartoon smoke cloud fills the frame and the next scene is revealed through a widening hole. Used at 17.6–18.3 s ("But the Navy") and 59.7–60.3 s ("punch a hole").
  5. **A personified gunpowder bag** with worried eyes and a sweat drop on "go off early" (29.0–30.2 s).
  6. **Sparks** on the iron hull on "bounced" (52.5 s).
  7. **A flat cartoon explosion** with flying planks (61 s), then a mushroom of black smoke. The comic button at the end is two soot-faced survivors floating in a barrel.
- **On-screen text:**
  - prop labels: HOT SHOT, LANGRAGE → GARBAGE, "CARCASS – KEEP FROM FLAME", POWDER, SHOT;
  - the "1000 lbs" caption.

### Camera and edit
- **Counts:** 28 shots, 27 transitions (24 dissolves of 4–32 frames, median 14; 3 cuts, including the smoke flash at 18.0 s). ASL is 2.27 s, median 1.3 s.
- **Two single-take camera moves:**
  - **6.47–18.0 s (11.5 s):** the camera follows the ball into the hull, across the deck and past the crew to the captain at the SHOT crate, then on to the langrage barrels.
  - **37.1–47.0 s (9.9 s):** the CARCASS crate → the pirates pouring tar → the cannon firing → following the fireball to the Navy ship burning in the distance.
- **Hook:** one continuous ride rather than cuts. The camera orbits the Navy cannon (roll 40.9°/s for the first 1.4 s), the cannon fires, and the camera rides the ball across the water (push-in 33.8%/s at 2.3 s).
- **Shake:** the most kinetic camera of the five, with duration-weighted jitter of 2.25 (the others are 1.1–1.5) and a maximum of 5.81 at 18.2 s. 18 of 28 shots roll.
- **Moves:** 10 push-ins, 14 pull-outs.
  - push-in at 54%/s through the hot-shot setup (19.4 s);
  - pull-out at 124%/s as the ball buries itself (31.67 s);
  - a near-static 2.2%/s hold on the lantern ship.
- **Sync:** 6 of 9 sentence starts have a transition within 0.25 s. Transitions also land on "Not" (−0.04 s), "Eventually," (+0.06 s), "America" (−0.13 s), "punch" (−0.05 s) and "big" (−0.03 s).

### Character animation
- **Navy captain:** smug.
- **Pirate captain:** a toothy grin (seen at 42 s).
- **Crews:** recoil from splinters with gritted teeth, and sweat.
- **Animation style:** limited pose swaps. Characters mostly react rather than speak; no in-world dialogue.
- **Comic beats** come from objects: the label swap, the sweating gunpowder bag, and the castaways in the barrel.

### Loop check
- **First frame:** the Navy officer and a cannon on deck under a US flag.
- **Last frame:** the smoke mushroom and the survivors in the barrel.
- No visual match.

---

## Video 15: "This Knight Found the Ultimate Loophole"

Runtime is 40.6 s, with 1.62M views. Uploaded 2026-10-18. It is the shortest of the five, has the fewest views, and has the highest edit rate.

### Transcript
> A knight paid a priest to forgive a crime he hadn't committed yet. You see, the priest was traveling from town to town selling forgiveness for coins. Lying had a price, stealing had a price, and the worse the sin, the more you paid. People lined up for hours to drop their money into his huge iron chest. So, the knight stepped up and asked to be forgiven for something he was planning to do next week. The priest hesitated, charged him extra, and stamped the paper anyway. A few days later, the priest left town through the forest, with the chest so full it took two men to carry it. That's where the knight was waiting. He took every last coin, and when the priest screamed that he'd go to hell for it, the knight just held up the paper. The crime he'd paid to be forgiven for was robbing the man who sold it to him.

### Script breakdown
- **Hook** (0.00–3.36 s, 13 words): "A knight paid a priest to forgive a crime he hadn't committed yet." Device: a logical paradox; the crime is withheld.
- **Backstory** (3.50 s): "You see," explains the trade in pardons.
  - Rule of three with a twist: "Lying had a price, stealing had a price, and the worse the sin, the more you paid."
  - A greed image: "huge iron chest".
- **Request** (16.14 s): "So, the knight… asked to be forgiven for something he was planning to do next week."
- **Greed beat:** a tricolon of verbs, "The priest hesitated, charged him extra, and stamped the paper anyway."
- **Set-up for the payoff** (24.22 s): the chest is "so full it took two men to carry it".
- **Turn** (29.82 s, about 73% in): "That's where the knight was waiting." A 6-word punch.
- **Escalation:** "He took every last coin… screamed that he'd go to hell… the knight just held up the paper."
- **Reveal and ending** (36.78–40.56 s, about 91% in): "The crime he'd paid to be forgiven for was robbing the man who sold it to him."
  - The last line resolves the hook's paradox; the twist is saved for the final sentence.
- **Loop:** none in the sentence. The ending closes the hook's question.
- **Point of view and tense:** third person, past tense, ending in the past perfect. No dialogue is quoted (the priest's scream is reported speech).
- **Devices:**
  - tricolons, twice
  - "the worse… the more" parallel
  - "So," twice
  - callbacks: "the paper", "forgiven"
  - no "but"
- **Pace:**
  - 233.7 wpm span and 258 wpm articulation.
  - Sentences average 15.8 words.
  - 10 pauses of 0.2 s or more, mostly 0.2–0.3 s after "You see," and inside the lists.
  - The final 3 sentences speed up to 270–318 wpm into the reveal.

### Visual
- **Settings:**
  - a medieval market town (half-timbered houses, thatched and terracotta roofs, a church spire);
  - the "Pardons" stall with a red-and-white striped awning and a crossed-keys banner;
  - a travel montage: the priest's donkey cart through a thatched village, a harbour, and a snowy town at night;
  - a forest of tall trunks;
  - a sunset road with a windmill and castle silhouettes.
- **Palette:** sky blue with puffy white clouds, red-and-white stripes, terracotta, grass green, parchment cream, the priest's red and gold robe, the knight's silver; forest khaki and sage; sunset orange, magenta and violet.
- **Lighting:**
  - **Town:** hard midday sun. The hook has the highest contrast of any section in these five videos (67.1).
  - **Forest** (27.5–33 s): volumetric light shafts slanting from the upper left through haze. Saturation drops to 66–78.
  - **Final shot:** sunset backlight with long shadows stretching toward the camera; vignette 36–42.
- **Colour by section (CSV):**

  | Section | luma | contrast | sat | warm | vignette |
  |---|---|---|---|---|---|
  | Hook 0–3.4 | 124.0 | 67.1 | 129.9 | +30.4 | 14.3 |
  | Backstory 3.4–16.1 | 131.1 | 56.0 | 125.9 | +14.2 | 13.2 |
  | Request 16.1–24.3 | 135.5 | 60.5 | 119.5 | +40.5 | 2.0 |
  | Forest 24.3–29.7 | 133.1 | 42.4 | 107.4 | +50.6 | 9.7 |
  | Robbery 29.7–36.7 | 149.3 | 50.7 | 85.0 | +47.3 | 9.5 |
  | Reveal / end 36.7–40.6 | 151.0 | 49.3 | 102.8 | +63.7 | 39.0 |

  - There is no dark or blue section; the snowy night shot is the only cool moment (warm −28 at 5–7.5 s).
  - Warmth climbs steadily to the end.
- **Depth of field:**
  - a macro shot of a quill writing "Next Week", with a strongly blurred background (19.5–20.6 s);
  - a sword-blade reflection shot with a blurred stall behind (21.0–21.8 s).
- **Effects:**
  1. **Coin-bag toss** in an arc with sparkle particles (0–1.5 s).
  2. **Pardon document card** (3.5 s). It has an illuminated initial "P" and reads "absolves the bearer of the sin of One Crime / to be committed Next Week". It carries a red FORGIVEN stamp and "Fee paid ~~10 coins~~ 40 coins!" (the price struck through), signed "Fr. Tetzel".
  3. **Foreground-object wipes** in the travel montage: a tree trunk at 5.0–5.2 s and a signpost at 6.0 s. The cart stays at the same screen position across village → harbour → snowy night.
     - The signpost reads MACKEREL / FRESH COD / BOSTON / NO. 7 PIER, which is out of period for a medieval story (possibly a reused asset; inference).
  4. **"Price of Sins" tower:** a camera tilt up an ever-taller stack of illustrated price cards, in ascending order:

     | Sin | Price |
     |---|---|
     | Lying | 2 |
     | Stealing | 5 |
     | Gambling | 12 |
     | Sloth | 20 |
     | Gluttony | 35 |
     | Cursing | 60 |
     | Kicking the Bishop's Goat | 150 |
     | The Very Worst (crowned seal) | 1000 |

     The tilt reaches the seal on "you paid" (10.5–12.2 s). The priest uses a pointer stick.
  5. **Sword-blade reflection** of the hesitating priest, with a sweat drop (21.3 s).
  6. **Forest god rays** (28–31 s).
  7. **Gold coin with a cross** thrown at the camera as a forced-perspective close-up (33.0 s).
  8. **The priest's whole body turns red** with rage (34.0 s).
  9. **Little red imps with pitchforks** and glowing lava cracks in the ground around the knight on "go to hell" (34.5–36.5 s).
  10. **The pardon card returns** full-frame on "The crime" (37–38.5 s).
- **On-screen text:** "Pardons" sign, the pardon document, the Price of Sins cards, FORGIVEN.

### Camera and edit
- **Counts:** 21 shots, 20 transitions (18 dissolves of 5–23 frames, median 12; 2 cuts). ASL is 1.94 s, the fastest of the five, and the longest shot is 4.77 s.
- **Hook:** a single 3.27 s push-in at 19.4%/s.
- **Travel montage** (3.27–6.23 s): shots of 0.47, 1.10, 0.90 and 0.50 s with pans of 0.23–0.51 w/s and rolls up to 46.4°/s (the largest roll measured in these five). Each shot is a tracking pan, with the transitions hidden by the passing tree and signpost.
- **Moves:** 10 push-ins, 9 pull-outs. The two most important:
  - 24.37 s: push-in at 46.3%/s plus a tilt-up, from an aerial of the town to the forest.
  - 30.47 s: push-in at 105%/s into the knight's close-up on "the knight was waiting". This is the fastest push in the video, placed on the turn.
- **Sync:** 7 of 10 sentences start within 0.25 s of a transition, for example "People" (+0.01 s), "The" (+0.08 s), "few" (+0.03 s), "He" (−0.06 s) and "knight" (+0.03 s).

### Character animation
- **Knight:** walks in with a bouncy armoured stride. His eyes are smug and half-lidded; in close-up he grins with one eye squinted (31 s).
- **Priest:** an open-mouthed money grin, then a sweat drop of hesitation, then a full red recolour with gritted teeth and angry brows, then a frown at the end.
- **Animation style:** expressions are swapped, not tweened (limited animation). The two porters carry the chest on a pole with a bobbing walk.

### Loop check
- **First frame:** the knight and the priest at the Pardons stall in daylight.
- **Last frame:** the priest sitting in the empty chest on a sunset road while the knight walks off with his horse.
- No visual or verbal loop. The ending closes the hook's question rather than leading back into it.

---

## Craft takeaways from these five (inference, drawn from the measurements above)
- **Write the hook as a paradox or a specific oddity of 13–19 words.** Hold back the "why" until 70–90% of the runtime, then spend no more than 16 s explaining. End on the explanation sentence itself and cut the audio and picture within 0.3 s.
- **Use "You see," as the hinge:** either right after the hook (backstory) or right before the reveal.
- **Add a skeptic** who laughs or mocks, and one quoted line of in-world dialogue, to raise the stakes.
- **Treat the edit as a continuous cross-dissolve flow**, 12–14 frames, about 24 transitions per minute, landing on clause starts. Hide bigger jumps inside objects:
  - smoke clouds
  - foreground passes
  - pushes into photos or phone screens
  - whip pans with speed lines
- **Keep the camera always moving.** Push-ins of 5–20%/s are the default. Use punch-ins of 60–105%/s on the key word and a slow roll of 2–10°/s.
- **Grade by story function:** blue night for suspense, warm gold or sunset for the payoff or ending. The darker-and-bluer reveal of #11 is one option, not a rule.
- **Put the jokes in props and text:** labels, price tags, documents and UI. Plant the solution prop (a key) in the opening shot.
