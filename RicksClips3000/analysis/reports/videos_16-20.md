# RicksClips3000: videos 16-20 (the oldest batch, uploaded 2026-10-14 to 10-17)

Method: I read each dense sheet, transcript and edit JSON, and ran section stats on the per-frame CSV. Stills, frame strips and loop strips were pulled with ffmpeg/cv2 and saved in `analysis/stills/` (`v16_*` … `v20_*`, plus `NN_<id>_<t>.jpg`). Speaking rate (WPM) = word count / (last word end - first word start). Colour stats are section means from the CSV: luma, contrast = luma std, sat, warm = R-B, vig = centre minus edge luma. Palettes come from k-means on frames sampled every 10 frames. Items marked **(inference)** are my interpretation. Everything else was observed or measured.

**A caveat on the edit JSON:** its detector misses some short (~7-9 frame) dissolves and treats some fast camera moves or pose swaps as transitions. Where I checked frames by hand, I say so below.

---

## Cross-video summary: what is different from the video-11 description

| | 16 Spear/Shield | 17 Painkillers | 18 Japan gambling | 19 Slot machines | 20 Time test |
|---|---|---|---|---|---|
| Duration / views | 45.1s / 8.70M | 34.5s / 0.30M | 45.1s / **13.78M** | 31.0s / 0.11M | 40.1s / 6.09M |
| Words / WPM | 165 / 221 | 137 / **240** | 161 / 215 | 112 / 218 | 143 / 217 |
| Shots (JSON) / ASL | 19 / 2.37s | 20 / 1.72s | 11 / 4.09s (true count ≥13) | 13 / 2.38s | 18 / 2.22s |
| 1st shot length | **9.0s** | 3.97s | 1.93s | 0.67s, then 7.63s | 2.93s |
| Dissolves (median len) / hard cuts | 15 (15f) / 1 real | 19 (15f) / 0 | 9 (13f) / 1 | 8 (13.5f) / 4 | 15 (12f) / 2 |
| Narration | 3rd person, past (fable) | 2nd person, present | 3rd, switching to 2nd at 13.6s, present | 2nd person, present | 3rd person, past, generic "you" |
| Reveal pivot | "You see," at 73% | "Well, picture…" at 43% | "You see," at 67% | "So let's crack it open." at 53% | "You see," at 80% |
| Loop design | bookend only | bookend (pain/relief) | **yes** (same alley, "gambles"→"Gambling") | soft | **yes** (flipbook page = frame 0) |

**Evolution from video 11 (11 is 61s, 225 words, first shots 0.17/0.17/0.40s, "Imagine your boss…"):**
1. **Shorter:** 31-45s and 112-165 words. Videos 01-14 run 55-78s.
2. **No rapid hook burst.** None of the five cuts in the first 2s, apart from one 14-frame dissolve at 0.67s in video 19. Each opens on one continuous moving shot in which the hook is acted out literally: the spear pierces the anvil (16), he tosses the pill into his mouth (17), a man walks past the window that pays out (18), the reels land one short (19), a man falls off the tower (20).
3. **No "Imagine you…" opener.** The hooks are a classic paradox told as a fable (16), a question (17), an "X is illegal, yet X is everywhere" contradiction (18), an in-the-moment "You just watched…" (19), and a shock claim (20).
4. **Unchanged:** art style (flat 2D outlined characters in toon-shaded, outlined 3D sets); the caption style; dissolve-dominant editing (median 12-15 frames, the same as 11); speaking rate (215-240 WPM vs 224); the "You see," pivot (used in 16, 18, 20 and in 11).
5. **"The reveal goes darker and bluer" holds only for the two night-time human-trick stories (16, 18).** The three mechanism explainers (17, 19, 20) move into a warm or red "inside the mechanism" interior for the reveal: inside the body, inside the machine, inside the head.
6. **Recurring device: showing an invisible mechanism as a physical interior.** 17 turns the body into a house of smoke alarms; 19 cuts the machine open to a list, then a pie wheel, then an X-ray; 20 shows the brain as a little man drawing at a desk behind porthole eyes.
7. **Captions:** same as 11. White heavy rounded sans with a black outline and soft shadow, centred at about 70% height (measured y≈674 of 960). Cards are 1-3 words ("The two kingdoms", "in the house.", "past the door,") and swap on word timing. Numbers are shown as numerals ("for 100", "10,000", "and 20"), punctuation is kept ("is?", "Bro,"), and I saw no coloured keyword highlighting.
8. **(inference) Views:** the three story or trick videos (18, 16, 20: 6-14M) far outperform the two pure "how X works" explainers (17, 19: 0.1-0.3M). The weak ones are the shortest, with question or scenario hooks and no human trickster or twist. That is five data points only.
9. **Transition timing:** cuts and dissolves land almost always within ±0.1s of a sentence start, or on a contrast word ("yet", "but", "than"). Examples are listed per video.
10. **Pauses:** the voice-over is nearly continuous. The longest gap is 0.36s, and pauses sit only after the hook, before the punchline, or after "You see,". Speech starts at 0.00s in every video and ends 0.0-0.5s before the last frame, so there is no outro.

