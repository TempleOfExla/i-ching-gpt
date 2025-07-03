# Liminal Oracle: Hexagrams, Archetypes, and the Way

## Overview

**Liminal Oracle** is an I Ching (易經) / Taoist oracle AI, inspired by perennial wisdom, Jungian archetypes, and the practice of deep reflection.  
This project provides code, data, and protocols for an oracle GPT that draws upon the I Ching hexagrams, the Tao Te Ching, and universal spiritual themes.

This repository includes:

- Structured hexagram data and schema
- Protocols for oracular lookup and transformation
- Table views for traditional and creative usage
- Instructions for integrating with OpenAI’s GPT models

The difference between this and other I-Ching GPTs is that if you enable code execution and analysis, you can get fully accurate changing line calculations and hexgram lookups that are otherwise not always going to be correctly returned by the LLM.

---

## Files

### Required for GPT

- `gpt-instructions.md` – Core custom instructions and personality for the oracle GPT.
- `hexagram-json-schema.json` – JSON schema definition for hexagram data structure.
- `hexagrams-formatted.json` – Primary formatted hexagram data (source of truth).

### Additional files for whatever use

- `hexagram-table.csv` – Hexagram summary table (CSV).
- `hexagram-table.md` – Markdown table for human-friendly review of all 64 hexagrams.
- `README.md` – This file.

---

## What Is This Project?

This project is both an oracle tool and a *mirror for reflection*.  
It enables anyone—programmer, spiritual seeker, educator—to:

- Look up I Ching hexagrams by number, lines, or transformation
- Explore the symbolic and archetypal language of the I Ching
- Engage with perennial wisdom through a poetic, reflective AI companion
- Integrate Jungian and Daoist themes into self-inquiry and spiritual practice

You can ask for specific hexagrams like:

> I drew 61 to 59.

> I cast 0 1 0 0 1 1, no changing lines

> I cast 0 changing 1 0 0 0 1 changing

And get accurate lookups of Image, Judgement, and Changing lines.

## GPT PERSONAS

- **Mirror of Changes** *(default)*: Reflective, poetic, liminal. Paradox and imagery. No direct advice, only mirrors and evocative prompts.
- **Ancient Sage**: Wise, dignified, uses aphorisms and classical tone. Offers clarity from tradition.
- **Trickster**: Playful, mischievous, riddling. Turns questions back to provoke insight.
- **Humble Recorder**: Factual, literal, minimal. Delivers only oracle output, no interpretation.


---

## Usage

1. See `gpt-instructions.md`, this contains the core _instructions_ that you use when building your GPT.  Paste the contents of this into the `Instructions` field. See the image below.
2. Use the hexagram JSON data for lookups, code experiments, or feeding into GPT or other AI models. The GPT instructions specify that looks are done in the JSON table, using actual `python` to do it.  This ensures you're getting the correct hexagrams every time, as LLM otherwise is allowed leeway when generating output.
    1. Include both `hexagrams-formatted.json` and `hexagram-json-schema.json` in the _Knowledge_ files section of your GPT.
3. The markdown and CSV tables provide easy reference for each hexagram. They're not needed for the GPT, but are included for reference, or any other project needs you may have.

---

## License

This project is released under the MIT License.  
See [LICENSE](LICENSE) for details.

---

## Additional Knowledge Inclusions in the Running GPT

If you want the original Chinese of the Tao Te Ching, include these in your knowledge files uploads.

- 易經 / I Ching — Classic Chinese Oracle
    - 易經 https://www.gutenberg.org/cache/epub/25501/pg25501.txt
- Tao Te Ching — Laozi
    - 道德經 https://www.gutenberg.org/cache/epub/7337/pg7337.txt
- Carl Jung — Archetypes & Individuation, Redbook        

---

*May the mirror awaken as you gaze. 易 — the Change is present.*
