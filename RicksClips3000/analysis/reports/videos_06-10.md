# RicksClips3000: Videos 06-10 (style and script analysis)

Sources: per-frame CSVs, edit JSONs (shots/transitions/camera moves), Whisper word timings, dense sheets, plus the stills and strips I extracted to `analysis/stills/` (`v06_key.jpg`, `v06_strip_open.jpg`, `v06_strip_eye.jpg`, `v06_strip_aura.jpg`, `v07_key.jpg`, `v07_strip_open.jpg`, `v07_strip_flash.jpg`, `v07_cap.jpg`, `v08_key.jpg`, `v08_strip_17.jpg`, `v09_key.jpg`, `v09_strip_porch.jpg`, `v10_key.jpg`, `v10_strips.jpg`, `v10_loop_crop.jpg`, `v06-10_loop.jpg`, `v06-10_fullres_crops.jpg`).
Transcripts below are Whisper text, checked against YouTube auto-captions and the burned-in captions. Three fixes were needed: 07 "rent **in** birthdays" (the burned caption confirms it), 09 "**Bodies** twitch" and "graves" in lowercase.
Section stats use the format **luma / contrast / sat / warm(R-B)**, averaged from the frames CSV. "Inference" marks anything I didn't measure directly.

---

## 0. Cross-video findings (checked against what video 11 showed)

| | 06 | 07 | 08 | 09 | 10 |
|---|---|---|---|---|---|
| Duration / views | 56.1s / 7.99M | 77.8s / 0.46M | 63.3s / 6.00M | 59.5s / 11.30M | 57.7s / 7.32M |
| Shots / ASL (median) | 20 / 2.80s (2.45) | 37 / 2.10s (1.53) | 20 / 3.16s (2.31) | 20 / 2.98s (2.23) | 22 / 2.62s (1.73) |
| Dissolves + cuts | 17 + 2 | 34 + 2 | 19 + 0 | 19 + 0 | 21 + 0 |
| Dissolve length mean (range) | 11.2f (4-20) | 15.5f (3-41) | 17.2f (3-31) | 16.9f (5-36) | 15.1f (4-21) |
| First shot | 0.67s | 0.80s | **5.20s** | 0.83s | 1.10s |
| WPM (speech span) | 235 | 228 | 221 | 223 | 209 |
| POV | **2nd person ("Imagine you")** | 3rd (he) | 3rd + imperative hook | 3rd (he/she) | 3rd (he) |
| Seamless loop? | no | verbal bookend only | no | palette bookend only | **yes (designed)** |

- **The hook burst did not show up in these five.** No video opens with 0.2-0.4s shots. The energy in the first 2s comes from one fast camera move instead:
  - 06: a bullet-tracking shot.
  - 09: a 120%/s push-in into the grave.
  - 08: one held 5.2s push-in, where the motion comes from a lighting change.
  - 07 and 10 have three shots in the first 1.6-2.4s, each about 0.8-1.3s long.
  - Shots under 1s cluster at **montage beats** instead: 07 at 47-57s and 64-65s, 10 at 21.6-25.5s and 53.8-55.6s.
- **Dissolves are the default transition:** 110 of 114 transitions.
  - The four hard cuts all land on a punch beat: 06 at 17.07 ("you're face down" gag), 06 at 45.93, 07 at 20.37 (on "300"), 07 at 29.83.
  - The very long dissolves (27-41f) mark jumps in time or memory: 07 at 38.43 (41f, into the memory polaroid), 09 at 51.87 (36f, night to sunrise), 08 at 17.23 (31f) and 49.67 (30f).
- **Edits follow sentences.** The share of transitions within 0.25s of a sentence start, against what random placement would give:
  - 06: 42% vs 13%
  - 07: 42% vs 16%
  - 08: 47% vs 14%
  - 09: 37% vs 16%
  - 10: 24% vs 8%
  - Inside a sentence, the picture usually changes on the noun being named ("300", "draw", "undercover").
- **The camera is not always moving.** 06, 09 and 10 have no static shots (or nearly none). 07 has 18.2s (23%) classified static and 08 has 7.6s (12%), placed on emotional dialogue or the reunion. Across the five, 62 shots push in and 38 pull out.
- **The longest take often holds the turn:**
  - 08: 51.13s, 8.83s long (lottery office).
  - 09: 29.07s, 8.10s long (wife in the dark).
  - 10: 32.43s, 11.17s long (the twist is staged inside the frame).
- **Second person is one mode, not the rule.** Only 06 uses "Imagine you..." (21 you-forms). 07-10 are third-person stories told mostly in the historical present.
  - "**You see,**" is the recurring hinge into exposition or the explanation: 06 at 36.5, 07 at 3.4, 09 at 3.2 and 54.0, 10 at 43.7.
- **The hook formula is one declarative sentence of 6-20 words describing a paradoxical or transgressive act:**
  - "had one rule. Never draw first"
  - "sold his happiest memory"
  - "One's a winner and one's garbage. Yet there's a way to tell"
  - "buried a man alive"
  - "said, sorry man, not a winner"
- **The narration barely pauses.** Mean gap between words is 0.02-0.04s, and each video has only 1-4 pauses of 0.3s or more. Those pauses sit after the hook sentence or just before the twist. The longest across all five is 0.56s, in 10: "congratulations, … just wait right here".
- **Grading: shadows are tinted purple.** In every video, the darkest k-means color cluster is a violet-tinted near-black, not neutral: #2c1b31, #151230, #1f182b, #2a193f, #2f232d.
  - The flat 2D characters pick up the scene light. Faces take the key color (blue in 07 at 72.5s, pink-violet in 09 at 33s, gold or green in 08 at 3s).
  - A thin rim highlight runs along the outline, and the background is soft from depth of field (1:1 crops in `v06-10_fullres_crops.jpg`).
- **"The reveal goes darker and bluer" holds for 06, 07 and 09.** It is inverted in 08, where the reveal is the brightest, highest-contrast and most neutral section. In 10 the reveal goes cooler and flatter, then warms back up to match the hook for the loop.
- **Information graphics are props inside the 3D set, never flat overlays.** Examples:
  - a ledger of "SOLD" years
  - a "HAPPINESS $" gauge
  - a corkboard bar chart labeled "CLERKS" vs "EVERYONE ELSE"
  - a Morse-style practice chart on a wall
  - a death certificate
  - a "THINK BEFORE YOU DRAW" sign
  - an odometer reading "300 BAHAMAS"
  - a road map with gas-pump pins
