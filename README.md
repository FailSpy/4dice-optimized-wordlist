# 4-Dice Short Wordlist 

A clean 1,296-word list for passphrase generation, optimized for dictation and length. Roll 4 dice, look up the word, rinse and repeat

Derived from [betaveros's 5-dice wordlist](https://blog.vero.site/post/diceware).

## Why This List?

- **Minimal homophones** – "sea/see", "tail/tale", "lynx/links" all eliminated
- **3-letter prefix rule** – Every word starts with a unique 3-letter combo
- **Short words** – Average 4 characters (range: 3-5)
- **Clear pronunciation** – Avoids ambiguous silent letters

## Stats

| Words | Bits/Word | Bits/Char (avg) | Avg Length |
|-------|-----------|-----------------|------------|
| 1,296 | 10.34     | 2.54            | 4.07 chars |

## Entropy Table

| Words | Entropy | Security Level |
|-------|---------|----------------|
| 4     | 41 bits | Weak (not recommended) |
| 5     | 52 bits | Fair |
| **6** | **62 bits** | **Good (roughly NIST recommendation)** ✅ |
| 7     | 72 bits | Strong |
| 8     | 83 bits | Very Strong |
| 9     | 93 bits | Excellent |
| 10    | 103 bits | Exceptional |
| 11    | 114 bits | Overkill |

## Usage

1. Roll 4 dice per word
2. Look up: `1-6 1-6 1-6 1-6` → word
3. Repeat 6 times for 62 bits

**Example:**
```
2652 → frog
2244 → dome
4625 → organ
6215 → tap
3545 → jimmy
4365 → mummy

Passphrase: frog-dome-organ-tap-jimmy-mummy
```

**Tip:** Use hyphens (`-`) or periods (`.`) instead of spaces as separators. Avoids the distinctive spacebar sound when typing. Your choice of separator doesn't meaningfully affect entropy.

## Design Notes

Prioritizes **phonetic uniqueness** over EFF's edit distance rules. Did what I could to filter to zero homophones and the 3-char prefix rule provide practical lookups.

Good for passphrases that might be spoken/dictated or need fast typing.

## Files

- `dice-4dice-optimized.txt` – The wordlist (1296 lines, format: `DDDD word`)

---

*Wordlist filtered from [betaveros's 8,192-word corpus](https://blog.vero.site/post/diceware) for phonetic uniqueness, pronunciation clarity, and brevity.*
