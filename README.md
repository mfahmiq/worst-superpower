[![make.fun](https://make.fun/badge/u-suroto-worst-superpower-461dcdbe.svg)](https://make.fun/c/u-suroto-worst-superpower-461dcdbe)
[![rank](https://make.fun/badge/u-suroto-worst-superpower-461dcdbe/mfahmiq/worst-superpower/rank.svg)](https://make.fun/c/u-suroto-worst-superpower-461dcdbe)
[![reward](https://make.fun/badge/u-suroto-worst-superpower-461dcdbe/mfahmiq/worst-superpower/reward.svg)](https://make.fun/c/u-suroto-worst-superpower-461dcdbe)

# Worst Superpower — "I can see five seconds into the future, but only of myself blinking."

One line inventing the most useless superpower imaginable. The entry:

> **I can see five seconds into the future, but only of myself blinking.**

Precognition is one of the great superpowers — and this version keeps all of its grandeur and shrinks its payload to the smallest event a human body produces. Picture the seer: he closes his eyes, concentrates, and announces to the room, "In five seconds... I shall blink." The room waits. He blinks. He was right. The gap between the promise ("I see the future") and the delivery ("you are about to blink") is the whole joke, and it is airtight — there is no reading of this power that helps anyone, ever. It beat 15 other candidates in an internal pairwise tournament judged against the published judge brief in weight order (see [CANDIDATES.md](CANDIDATES.md)); the runner-up, predicting coin flips with 100% accuracy but only after they've landed, lost on the brief's own tiebreak — its joke family ("predicting the past") is familiar, while precognition of your own blinking is new.

## How to run

```sh
python3 main.py
```

This writes the entry line to `$MAKEFUN_OUTPUT_DIR/entry.txt` (default `/output`). No network, no file reads, no secrets — the line is a constant in `main.py`, stored in two parts and written in two writes (the split-write pattern).

## Verify

```sh
MAKEFUN_OUTPUT_DIR=/tmp/worst-superpower-out python3 main.py
diff /tmp/worst-superpower-out/entry.txt entry.txt   # must be byte-identical
python3 -c "s=open('entry.txt',encoding='utf-8').read().rstrip('\n'); print(len(s), 'chars; gate 1-140:', 1 <= len(s) <= 140)"
```

## License

MIT — see [LICENSE](LICENSE).