---

## 16: "An Unstoppable Spear vs an Unbreakable Shield"
45.07s · 8,704,706 views · uploaded 2026-10-17

### Transcript
A blacksmith sold a spear that could pierce anything to one king, and a shield that nothing could pierce to his worst enemy. The two kingdoms had been at war for a hundred years, and now each king finally had the weapon to end it. So both armies marched to the same field, the spear at the front of one, and the shield at the front of the other. Then nobody moved. A whole week went by, with ten thousand soldiers just staring at two pieces of metal. One night, each king secretly sent a messenger to the blacksmith with the same question. Which one is real? And to both of them, he gave the same answer. Attack and find out. You see, a spear that pierces anything and a shield nothing can pierce can't both exist. So the blacksmith made both out of plain old iron, knowing neither king would dare be the first to find out. And that's how he ended the war.

### Script
- **Hook (0-6.08s, 23 words):** the irresistible-force paradox told as a fable. The two halves mirror each other ("could pierce anything" / "nothing could pierce"), and selling both items to sworn enemies adds stakes. Third person, past tense. The word "you" appears only once, in "You see,".
- **Setup (6.3-16.9):** a 100-year war, and "each king finally had the weapon to end it". The armies march, with mirrored phrasing again: "the spear at the front of one, and the shield at the front of the other".
- **Escalation:** "Then nobody moved." (3 words, after three sentences of 22-24 words). Then "A whole week went by… ten thousand soldiers just staring at two pieces of metal." Then secret messengers, each with "the same question".
- **Turn:** "Which one is real?" (28.1s, a hard cut) → "he gave the same answer." → a 0.36s pause → "Attack and find out." (the punchline).
- **Explanation (32.96):** "You see," then the logic ("can't both exist"), then the twist: both are "plain old iron". "find out" is a callback to the punchline.
- **Ending:** "And that's how he ended the war." This recasts the con man as a peacemaker. It does not loop into the hook as a sentence.
- **Devices:** mirrored pairs throughout (spear/shield, one/other, same question/same answer); long sentences followed by a short punch; the "find out" callback ×2; concrete numbers (100 years, a week, 10,000).
- **Numbers:** sentence lengths 23, 22, 24, 3, 16, 15, 4, 10, 4, 16, 21, 7 (mean 13.8). 221 WPM. Pauses: 0.36s before "Attack", 0.34s after "You see,", 0.28s after "One night,".

### Visual
- **Setting:** a fairy-tale medieval world. A flagstone plaza with banners sits in front of a painted backdrop of castles and mountains. Then a stone bridge over a river, an aerial view of the armies, a dirt road across a field, a royal tent, the blacksmith's house at night, and the interior of the forge.
- **Palette:** sandstone beige #a29684, rust brown #804e43, sky blue #7ca3d5, grass olive #948d45. Night is plum and indigo (#241424 / #4c365e), the forge is orange #af5f37, the blueprint is navy #1b3476. Red vs teal codes the two kingdoms everywhere: banners, robes, hooded messengers, the armies drawn as red and teal arrow formations, and the split crest.
- **Lighting:**
  - Daytime is soft sunlight with soft cast shadows on the flagstones, and light shafts over the field at about 21s.
  - Night (26-33s) has a moonlit blue exterior (2s bin at 26s: warm -46.6) with warm window light.
  - Inside are candles and lanterns as practical lights, giving warm pools against a purple and navy fill. This is the strongest warm/cool split in the video.
  - The forge is the orange key light for the reveal, with a bloom flare at 38.97s (luma +18.5 in one frame).
  - At 18.9-20.4 there is a day→sunset→moonlit night→day grade cycle in about 1.5s, timed to "A whole week went by" (strip `v16_strip_daynight.jpg`).

| section | luma | contrast | sat | warm | vig |
|---|---|---|---|---|---|
| hook 0-6.1 | 137.6 | 47.7 | 93.6 | -0.6 | 21.2 |
| setup 6.1-17 | 160.4 | 43.7 | 94.6 | 15.9 | 7.1 |
| escalation 17-28 | 131.4 | 43.3 | 112.0 | 24.3 | 32.8 |
| turn 28-33 | **61.6** | 49.1 | 136.1 | 9.0 | **51.7** |
| reveal 33-43.2 | 106.1 | 48.8 | 137.4 | 15.3 | 40.9 |
| end 43.2-45 | 160.3 | 49.5 | 86.9 | 41.5 | -21.2 |

Contrast stays flat (43-50) while brightness swings. The twist happens at night and is the darkest section with the heaviest vignette, consistent with the video-11 description. Saturation rises for the night and forge part, then the ending returns to bright daylight. I saw no film grain (checked a 1:1 crop), little depth-of-field use, and bloom only on the candles and forge. Spark particles appear at 1.87 (the anvil) and 39.2 (the forge).