- **Captions match video 11** (white heavy rounded sans, black outline, about 70% down the frame). Chunks run up to 3 words, for example "You caught it", "you had to", "How does the".
- The YouTube auto-captions contain `[music]` tags, so there is a music bed. I did not analyze the audio.
- **Views (inference only):** 07 is the only invented-world fable with no real-world claim, and the longest at 78s. It got 13-24x fewer views than the other four.

---

## Video 06: "Why the Second Draw Always Wins"
56.07s · 7,987,648 views · 276k likes · uploaded 2026-10-27

### Transcript
> The fastest gun in the West had one rule. Never draw first. Imagine you're standing in the street at noon, staring down a guy everyone calls Slow Eddie. His hands are at his sides, he hasn't even looked at his gun, and he just nods at you and says, "After you." So you grab for your gun faster than you've ever moved in your life, yet you're face down in the dirt before it clears the holster. How is that possible? Eddie isn't even fast. He'd lose a race to the saloon against a guy carrying two beers. But men ride in from three states away to duel him, and every one of them goes down the exact same way. The only weird thing anyone ever notices is that Eddie never looks at your face, he just stares at your hand. You see, think about the last time your phone slid off a table. You caught it before you even realized it was falling, because you never decided to catch it, your body just did. But when you went for your gun, you had to decide the exact moment to draw, and that tiny decision slowed your hand down. Eddie never decides anything, he just waits for your hand to twitch and lets his body react on its own.

### Script breakdown
- **Hook (0.00-3.46):** "The fastest gun in the West had one rule. / Never draw first."
  - 9 + 3 words, with a 0.38s pause between them.
  - Device: paradox. The fastest gun wins by not drawing first. A superlative is set against a rule that seems to contradict it.
- **Setup (3.78-12.9):** second-person immersion, "Imagine you're standing in the street at noon…".
  - A three-part description of Eddie's nonchalance (hands at his sides / hasn't looked at his gun / just nods).
  - Ends on the line of dialogue "After you."
- **Escalation (12.9-20.7):** the action and its failure, linked by "So… yet…". Then the rhetorical question "**How is that possible?**" at 20.0.
- **Comic deflation (20.9-25.3):** "Eddie isn't even fast. He'd lose a race to the saloon against a guy carrying two beers." (hyperbole gag)
- **Raising the scale (25.3-30.2):** "But men ride in from three states away… every one of them goes down the exact same way."
- **Clue (31.0-36.5):** "Eddie never looks at your face, he just stares at your hand."
- **Explanation (36.5-49.1):** "You see," then a relatable everyday analogy (catching a falling phone), then the reflex-vs-decision contrast "But when you went for your gun…".
- **Ending (50.9-55.94):** "Eddie never decides anything… lets his body react on its own."
  - Calls back to "your body just did" and resolves the hook's rule.
  - **No loop:** the last line does not flow grammatically into the first, and the frames don't match (night vs noon).
- **Style:**
  - 14 sentences, averaging 15.6 words (range 3-26).
  - Present tense, with the past only inside the analogy.
  - 21 you-forms against 10 he-forms.
  - Two "But" pivots, one "yet", one rhetorical question.
  - 235 wpm. The 10s buckets run 216/258/234/240/228/232, so the pace stays flat and fast.
  - Only two pauses of 0.3s or more, both inside the hook.
  - Inference: the explanation is the real "reaction beats action" idea, but the script never names a source.

### Visual
- **Settings, progressing from noon to night:**
  - 0-25s: Western main street at noon. Cobalt sky, cartoon clouds, a sand street, false-front buildings ("GU…", "PHOTOGRAPHS").
  - 25.6-31s: the same street at **golden hour**. Backlit riders, sun flare and light shafts, dust haze, long shadows toward the camera, sparkle motes.
  - 31-36.6s: in front of the PHOTOGRAPHS store.
  - 37-44.5s: **saloon interior.** Red damask wallpaper, purple shadows, a round poker table, and a glowing **smartphone** with a lock-screen UI. The anachronism is deliberate, to stage the analogy.
  - 44.7-51s: wood-paneled room with round porthole windows onto the street. A sign reads "THINK BEFORE YOU DRAW", plus a wanted-style poster.
  - 51-54s: the same room at **night**, blue, with light shafts through the portholes making pools on the floor.
  - 54.1-56s: night street outside "FIRST BANK". Eddie fires from the hip (muzzle flash at about 55.0s) while the challenger's gun is still in its holster.
- **Palette** (k-means): plum near-black #2c1b31, sand tan #cca885, brick-maroon #763c38, slate indigo #3a3f6d, terracotta #b77f5b, sky azure #439bf2.
- **Lighting:**
  - Noon has hard, short shadows falling down-left (0.3s), which fits the script's "at noon".
  - Sunset is backlit, with rim-lit riders, a lens flare and god rays.
  - The saloon has warm practicals, and the phone screen lights the hand.
  - Night is blue moonlight with shaft pools.
- **Sections (luma / contrast / sat / warm):**

  | Section | Time | Luma | Contrast | Sat | Warm | Vignette |
  |---|---|---|---|---|---|---|
  | Hook | 0-3.5s | 137 | 46 | 94 | -4 | 5 |
  | Setup | 3.5-20.8s | 142 | 49 | 108 | -9 | 4 |
  | Middle | 20.8-36.6s | 113 | 50 | 113 | +36 | 10 |
  | Reveal | 36.6-50.9s | 81 | 60 | 138 | +30 | 34 |
  | End | 50.9-56.1s | 59 | 46 | 171 | -56 | 29 |

  - The middle is the golden hour. The reveal is darker and higher-contrast, and warm because of the red saloon. The end is darkest, bluest and most saturated.
  - Warmest frame: 14.5s (+64, the gold aura). Coolest: 52.8s (-69).
  - Brightest frame: 44.2s (luma 178, cream eye close-up). Darkest: 52.5s (41).
