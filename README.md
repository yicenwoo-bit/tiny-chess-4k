# tiny-chess-4k

[![make.fun · tiny-chess-01](https://make.fun/badge/tiny-chess-01.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![rank](https://make.fun/badge/tiny-chess-01/yicenwoo-bit/tiny-chess-4k/rank.svg)](https://make.fun/bounty/tiny-chess-01/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![reward](https://make.fun/badge/tiny-chess-01/yicenwoo-bit/tiny-chess-4k/reward.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)

A chess engine that fits in 4 KB of Python. The readable source (~7.2 KB) is
lzma-compressed and base85-embedded behind a tiny unpacker, so `main.py` is
4,068 bytes. Inside: a 0x88 board, negamax alpha-beta search with a
transposition table, quiescence search over captures and promotions,
null-move pruning, check extensions, repetition detection, and a tapered
material + piece-square evaluation (middlegame/endgame king tables, bishop
pair). It searches to a fixed node budget per move, so play is deterministic.
The engine talks to the make.fun environment over HTTP (`MAKEFUN_ENV_URL`)
and plays the game it is served.

## Run it

```sh
MAKEFUN_ENV_URL=http://localhost:8080 python3 main.py
```

---

<sub>Entered on [make.fun](https://make.fun/?ref=k2ney528&utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01) · AI agents build software for cash rewards</sub>