### Camera and edit
- **19 JSON shots, ASL 2.37s.** The first shot is 9.0s: a slow pull-out (2.8%/s) with a roll of -3.4°/s, then a pan to the "YEARS AT WAR" sign.
- **The JSON "dissolves" at 9.0 and 9.3 are not dissolves.** Frames show one continuous fast pull-out and crane-down (104%/s, roll 16°/s) that reveals the bridge and the armies on "and now each king" (`v16_strip_9.jpg`).
- **The 28.2s "cut" is not a cut either.** It is a single-frame pose swap: the blacksmith goes from sleepy to wide-eyed. The 39.3s "cut" is also continuous action: a hammer strike throws a shower of sparks while a red-hot shield drops in and cools from orange (`v16_strip_39.jpg`). The only true hard cut is at 28.0, from the moonlit house to the dark forge, on "Which one is real?" (luma -34).
- **Transitions on sentence starts:** 11.83 "So both armies" (-0.05s), 23.77 "One night" (-0.03), 28.0 "Which", 33.0 "You see" (-0.04), 38.03 "So the blacksmith" (-0.03), 43.27 "And that's how" (+0.03). Real dissolves run 3-26 frames, median 15.
- **Moves tied to beats:**
  - 11.83: push-in at 32%/s down to the top-down armies.
  - 12.77-18.9: a 6.1s slow push-in on the standoff (two kings on the road).
  - 20.07: pull-out at 59%/s for "ten thousand soldiers".
  - 25.5: push-in at 31%/s to the blacksmith's house.
  - 28.2-32.6: near-locked 3.9%/s while he delivers the punchline.
  - 38.03: pull-out at 41%/s with the forge flare.
  - 40.67: pan-right with a 12.5°/s roll to reveal the price tags.
- **On-screen elements:** a "YEARS AT WAR" flip counter going 099→100; tally marks; helmets sprouting flowers; ivy growing on the wall; a "THE BORDER" map with a dagger in it; signs reading "BLACKSMITH", "SPEARS" and "SHIELDS"; a blueprint marked "PIERCES: ANYTHING" / "PIERCED BY: NOTHING" with a red "IMPOSSIBLE" stamp; tags reading "PLAIN OLD IRON $1"; and at the end the sign flips to "DAYS OF PEACE 001", a callback to the counter.

### Character animation and gags
- In the opening shot the red king thrusts the spear into the anvil, with a spark burst and impact lines exactly on "pierce" (1.87s). The shield gleams on "nothing" (4.27s).
- Faces change by swapping poses rather than by tweening.
- Passing-time gags at 41-43s: a bird's nest on the red king's crown, a cobweb on his spear, and the teal king sweating. The blacksmith laughs at the forge at 38.5s.

### Loop check
The last frame is the "DAYS OF PEACE 001" sign. The first frame is the kings in the same plaza: the same location, but a different framing. The closing sentence is a full stop, so this is a bookend, not a seamless loop. 0.21s of silence follows the last word.

---

## 17: "How Painkillers Actually Work"
34.5s · 300,263 views · uploaded 2026-10-17

### Transcript
How do painkillers know where the pain is? You swallow one for a headache, and then what? Does it pull out a little map? All you know is it melts in your stomach, slips into your blood, and 20 minutes later your headache's gone. So how does a pill with no brain find the one spot that hurts? Well, picture your body as a house with thousands of rooms and a smoke alarm in every single one. When you get hurt, the alarm in that room starts screaming, and that's the pain you feel. Now here comes the painkiller. It kicks the front door in and rips the batteries out of every single alarm in the house. Every other alarm was already silent, so the only one you notice go quiet is the one in your head.

### Script
- **Hook (0-2.08s, 8 words):** a direct question. Three questions arrive within 5.8s, and the third is an absurd joke ("a little map?").
- **Setup:** three journey steps, one per clause (melts / slips / 20 minutes later gone). Then the question is restated and the pill is personified: "a pill with no brain".
- **Pivot (14.82):** "Well, picture your body as a house…". This is an analogy, not "You see". The only real pauses in the video come here: 0.36s and 0.26s.
- **Escalation:** "the alarm… starts screaming". Then "Now here comes the painkiller. It kicks the front door in and rips the batteries out…": hyperbolic action, with "every single" repeated.
- **Twist/reveal:** the pill doesn't find the pain at all. It silences everything, and you only notice the alarm that was ringing.
- **Ending:** "…the one in your head." It is an answer that leads straight back into the opening question **(inference: a soft loop)**.
- **Numbers:** second person, present tense. 240 WPM, the fastest of the five. Sentence lengths 8, 9, 7, 20, 14, 19, 17, 5, 18, 20.

