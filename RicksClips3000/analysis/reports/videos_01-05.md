# RicksClips3000: videos 01-05 analysis

Sources: Whisper word timings, `edit/*_edit.json` (transitions, shots, optical-flow moves), `frames/*_frames.csv` (per-frame stats), dense sheets, plus stills and frame strips I pulled (saved in `analysis/stills/`, listed at the end).

How to read the numbers:
- luma, contrast (luma std), and sat are on a 0-255 scale.
- warm = mean R minus B. Pink and magenta scenes come out positive (warm) because red is higher than blue.
- vignette = center luma minus edge luma. Composition affects it, so it's only a rough guide.
- Palettes come from k-means on frames sampled at 2 fps.
- Anything I couldn't measure is marked **(inference)**.

---

## 0. Cross-video findings: what to update in the channel model (from video 11)

| Prior claim (from video 11) | What 01-05 show |
|---|---|
| Narration is second-person "Imagine you..." | **None of the 5 do this.** All are **third person** ("He", "They", "Gary"). The hook is in the **past tense** and the story then **jumps to present tense** (01-04). 05 is present tense throughout. "You" appears only in the bridge phrase **"You see,"** (01 @52.7, 02 @3.4, 03 @42.9, 04 @45.3) and in one direct question to the viewer (03 "Ever blown on a bowl of soup?"). |
| First ~2 s is a burst of 0.2-0.4 s shots | **Only 02 and 03** do this. 02 cuts at 2.00/2.17/2.77, mostly roll-whips. 03 dissolves at 0.90/1.37/2.27, following the oil stream down. **01, 04 and 05 open on one 3.3-3.7 s shot.** In 01 and 04 that shot is one continuous move from the action to its consequence. 05 opens on a **locked-off static** shot, the only static shot in all five videos. |
| Transitions are mostly 10-17 frame dissolves | Confirmed: 21-31 dissolves per video, median 9.5-16.5 frames, range 3-45. **Hard cuts are rare (2-6 per video) and saved for emphasis**: punchlines, the rage pop, the explosion, "the houses are gone", "48 scratches". |
| Camera is always moving | Confirmed. Exceptions: 05's opening and the near-locked "stillness" shots that come right before a payoff (02 36.7-47.8, 11.2 s; 05 60.5-65.5). The longest shot in every video holds on the beat with the most information (an evidence scene, the explanation, or the payoff). |
| Reveal/twist goes darker and bluer | **Only partly.** The darkest, bluest *mid-video* block is the *complication* (night or storm): 01 @42.5-45 (luma 98, warm -44; 01's very darkest stretch is actually its teal opening at 84.6), 03 storm, 04 end, 05 night press. The **explanation/reveal often flips to warm and bright**: 03's galley is warm +88 against a storm at -87 to -130, and 05's morning field is luma 147 / warm +41 against night at 79 / -36. In 02 the climax is the warmest stretch (heat is the cause). |
| Captions: 1-2 words, white heavy rounded sans, black outline, ~70% down | Confirmed. Caption center measures at about **0.70 of frame height** (01, 05). They **switch instantly**: frame-by-frame there is no scale pop or fade. Chunks are sometimes 3 words ("the whole thing", "the first coat"). Captions **lead the audio by about 2-3 frames** (03: "poured" shows at 0.13 s, the word starts at 0.22 s). Numerals are used ("300 lbs" while the voice says "300 pounds", "47 tiny"), but 04 spells out "nine". |
| 2D flat characters in toon-shaded 3D sets | Confirmed. Extension: 05's founders statue is a **fully 3D sculpted bronze version** of the 2D characters, with metallic patina and outlines. |

New patterns across all five:
- **The hook is the protagonist's absurd action, stated flatly and in the past tense** (9-21 words), with no reason given. It almost always carries a superlative or exact number: "every 39 feet", "life savings / slowest horse", "not just any pink".
- **Mockery and vindication arc.** A doubter gets a quoted line about every 10-15 s ("Barbie's gonna love it in here", "You're wrecking my railroad!", "...and you're making soup?", "Hey, Mirror Man, maybe try wiping it", "Pal, that horse lost a race to the milk cart..."). The ending reverses the mockery.
- **An "ironic joy" beat comes right before the reversal**: 01 "The guards are thrilled." 02 "And his boss is thrilled." 03 "...the pirates couldn't be happier." 04 "...almost feels bad taking it."
- **The "so X (that) Y" hyperbole** shows up in 4 of 5: "a canyon so deep you can't see the bottom", "so close behind them he could hear the pirates laughing", "so far ahead its jockey is waving to his mom", "a wall so tall nobody's ever seen over it".
- **Timeline escalation in steps with concrete units**: 01 "At 15 minutes... At 20... by the time they open the door". 02 finger-wide gap, then a coin in May, then a sheet of paper by July, then touching.
- **Pacing.** Speech starts at **0.00 s** in all five and ends 0.13-0.33 s before the last frame. There is no intro, outro or CTA. Narration runs **200-231 WPM**, with only 2-10 pauses of 0.25 s or more per video (max 0.48 s). Sentences mix 20-37-word run-ons chained with "and/but/so" against 1-7-word punches.
- **Literal visual gags.** On-screen props make the narration literal: the guard watches the button through binoculars on "never take their eyes off it"; "PARKING 10¢" signs on "practically in the parking lot"; "THAT'S MY BOY! ♥" sign on "waving to his mom"; a tumbleweed and "ALL ABOARD!" sign at the deserted station.
- **Loops.** **Only 05 is built to loop**, and its loop is narrative. 01-04 end on punchline images and lines that don't run into the hook.

---

## 01: "The Pink Prison Cell Experiment"
Measured 65.23 s (1957 frames). Info.json: 65 s, **72,975 views**, 4,997 likes, uploaded 2026-11-04 (same day as the data pull, so the low count reflects age).

### Transcript (verbatim)
> They painted the jail cell pink, and not just any pink. A scientist mixes exactly one pint of red into a gallon of white and makes the guards repaint the whole thing because the first coat was the wrong shade. The guards are thrilled. Barbie's gonna love it in here. Then he gives them one strange rule. Every prisoner who goes in comes out after exactly 15 minutes and he waits at the door with a stopwatch. So the first guy they throw in is the biggest inmate in the building, 300 pounds of tattoos laughing at the walls. But when they pull him out 15 minutes later, the scientist asks the skinniest guard there to arm wrestle him, and the guard slams his hand down in two seconds. Wait, what? Well, nobody can explain it. But within a year, jails all over the country are painting their cells by the truckload. Until one night, a guard forgets about the guy in the pink cell. At 15 minutes, he's sitting quietly. At 20, he's pacing. And by the time they open the door, he's trying to rip the bench out of the floor. You see, the scientists swore this pink drained the fight out of anyone in 15 minutes, so jails used it to calm their most violent prisoners. But it only works for 15 minutes. Leave someone in any longer, and it does the exact opposite.

### Script breakdown
- **Hook (0.00-3.20)**: "They painted the jail cell pink, and not just any pink." 11 words. Device: an odd act plus a specificity tease ("not just any"). The real name, "BAKER-MILLER PINK", appears only on screen, never spoken.
- **Setup (3.34-22.06)**: the exact recipe, the obsessive repaint, the ironic joy beat ("The guards are thrilled"), the doubter line ("Barbie's gonna love it in here"), and "one strange rule" (exactly 15 min plus a stopwatch).
- **Escalation (22.28-35.82)**: the test. The biggest inmate gets the hyperbole "300 pounds of tattoos laughing at the walls"; then "But..." the skinniest guard wins the arm wrestle in two seconds.
- **Audience interjection (36.12)**: "Wait, what?" then "Well, nobody can explain it." (pauses of 0.30/0.26/0.34 s around it, the most clustered in the video).
- **Spread (38.54-42.62)**: "jails all over the country... by the truckload."
- **Turn (42.72)**: "Until one night, a guard forgets..." Then the triad timeline "At 15 minutes... At 20... by the time they open the door" builds to "rip the bench out of the floor".
- **Explanation (52.68)**: "You see, the scientists swore..." (past tense).
- **Twist and ending (60.08-65.00)**: "But it only works for 15 minutes. Leave someone in any longer, and it does the exact opposite."
- **Loop?** No. "...the exact opposite." → "They painted the jail cell pink" doesn't flow. Visually the final frame (inmate with red rage aura in the pink cell) **calls back the 27 s rage image**, not the teal opening.
- POV/tense: third person. Past hook, present narration, past for the explanation, present for the rule/twist.
- Devices: "15 minutes" repeated 5 times as a motif; contrast "But" ×4; triad timeline; one rhetorical question ("Wait, what?").
- Stats: 237 words, **219 WPM**. 18 sentences, mean 13.2 words (range 2-30). 7 pauses of 0.25 s or more (max 0.44 s after "year,").

### Visual
- **Settings**: teal concrete-block cell with barred window; a top-down mixing table (green cutting mat, digital scale, "STATE CORRECTIONAL" paint can, note "P-618 = 1 PT RED + 1 GAL WHITE"); prison cafeteria/cell block; aerial patchwork farmland map with clouds; pink trucks at a jail; night guard booth; hot-pink cell.
- **Palette**: slate teal #30576a / #3c576f, blue-grey #70838f / #9fadb5, hot pink #e46da1 / magenta #d14386, pale pink-white #e5d4d7, navy shadow #22283e, deep rose #a44f63.
- **Lighting**: the opening uses hard **god-ray shafts** through the barred window onto a cool teal room, plus a practical fluorescent tube with slight glow. The cafeteria has bright window light casting hard striped shadows (30-37 s). The night beat is a cool blue room lit by a warm desk lamp. The pink cell gets soft, bright fill and a magenta beam at 51 s. At 51.2 s a huge dark silhouette shadow sits on the wall behind the raging inmate.
- **Section stats**:

| section | luma | contrast | sat | warm | note |
|---|---|---|---|---|---|
| hook 0-3.5 | 84.6 | 36.5 | 115 | -41.6 | darkest, coolest open |
| setup 3.5-22.3 | 140.2 | 54.8 | 84 | -16.0 | |
| escalation 22.3-38.5 | 125.3 | 52.9 | 95 | -13.3 | pink-cell bin 25-27.5: warm +42.9 |
| spread 38.5-43 | 169.6 | 46.4 | 89 | +11.0 | brightest (aerial daylight) |
| twist 43-52.6 | 114.8 | 46.0 | **139** | +12.6 | night bin 42.5-45: luma 98, warm -44; pink 47.5-50: sat 159.5, contrast 32 |
| explanation 52.6-60 | 140.0 | 44.2 | 79 | +3.3 | vignette 31.8 (highest) |
| end 60-65.2 | 154.2 | 46.4 | 89 | +32.3 | |

- **Effects**: the **"rage aura"** at 26.3-28.5 and 64.5-65.2. The upper head goes to a dark gradient, the eyes glow red, red vein-cracks radiate over the walls and floor, and a faint **circular shockwave ring** expands. Saturation jumps 80 → 122 and warm 23 → 45 over about 12 frames (64.30-64.70). Other effects: an animated paint swirl (red into white turning pink, 6.5-8 s) and debris particles at the bench rip (51 s).
- No visible film grain. Bloom is mild (fluorescent tubes, window).

### Camera & edit
- **26 shots, ASL 2.51 s** (median 2.05). 22 dissolves (median 16.5 frames, range 3-37). Hard cuts at 3.53, 26.30, 26.50, 42.90 and 55.07.
- **No hook burst.** Shot 1 (0-3.53) is a continuous push-in at 14.7 %/s plus a left pan. The guard paints a pink stripe that pops on, then the camera travels to a taped sheet reading "P-618 / BAKER-MILLER PINK / 1 PINT RED + 1 GALLON WHITE / EXACTLY!".
- Beat map:
  - 5.57: top-down pour, push-in 58.5 %/s with **roll 25°/s**.
  - 10-11: the scientist squints and holds up the P-618 chip on "wrong shade".
  - 19.33 (0.87 s): **whip push-in 61 %/s with pan 0.43 w/s** to an extreme close-up of the scientist and stopwatch on "exactly 15 minutes".
  - 26.30 / 26.50: two cuts (a 0.2 s shot) pop on the rage aura at "300 pounds of tattoos".
  - 30.37-38.2: the **longest shot (7.83 s)**, a slow 4.5 %/s push on the arm-wrestle cafeteria.
  - 38.47: **crane-up at 136 %/s** from an overhead floor shot through the roof, a 37-frame dissolve into the aerial map, a roll of -17.5°/s through clouds, then a push-in at 56 %/s to the pink trucks.
  - 42.9: cut to night.
  - 51.47 (0.33 s): violent **pull-out at 208 %/s, pan 0.87 w/s, roll -24°/s** on "rip the bench".
  - 57.1-65.23: final held shot of 8.13 s with a 2.5 %/s pull-out. The calm inmate knits a pink-striped scarf, the stopwatch circles in, and he snaps into the rage aura at "opposite".
- **Sync**: 4 of 25 transition times land within 0.25 s of a sentence start, which is about chance (~3.5). Cuts are tied to content words ("exactly", "rip"), not to sentence boundaries.
- **On-screen elements**: the P-618 sheet, the handwritten recipe, the paint chip, the "STATE CORRECTIONAL" can, a stopwatch, inmate number "4417", tally marks on the wall, a wall clock, the aerial map with jail icons, the pink trucks.

### Character animation
- Expressions are instant face swaps, not tweens. The inmate goes calm → furrowed → gritted teeth → sinister grin in about 4 frames (64.40-64.53).
- The guard's sprite flips and leans while painting.
- Body bob and arm pumping in the arm-wrestle crowd.
- The scientist's default is a deadpan, half-lidded squint **(inference: the "knowing protagonist" look)**.
- The only quoted line ("Barbie's gonna love it in here") plays over a group shot of laughing guards. I did not check lip-sync frame by frame here.

### Distinctive
The bookend rage aura, the hidden real-world label on screen, and the crane through the roof into a map to say "all over the country".

---

## 02: "Why Perfect Railroads Don't Work"
Measured 65.17 s. Info.json: 65 s, **19,537,481 views**, 420,911 likes, 2026-11-01.

### Transcript (verbatim)
> He sawed gaps into a railroad every 39 feet. You see, two companies are racing to build a railroad along a canyon so deep you can't see the bottom. And whoever finishes first gets the whole country's business. He's the youngest engineer on the job. And when his boss sees a finger-wide gap between every single rail, his face goes purple. You're wrecking my railroad! But he won't close a single one. The other company lays their rails end to end, perfectly smooth, and finishes first. Their trains glide across the canyon without a sound. While his go clickety-clack over every gap, the newspapers start calling it the clickety-clack line, and everyone switches to the quiet trains. Then summer comes, and something weird happens. His gaps start shrinking. In May, you can fit a coin in them. By July, barely a sheet of paper. And his boss is thrilled. See? Even your gaps know you were wrong. Meanwhile, on the perfect railroad, the rails have started groaning in the afternoon sun, pushing against each other like they want to get out. On the hottest day anyone can remember, his gaps finally close. Rail touching rail. And halfway across the canyon, the perfect railroad kicks sideways like a snake, right as a train rolls onto it.

### Script breakdown
- **Hook (0-3.22)**: "He sawed gaps into a railroad every 39 feet." 9 words, the shortest hook here. Device: an act that looks like self-sabotage, plus a precise number.
- **Setup (3.40-11.44)**: "You see," is used early, as a scene-setting bridge rather than as the explanation. Stakes: a race, the canyon hyperbole, winner-takes-all.
- **Conflict (11.70-21.56)**: youngest engineer; the boss's face "goes purple"; the quoted doubter line "You're wrecking my railroad!"; "But he won't close a single one."
- **Losing (21.66-35.80)**: the rival finishes first and runs quiet. His line is mocked as "the clickety-clack line" (onomatopoeia repeated twice) and everyone switches.
- **Turn (36.10)**: "Then summer comes, and something weird happens." The gap-shrinking ladder: coin (May), then sheet of paper (July). Ironic joy: "And his boss is thrilled. See? Even your gaps know you were wrong."
- **Cross-cut (47.94)**: "Meanwhile, on the perfect railroad..." with personification ("groaning... like they want to get out").
- **Climax (54.36-64.94)**: "his gaps finally close. Rail touching rail." (a 3-word sentence), then "kicks sideways like a snake, right as a train rolls onto it."
- **The explanation is never spoken.** Thermal expansion is shown (heat-coloured rails, thermometer, calendar), never named.
- **Loop?** No. "...rolls onto it." doesn't lead into "He sawed gaps". The ending is a catastrophe beat.
- POV/tense: third person, past hook, present narrative.
- Devices: "But", "Meanwhile", "Then"; the escalating gap ladder; a callback ("perfect railroad" ×3, "gaps" ×6); a rhetorical "See?".
- Stats: 218 words, **201 WPM** (slowest of the five). 21 sentences, mean **10.2 words** (shortest), range 1-24. 6 pauses of 0.25 s or more (max 0.30).

### Visual
- **Settings**: a red sandstone slot canyon with rails and an approaching steam loco (#7) trailing a black smoke column; a blue-shadow canyon fly-through with cranes; "UNION" station hall with the banner "FIRST LINE IN GETS IT ALL!", $ bags and gold bars; a plush red-velvet "VANDERGOLD" car with brass pendant lamps; a station with a checkered floor; a viaduct at sunset.
- **Palette**: oxblood canyon red #6b302c / #71262f, burnt orange #d7682e / #ec8f3c, dusty mauve #8a6264, deep indigo #2b294e, sky blue #5e88cf, sand #c99a82 / #e2cab5.
- **Lighting**: hard sun on the rails with crisp shadows. The canyon walls have a **painterly hand-hatched / streaked texture** (full-res crop). Warm practical pendant lamps light the luxury car interior (27-29 s; luma 66, sat 164, the darkest and most saturated bin). The headlight glows with bloom. The climax is sunset back-light with pink haze.
- **Heat as colour**: in summer the rails glow on a **purple → magenta → yellow gradient** (38.5-45 s, again 50-51 s and 57 s), a stylised thermal display.
- **Section stats**:

| section | luma | contrast | sat | warm | note |
|---|---|---|---|---|---|
| hook 0-3.5 | 92.4 | 48.0 | 133 | +38.8 | dark red canyon |
| setup 3.5-21.6 | 112.1 | 50.1 | 125 | -15.3 | blue canyon bin 5-7.5: warm -88 |
| rivalry 21.6-36 | 95.5 | 47.6 | 126 | +15.9 | interior 27.5-30: luma 66 |
| turn/summer 36-47.8 | 127.3 | 55.2 | 138 | **+86.1** | warmest |
| perfect line 47.8-57.9 | 114.1 | 54.6 | 114 | +15.1 | contrast 62 at 50-52.5 |
| climax 57.9-65.2 | 141.2 | 53.5 | 101 | +37.4 | explosion bin 62.5-65: luma 159 |

- **Effects**:
  - Cartoon **ear-steam puffs** and a purple face (17-19.4).
  - Tumbleweed rolling past an "ALL ABOARD!" sign (35.5-36).
  - The rails kinking into an S-curve (62-63).
  - A **flash-frame explosion** at 64.23 (luma +30 in 1 frame), then a volumetric fireball with sparks, a mushroom cloud, and a reaction shot where the boss's bowler hat flies off.
  - Particles: dust, sparks, smoke columns.

### Camera & edit
- **33 shots, ASL 1.98 s** (median 1.40, the fastest of the five). 31 dissolves (median 14 frames, range 3-27). Hard cuts at 2.00 and 64.23 (flash plus a 27-frame dissolve).
- **Hook burst**: 0-2.0 push-in at 34 %/s on him sawing. Then a **camera roll-whip** at 55°/s (2.00, 0.17 s) and 115°/s (2.17, 0.60 s) orbits him as he stands up smug, hands on hips, and the wall turns from red to sunlit orange. A pull-out follows at 2.77.
- Beat map:
  - 3.53-8.47: canyon fly-through push at 33.5 %/s, tilting down into the abyss on "can't see the bottom".
  - 8.47-11.5: a mini-burst of 4 dissolves (1.2 / 0.73 / 0.57 / 0.53 s) pushing in at 41-78 %/s to the "FIRST LINE IN" banner on "whoever finishes first gets the whole country's business".
  - 21.27: whip (pan 0.86 w/s, roll -23°/s) to the rival crew.
  - 23.9 and 24.83: whip pans of 0.73 and 0.53 w/s (jitter 5.6, the highest in the video).
  - 26.10: **push-in at 104 %/s** into the luxury car on "glide".
  - 29-31: shaky, rattling camera (jitter 3.0) on "clickety-clack".
  - 35.97: pull/roll 49.6°/s through the calendar and thermometer.
  - **36.67-47.83: longest shot (11.17 s)**, nearly locked (pull-out 2.9 %/s), covering the whole gap-shrinking sequence: calendar "1880 / MAY", thermometer, caliper, glowing rails, and the boss's gloat.
  - 47.83: push-in with roll 22°/s onto the perfect railroad.
  - 64.23: explosion.
- **Sync**: 10 of 32 transitions fall within 0.25 s of a sentence start (chance about 5), so roughly double chance.
- **On-screen elements**: the "FIRST LINE IN GETS IT ALL!" banner, "UNION", "VANDERGOLD" and "CANYON S..." car names, newspaper "The Red Mesa Herald: THE CLICKETY CLACK LINE!" with a train engraving, the "ALL ABOARD!" sign, the "CALENDAR for the Year 1880 / MAY" page, the thermometer, the caliper.

### Character animation
- The engineer leans and saws with his whole body, then stands with hands on hips: smug, half-lidded, smirking.
- The boss shows **mouth-flap lip-sync** on "You're wrecking my railroad!": mouth shape changes every 2-4 frames between open, gritted and flat (strip at 18.15 s), and the steam puffs pulse.
- The tycoon sips tea and smiles with closed eyes; he winks at the station.
- The end reaction swaps both faces to wide eyes, the boss gets a sweat drop, and the hat pops off.

### Distinctive
The fastest cutting of the five. The science is never spoken. The ending is a slapstick explosion rather than an explanation. The colour temperature follows the physics (heat = warm).

---

## 03: "Why Sailors Carried Storm Oil"
Measured 64.57 s. Info.json: 65 s, **12,924,636 views**, 290,981 likes, 2026-10-30.

### Transcript (verbatim)
> He poured cooking oil into the sea, with a pirate ship so close behind them he could hear the pirates laughing. His captain grabs him by the collar and goes, We're about to get boarded, and you're making soup? But he doesn't even look up, he just points at the black clouds. Steer into the storm. The captain yells that they'll never survive it, and all he gets back is, Trust the oil. But then, a grappling hook clangs off the railing, so the captain turns the wheel, and the pirates couldn't be happier. Why waste a cannonball when the storm will do it for free? Deeper in, the waves get taller than the mast, and the crew is tying themselves to anything bolted down, but he's still pouring, a little at a time, always on the side the wind is coming from. Then the pirates swing in to board, and up ahead, a wave big enough to swallow both ships rises out of the dark. You see, sailors really carried oil just for this. They called it storm oil. Ever blown on a bowl of soup? The broth ripples, but the oily spots stay perfectly smooth, because your breath can't grab them, and a wave can't crash if the wind can't grab it. So when the wave reaches their oily patch of sea, it just lifts the ship and sets it down, and 50 yards behind, it curls over and drops straight onto the pirate's deck.

### Script breakdown
- **Hook (0-5.44)**: 21 words, the longest hook here. Device: a mundane act under mortal stakes ("so close... he could hear the pirates laughing").
- **Setup (5.62-18.48)**: the captain's doubter line "We're about to get boarded, and you're making soup?". The protagonist's terse commands are 4-word and 3-word sentences: "Steer into the storm." "Trust the oil."
- **Escalation (18.64-36.52)**: grappling hook, then the ironic joy beat ("the pirates couldn't be happier"), then the pirate quote "Why waste a cannonball when the storm will do it for free?". "Deeper in" gives the wave hyperbole. A 37-word run-on ends with "he's still pouring, a little at a time, always on the side the wind is coming from" (a precise procedure detail).
- **Climax setup (36.70-42.74)**: "a wave big enough to swallow both ships rises out of the dark."
- **Explanation (42.90-55.98)**: "You see," comes after the **longest pause in all five videos (0.48 s)**, then the real-world claim and its name ("storm oil"). Next a **direct second-person question, "Ever blown on a bowl of soup?"**, which **calls back the captain's insult**: the "soup" that was mocked becomes the analogy. A parallel follows: "your breath can't grab them... a wave can't crash if the wind can't grab it."
- **Payoff (55.98-64.44)**: the wave lifts their ship "and 50 yards behind, it curls over and drops straight onto the pirate's deck."
- **Loop?** No (night storm wreck vs sunny opening; the sentences don't link).
- POV/tense: third person, past hook, present narrative, past for the history claim.
- Stats: 247 words, **230 WPM**. 14 sentences, mean **17.6 words** (longest), range 4-37. Only 2 pauses of 0.25 s or more, so the narration is nearly continuous.

### Visual
- **Settings**: sunny ship deck (red/cream hull, brass portholes); pirate ship with an **orange sail bearing a toothy skull**; a large spotted dog among the pirates; black storm clouds; night storm with a distant lighthouse; a warm wooden galley (porthole, hanging lantern, copper pot, "STORM OIL" tin); a top-down soup bowl; a giant translucent wave.
- **Palette**: ultramarine #375ad3 / #2e57d9, deep cobalt #212f8e / #131c84, near-black plum #291822, copper-brown wood #80452a / #934924, amber #d78033 / #e9ac74, pale sky #d2e1ee.
- **Lighting**:
  - Day: bright, high contrast (contrast 67-72, the highest daytime contrast of the five), with hard sun.
  - Storm: monochrome blue (warm -87 to -141), low contrast (24-41), with **lightning sky-flashes** of 1-2 frames (luma +16 to +27 at 28.87, 39.37, 40.63, 41.97, 42.97), rain streaks, and red/green lantern points on the ships.
  - Galley: warm lantern key with deep vignette (41-46).
  - Payoff: **god rays** slant from the upper left through the rain onto the wave (60-64.5).
- **Section stats**:

| section | luma | contrast | sat | warm | note |
|---|---|---|---|---|---|
| hook 0-5.6 | 112.0 | 70.1 | 154 | +14.4 | |
| setup 5.6-18.6 | 120.9 | 72.4 | 137 | +34.5 | |
| escalation 18.6-26.6 | 110.0 | 67.2 | 141 | +25.7 | |
| storm 26.6-42.8 | 75.0 | 40.9 | 182 | -87.1 | |
| explanation (galley + bowl) 42.8-52.3 | 137.3 | 65.0 | 151 | **+87.6** | bowl bin 50-52.5: luma 200, warm +145 |
| payoff 52.3-64.6 | 80.8 | 37.1 | **188** | **-130.2** | |

- **Effects**:
  - The oil stream is the graphic through-line of the opening.
  - A sea splash where the oil lands (2.0 s).
  - Concentric ripples with oil discs in the bowl.
  - **Cel-style FX at the end**: a faceted white smoke stack, an orange cel-shaded fireball, debris, and the pirates' hats floating in the water as a coda (63.5-64.5).

### Camera & edit
- **29 shots, ASL 2.23 s** (median 1.63). 22 dissolves (median **9.5 frames**, the shortest; range 3-45, the longest being 45 frames, 1.5 s, at 18.67). 6 hard cuts at 12.00, 12.57, 25.60, 25.80, 29.27 and 60.03.
- **Hook burst**: dissolves at 0.90, 1.37 and 2.27 follow the oil stream from pot to hull to sea (tilt-down 0.83 h/s). The yellow stream stays in about the same screen spot, so it reads as a match-flow. Then a push-in at 76 %/s toward the pirate ship (2.27-5.8).
- Beat map:
  - 5.8-12.0: a 6.2 s pan on the captain-and-cook dialogue.
  - 12.00 / 12.57: hard cuts to the black clouds on "points at the black clouds".
  - 18.67: push-in at 63.5 %/s, jitter 6.0 (the highest), on the grappling-hook clang (luma +21 at 19.3).
  - 25.60 / 25.80: **two hard 0.2 s punch-in cuts** on the pirate captain's punchline ("...the storm will do it for free?").
  - 27-36: storm, with roll moves of 6-13°/s and one at -56°/s (31.87) for the rocking ship. The deck is dutch-tilted while he pours.
  - 42.67-49.8: a 7.13 s near-static shot in the galley.
  - 49.8: push-in at 41 %/s to the top-down bowl.
  - 52.33-60.03: 7.7 s push-in with roll 13°/s as the wave lifts the ship.
  - 60.03: hard cut, then a pull-out at 21 %/s as the wave crashes on the pirates.
- **Sync**: 6 of 28 transitions are within 0.25 s of a sentence start (chance about 3).
- **On-screen elements**: the skull sail, the "STORM OIL" tin, the lighthouse. No numbers or labels besides that.

### Character animation
- The cook keeps a **deadpan, half-lidded face** throughout, even while grabbed by the collar.
- The captain (bicorne with red cockade, moustache) shouts with a wide mouth and squeezed eyes.
- The pirate captain (feathered hat, a parrot on a crewmate's shoulder) gloats with a wide mouth.
- Pirates swing in on ropes. The crew clings to fixtures.
- **(inference)** Dialogue lines appear to get mouth changes like 02 and 05, but I did not run a frame strip here.

### Distinctive
The insult-becomes-explanation callback ("making soup?" → "Ever blown on a bowl of soup?"). The warm galley sits as an island between two blue storm blocks. The cel FX explosion is 2D-styled rather than the volumetric one in 02.

---

## 04: "How a Mirror Rigged a Horse Race"
Measured 64.07 s. Info.json: 64 s, **4,992,807 views**, 142,982 likes, 2026-10-29.

### Transcript (verbatim)
> He bet his life savings on the slowest horse in the race. The whole betting room is laughing at him, because all day long, he hasn't bet a single dollar. He just sits by the window, smiling, because he has a mirror. Wait, what's a mirror going to do? Well, the race track is right over the hill from town, and his buddy is up on that hill with the biggest mirror he could find. Race after race, the favorite wins, and the hill stays dark. And by the fifth, the regulars are betting on whether he'll ever bet. Hey, Mirror Man, maybe try wiping it. In the last race, the favorite's so far ahead its jockey is waving to his mom, and horse 9 is so far behind it's practically in the parking lot. Then, the hill flashes, and he puts every dollar he has on horse 9. The guy behind the counter almost feels bad taking it. Pal, that horse lost a race to the milk cart, and it was pulling the milk cart. You see, back then, betting rooms didn't find out who won until the winner came clicking in over a wire. And until it did, bets stayed open. Up on that hill, his buddy just watched horse 9 come out of nowhere and steal it by a nose. So, while the room is still laughing, the wire starts clicking, and by the time it spells out 9, nobody's laughing anymore.

### Script breakdown
- **Hook (0-3.06)**: "He bet his life savings on the slowest horse in the race." 12 words. Device: an irrational, all-in bet built on two superlatives.
- **Setup (3.24-18.22)**: the mocking room, the odd detail "he has a mirror", and the **voiced audience interjection "Wait, what's a mirror going to do?"**, answered with "Well,..." (the same pattern as 01's "Wait, what? Well,...").
- **Waiting/mockery (18.54-34.54)**: "Race after race... the hill stays dark." A wordplay gag: "betting on whether he'll ever bet". Doubter line: "Hey, Mirror Man, maybe try wiping it." Paired "so far ahead / so far behind" hyperboles.
- **Turn (34.74)**: "Then, the hill flashes", he goes all-in, and the clerk's quote doubles as a joke with a reversal: "Pal, that horse lost a race to the milk cart, and it was pulling the milk cart."
- **Explanation (45.34-50.38)**: "You see, back then..." The telegraph delay means bets stay open.
- **Payoff (50.40-63.74)**: horse 9 wins "by a nose". **Callback**: "the room is laughing at him" (3 s) becomes "nobody's laughing anymore" (63 s).
- **Loop?** No. The final line closes the arc ("anymore").
- POV/tense: third person, past hook, present narrative, past explanation.
- Stats: 245 words, **231 WPM** (fastest). 16 sentences, mean 15.3 words (range 7-29). 10 pauses of 0.25 s or more, the most of the five; they sit at clause commas ("Then, | the hill flashes", "back then, | betting"). That gives a slightly more spoken, comic-timing rhythm **(inference)**.

### Visual
- **Settings**: a table outdoors by the racetrack rail (piggy bank); a period betting room (odds board, "BETS OPEN" sign, window onto a main street with a hill beyond); a green hill with a giant ornate gold mirror; the "HILLSIDE DOWNS" grandstand with a "JUDGES" booth and bunting; a dirt lot with "PARKING 10¢" signs; a dark red damask cashier cage; a main-street milk-cart race ("MILK RUN DAIRY", "FINISH" banner, "MERCANTILE", barber shop); a telegraph desk; the hill at a purple-orange sunset; the betting room at night.
- **Palette**: warm grey/olive #5a524d / #777d6e, dark maroon-brown #342329 / #552623, clay-track orange #b2612f, sky blue #66a5ee, cloud white #d3d8e4, night violet #413a55 / #5c5775.
- **Lighting**: sunny exteriors with hard fence shadows. The **mirror flash** (35.5-36.3) is a star-glint sun flare on the hill seen through the window, and it **lights the protagonist's face** with a warm yellow patch while the cigar-smoker squints. The cashier interior is dark and moody (luma 70-72, vignette 63 at 40-42.5, the highest anywhere). The sunset hill has a soft gradient sky. The end is cool violet night through the window with warm interior practicals.
- **Section stats**:

| section | luma | contrast | sat | warm | note |
|---|---|---|---|---|---|
| hook 0-3.3 | **149.0** | 53.5 | 125 | -2.9 | brightest open of the five |
| setup 3.3-18.4 | 129.3 | 58.5 | 99 | -3.9 | |
| waiting/mockery 18.4-34.8 | 126.8 | 53.0 | 118 | +25.5 | race bins sat 150-154 |
| flash + bet 34.8-45.3 | 94.0 | 56.5 | 109 | +21.2 | cashier 37.5-42.5: luma 70-72 |
| explanation 45.3-57.6 | 109.5 | 49.8 | 129 | +44.8 | sunset 55-57.5: warm +74 |
| payoff 57.6-64.1 | 82.8 | 46.9 | 104 | -17.1 | night, darker and cooler |

- **Effects**:
  - The piggy bank shatters into ceramic shards and coins (1.5-2.0).
  - Horses kick up dust.
  - A **telescope iris mask** (circular view with black surround, 18.3-20.3).
  - Speed-blur on horse 9 "out of nowhere" (55.5).
  - **Money rain**: cash bundles fall and pile at his feet (62-64).
  - Cigar smoke.
  - Shallow-DOF backgrounds in close-ups.

### Camera & edit
- **27 shots, ASL 2.37 s** (median 1.80). 24 dissolves (median 16 frames, range 5-32). Cuts at 18.93, 33.17 and 48.80.
- **No hook burst.** 0-3.3 is one continuous move: the hammer smashes the piggy bank, then a whip-pan right (pan 0.20 w/s, roll 11°/s) to the track as horses thunder past and the slow horse plods in.
- Beat map:
  - 5.37-12.37: a 7.0 s slow push-in at 12.5 %/s on him smiling by the window.
  - **12.37: a 32-frame dissolve through his round hand mirror.** The camera pushes at 81 %/s into the mirror, whose reflection becomes the next scene (town, hill). This is a "through-the-object" transition.
  - **18.23-20.30: a rhythmic montage** alternating telescope-POV and the buddy, with single-frame luma swings of ±60-73 at 18.27, 19.03, 19.73 and 20.30 (they read as hard cuts, though the detector logged some as short dissolves). It lands on "Race / after race / the favorite / wins".
  - 27.13-33.17: a 6 s tracking shot along the grandstand.
  - 33.17: cut to the parking-lot gag.
  - 36.70: the **fastest whip pan of the set, 1.24 w/s with roll -24.5°/s**, from window to counter on "he puts every dollar".
  - 46.53-50.73: an explanation mini-burst (0.63 / 0.83 / 0.80 / 1.93 s) with push/pull moves of 69-83 %/s: telegraph poles, the key, the odds board.
  - 57.90-64.07: final held shot of 6.17 s with a 4.7 %/s pull-out: the board changes to "WINNER NINE", the money rains, jaws drop.
- **Sync**: 6 of 26 transitions are within 0.25 s of a sentence start (chance about 3.3).
- **On-screen elements**: odds board ("HIGH HAT 1-5 / BEE'S KNEES 4-1 / WHOOPEE 6-1 / APPLESAUCE 8-1"); "9 MILK RUN 1000-1", so **horse 9 is named "Milk Run"**, a visual callback to the milk-cart joke; "WINNER / NINE"; "BETS OPEN"; "HILLSIDE DOWNS"; "JUDGES"; "THAT'S MY BOY! ♥" held by the jockey's mom; "PARKING 10¢"; "FINISH"; "MILK RUN DAIRY"; "MERCANTILE".

### Character animation
- The protagonist (boater hat, mint shirt, polka-dot bow tie) keeps a **smug half-lidded smile** for the whole video.
- The bettors' faces swap from laughing to shocked with sweat.
- The clerk (green visor) laughs with a wide-open mouth during his line.
- On the contact sheet, the speakers' mouths change open/closed during the regular's "Hey, Mirror Man" (25-26.5 s) and the clerk's "Pal..." (41-42 s). I didn't run a frame strip; **(inference)** this is the same mouth-flap system as 02/05.
- The buddy peers through a spyglass with the race reflected in the lens.

### Distinctive
The most comedy-dense script (three stacked jokes in 30-45 s). The mirror-portal transition. The iris montage. The callback hidden in the horse's name.

---

## 05: "The Town Built Around a Button"
Measured 65.50 s. Info.json: 66 s, **3,542,075 views**, 104,393 likes, 2026-10-28.

### Transcript (verbatim)
> There's a button in the middle of town, and nobody's allowed to press it. The whole town is built around it in perfect circles, every house facing the center, where the button sits under a glass case, with two guards who never take their eyes off it. Around all of it is a wall so tall nobody's ever seen over it. At night, a glow comes from the other side, and every year it gets a little dimmer. But Gary's always noticed two weird things. Under the glass, there are 47 tiny scratches nobody can explain, and the statue of the town's founders has a woman who looks exactly like his mom. So when his friends bet him five bucks he won't press it, he can't say no. At three in the morning, the guard swaps shifts, and he's got about 30 seconds. He lifts the glass, holds his breath, and presses it, but nothing happens. Just a tiny scratching sound under the glass. But as he walks home, the glow over the wall is brighter than it's ever been. The next morning, Gary wakes up in the grass. The houses are gone, the guards are gone, and the whole town is standing in an empty field around the button, staring at it like they've never seen it before. Around the button, there are 48 scratches. Then, his mom steps out of the crowd and says, Nobody touches this. We'll build our town right here.

### Script breakdown
- This is a **fiction/mystery** script (time loop), not a real-world explainer. It has no "You see," and no explanation.
- **Hook (0-3.40)**: "There's a button in the middle of town, and nobody's allowed to press it." 14 words. Device: a forbidden object (it invites the question "what happens if...?"). Present tense.
- **Worldbuilding (3.48-20.48)**: perfect circles, the glass case, guards, a wall "so tall nobody's ever seen over it", and a glow that dims every year (a planted clue).
- **Clues (20.58-30.90)**: "two weird things": **47 scratches** and the founders statue that looks like his mom.
- **Inciting act (31.06-41.90)**: a $5 dare, a 30-second window, and a triad "lifts the glass, holds his breath, and presses it", then "but nothing happens".
- **Turn (42.02-48.24)**: the scratching sound; the glow is "brighter than it's ever been".
- **Reveal (48.34-60.10)**: wakes in grass. Anaphora tricolon: "The houses are gone, the guards are gone, and the whole town is standing...". Then "there are **48** scratches", a numeric callback that implies the 48th reset **(inference)**.
- **Ending (60.42-65.28)**: mom: "Nobody touches this. We'll build our town right here."
- **Loop? YES, by design.** The last line ("We'll build our town right here.") leads straight into the first ("There's a button in the middle of town, and nobody's allowed to press it."). "Nobody touches this" echoes "nobody's allowed to press it". Visually the frames rhyme without matching: the last frame has mom and kneeling Gary above the red button at bottom-centre; the first frame has the guard and Gary above the red button at bottom-centre. The setting differs (grass field vs stone plaza), so the loop is narrative, not a pixel match.
- Stats: 245 words, **225 WPM**. 16 sentences, mean 15.3 words (range 6-33). Only 3 pauses of 0.25 s or more, all in the last 16 s ("morning, | Gary", "scratches. | Then", "says, | Nobody"). The narration slows into the ending **(inference: deliberate)**.

### Visual
- **Settings**: a stone plaza with a pedestal, gold plate and red button under a glass dome; an aerial of **concentric rings of houses inside a colosseum-like wall**; a towering wall with a long ladder; the night sky over the wall showing a **glowing ring/halo** (orange-pink corona around a dark disc, with radial streaks); Gary's attic bedroom (window onto the halo, target-pattern rug); a bronze founders statue; the night town with warm lit windows and street lamps; a picket-fenced street at dawn with a giant sun-like glow over the wall; an empty green field with a crowd ring.
- **Circular motif everywhere** (observed): the button, the dome, the ring roads, the halo, the rug, the counter dial, the crowd ring, the plaza tiles.
- **Palette**: royal/night blue #31458c / #1b3788, warm grey stone #948789 / #a6a59e, cream #d6c9b3, grass green #529c34 / #519e33, periwinkle #6f8ecb, amber glow #d59447 / #e2a041.
- **Lighting**:
  - The opening has diagonal light shafts in the background.
  - Day plaza: soft, even, and desaturated (sat 59-60 at 7.5-12.5, the lowest of any section here).
  - Night: deep blue with warm window practicals and a flashlight beam.
  - The halo is an emissive ring with bloom.
  - 46.5-48.5: the glow blows out warm (warm +69). The morning field is bright green.
  - **Shallow DOF** on the statue shot: the background houses are heavily blurred (full-res crop at 29.5).
- **Section stats**:

| section | luma | contrast | sat | warm | note |
|---|---|---|---|---|---|
| hook 0-3.5 | 114.4 | 51.7 | 110 | -32.3 | |
| world 3.5-20.6 | 131.3 | 42.2 | 97 | -32.7 | halo bins 15-20: luma 83-110, warm -62 to -68 |
| Gary/clues 20.6-34.4 | 120.8 | 45.7 | 104 | +3.2 | |
| night press 34.4-44.6 | **78.9** | 41.0 | 146 | -35.6 | darkest |
| glow 44.6-48.5 | 124.6 | 42.0 | 131 | +22.1 | |
| reveal (field) 48.5-60.4 | **147.0** | 47.1 | 125 | **+41.4** | brightest, warmest |
| end 60.4-65.5 | 130.3 | 51.3 | 119 | +32.7 | |

- No luma jumps over 12 per frame anywhere: no flashes, the smoothest grade of the five.

### Camera & edit
- **26 shots, ASL 2.52 s** (median 2.30). 21 dissolves (median 14 frames, range 3-24). Hard cuts at 20.57, 38.70, **50.80** ("The houses are gone") and **58.03** (the "48" counter macro). The reveals get the hard cuts.
- **Hook**: 0-3.70 **locked-off static** (no optical-flow motion). The guard looks sideways; Gary grins and reaches toward the dome, and a sweat drop appears.
- Beat map:
  - 3.70-5.30: **crane-up pull-outs at 93-124 %/s with roll ±13-16°/s** from the pedestal to the aerial rings on "built around it in perfect circles".
  - 7.73 (0.40 s): a **dive push-in at 166 %/s** (the fastest push-in in all five; 01 has a faster 208 %/s pull-out) back down to the button on "the button sits under a glass case".
  - 11-12: the guard stares through binoculars on "never take their eyes off it".
  - 12.27: tilt up the wall and ladder.
  - 23.17: macro of the button with the counter "47".
  - 27.23: the statue, with mom peeking in from the bottom of frame as a comic reveal.
  - 38.70-42.97: a 4.27 s steady push on the press.
  - 42.97: push-in at 41 %/s to the plate macro for the "scratching sound".
  - **50.80-58.03: longest shot (7.23 s), pull-out at 22.8 %/s** to the aerial crowd ring.
  - 60.50-65.50: a 5.0 s near-static final shot.
- **Sync**: **12 of 25 transitions are within 0.25 s of a sentence start (chance about 3)**, the strongest sentence-locked cutting of the five. Examples: 12.27 "Around", 15.90 "At night", 23.17 "Under", 31.10 "So", 44.60 "But", 60.50 "Then".
- **On-screen elements**: a 4-digit mechanical tally counter "0047" → "0048", the "THE FO[UNDERS]" plaque, the glass dome. No other text.

### Character animation
- **Mouth-flap lip-sync** confirmed on mom's line (strip at 62.6 s): open-oval, flat and small shapes change every 2-4 frames.
- Gary's expression snaps from a side-glance pout to wide-eyed gritted teeth on "this" (63.2).
- The townspeople are dozens of near-identical instanced figures, standing still.
- The statue is a 3D sculpt of the same character design.
- Sweat drops appear on the guard and Gary at 3.5 s.

### Distinctive
The only seamless narrative loop. The only static hook. The only fiction premise. The reveal goes *brighter and warmer*, not darker. The circle motif carries the design.

---

## Quick comparison table

| | 01 Pink Cell | 02 Railroads | 03 Storm Oil | 04 Mirror | 05 Button |
|---|---|---|---|---|---|
| views | 73K (day 0) | 19.5M | 12.9M | 5.0M | 3.5M |
| hook words / tense | 11 / past | 9 / past | 21 / past | 12 / past | 14 / present |
| WPM | 219 | 201 | 230 | 231 | 225 |
| mean sentence (words) | 13.2 | 10.2 | 17.6 | 15.3 | 15.3 |
| shots / ASL | 26 / 2.51 | 33 / 1.98 | 29 / 2.23 | 27 / 2.37 | 26 / 2.52 |
| dissolve median (frames) | 16.5 | 14 | 9.5 | 16 | 14 |
| hard cuts | 5 | 2 | 6 | 3 | 4 |
| sub-1 s hook burst | no | yes (roll-whips) | yes (pour-follow) | no (whip in one move) | no (static) |
| "You see," at | 52.7 s | 3.4 s (setup) | 42.9 s | 45.3 s | none |
| spoken explanation | yes | no (shown only) | yes + analogy | yes | no (mystery) |
| darkest block | hook 0-3.5 (84.6); mid: night @42.5 (98) | train interior @27.5 (66) | storm/payoff (61-81) | cashier @40 (70) / night end (78-83) | night press @35-42 (73-79) |
| loops into hook | no | no | no | no | **yes** |

## Files produced
- Report: `C:/Users/JARVIS/Desktop/Claude-Vd/RicksClips3000/analysis/reports/videos_01-05.md`
- Stills (540 px wide) and stacks in `C:/Users/JARVIS/Desktop/Claude-Vd/RicksClips3000/analysis/stills/`:
  - Stacks: `0N_stack.jpg` (N = 1-5) and individual stills `0N_<id>_<t>.jpg`.
  - Open/end strips: `01_strip_open/end`, `02_strip_open/end`, `03_strip_open/end`, `04_strip_open/end`, `05_strip_open/end`, `05_loop.jpg`.
  - Effect strips: `01_strip_rage`, `01_strip_whip`, `02_strip_spin`, `03_strip_light`, `04_strip_flash`, `04_strip_mirror`, `05_strip_crane`.
  - Check images: `mouth_check.jpg`, `03_caption_frames.jpg`, `fullres_crops.jpg`, `props_check.jpg`, `text_check.jpg`, `moves_check.jpg`.
