# roman-urdu-nlp

NLP toolkit for **Roman Urdu** (Urdish) — the Latin-script Urdu that hundreds of millions of people actually type every day on WhatsApp, Facebook and YouTube comments.

Urdu NLP tooling overwhelmingly assumes Nastaliq script, yet most real-world Urdu text is written in Roman script with wildly inconsistent spelling (`acha` / `accha` / `achha` / `achchha` are all the same word). This library handles that gap.

## Features

- **Normalization** — collapse spelling chaos into canonical forms (`"kya haal haiii"` → `"kya haal hai"`)
- **Tokenization** — simple, punctuation-aware tokenizer tuned for casual text (emoji, mixed English/Urdu)
- **Stopwords** — curated Roman Urdu stopword list (~150 words)
- **Sentiment** — lexicon-based polarity scoring with negation handling
- **Transliteration** *(roadmap)* — Roman Urdu ↔ Urdu script

## Quick start

```python
from roman_urdu_nlp import normalize, tokenize

normalize("Kyaaa haal haiii bhaaai??")   # "kya haal hai bhai"
tokenize("yaar ye kya kar diya :(")       # ["yaar", "ye", "kya", "kar", "diya", ":("]
```

## Installation

```
pip install roman-urdu-nlp
```

## Why this exists

- ~350M+ Urdu speakers, most of whom type in Roman script
- Existing Urdu NLP resources target Arabic-script Urdu and choke on Roman text
- No maintained, pip-installable Roman Urdu toolkit existed — this fills that gap

## Roadmap

- [x] v0.1 — normalizer + tokenizer + stopwords
- [ ] v0.2 — sentiment lexicon & scorer
- [ ] v0.3 — transliteration (Roman ↔ Urdu script)
- [ ] v0.4 — language detection (Roman Urdu vs English vs Hinglish)

## License

MIT