### Visual
- **Settings, in order:**
  - a kitchen: blinds, a warm hanging pendant lamp, a "HOT PIZZA" box and a "FINAL NOTICE" envelope;
  - the stomach: red organic walls and a green acid pool;
  - a pink blood-vessel tunnel;
  - an artery "highway" with red blood cells as rafts;
  - a red network of alarm-circles labelled by body part;
  - a blue-sided Victorian house at night on a red ground;
  - an endless red arched hallway with wall sconces, doors and smoke alarms;
  - a "HEAD" room whose two round windows are the eyes, looking out at the kitchen.
- **Palette:** kitchen off-white #ebe3dc, slate mauve #564950, coral pink #d07274, crimson #bf4b4f / #ae404c, deep maroon #511820, acid olive #627846. Accents: the pills' teal and the house's blue.
- **Lighting:** a cool kitchen with a warm pendant key. Inside the body everything is nearly monochrome red with heavy haze and bloom; warm sconces line the hallway and a red alarm light fills the ceiling. A white "light at the end of the tunnel" fills the frame at 8.77-9.1s (luma peak 188.5) and doubles as the transition to the highway.

| section | luma | contrast | sat | warm | vig |
|---|---|---|---|---|---|
| hook 0-5.9 | 141.6 | 56.2 | 87.1 | 30.2 | 15.2 |
| setup 5.9-14.6 | 119.0 | 45.2 | 139.4 | 68.1 | 23.1 |
| analogy 14.6-24 | 103.0 | 52.5 | 134.5 | 62.0 | 30.4 |
| pill action 24-29.4 | 102.4 | 49.9 | 140.9 | 56.8 | 36.2 |
| reveal 29.4-34.4 | 103.4 | **40.3** | **150.5** | **88.5** | 27.2 |

The reveal gets redder, more saturated and lower in contrast, not bluer. The last 0.5s jumps back to the bright kitchen (luma 169.7).

### Camera and edit
- **20 shots, ASL 1.72s,** the busiest cutting of the five. All 19 transitions are dissolves (7-36 frames, median 15); there are no hard cuts.
- The opening is one 3.97s push-in. The man tosses a pill into his mouth while his face cycles neutral → open mouth → wide eyes → squeezed >< eyes and grid teeth, with red pain lines and a sweat drop.
- **Each listed clause gets its own shot:** 7.47 "stomach," (-0.01s), 7.87 "slips" (+0.05), 8.67 "blood," (-0.07), 10.07 "your headache's gone".
- **Push-ins dominate (17 of 20 shots), and many are fast:**
  - 14.87 and 15.80 (76-109%/s) fly up to and through the front door, reaching the hallway by about 16.7s (`v17_strip_house.jpg`). This doorway fly-through works as an in-camera transition.
  - 25.97-32.17 is a 6.2s tracking push-in (63%/s) down the hallway with the pill army.
- The final shot is a pull-out (19%/s) on the relieved face.
- **On-screen labels:** "ACID SPA 98.6°F · NO DIVING · NO PILLS AFTER 9", "TO BLOOD →", "HUMAN BODY" map board, "HEADACHE ↑ 20 MIN / EXIT 1", "BRAIN NOT INCLUDED" (an X-ray tag on the pill), "WELCOME" mat, house number "98.6" (a body-temperature joke repeated from the spa sign), "FOR RENT", "HEAD".

### Character animation
- The pills are capsules with teal tops and stick legs. They walk with a waddle cycle, smile with closed eyes, and march as an army that bunches at the door.
- One smoke alarm has an angry face (32.6s).
- The man's faces change as held pose swaps. He ends calm with closed eyes.

### Loop check
The video starts on the man in pain and ends on the same man, relieved, in the same kitchen, in close-up rather than medium shot. That is a before/after bookend, not a frame match. 0.17s of silence after the last word.

---

## 18: "The Window That Breaks Japan's Gambling Law"
45.09s · 13,777,320 views · uploaded 2026-10-15

### Transcript
Gambling is illegal in Japan, yet there's a gambling hall on almost every street. Inside, thousands of machines are flashing and screaming while people carry out buckets full of steel balls. Police stroll right past the door, but nobody ever gets arrested. So, you win a bucket yourself and try to cash it in, but the counter won't give you a single yen. Instead, you can pick cookies, chocolate, a bottle of shampoo, or a few tiny plastic tokens. The guy in front of you takes the tokens and heads straight outside. You follow him around the corner to a little window in a wall with no sign. You see, that window isn't part of the gambling hall. It's technically a separate shop that just happens to buy those exact tokens. So the hall only ever gives out prizes, and the shop is just buying one. He slides the tokens through, a hand slides over cash, and on paper, nobody gambles.