- **Depth of field:** strong background blur in the bullet shot (1.0-2.5s) and the holster close-ups.
- **Effects (strips `v06_strip_open.jpg` and `v06_strip_aura.jpg`):**
  - 0.70s: a flame muzzle flash with the gun recoiling upward.
  - 1.1-1.2s: a slow-motion bullet with a light trail and a shockwave ring.
  - 14.1-16.5s: a "power-up" look. Rising golden flame particles, glowing eyes with concentric rings, white speed lines, a whip down to the holster with a motion-blur streak, and a star and ring **impact flash** on the holster (14.50-14.70). Sweat drops.
  - No film grain was visible at 1:1.

### Camera and edit
- **20 shots**, ASL 2.80s. 17 dissolves averaging 11.2f, which is **the shortest dissolves of the five**, plus 2 hard cuts:
  - 17.07: on "you're [face down]", for the face-plant gag.
  - 45.93: inside the porthole sequence.
- **Opening:**
  - A 0.67s shot of the gunman. His expression swaps from smirk to gritted-teeth grid at 0.3s.
  - An 18f dissolve into a 2.03s **bullet-tracking shot** (push-in 15.5%/s, pan-right 0.25 w/s, roll -6.2°/s).
  - Then a 2.47s pull-out from a holster close-up with a **roll of -10.1°/s**, revealing Eddie.
- **Notable moves:**
  - 15.03: pull-out at 22.7%/s on "faster than you've ever moved".
  - 17.07: push-in at 18.4%/s on the fall.
  - 40.87: push-in at 47.4%/s plus a 12.5°/s roll on "realized it was falling" (the phone catch).
- **Match-shape transition (`v06_strip_eye.jpg`):**
  - 43.8-44.6s: the camera pushes into the challenger's eye until the pupil fills the frame. The frame is black on the word "But".
  - 44.73: the black pupil becomes a round porthole looking onto Eddie in the street.
  - 45.30: a **183%/s pull-out** reveals the room.
- **Sentence-start transitions:** 8.37 "His", 20.97 "Eddie", 25.57 "[But] men", 31.07 "The only", 36.63 "You see", 44.53 "But", 50.93 "Eddie".
- **On-screen elements:** storefront signs (PHOTOGRAPHS, FIRST BANK), a "COLORADO" saddle blanket, the phone UI, the "THINK BEFORE YOU DRAW" sign, a poster.

### Character animation
- Pose-to-pose with expression swaps:
  - smirk to teeth-grid (0.3s)
  - ring eyes glowing gold (aura)
  - a sand-covered dazed face-plant with dizzy eyes (20-21s)
- Eddie keeps a flat, unbothered half-lid throughout and has something in his mouth (a toothpick or cigarette).
- The comic beat is the challenger's full-body face-plant (17.0-19.5s), played in a static-ish pull-out.
- His mouth moves on "After you" (dense sheet). Narration is not lip-synced.

### Distinctive
- The pupil-to-porthole match transition.
- The day-to-night progression that matches the argument.
- An anime-style power-up parody to visualize "faster than you've ever moved".

---

## Video 07: "Every Memory Has a Price"
77.8s · 462,927 views · 19.1k likes · uploaded 2026-10-26

### Transcript
> He sold his happiest memory to a stranger behind a counter. You see, memories are money here. There's a shop on every corner that'll pull one right out of your skull. Landlords take rent in birthdays, and a bag of groceries costs the day you learn to ride a bike. The city is split in two by a giant wall. On one side, the rich just buy everyone else's summers. So some guy over there has been to the Bahamas 300 times without leaving his couch. On the other side, people stare at old photos of themselves smiling, with no idea why. And since the rich only want the good stuff, the happier the memory, the more it pays. Jerry only sold his to cover rent. But that same week, his little brother gets sick. And every night in the hospital, he begs for the same bedtime story: the summer they caught a frog the size of a football at the lake. But the medicine costs way more than rent. So Jerry goes back and sells that summer for a week of it. The best birthday he ever had pays for the surgery. And soon, he's selling whole years, until his head is mostly bad days and bus rides. His brother keeps getting worse, until there's only one good year left. And the guy behind the counter stares at him and says, "Kid, you sell this, there's nothing happy left in there." He sells it anyway, and it pays for everything. A week later, his brother sits up in bed, cured, and says, "Hey Jerry, tell me the frog story." And Jerry has no idea who this kid is. He sold every happy year he ever had. And his brother was in every single one.

### Script breakdown
- **Hook (0-3.22):** "He sold his happiest memory to a stranger behind a counter."
  - 11 words. Opens in the middle of the action with a superlative, and literalizes an idiom (the memory becomes an object you can sell).
- **Worldbuilding (3.40-31.18), about 28s before the hero is named:**
  - The rule: "memories are money here".
  - Concrete prices: rent in birthdays; groceries cost "the day you learn to ride a bike".
  - A wall that splits rich from poor.
  - A gag: "Bahamas 300 times without leaving his couch".
  - A sad mirror image: poor people staring at photos "with no idea why".
  - The pricing rule that drives the plot: "the happier the memory, the more it pays."
- **Inciting incident (31.46-35.5):** Jerry is named. "But that same week, his little brother gets sick."
- **Plant (35.7-42.0):** the bedtime frog story, which is the callback object.
- **Escalation ladder (42.1-57.7):** linked by But, So, And soon, until:
  - sells the summer for a week of medicine
  - the best birthday pays for the surgery
  - whole years
  - "only one good year left"
- **Warning (57.9-63.0):** "Kid, you sell this, there's nothing happy left in there." This holds the only 0.3s+ pause in the video (after "Kid,").
- **Climax (63.1-65.4):** "He sells it anyway, and it pays for everything."
- **Twist (65.7-72.9):** the brother is cured, asks for the frog story, and "Jerry has no idea who this kid is."
- **Explanation and ending (73.1-77.66):** "He sold every happy year he ever had. And his brother was in every single one."
  - O. Henry-style irony.
  - Echoes the hook verbally ("He sold his happiest memory" becomes "He sold every happy year…").
  - Not a seamless sentence loop, and the frames don't match.
- **Style:**
  - 24 sentences, averaging 12.3 words (range 6-21). The most even rhythm of the five.
  - Polysyndeton: "and" appears 13 times, often to open a sentence. "until" appears twice for escalation.
  - No questions.
  - Third person in the historical present, apart from the past-tense hook and ending.
  - 228 wpm.
  - The only video of the five with no real-world claim (pure fable).

