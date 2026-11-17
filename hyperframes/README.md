# Plan G vs Plan N vs High-Deductible G (2027): HyperFrames composition

16:9 at 1920×1080. The Arric Allen A-roll fills the left 900 px and the motion graphics play on the right stage. Every cue is timed to the word timestamps of the final HeyGen voiceover, which runs **4:10.24**. The script's estimated 5:25 is not used.

```
index.html                 root: A-roll + chapter rail + 7 scene hosts (250.24 s)
compositions/chapters.html brand strip, "Now comparing" badge, 5 progress-fill chapter bars
compositions/s1-hook.html       cost-over-time two-line graph → authority card
compositions/s2-shared.html     U.S. map lights up + "Any Medicare doctor" stamp
compositions/s3-dashboard.html  3-dial dashboard: premium gauge, predictability lock/coins, break-even scale (Plan G + Plan N)
compositions/s5-hdg.html        deductible bucket meter, annual premium bars, worst-case ceiling chart
compositions/s6-myth.html       comfort check, myth/fact, teaser-rate trap curve
compositions/s7-cta.html        3-point scorecard triangle → Medicare.gov + Allen & Associates card
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
| 3+4 Plan G vs N dashboard | 1:10–2:38 | 1:09.8–2:12.3 |
| 5 High-Ded G + MA | 2:38–3:42 | 2:12.3–2:58.9 |
| 6 Carrier Myth | 3:42–4:42 | 2:58.9–3:38.4 |
| 7 Checklist & CTA | 4:42–5:25 | 3:38.4–4:10.24 |

## Audio mix (built in)

- **Voice:** A-roll audio, normalized from -28.8 to **-16 LUFS** (`assets/audio/vo-normalized.m4a`). The A-roll `<video>` is muted.
- **Music:** `assets/audio/music-bed.mp3`, ElevenLabs instrumental (soft piano and acoustic guitar, no drums or vocals). It plays at -23 dB, about 24 dB under the voice, with a 2 s fade-in and a short lift after the last word.
- **Sound effects:** 14 soft cues on one lane, peaking 12–16 dB below the voice. The negation buzzer, music hard stop, dial-tone ticks, triple pops and ratchet ticks from the original script were cut on purpose for a 65+ audience.
- **Final mix:** -16 LUFS integrated, -1 dBFS peak. Levels were measured, not listened to.

| Start | File | Gain | Cue |
|---|---|---|---|
| 0:19.62 | `sfx-whoosh1.mp3` | -12.7 dB | Authority card slides in |
| 0:38.46 | `sfx-whoosh2.mp3` | -17.1 dB | Chapter 1: Shared Freedom |
| 1:01.29 | `sfx-unlock.mp3` | -12.3 dB | Padlock springs open ("zero referrals") |
| 1:09.87 | `sfx-whoosh1.mp3` | -12.7 dB | Chapter 2: Plan G vs N |
| 1:24.72 | `sfx-lock.mp3` | -16.1 dB | Plan G padlock snaps shut ("100%") |
| 2:09.19 | `sfx-thunk.mp3` | -12.6 dB | Break-even scale tips to Plan N |
| 2:12.31 | `sfx-whoosh2.mp3` | -17.1 dB | Chapter 3: High-Deductible G |
| 2:24.94 | `sfx-pour.mp3` | -7.0 dB | Deductible bucket fills |
| 3:07.54 | `sfx-whoosh1.mp3` | -12.7 dB | Chapter 4: Carrier Myth |
| 3:21.88 | `sfx-stamp.mp3` | -0.4 dB | "NOT" stamp |
| 3:34.75 | `sfx-wall.mp3` | +3.4 dB | Underwriting wall drops |
| 3:38.41 | `sfx-whoosh2.mp3` | -17.1 dB | Chapter 5: Action Plan |
| 4:02.68 | `sfx-click.mp3` | -9.3 dB | Phone number appears |
| 4:07.98 | `sfx-click.mp3` | -6.3 dB | Cursor clicks website |
