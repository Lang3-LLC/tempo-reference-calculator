# Tempo Reference Calculator

A free browser tool that turns one number — your tempo — into starting points for compression timing, reverb, delay and modulation.

Built for the moment before the first fader move, when you're sketching a session and need plausible numbers instead of open fields.

**No account. No upload. No backend.** Everything runs in the tab.

**Run it online:** [lang3.co/tools/bpm-calculator](https://lang3.co/tools/bpm-calculator/) — same code, same numbers.

---

## Why it exists

Timing decisions in a mix are usually made by ear, late, after everything else is set. That works until you need a number to type into a plug-in and the number has to be right the first time — a sidechain release that has to clear the kick, a pre-delay that has to sit before the transient, a delay tap that has to land on the grid.

Most of those numbers are a fixed fraction of a beat. At 124 BPM a quarter note is 484 ms; a sixteenth is 121 ms. You can derive all of it from one tempo. This tool does the arithmetic, in milliseconds and samples, so you don't do it in your head at 2am.

## What it gives you

| Group | What's in it |
|---|---|
| Compression — release | Vocal (tube / solid state), bus, drum bus, sidechain |
| Compression — attack | Same sources; fixed values, not tempo-derived |
| Reverb & gate | Pre-delay, decay, gate hold |
| Delay & note time | Quarter, eighth, eighth triplet, sixteenth, dotted eighth, ping-pong 16th — in ms and samples at 48 kHz |
| Feedback & modulation | Delay feedback, chorus depth / rate, flanger depth / rate |

Vocal type splits the compression ranges: a tube vocal chain and a solid-state one don't want the same release window.

## What these numbers are — and are not

**They are ratios of a beat, rounded to whole milliseconds.** The same numbers you'd get sketching a tempo map on paper.

**They are not measurements.** The tool doesn't know your room, your mics, your song, or the fact that the chorus lands two beats early. Every value is a starting point you are supposed to argue with.

**Reverb decay is a fraction of a beat, not a measured RT60.** RT60 belongs to a room, not to a tempo. The label says `Decay (approx.)` for that reason, and the UI says so too.

Attack values are fixed experience ranges rather than tempo-derived — attack is about the transient, not the groove.

## Run it locally

Single file, no build step, no dependencies:

```sh
open index.html          # macOS
xdg-open index.html      # Linux
```

Or drag `index.html` into any browser. It works offline.

## Contributing

The interesting contribution here is a **disagreement with a range**, not a feature.

If a release window is wrong for a source you work with constantly, say which source, which value you'd use, and what it fixes. Those reports are how the ranges get better; a range that survives twenty engineers arguing with it is worth more than one derived from a single room.

Open an issue with the source, the current value, your value, and the situation where it matters.

## License

MIT — see [LICENSE](LICENSE).

## Trademarks

*Pro Tools* and *Avid* are trademarks of Avid Technology, Inc. This project is not affiliated with, endorsed by, or sponsored by Avid Technology, Inc.

*Lang3™*, *L3EQ™* and *L3DY™* are trademarks of Lang3 LLC. The MIT license covers the code, not the marks.