### Visual
- **Settings:**
  - A rainy night city with wet, reflective pavement, rain streaks at about 9s and a "DELI GROCERY" awning.
  - A memory shop with a green-shaded pendant lamp and a hooded shopkeeper with glowing eyes and a **Cheshire grin** (1.6-2.0s, 28-31.5s).
  - An extraction chair with a metal helmet on a checkered floor, under a cone of lamp light ("CASH ON THE SPOT" sign).
  - **Rich side (16-23.5s):** a sunlit turquoise pool with caustics, palms, a terraced garden tower and a sun flare. This is the brightest stretch (luma 162-180).
  - **Poor side:** a dim blue bench with the sign "MEMORIES BOUGHT & SOLD 555-0142".
  - A "HAPPINESS $" gauge.
  - A blue hospital at night.
  - The frog memory: a golden sunset lake with sparkles, introduced through a polaroid with "the frog!" handwritten on it (39.0s).
  - A ledger listing YEAR 2025 through 2016, each stamped **SOLD**, except **YEAR 2018 ★** with a baby icon (57.0s).
  - The shop seen from inside, with "MEMORIES bought & sold" lettering mirrored on the glass (60.5s).
  - A warm golden hospital reunion, then a cold blue close-up for the twist.
- **Palette:** deep navy-violet #151230 (25% of pixels), ultramarine #202f75, periwinkle #535996, maroon #5f393f, sand #d3b491, powder blue #82a1c5. Accents are tungsten amber, turquoise and carrot-orange hair.
- **Lighting:** practical pendant lamps throwing visible cones, warm tungsten windows against blue night ambient, bloom on the lamps and the memory chip, shallow depth of field in the hospital, and a rim highlight on Jerry's face at 72.5s.
- **Sections (luma / contrast / sat / warm):** the coolest video overall (warm -19) with the strongest vignette (average 35).

  | Section | Time | Luma | Contrast | Sat | Warm | Vignette |
  |---|---|---|---|---|---|---|
  | Hook | 0-3.3s | 63 | 43 | 124 | -2 | 47 |
  | World | 3.3-31.4s | 105 | 49 | 122 | -19 | 23 |
  | Escalation | 31.4-57.8s | 79 | 49 | 143 | -32 | 37 |
  | Climax | 57.8-65.7s | 73 | **67** | 131 | -8 | 55 |
  | Reunion | 65.7-70.6s | **140** | 63 | 116 | **+45** | 32 |
  | Twist | 70.6-77.9s | 90 | 62 | 158 | **-38** | 53 |

  - The flip from warm to cold happens at the 71.20 dissolve (14f, on "no [idea]"). The 2s average goes from +44 to -68.
  - Darkest frame: 64.37s (luma 16.6), just before the glow. Warmest frame: 65.63s (+77).
- **Effect (`v07_strip_flash.jpg`), a glow-out transition from 64.3 to 65.9s:** the memory chip brightens until it blooms to a gold-white whiteout on "everything.", then a 22f dissolve into the golden hospital.
- **Particles:** rain, sparkles on the lake, floating dust.

### Camera and edit
- **37 shots** (the most), ASL 2.10s. 34 dissolves (3-41f) plus 2 cuts:
  - 20.37: on "300", to an odometer reading "300 BAHAMAS".
  - 29.83: to the gauge on "the happier".
- **Opening (`v07_strip_open.jpg`):**
  - 0.80s push-in on Jerry (he **blinks** at frame 0).
  - 0.77s top-down shot of the glowing memory chip on the glass.
  - 3.37s pull-out to the grinning shopkeeper.
