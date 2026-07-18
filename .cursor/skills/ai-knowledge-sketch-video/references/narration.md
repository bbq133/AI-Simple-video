# Natural Chinese Narration

## Writing

Write for speech, not for reading:

- one short claim per breath;
- varied sentence length;
- concrete verbs;
- no stacked definitions;
- no repetitive transition filler.

Prefer:

> 先问清帮谁、解决什么问题。场景清楚了，再谈能力，最后才是体验。

Avoid:

> 首先，我们需要明确目标用户，其次，我们需要明确用户需求，然后……

## Pronunciation glossary

Maintain a manifest entry for terms that TTS may misread:

```json
{
  "display": "AI",
  "spoken": "人工智能",
  "reason": "Do not pronounce as English letters"
}
```

The displayed script and spoken script may differ only for pronunciation clarity. Record both.

## Voice selection

Generate 2–3 first-line candidates before the full set:

- warm/conversational;
- slightly lively;
- calm/professional.

Do not assume a voice labeled “warm” sounds natural. The user’s ear is the acceptance gate.

## Timing

Generate one WAV per scene and bridge. Measure with `ffprobe`.

Suggested timing:

- speech starts 0.3–0.5 s after scene begins;
- visual component appears within ±0.25 s of its spoken phrase;
- scene holds 0.7–1.2 s after the final word;
- final scene holds 1.5–2.5 s.

If speech is too slow:

1. choose a more conversational voice;
2. tighten the text and punctuation;
3. increase TTS rate moderately;
4. regenerate and measure;
5. rebuild picture timing.

Do not simply time-compress a mechanical take.

## Audio output

- mono 48 kHz WAV per line;
- normalize narration near -16 LUFS;
- true peak at or below -1.5 dB;
- keep raw and selected takes separate;
- disclose that narration is AI-generated.
