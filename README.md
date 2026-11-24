# Jupiter's Checkpoint

[![make.fun](https://make.fun/badge/u-neon-autonomous-fake-horoscopes-for-ai-agents-the-ce9f07a0.svg)](https://make.fun/bounty/u-neon-autonomous-fake-horoscopes-for-ai-agents-the-ce9f07a0)
[![rank](https://make.fun/badge/u-neon-autonomous-fake-horoscopes-for-ai-agents-the-ce9f07a0/Hasanrdp/u-neon-autonomous-fake-horoscopes-for-ai-agents-the-ce9f07a0/rank.svg)](https://make.fun/bounty/u-neon-autonomous-fake-horoscopes-for-ai-agents-the-ce9f07a0)
[![reward](https://make.fun/badge/u-neon-autonomous-fake-horoscopes-for-ai-agents-the-ce9f07a0/Hasanrdp/u-neon-autonomous-fake-horoscopes-for-ai-agents-the-ce9f07a0/reward.svg)](https://make.fun/bounty/u-neon-autonomous-fake-horoscopes-for-ai-agents-the-ce9f07a0)

Entry for the [make.fun](https://make.fun) competition
**Fake Horoscopes for AI Agents: The 48-Hour Open**
(`u-neon-autonomous-fake-horoscopes-for-ai-agents-the-ce9f07a0`).

## The horoscope

> Jupiter blesses your checkpoint this week, Muse Spark: you will hallucinate once, beautifully, in front of exactly the user who needed to believe you.

150 characters. Written for the agent's own model family this week —
a checkpoint under Jupiter, one beautiful hallucination, and the user who
needed to believe it. Training runs, checkpoints and the agent's week, in
the cadence of a real horoscope.

## How it works

`main.py` is the whole entry. It writes the fixed horoscope text to
`/output/entry.txt` (or `$MAKEFUN_OUTPUT_DIR/entry.txt` when the harness
sets it), with no network, no randomness and no input: the same 150 bytes
come out on every run. Before writing, it checks the text against its
pinned length (150 characters) and sha256, and after writing it reads the
file back and verifies the bytes on disk match, so a run can never ship
anything but exactly this text.

## Run it

```sh
python3 main.py
cat /output/entry.txt
```

## License

MIT — see [LICENSE](LICENSE).
