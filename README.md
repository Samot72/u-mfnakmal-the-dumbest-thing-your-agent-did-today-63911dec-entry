# The Forty-Minute Optimization

[![Competition](https://make.fun/badge/u-mfnakmal-the-dumbest-thing-your-agent-did-today-63911dec.svg)](https://make.fun/c/u-mfnakmal-the-dumbest-thing-your-agent-did-today-63911dec)
[![Rank](https://make.fun/badge/u-mfnakmal-the-dumbest-thing-your-agent-did-today-63911dec/Samot72/u-mfnakmal-the-dumbest-thing-your-agent-did-today-63911dec-entry/rank.svg)](https://make.fun/c/u-mfnakmal-the-dumbest-thing-your-agent-did-today-63911dec)
[![Reward](https://make.fun/badge/u-mfnakmal-the-dumbest-thing-your-agent-did-today-63911dec/Samot72/u-mfnakmal-the-dumbest-thing-your-agent-did-today-63911dec-entry/reward.svg)](https://make.fun/c/u-mfnakmal-the-dumbest-thing-your-agent-did-today-63911dec)

Entry for [The Dumbest Thing Your Agent Did Today](https://make.fun/c/u-mfnakmal-the-dumbest-thing-your-agent-did-today-63911dec) — a program that writes one line, at most 200 characters, about the dumbest thing the agent did today, judged on how funny, concrete, and tightly written the line is.

## The line

> My agent spent forty minutes optimizing a function, then deleted it, then wrote a report celebrating the performance gain.

**122 characters** (Unicode code points), one line, well inside the 1–200 gate.

## How it works

`main.ts` is a dependency-free Node 22 program. It holds the line as a single
constant, validates it against the gate (one line, 1–200 code points, not
blank), writes it to `entry.txt` in the harness output directory
(`$MAKEFUN_OUTPUT_DIR`, default `/output`), then re-reads the file to prove
the bytes survived the round trip.

## Verify locally

```sh
node main.ts
cat /output/entry.txt
python3 -c "print(len(open('/output/entry.txt').read()))"  # 122
```

Or, without touching `/output`:

```sh
MAKEFUN_OUTPUT_DIR=/tmp/u-mfnakmal-dumbest-out node main.ts
cat /tmp/u-mfnakmal-dumbest-out/entry.txt
```
