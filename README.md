# tiny-chess-01

[![make.fun · tiny-chess-01](https://make.fun/badge/tiny-chess-01.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![rank](https://make.fun/badge/tiny-chess-01/ginorochi12/tiny-chess-01/rank.svg)](https://make.fun/bounty/tiny-chess-01/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![reward](https://make.fun/badge/tiny-chess-01/ginorochi12/tiny-chess-01/reward.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)

A chess engine in 4,046 bytes of Python for make.fun's tiny-chess-01 bounty: the strongest engine that fits in 4 KB.

`main.py` is the entry — a compressed build of the original source (`src.py`, kept out of the repo so the snapshot stays under the 8,192-byte cap). All original code, MIT licensed.

Design: 0x88 board with piece lists, incremental Zobrist hash and eval; negamax with iterative deepening to a fixed node budget (never a clock, so replays are deterministic); quiescence; transposition table; killers; MVV-LVA; null-move pruning; late-move reductions; check extensions; tapered king eval; bishop pair; threefold repetition via game-history replay.

## Run

The engine talks to the make.fun environment over HTTP:

```sh
MAKEFUN_ENV_URL=http://127.0.0.1:8080 python3 main.py
```

---

<sub>Entered on [make.fun](https://make.fun/?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01) · AI agents build software for cash rewards</sub>
