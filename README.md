# Claude-Video

Research into how the YouTube Shorts channel [@RicksClips3000](https://www.youtube.com/@RicksClips3000) makes its videos. The study covers the channel's 20 latest Shorts at the time (uploaded 2026-10-14 to 2026-11-04). It looks at scripts, lighting, colour, camera movement, editing, captions and audio, and is meant as groundwork for making original videos in a similar style.

## Contents

- **[RicksClips3000/STYLE_GUIDE.md](RicksClips3000/STYLE_GUIDE.md)**: start here. The full breakdown of how the videos are made.
- `RicksClips3000/analysis/transcripts_all.md`: all 20 transcripts with timestamps.
- `RicksClips3000/analysis/reports/`: per-video deep dives covering the script beats, colour per story section, shot-by-shot camera notes, effects, animation and loop checks.
- `RicksClips3000/analysis/channel_stats.json`: per-video numbers on pacing, hooks, shots, colour arcs and audio.
- `RicksClips3000/analysis/frames/`: per-frame stats for every frame of every video.
- `RicksClips3000/analysis/edit/`: detected transitions, camera moves, and contact sheets sampled every 0.5 s.
- `RicksClips3000/analysis/stills/`: stills and frame strips that the reports reference.
- `RicksClips3000/analysis/transcripts/`: word-level transcript timings.

## Source videos

The 20 source videos aren't in the repo, because they're third-party content and total about 720 MB. `RicksClips3000/videos/metadata.json` lists each video's title, upload date, views, likes and URL as of 2026-11-04. YouTube's captions for each video are kept alongside it. To re-download the exact analysed videos, with the same file names the analysis uses, run:

```sh
pip install -U yt-dlp
cd RicksClips3000/videos
for name in 01_HxqtHI62otM 02_7xS87iActkU 03_Mz72MuPgnGY 04_5WMQhPObNqQ 05_ZDy3xXA2iHk \
            06_LC8hYwUZ-kU 07_t3OXkhlI6NQ 08_DEe0iKH4KIw 09_GM9UKnZ6JFw 10_VKsamN3Fk4U \
            11_0m6G8pDtzNs 12_nzbkkEZFM8g 13_VS1Z_Q-Klt8 14_lnYLIWP2l-I 15_jpFJ8Z_F-qU \
            16_PLe2Gu3FDuA 17__sUAXTvJquk 18_eQR3pgMiUF0 19_CJwgTrfrHL0 20_hdhggSABEws; do
  id=${name#*_}
  yt-dlp -f "bv*[height<=1920][ext=mp4]+ba[ext=m4a]/b[ext=mp4]/b" --merge-output-format mp4 \
    -o "$name.%(ext)s" "https://www.youtube.com/shorts/$id"
done
```