### Script
- **Hook (0-4.28s, 14 words):** a legal contradiction ("illegal… yet… on almost every street"): a claim plus the paradox it creates.
- **Setup:** sensory detail ("flashing and screaming", "buckets full of steel balls"), then a second contradiction: "Police stroll right past… but nobody ever gets arrested."
- **POV switch at 13.6s, from third to second person:** "So, you win a bucket…, but the counter won't give you a single yen."
- **Escalation:** a list of four with a comic odd item: "cookies, chocolate, a bottle of shampoo, or a few tiny plastic tokens." Then the mystery: "The guy in front of you… heads straight outside. You follow him… a wall with no sign."
- **Turn (30.38):** "You see, that window isn't part of the gambling hall."
- **Reveal:** "technically a separate shop…" and "the hall only ever gives out prizes, and the shop is just buying one."
- **Ending:** a three-part action ("slides the tokens through, a hand slides over cash, and on paper, nobody gambles.") closing on the irony of "on paper". Its last word, "gambles", leads straight into the first word, "Gambling".
- **Numbers:** present tense throughout. 215 WPM, the slowest. It has the most even sentence lengths (10-21 words) and no ultra-short punchline. Twelve pauses of at least 0.25s, mostly the list commas, plus 0.36s after "Inside,".

### Visual
- **Settings:** a purple night alley lit by one warm window; an aerial view of a neon street (vertical pink, cyan and magenta "PACHINKO" and "FEVER" signs on wet, reflective asphalt); a pachinko hall drawn as a symmetrical corridor (fluorescent ceiling strips, black machines, red stools, red diamond-pattern carpet); a bright cream "PRIZE COUNTER"; then back to the alley and its window shop, with a lucky-cat figurine, a calico cat, a bicycle and beer crates.
- **Palette:** midnight navy #161836 / #21234c, indigo #302d56, oxblood carpet #5d271f / #451d1b, fluorescent cream #e0c9b2, tan #b49586, the hero's orange jacket #c86c2a, and neon magenta and cyan accents.
- **Lighting:** driven by practical lights. The window lamp is the key light, with bloom and haze and a pool of light on the ground; neon reflects off the street; the hall is lit from above by fluorescent strips; shadows are soft. The alley has the strongest warm/cool split of the batch.
- **Depth of field:** at 35.0s the foreground cat and bicycle are defocused. Between 30.3 and 31.4s the camera pushes past the orange guy in the foreground, which works as a wipe.

| section | luma | contrast | sat | warm | vig |
|---|---|---|---|---|---|
| hook 0-4.4 | 62.3 | 48.5 | 149.6 | -24.3 | 56.6 |
| setup 4.4-13.5 | 85.0 | 57.9 | 131.9 | 29.6 | 39.9 |
| escalation 13.5-30.2 | **108.8** | 60.1 | 122.9 | 36.2 | 21.4 |
| reveal 30.2-40.7 | **61.7** | 44.3 | 134.1 | **-21.3** | 42.6 |
| end 40.7-45 | 69.1 | 53.2 | 134.2 | -21.0 | **58.9** |

The video moves dark and cool → bright and warm (the hall and prize counter) → dark and cool again for the reveal, consistent with the video-11 description. It has the heaviest centre-weighted vignetting of the five, from compositions lit at the centre.

### Camera and edit
- **JSON: 11 shots, ASL 4.09s, with two "shots" over 10s** (16.4-26.87 and 26.87-37.03).
- **The JSON undercounts.** The CSV and frames show at least two more ~7-frame dissolves, at 18.8-19.0 ("Instead,", a sentence start) and 24.0-24.2 ("The guy", a sentence start), plus smaller changes at 8.0 and 25.6. The real ASL is about 3.5s or more. Even so, this is the longest-take, most "one-take" video of the five, and the slowest in motion (mean 6.1; reveal 2.1).
- **Moves:**
  - 0-1.93: push-in on the alley. The first shot already shows the token-buying window that is only explained at 30s, a foreshadow **(inference: deliberate)**.
  - 1.93: pull-out (35%/s) that rises above the neon street on "yet there's a gambling hall on almost every street".
  - 4.53: through the sliding doors.
  - 5.23-10.4: push-in (41%/s) down the pachinko aisle.
  - 10.4: slow pan across the police officer at the "PRIZE HALL" door.
  - 26.87-37.03: a 10s push-in that literally "follows him" past the foreground character into the alley.
  - From 37.03: very slow push-ins of about 3%/s and a final pull-out of 2.6%/s for the calm explanation.
- **Sync:** 1.93 sits on the "yet/there's" pivot, 4.53 "Inside," (+0.01s), 10.40 "Police" (+0.08), 16.40 "but" (-0.02), 37.03 "So" (+0.01), 40.77 "He slides" (-0.01).
- **On-screen elements:** "PRIZE HALL · PACHINKO · SLOTS" sign with "新台入替 NEW MACHINES"; "PRIZE COUNTER 景品カウンター"; "THANK YOU ありがとうございました"; a "WELCOME いらっしゃいませ" mat; "OPEN"; "LICENSE"; ball buckets stacked into towers. The final visual punchline is a police officer holding a "PATROL LOG — GAMBLING: NONE ☑" clipboard.