- **Montage:** 11 shots in 46.97-57.87s, many 0.5-1.0s, several classified static, covering "selling whole years". Then 0.67/0.33/0.73s shots in the climax at 64.0-65.7s.
- **Static holds on the emotion:** 57.87-64.0 (6.13s, the counter guy's warning) and 65.73-71.2 (5.47s, the reunion). Static shots total 23% of runtime.
- **Fastest moves:** a 65%/s push-in with a 23.8°/s roll at 15.57, on "On one side…" (it moves over the wall into the rich side), and an 84%/s push-in at 64.0.
- **Longest dissolve of all five:** 41f at 38.43, into the polaroid memory. Inference: dissolve length scales with the time jump.
- **On-screen elements:** shop signs, the odometer, the gauge, the polaroid caption, the ledger, the mirrored window lettering, the landlord's tablet.

### Character animation
- Jerry: orange spiky hair, mustard jacket, a frog pin or plush on his jacket. That is a visual plant for the frog story.
- Expressions:
  - ring-eyed worry
  - a content closed-eye smile under the helmet (7.5s)
  - an elderly couple with glazed smiles
  - the twist face: dot eyes with a small empty smile, lit cold blue (72.5s). It reads as blankness rather than shock.
- Mouth flaps for quoted speakers (the landlord at 9.5s, the counter guy). No lip-sync on narration.

### Distinctive
- The longest video, the most shots, and the only pure fiction.
- It has the lowest views, 13-24x fewer than the others (correlation only).
- It runs a full glow-to-whiteout transition and swings hard between warm and cold for its emotional beats.

---

## Video 08: "He Could Spot Winning Tickets Just by Looking"
63.27s · 6,001,796 views · 175.8k likes · uploaded 2026-10-25

### Transcript
> Look at these two scratch cards. One's a winner and one's garbage. Yet there's a way to tell without scratching either of them. It all started when a guy got fired and spent five bucks on two scratch cards on the way home. He scratches one and wins his five bucks back. But instead of celebrating like a normal person, he gets suspicious. If the lottery decides exactly how many winners get printed, how does the machine know which ones they are? So he does what any sane person would do. He blows his entire severance check on a huge stack, spreads them across his apartment floor, and stares until something jumps out. Every card has little grids of numbers printed right on the front, and most of the numbers show up two or three times. But a few only show up once. And whenever three of those loners line up in a row, it's a winner. Which means this guy just cracked the lottery. He could walk into every gas station in the state and clean them out. So what does he do? He calls the lottery. "Sir, that's impossible." Okay, so he walks into their office with a box full of cards he's never scratched, sorted into winners and losers, and gets 90% of them right. By the end of the week, the game is gone from every store.

### Script breakdown
- **Hook (0-6.42):** "Look at these two scratch cards. / One's a winner and one's garbage. / Yet there's a way to tell without scratching either of them."
  - 6 + 6 + 11 words. An imperative aimed at the viewer, a binary choice, then "Yet" plus a promise of a secret.
  - Pauses of 0.36s and 0.34s after the first two sentences: the most deliberately paced opening of the five.
- **Origin (6.5-13.6):** "It all started when a guy got fired…" A small win of five bucks back.
- **Turn to curiosity (13.7-22.3):** "But instead of celebrating like a normal person, he gets suspicious." Then a logical if/how question.
- **Escalation (22.4-31.6):** ironic "what any sane person would do", then three verbs: blows, spreads, stares.
- **Discovery (31.7-42.3):** "most show up two or three times. But a few only show up once. And whenever three of those loners line up in a row, it's a winner."
- **Stakes (42.5-48.0):** "this guy just cracked the lottery… clean them out."
- **Subversion (48.1-51.8):** the self-answered question "So what does he do? He calls the lottery." Then a quoted rebuttal: "Sir, that's impossible."
- **Proof (52.0-59.9):** 90% of the unscratched cards called correctly.
- **Ending (60.0-62.98):** the consequence, "the game is gone from every store". **No loop.**
- **Style:**
  - 19 sentences, averaging 12.2 words (range 3-28).
  - **Zero you-forms**; the viewer is addressed only by the imperative hook.
  - 2 questions, 2 "But", 1 "Yet", 3 "So".
  - 221 wpm. It slows to 186 around the dialogue at 50-60s, then the final line runs at 262 wpm.
  - Inference: it appears to dramatize a real scratch-card case, but the script never says "real" or names anyone.

### Visual
- **Settings:**
  - Hook: an office desk with a dark green wall, desk lamp, phone, red bulb and wood desk. The man wears a mustard sweater with an ID lanyard.
  - A macro shot of an LED-dot number grid.
  - A sunset lobby for the firing.
  - A convenience store under white fluorescents (9-11s, 23-27.5s, 60-63s).
  - "Vault BUSTER $2, WIN UP TO $500,000" ticket macros.
  - A teal and yellow **printing factory** with a "WINNERS 400,000" counter (19-22.5s).
  - A dark blue apartment whose floor is carpeted in cards.
  - Color-coded number grids that look like a rainbow heatmap.
  - A "STATE ROAD MAP" with gas-pump pins and a red circle drawn round it.
  - A phone keypad.
  - A white and navy lottery office with a star emblem and a smug official in a headset.
- **Light synced to words in the hook:**
  - The winning card glows gold and lights his face from below (2.5-3.0s, 4.5-5.0s).
  - The losing card gives off a **sickly green** glow with stink lines that turn his face green (3.5-4.0s), on "garbage".
  - The warmest frame across all five videos is at 5.17s (+130).
- **Palette:** plum-black #1f182b, warm off-white #e3dcd2, chestnut #62382f, navy #2f386a, rust #a85e31, gold #daa047. Accents are lime green, red ($5 circles) and teal.
- **Sections (luma / contrast / sat / warm):**

  | Section | Time | Luma | Contrast | Sat | Warm | Vignette |
  |---|---|---|---|---|---|---|
  | Hook | 0-6.5s | 94 | 55 | 147 | **+72** | 48 |
  | Setup | 6.5-22.4s | 104 | 60 | 127 | +35 | 18 |
  | Escalation | 22.4-42.5s | **83** | 58 | 116 | -5 | 9 |
  | Turn | 42.5-50.2s | 125 | 54 | 115 | +38 | 39 |
  | Reveal/end | 50.2-63.3s | **138** | **83** | 88 | -4 | -6 |

  - The hook is the warmest section in any of the five videos.
  - The escalation is darkest because of the apartment (warm -45 at 28-30s).
  - The turn section includes the map, where luma peaks at 189 (46-48s).
  - The reveal and end are the brightest, highest-contrast (84-92 at 50-60s) and least saturated: neutral fluorescent white. **This inverts the "darker reveal" pattern.**
  - Coolest frame: 28.2s (-60).
- **Plant and payoff:** at 6.0s the macro grid highlights the row "19 08 24". At 40.5-41.5s a pencil strikes through that same row as the "loners in a row".
- **Prop callback:** the "DESK STUFF" box from his firing (27.2s) comes back at 54-58s holding the sorted cards.
- **Effects:** sparkles around the winning card, cards flying while he throws cash (27.2s), the red circle drawn on the map (47.5-48s).

### Camera and edit
- **20 shots**, ASL 3.16s (the longest of the five). 19 dissolves (3-31f, mean 17.2), **no cuts**.
- **No opening burst:** one 5.20s push-in at 10.2%/s, with the first transition (25f) on "scratching".
- **Notable moves:**
  - 17.00: a 0.23s **whip** (roll 27.8°/s, pan 0.51 w/s) from his suspicious squint to the card he holds up (`v08_strip_17.jpg`).
  - 17.23: a 5.20s pull-out at 39%/s from the card back into the printing press, revealing the factory.
  - 34.0-42.5: an 8.5s tilt-up across the number grids during the pattern explanation.
  - 51.13: an 8.83s slow pull-out in the lottery office.
- Static shots: 8.53 (2.30s) and 22.43 (5.33s, "any sane person").
- **Transitions on sentence starts:** 13.60 "But", 22.43 "So", 31.67 "Every", 42.50 "Which", 44.83 "He", 59.97 "By". This video has the highest alignment of the five (47% vs 14% chance).
- **On-screen elements:** ticket designs, LED number grids, the factory counter, the heatmap grids, the pencil, the road map, the phone keypad, the headset, "LOTTERY / GAME CLOSED" signs, the DESK STUFF box.

### Character animation
- Expressions:
  - determined brows (0.5s)
  - side-glance smirk (3.0s)
  - green teeth-grid grimace (3.8s)
  - a one-lid **suspicious squint** held for about 3s (14-17s)
  - a manic toothy grin while flinging cards (24-27s)
  - wide ring eyes on "jumps out" (31.5s)
- The official is smug and half-lidded, with mouth flaps on "Sir, that's impossible".
- Movement is mostly posed holds plus camera motion. I didn't see squash and stretch in the frames I checked.

### Distinctive
- Light color is used as the meaning: gold means winner, green means garbage.
- The answer is shown in the hook-adjacent macro at 6s.
- The ending is clinical, bright and neutral rather than dark.

---

## Video 09: "What the Grave Bell Really Meant"
59.5s · 11,296,143 views (the top of this set) · 254k likes · uploaded 2026-10-24

### Transcript
> They buried a man alive with a bell tied to his finger. You see, people were so scared of waking up in a coffin that graves came with a little bell on top, tied by a string to the body's finger. Except when his bell starts ringing at two in the morning, the guy next door decides it's probably the wind. Then it rings faster, and now the whole street is out on their porches, going, "You go check!" "No, you go check!" Somebody drags the doctor out of bed, and he goes, "Bodies twitch. He's dead. I signed the paper myself." But his wife isn't on her porch. She's sitting in the dark with a shovel by the door, because she knows that ring. Three short, one long. The exact signal they practiced. Wait, practiced? Well, he was never dead. He owed money to half the town, so he faked his death. And the second that bell rang, she was supposed to grab the shovel, dig him up, and skip town with him. Instead, she just sits there all night, listening to it ring fast, then slow, then once every few minutes, until sunrise, when it finally stops. You see, with him in the ground, every debt got buried right along with him, and the house was all hers.

### Script breakdown
- **Hook (0-3.00):** "They buried a man alive with a bell tied to his finger." 12 words, a shocking image presented as historical fact.
- **Context (3.2-10.0):** "You see," then the historical mechanism, in a single 29-word sentence (the longest in the video).
- **Inciting incident (10.1-15.2):** "Except when his bell starts ringing at two in the morning…" Comic dismissal: "probably the wind".
- **Escalation (15.3-26.9):**
  - "Then it rings faster".
  - The neighbors' back-and-forth "You go check!" / "No, you go check!".
  - The doctor's three short lines: "Bodies twitch. / He's dead. / I signed the paper myself."
- **Turn (27.1-35.6):** "**But** his wife isn't on her porch." She's in the dark with a shovel. "Three short, one long. The exact signal they practiced."
- **Self-interruption (35.9-36.7):** "Wait, practiced?" The narrator voices the viewer's question, followed by two 0.32s pauses before "Well,".
- **Reveal 1 (37.0-45.9):** he faked his death to escape his debts. The plan comes as three verbs: grab the shovel, dig him up, skip town.
- **Reveal 2, the double twist (46.0-53.8):** "**Instead**, she just sits there all night…" The ringing decays in three steps ("fast, then slow, then once every few minutes") until "sunrise, when it finally stops."
- **Explanation and ending (54.0-59.26):** "You see, with him in the ground, every debt got buried right along with him, and the house was all hers."
  - Puns on "buried", calling back to the hook.
  - Not a seamless sentence loop. It is a **palette bookend**: frame 0 is a pink-lavender dusk over the grave and the last frame is a pink dawn graveyard.
- **Style:**
  - 18 sentences, averaging 12.2 words, with the **widest range (2-29)**. Fragments like "Three short, one long." and "Wait, practiced?" sit beside long run-ons.
  - Third person (13 he-forms, 5 she-forms). "You see" appears twice.
  - Tenses: past for the hook and reveal, historical present for the night.
  - 223 wpm, with the most pauses (four of 0.3s or more).

### Visual
- **Settings:**
  - Hook: a graveside at dusk. Pink-lavender sky, autumn grass, rust soil, and a gravedigger in a bowler hat with a cigarette.
  - The lavender-lined coffin.
  - A **cutaway diorama** (5.5s): a row of bell posts above ground, soil layers, the coffin below, and a neighbor's window above.
  - A snowy night with falling snow and a bell post marked "S. HOLT 1849-1894".
  - A warm candlelit attic bedroom with a patchwork quilt.
  - Lantern-lit porches.
  - The wife's dark violet parlor with window light.
  - A wall with the bell, a dot-dash practice chart and handwritten dates (36.3s).
  - **Daylight flashback** in saturated green: a crowd of townsfolk with flying papers (bills or IOUs; the text is not legible), and a "CERTIFICATE OF DEATH… S. HOLT… A. Hale, M.D." with the caption "he faked".
  - The imagined plan in bright day: he bursts out of the dirt with clods flying.
  - Night again, the wife in a rocking chair.
  - Pink dawn: the wife with a shovel on the snowy mound beside the bell.
- **Visual foreshadowing:** the "dead" man is **smirking**, with a twirled orange moustache, from 0.0 to 2.0s. Inference: the twist is planted in the hook image.
- **Lighting signature:** a soft-edged horizontal **bar of window light across the wife's eyes** (32.5-34.0s, 48-49s), a noir eye-light, plus a warm rim line on her head. Candle and lantern practicals stand against blue snow ambient.
- **Palette:** aubergine #2a193f, rust #784036, blush pink #e0b8b5, indigo #3e3787, mauve #917b90, ochre #a48843, royal blue #5162d4.
- **Sections (luma / contrast / sat / warm):**

  | Section | Time | Luma | Contrast | Sat | Warm | Vignette |
  |---|---|---|---|---|---|---|
  | Hook | 0-3.2s | 101 | 43 | 164 | **+82** | 9 |
  | Setup | 3.2-27.0s | 105 | 51 | 132 | -14 | 34 |
  | Turn | 27.0-36.9s | **69** | 48 | 157 | **-50** | 16 |
  | Flashback | 36.9-45.9s | 119 | 56 | 129 | +23 | 13 |
  | Night twist | 45.9-53.9s | 83 | 45 | 145 | -20 | 19 |
  | Dawn end | 53.9-59.6s | **171** | 50 | 84 | +30 | -15 |

  - The hook is a warm dusk. The turn is darkest and bluest, with the darkest frame at 28.9s (luma 43).
  - The dawn ending is the brightest and least saturated section. The negative vignette means the edges are brighter (sky and snow).
  - Coolest frame across all five videos: 10.33s (-133, the snowy bell).
- **Particles:** snowfall, flying dirt clods, flying papers.

### Camera and edit
- **20 shots**, ASL 2.98s. 19 dissolves (5-36f, mean 16.9), no cuts.
- **Opening:**
  - A 0.83s push-in at **120.5%/s**, the fastest opening move of the five, from the graveside wide shot into the grave.
  - A 5f dissolve.
  - A 2.40s **tilt-up at 0.46 h/s** from the coffin up the string to the bell.
- **Exposition** is held on the cutaway for 5.57s (4.30-9.87s) with a slow 2.4%/s push.
- **Longest take = the turn:** 29.07-37.17s (8.10s), a push-in at 18.2%/s on the wife, covering "She's sitting in the dark… Wait, practiced?".
- **Reveal cluster at 37.2-41.2s:** a 36%/s pull-out, a 48%/s push-in, then a 60%/s pull-out with a 0.33 h/s tilt, on "never dead / owed money / faked his death".
- **Time-lapse:** a 36f dissolve at 51.87 from night to sunrise, then a 7.63s slow pull-out to end.
- **Sentence-start transitions:** 3.23 "You see", 21.77 "Somebody", 27.10 "But", 37.17 "Well", 41.20 "And", 46.13 "Instead".
- **On-screen elements:** the grave marker with name and dates, the Morse practice chart with dates, the death certificate.

### Character animation
- **Lip-synced dialogue (`v09_strip_porch.jpg`):** on "You go check!" the man's mouth changes shape (closed under the moustache, an open "O", teeth) every 2-4 frames. A sweat drop sits on him. The shovel is pushed back and forth between the two characters as a physical gag.
- The doctor (striped pajamas, glasses) has mouth flaps.
- The wife's face barely changes: half-lidded deadpan with a teacup. Inference: her stillness is the tell.
- The husband: a smirk in the coffin, then smug, closed-eyed and blushing in the certificate shot.

### Distinctive
- A double twist (he faked it, then she betrayed him).
- The narrator's self-interruption "Wait, practiced?".
- The cutaway diorama as an explainer.
- The noir eye-bar of light.
- The time-of-day arc from dusk to night to day-flashback to night to dawn.
- The most-viewed video of the set.

---

## Video 10: "Why Cashiers Keep Winning The Lottery"
57.73s · 7,323,594 views · 218.9k likes · uploaded 2026-10-23

### Transcript
> He scanned a customer's lottery ticket, saw it had won a million dollars, and said, "Sorry, man, not a winner." The guy just shrugs, says, "Story of my life," and walks out. The second the door closes, the cashier is elbow-deep in the trash can, fishing the ticket back out and tucking it into his wallet like it's been his all along. By midnight, he's already bought a boat, a mansion, and a whole new set of friends, at least in his head. So, the next morning, he drives two hours to the lottery office, slides the ticket under the glass, and the lady at the counter smiles and says, "Wow, congratulations, just wait right here." So, he waits. Five minutes go by, then ten, until finally, a door opens behind him. In walks the guy from the store, except now he's wearing a suit with a badge on his belt, followed by two police officers. You see, in real life, lotteries noticed that store clerks were winning way more often than everyone else, which is statistically a little suspicious. So, they started printing winning tickets as bait and sending undercover agents into stores pretending to be regular customers.

### Script breakdown
- **Hook (0-9.20):** "He scanned a customer's lottery ticket, saw it had won a million dollars, and said, 'Sorry, man, not a winner.'"
  - 20 words: a three-verb chain, dramatic irony (we know he's lying) and a dialogue punchline.
  - Followed by the mark's deadpan "Story of my life."
- **Setup (9.3-17.1):** the trash-can retrieval gag, "elbow-deep".
- **Fantasy (17.2-21.4):** three items ("a boat, a mansion, and a whole new set of friends") with the deflating tag "**at least in his head**".
- **Journey (21.5-31.5):** "So, the next morning…" a three-step chain (drives, slides, the lady smiles). Then "Wow, congratulations, **[0.56s pause]** just wait right here." This is the longest pause in all five videos and works as a suspense beat.
- **Suspense (32.5-39.0):** "So, he waits." (3 words). "Five minutes go by, then ten, until finally, a door opens behind him."
- **Twist (39.2-43.5):** "In walks the guy from the store, **except** now he's wearing a suit with a badge…, followed by two police officers."
- **Explanation (43.7-57.46):** "You see, **in real life**, …"
  - A real-world claim.
  - Understatement: "statistically a little suspicious".
  - "as bait" pays off the bait-shop setting.
- **Ending, which loops back into the hook:** "...pretending to be regular **customers**." flows into "He scanned a **customer's** lottery ticket…". **This is the designed loop** (see Visual).
- **Style:**
  - Only 10 sentences, with the **longest average (20 words)** and a range of 3-33. Long chained sentences broken by one 3-word stop.
  - Third person: past tense for the hook, then present, then past for the explanation.
  - 209 wpm, the slowest of the five. It slows to 186 during the wait and to about 169 in the final explanation.
  - No "But" and no questions. Contrast comes from "except" and "until".

### Visual
- **Settings:**
  - A **bait-and-tackle convenience store**: sage green walls, a pegboard of lures ("LURES · TACKLE"), a "LOTTERY" sign, a scratch-card dispenser, a green pendant lamp and a "LIVE BAIT" counter front.
  - Cashier in a red polo with the name tag "KYLE". Customer in an olive bucket hat stuck with lures.
  - Ticket macro: "REEL BIG CASH $20, WIN UP TO $1,000,000", lit by the red scanner light. The register LED reads "$1,000,000".
  - A trash can.
  - **Fantasy (17.5-21.5s):** a purple night sea, a giant pink moon, the yacht "FINDERS KEEPERS" with string lights, a castle, fireworks.
  - A pink-sunrise drive in a red car.
  - A teal **Prize Claims** office: "PLACE TICKET HERE ▶", a "SECURITY" button (inference: planted for the twist), "EMPLOYEE OF THE MONTH", a prize-claim form.
  - A bright yellow "**OUR WINNERS**" waiting room.
  - An investigation set: a photo labeled "KYLE · LAKE RD" on a pin, with **venetian-blind shadow stripes** (44-45s).
  - A corkboard **bar chart, "CLERKS" vs "EVERYONE ELSE"**, made of pinned photos (45.5-49.5s, blue).
  - A cabinet with tickets **hung on fish hooks** "as bait" (53.5s).
  - A "GONE FISHIN'" door sign and a night storefront reading "BAIT · GAS".
- **A system of fishing puns** runs through the visuals: the bait shop, the lure hat, "fishing the ticket out", REEL BIG CASH, the hooks, FINDERS KEEPERS. Inference: the set was built out of the script's idioms.
- **Palette:** pale lilac-white #d7cfd3, taupe #9e8e7c, plum-black #2f232d, steel blue #3e5a7b, rust #8e4e32, sky blue #6ba6d5, mustard #d9b130. Accents are fire-engine red, magenta-pink and teal.
- **Sections (luma / contrast / sat / warm):**

  | Section | Time | Luma | Contrast | Sat | Warm | Vignette |
  |---|---|---|---|---|---|---|
  | Hook | 0-9.2s | 134 | 60 | 102 | +47 | 18 |
  | Setup | 9.2-29.5s | 115 | 58 | 126 | -16 | 36 |
  | Escalation | 29.5-43.6s | **171** | 58 | 94 | +15 | **-24** |
  | Reveal | 43.6-55.4s | 110 | **41** | 116 | **-37** | 13 |
  | End | 55.4-57.8s | 115 | 58 | 139 | **+45** | 20 |

  - The setup includes the purple fantasy (warm -73 at 18-20s).
  - The escalation is brightest, with no vignette (the yellow room).
  - The reveal has the lowest contrast of any section in the five videos: a soft blue investigation look.
  - The end returns to the hook's warmth, which helps the loop. Coolest frame: 49.93s (-130).
- **The iris effect (`v10_strips.jpg`, 12.5-14.0s):** everything outside a circle around Kyle's face drops to near-black. A villain spotlight while his grin changes from squint to toothy to smug.
- **The loop (`v10_loop_crop.jpg`):** the last frame recreates frame 0's composition (cashier at the counter under the green lamp, scanner in hand, ticket on the counter). But the name tag now reads "**TRAINEE**" and the cashier has a different hairstyle. Inference: a new clerk, so the cycle repeats.

### Camera and edit
- **22 shots**, ASL 2.62s. 21 dissolves (4-21f, mean 15.1), no cuts.
- **Opening:** a 1.10s push-in, a 17f dissolve, a 1.27s push-in at 62%/s with a 6.2°/s roll onto the ticket on "won a million", then a 3.53s pull-out to Kyle and the register.
- **Montage bursts:**
  - 21.63-25.47: four shots of 0.73-1.17s on "So, the next morning, he drives two hours…".
  - 53.77-55.60: shots of 0.47/0.93/0.43s on "sending undercover agents into stores".
- **The longest shot in all five videos:** 32.43-43.60 (**11.17s**), nearly locked off with only a -1.7°/s roll, in the waiting room, covering "So, he waits… followed by two police officers."
  - **The twist is staged in depth instead of with a cut:** the agent appears in the back doorway at about 37.5-38.5s, and the officers are in frame by about 42-43s. Kyle cheers in the foreground with his arms up.
- **Wipe at 54.23:** a 127%/s pull-out with high jitter (10.9). The agent's bucket hat sweeps through the foreground as a wipe from the ticket cabinet to the BAIT · GAS exterior.
- **Edits are the least tied to sentences of the five:** 24% within 0.25s of a sentence start (8% chance), and clause alignment is near chance (38% vs 34%). Cuts follow the images named instead: "won", "out", "along.", "office,", "undercover", "stores".
- **On-screen elements:** the ticket, register LED, name tags (KYLE, then TRAINEE), PRIZE CLAIMS, PLACE TICKET HERE, SECURITY, OUR WINNERS, the KYLE · LAKE RD photo, the CLERKS / EVERYONE ELSE chart, GONE FISHIN', BAIT · GAS, FINDERS KEEPERS.

### Character animation
- Kyle's expressions:
  - smug half-lid (0s)
  - ring-eyed shock with a sweat drop, then a closed-eye fake smile (3.0-3.5s)
  - mouth flaps on "Sorry / Not / a winner" (4.5-5.5s)
  - **legs sticking up out of the trash can** (11.5-12.0s), a full-body gag
  - a sly grin under the iris
  - happy closed eyes (16.5-17s)
  - arms-up cheering in the waiting room while the agent walks in behind him (dramatic irony staged in a single frame)
- The customer shouts "Story of my life" with an open mouth (8.0s).
- The prize lady has curly hair, glasses and a big grin, and waves.

### Distinctive
- The only true seamless loop: the sentence and the image both close, with a "TRAINEE" variation.
- The twist is staged in depth during an 11s take.
- A complete fishing visual-pun world.
- Noir blind shadows mark the investigation.

---

## Craft takeaways from 06-10 (summary, partly inference)
1. **Hook:** one concrete, slightly wrong act ("never draw first", "sold his happiest memory", "buried alive", "not a winner") in 6-20 words. If you stop after the first sentence, add a "Yet…" promise (08). Show the answer or a tell in the first frames: 09's smirk, 08's glowing row.
2. **Structure:** setup with comic specifics, then a "But" or "Except" turn, then escalation in threes, then a twist line, then "You see," with the explanation. End on a line that echoes the hook's key word (sold, buried, body, customer).
3. **Narration:** about 210-235 wpm with almost no pauses. Spend your only pause right before the twist ("Wait, practiced? / Well,"; "congratulations, … just wait").
4. **Edit:**
   - Dissolves of 10-20f by default.
   - Dissolves of 30-40f for time jumps.
   - Hard cuts only for a gag impact or a number reveal.
   - Change the picture at sentence starts and on the noun being named.
   - Hold the longest take on the turn.
5. **Light as story:** good is gold and bad is green (08). Warm reunion, cold realization (07). Time-of-day arcs (06 noon to night, 09 dusk to dawn). Shadows graded violet, characters tinted by the key light and given a rim highlight.
6. **Diegetic infographics and puns:** build the explainer out of objects in the world (ledgers, gauges, corkboards, maps, certificates, signs), and furnish the set with the script's idioms (10's bait shop).
