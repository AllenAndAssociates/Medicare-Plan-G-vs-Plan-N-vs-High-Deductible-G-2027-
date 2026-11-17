# Plan G vs Plan N vs High-Deductible G (2027): HyperFrames composition

16:9 at 1920×1080. The Arric Allen A-roll fills the left 900 px and the motion graphics play on the right stage. Every cue is timed to the word timestamps of the final HeyGen voiceover, which runs **4:10.24**. The script's estimated 5:25 is not used.

```
index.html                 root: A-roll + chapter rail + 7 scene hosts (250.24 s)
compositions/chapters.html brand strip + 5 chapter tabs
compositions/s1-hook.html … s7-cta.html
assets/arric-aroll.mp4     A-roll re-encoded with 1 s keyframes (required for frame-accurate seeking)
```

Preview, check and render it with the HyperFrames CLI. Run each command from this folder:

```bash
npx hyperframes check --json
```

```bash
npx hyperframes preview
```

```bash
npx hyperframes render --quality delivery -o out.mp4
```

Editable variables: `phone`, `site` and `disclaimer` are in s7. `brandName`, `gold` and `navy` are on the root.
Logo: `assets/aa-logo.png` appears on a white plate in the s1 authority card and the s7 end card.

## Scene timing (actual VO)

| Scene | Script est. | Actual |
|---|---|---|
| 1 Hook & Authority | 0:00–0:34 | 0:00.0–0:38.4 |
| 2 Shared Freedom | 0:34–1:10 | 0:38.4–1:09.8 |
| 3 Plan G | 1:10–1:48 | 1:09.8–1:39.6 |
| 4 Plan N | 1:48–2:38 | 1:39.6–2:12.3 |
| 5 High-Ded G + MA | 2:38–3:42 | 2:12.3–2:58.9 |
| 6 Carrier Myth | 3:42–4:42 | 2:58.9–3:38.4 |
| 7 Checklist & CTA | 4:42–5:25 | 3:38.4–4:10.24 |

## SFX cue sheet (re-timed to the actual VO, for the audio pass)

No sound effects are baked into the composition. Drop these on one SFX lane, with each peak landing about one frame after its visual.

| Time | Cue | Trigger word / visual |
|---|---|---|
| 0:00.3 | Soft UI pop | Hook card 1 |
| 0:10.4 | Soft UI pop | Hook card 2 ("Or what if") |
| 0:19.6 | Whoosh | Authority card ("I am Arric Allen") |
| 0:29.6 / 0:30.9 / 0:32.0 | 3 quick pops | Plan G / Plan N / High-Ded G chips |
| 0:43.1 / 0:54.6 / 0:59.9 | Checkmark ding ×3 | Shared-benefit rows |
| 1:04.1 | Highlighter swipe | "Same Doctor Freedom" |
| 1:10.6 | Card pop | Plan G column |
| 1:24.4 | Padlock click + green chime | "100%" Part A & B |
| 1:51.7 / 1:54.3 / 1:59.6 | Ascending pops ×3 | $20 / $50 / excess charges |
| 2:05.4 | Warm double-chime | Pro-tip banner |
| 2:09.4 | Highlighter swipe | "$60–$100" |
| 2:16.0–2:17.2 | Ratchet ticks | Counter to $3,050 |
| 2:40.2 | Cash/price-tag chime | "Save $1,500/yr" |
| 2:46.7 / 2:49.3 | UI pops | MA $300 / $6–7k limit |
| 2:51.9–2:52.2 | UI pop | HDG $3,050 ceiling |
| 2:58.9 | MUSIC HARD STOP + warning double-chime | "However…" |
| 3:09.5 | Negation buzzer | MYTH card |
| 3:18.0 | (strike-through) | "While the plan letters…" |
| 3:22.0 | Rubber-stamp thud | "NOT" |
| 3:23.0 | Groove resumes softly | Flowchart |
| 3:34.4 | Padlock click | Medical underwriting |
| 3:43.0 / 3:44.6 / 3:47.2 | Ascending pops 1-2-3 | Checklist |
| 3:49.9 | Music swells to −22 dB + pop | Medicare.gov |
| 4:02.8 | Dial-tone ticks (−22 dB) | Phone number |
| 4:07.2 / 4:08.2 | Pop + mouse click | Website + cursor click |
| 4:10.2 | Resolving chord | End |