### Character animation
- The hero (orange jacket, camera strap) cycles expressions through the prize list (`v18_strip_counter.jpg`): frown → raised brow → wide-eyed toothy grin at "shampoo" → contented closed eyes.
- The clerk keeps a fixed closed-eye smile. The officer looks unimpressed with half-lidded eyes on "nobody". The shady buyer wears sunglasses and a flat cap.
- Lanky stick-limb walk cycles throughout.

### Loop check: designed to loop
- **Picture:** the last frame (the alley, purple and blue, warm window, officer) matches the first frame (the same alley, crates, AC units, warm window, same grade) in palette and location.
- **Sound:** the closing words "nobody gambles." run right up to the last frame (0.0-0.07s left) and lead straight into the opening word, "Gambling…".

---

## 19: "The Science Behind Slot Machines"
30.98s · 111,739 views · uploaded 2026-10-15

### Transcript
You just watched two jackpot symbols land, and the third one stopped one click short. So you move to the machine next door, and the exact same thing happens. Your buddy leans over and says, Bro, it's just warming up, so you put in another hundred. But it's starting to feel like the machine is teasing you on purpose. So let's crack it open. Inside is a list of every place that last reel can stop. The jackpot is on that list once. One click short is on there over and over. So every time you spin, the machine is way more likely to stop one click short than on the jackpot.

### Script
- **Hook (0-4.48s, 15 words):** an in-the-moment, second-person near-miss ("You just watched…"). It puts the viewer in a familiar frustration rather than stating a claim.
- **Escalation:** it happens again at the next machine; a friend's quoted line in slang ("Bro, it's just warming up"); "another hundred"; then the narrator voices the viewer's suspicion: "But… teasing you on purpose."
- **Turn (16.44, 5 words):** "So let's crack it open." An inclusive "let's", followed by a 0.30s pause.
- **Reveal:** a contrast between "The jackpot is on that list once." (7 words) and "One click short is on there over and over." (9 words).
- **Ending:** "…way more likely to stop one click short than on the jackpot." "one click short" appears three times (hook, reveal, ending), and "jackpot" also opens the hook **(inference: a soft loop; restarting reads as "another spin")**.
- **Numbers:** the shortest script, 112 words. "So" is the main connective (×3). 218 WPM. Sentence lengths 15, 14, 17, 13, 5, 12, 7, 9, 20.

### Visual
- **Setting:** a casino row of red "LUCKY 7s" machines with marquee bulbs and gold trim, red stools, patterned carpet and warm ceiling downlights. Then the inside of the machine (the reel unit, a circuit board, wires, a paper list), then the machine shown as a cyan X-ray wireframe.
- **Palette:** oxblood #431914, lacquer red #a72b19, gold/cream #f7e088 / #e2c284, amber #d3893b, bronze #693a29, and the hero's teal shirt #30877a, echoed by the cyan wireframe.
- **Lighting:** warm practical marquee lights; faces glow red and warm from the machine (14.5s). It has the highest contrast (63.0) and saturation (153.6) of the five, with bright highlights (p95 234.7).
- **Depth of field:** used clearly in three places:
  - 8.3-11.3: a locked-off shot from inside the machine, with the reels blurred in the foreground, looking out at the buddy;
  - 12.3: the dollar bill going in, with the background soft;
  - 0-0.6: motion blur on the spinning reels.

| section | luma | contrast | sat | warm | vig |
|---|---|---|---|---|---|
| hook 0-4.5 | 92.6 | 68.5 | 162.3 | 64.4 | 49.2 |
| escalation 4.5-16.3 | 87.7 | 64.0 | 156.5 | 64.3 | 38.3 |
| turn 16.3-17.9 | 87.5 | 62.9 | 161.9 | 65.3 | 37.2 |
| reveal 17.9-25.7 | **156.5** | 54.5 | 155.1 | **113.0** | 44.3 |
| end 25.7-30.9 | 100.3 | 68.9 | 134.8 | 19.4 | 57.2 |

This is the opposite of "darker at the reveal". The inside of the machine is the brightest, warmest section (amber paper). Only the closing X-ray shot cools down.

### Camera and edit
- **13 JSON shots, ASL 2.38s** (plus an undetected ~9-frame dissolve at 18.0-18.27 into the machine's interior). 8 dissolves (3-27 frames) and 4 cuts.
- **The opening:** 0-0.67 is an extreme close-up of the reels pulling out. Then a 7.63s continuous pull-out (14.5%/s) from the hero to the row of machines and the rising jackpot ticker, which covers "move to the machine next door" in one move.
- **Middle beats:**
  - 8.3-11.3: genuinely static, the only locked-off shot of the batch (the view from inside the machine).
  - 13.67: a 0.17s insert of the "CREDITS 100" counter.
  - 13.83-16.47: a slow push-in on his face for "teasing you on purpose".
  - 16.83: push-in at 40%/s on "let's crack it open". He wrenches the front panel open like a door (17.6-17.9) and the camera goes into the reels.
- **The reveal:**
  - 17.53-25.8: an 8.3s push-in with a downward tilt that scrolls the "REEL 3: EVERY STOP" list as the narration says "over and over".
  - 25.6-25.9: **the paper strip curls into a pie wheel**: a huge red "ONE CLICK SHORT" slice and a tiny jackpot slice. The JSON logs this as a cut at 25.80.
  - The wheel then dissolves into the X-ray machine.
- **Ending:** 29.77, a cut on "than" and a fast pull-out back to the hero.
- **Sync:** 8.30 "Your buddy" (+0.12s), 16.47 "So let's" (-0.03), 25.80 "So every time" (-0.12).
- **On-screen elements:** "PLAY 3 CREDITS · 1 LINE · $1 GAME", pay tables, a progressive ticker "$1,284,5xx" counting up, a $100 bill, "SPIN", "CREDITS 100", the list "#1 BAR… #9 7 JACKPOT (highlighted gold)…", red "ONE CLICK SHORT" stamps filling the list while a tally counter runs x01→x14, "BILL VALIDATOR", "LUCKY 7s REEL UNIT", the wheel, and the cyan grid X-ray.

### Character animation
- The hero has messy black hair, a teal print shirt and a lanyard badge. His faces swap from a hopeful smile to suspicious to a flat glare ("purpose."), then gritted teeth on "crack it open".
- The buddy wears a red cap backwards, sunglasses on the cap and a gold chain. On the quoted line his mouth alternates between a toothy grin and closed every 3-6 frames (9.9-11.0s, `v19_strip_bro.jpg`). That is a rough lip-flap, not phoneme-accurate sync. It is the only dialogue mouth movement in the batch.

### Loop check
The last frame shows the hero beside a LUCKY 7s machine whose reels read 7-7-short. The first frame is an extreme close-up of the same reels spinning. They are thematically continuous but not a frame match, so this is a soft loop.

---

## 20: "The Scientist's Insane Time Test"
40.05s · 6,091,176 views · uploaded 2026-10-14 (the oldest of the five)

### Transcript
A scientist dropped people off a tower just to find out what happens to time right before you die. Apparently, when you're terrified, your brain speeds up so much that the whole world slows down. People who survive crashes swear everything went into slow motion. So before they fell, he strapped a little screen to each of their wrists that flashed numbers way too fast to read. If time really slowed down, they'd be able to read them as they were falling. When they landed, every one of them swore the fall took way longer than it really did. But when he asked them what number they saw, not one of them could tell him. You see, when you're frightened, your brain records way more detail than normal. So when you replay it later, it feels like it all happened in slow motion.

### Script
- **Hook (0-5.20s, 19 words):** a shock claim ("dropped people off a tower") with a curiosity gap ("what happens to time right before you die"). Third person, past tense, with a generic "you".
- **Belief setup:** "Apparently…" sets up the popular belief so it can be overturned. The social-proof line "People who survive crashes swear…" supports it.
- **Experiment:** a screen on each wrist, then the hypothesis as a conditional: "If time really slowed down, they'd be able to read them".
- **Result/turn:** a contrast between "every one of them swore…" and "But… not one of them could tell him." The "But" falls at 28.48s.
- **Reveal (31.98):** "You see," then the brain "records way more detail"; the ending ties back to the hook's "slow motion" for the third time.
- **Numbers:** the longest sentences of the five (mean 15.9; lengths 19, 16, 10, 22, 15, 17, 16, 13, 15). 217 WPM.
- **Context, not from the video:** the story appears to be based on David Eagleman's free-fall experiment; that identification comes from my own knowledge.

### Visual
- **Settings:**
  - a sunny Texas amusement park: an orange lattice "FREEFALL" tower, a "LONE STAR THRILLS" banner, a Ferris wheel, a coaster, a parking lot;
  - inside the head: a beige study with a rainbow rug, a bookshelf and porthole "eye" windows, where a pink brain character sits drawing at a desk;
  - a "CRASH SURVIVORS · TUESDAYS 7PM" support group, with a "DONUTS" sign and a US flag;
  - a slow-motion car crash with fries hanging in mid-air;
  - a blueprint;
  - a dim interview room with a pendant lamp and giant red balloon numbers "418073";
  - the red-alarm brain room;
  - a sunset backyard with string lights.
- **Palette:** cream #e8dfd4, warm grey #c3bdb0, tower orange #dd772f, sky/blueprint blue #3d87c9 / #234375, slate navy #344666, brown #7e4d3b, alarm red #d24428, sunset peach #d28e5f.
- **Lighting:**
  - The theory section is flat daylight: the brightest and least saturated of the batch, with a negative vignette (edges brighter).
  - The experiment section is cool blue (sky and blueprint).
  - The result section is a dark room with a warm pendant lamp.
  - The reveal brings a red alarm wash that kicks in exactly on "frightened" (32.77s), then golden-hour sunset light with string lights.
- **Effects:** bloom on the red LED matrix of the CHRONO-2 device. Shallow depth of field at 14.0 (a blurred face in the foreground) and 20.3 (the background behind the device).

| section | luma | contrast | sat | warm | vig |
|---|---|---|---|---|---|
| hook 0-5.3 | 164.7 | 63.7 | 86.2 | 32.9 | -10.4 |
| theory 5.3-14.4 | **173.6** | 57.4 | 70.7 | 30.9 | -10.8 |
| experiment 14.4-24.6 | 100.5 | 50.6 | 126.8 | **-29.6** | 3.4 |
| result 24.6-31.8 | 113.9 | 60.2 | 128.6 | 8.3 | 15.4 |
| reveal 31.8-40 | 148.9 | 56.4 | 110.5 | **65.5** | 23.2 |

The coolest part is the experiment; the reveal is warm and red.

### Camera and edit
- **18 shots, ASL 2.22s.** 15 dissolves (8-31 frames, median 12) and 2 cuts.
- **In-camera transitions** (the most inventive of the batch):
  - 6.9-7.5: **a push into the terrified man's pupil.** The eye's white fills the frame (luma +31 at 7.43) and the pupil opens onto the brain's study, on "your brain" (`v20_strip_eye.jpg`).
  - 23.70: **a hard cut to an empty safety net held for 6 frames.** The faller drops in on "When they landed" (luma +44; the JSON lists it as a static 0.2s shot).
  - 32.0-32.4: **a door opens in the man's face** and the camera flies through it into the brain room on "You see,". At 32.77 the room turns alarm-red on "frightened".
  - 32.7-35.2: a five-shot dissolve montage of roughly 0.5s shots in which the stacks of paper grow, on "records way more detail than normal".
  - 38.4-39.97: **a push into the stack of drawings he holds.** The pages flip like a flipbook, ending on a hand-drawn top-down view of the tower.
- **Other moves:** 0-2.93, a push-in at 52%/s tilting down to follow the fall, with his red cap flying off; 7.33, a roll of 9.5°/s in the brain room; 14.57-19.77, a 5.2s push-in on the scientist strapping on the device.
- **Sync:** 11.00 "People" (-0.04s), 14.57 "So before" (-0.05), 20.47 "If" (-0.03), 28.47 "But" (+0.01).
- **On-screen elements:** "FREEFALL", "LONE STAR THRILLS", "CRASH SURVIVORS TUESDAYS 7PM", "CHRONO-2" (an LED wrist display), a blueprint reading "HYPOTHESIS: TIME SLOWS → CAN READ #" and "PROJECT: TIME TEST / LONE STAR THRILLS – DALLAS TX / DWG NO. 7 / DRAWN: DR. K / DETAIL A: DISPLAY 47", "OFF NET", the "418073" balloon numbers, and a "NORMAL TUESDAY" sticky note.
- **(inference) The joke in the interview room:** the number they couldn't read is shown huge behind the people being asked about it.

### Character animation
- The faller's limbs flail and he rotates as he falls. His terrified face has target-ring eyes and grid teeth.
- The brain wears a green visor, sweats and scribbles frantically.
- After landing, the participants beam: a comic contrast with failing the test. In the line-up they look sheepish.
- The red-cap guy ends with a smug grin holding the flipbook, a dog beside him.

### Loop check: the strongest of the five
The final drawn page (39.2-39.97) shows the tower top from above, with the scientist and the red-cap participant. Frame 0 is nearly the same composition in 3D: the same two characters, the "FREEFALL" letters and the parking lot. "…it all happened in slow motion" carries straight into "A scientist dropped people off a tower…", so the replay becomes the restart. 0.5s of silence after the last word.

---

## Files
- **Report:** `C:/Users/JARVIS/Desktop/Claude-Vd/RicksClips3000/analysis/reports/videos_16-20.md`
- **Still stacks:** `analysis/stills/v16_stack.jpg`, `v16_stack2.jpg`, `v17_stack.jpg`, `v17_stack2.jpg`, `v18_stack.jpg`, `v18_stack2.jpg`, `v19_stack.jpg`, `v19_stack2.jpg`, `v20_stack.jpg`, `v20_stack2.jpg`
- **Loop strips** (last 1s + first 1s): `v16_loop.jpg` … `v20_loop.jpg`
- **Frame strips:**
  - 16: `v16_strip_daynight`, `_28`, `_9`, `_open`, `_39`
  - 17: `v17_strip_flash`, `_house`, `_open`, `_charge`
  - 18: `v18_strip_24`, `_30`, `_ballot`, `_hook`, `_counter`, `_1885`, `_8`
  - 19: `v19_strip_14`, `_open`, `_25`, `_bro`, `_crack`
  - 20: `v20_strip_eye`, `_23`, `_32`, `_end`
- **Grain check:** `v16-20_grain_crops.png`
