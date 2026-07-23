# Juzz 30 — Last 11 Surahs Learning System

A single-file, offline-friendly web app for studying and memorizing selected surahs from Juz 30 of the Qur'an — combining Arabic text, English translation, key-word breakdowns, Tajweed rules, and recitation audio by **Sheikh Mahmoud Khalil Al-Hussary**.

No build step, no server, no dependencies — it's one self-contained `.html` file that runs entirely in the browser.

## Features

- **14 surahs covered**: Al-Fatihah plus 13 surahs from Juz 30 (see table below)
- **Four learning modes** per surah: Understand, Key Words, Recite, Memorize
- **Key-word breakdowns**: important words in each ayah are highlighted in the Arabic text and tagged with English meaning + notes (root letters, frequency in the Qur'an, grammatical notes). Numbering follows the natural right-to-left reading order of the Arabic text, matched left-to-right in the English tag list below it.
- **Tajweed throughout**:
  - Every ayah is tagged with the Tajweed rules it contains
  - **"Tajweed in Ayah"** — a focused breakdown of just the rules present in that one verse, with the ayah's own text colour-coded per rule
  - **"Tajweed in Surah"** — a full breakdown of every rule found anywhere in the surah, with examples pulled from that surah
  - A global reference covering all 10 rules: Ghunnah, Izhaar, Idghaam, Iqlaab, Ikhfaa, Qalqalah, Madd, Tafkheem, Meem Sakinah, and Waqf
- **Surah Overview**: a Key Themes summary for every surah — the main ideas and message at a glance
- **Recitation audio**: play or download the Al-Hussary recitation for any individual ayah
- **Works offline**: all text, translations, and Tajweed data are embedded in the page — only audio playback requires an internet connection (streamed from everyayah.com)

## Surahs Included

| # | Surah | Meaning | Ayahs |
|---|-------|---------|-------|
| 1 | Al-Fatihah | The Opening | 7 |
| 78 | An-Naba | The Tidings | 40 |
| 79 | An-Nazi'at | Those Who Drag Forth | 46 |
| 80 | Abasa | He Frowned | 42 |
| 81 | At-Takwir | The Overthrowing | 29 |
| 82 | Al-Infitar | The Cleaving | 19 |
| 83 | Al-Mutaffifin | The Defrauders | 36 |
| 85 | Al-Burooj | The Great Stars | 22 |
| 86 | At-Tariq | The Morning Star | 17 |
| 87 | Al-A'la | The Most High | 19 |
| 88 | Al-Ghashiyah | The Overwhelming | 26 |
| 89 | Al-Fajr | The Dawn | 30 |
| 92 | Al-Lail | The Night | 21 |
| 96 | Al-Alaq | The Clinging Clot | 19 |

## Getting Started

### Option 1 — Just open it
Download `juzz30_learning_system_12.html` and open it directly in any modern browser (Chrome, Safari, Firefox, Edge). That's it.

### Option 2 — Host it with GitHub Pages
1. Rename the file to `index.html`
2. Push it to a GitHub repository
3. Go to **Settings → Pages**, and set the source to your main branch
4. Your app will be live at `https://<your-username>.github.io/<repo-name>/`

## Attribution

- Recitation audio: Sheikh Mahmoud Khalil Al-Hussary, streamed from [everyayah.com](https://everyayah.com)
- Arabic text, translations, and Tajweed annotations compiled for educational use

## Notes

- This is a static, front-end-only project — no data is collected, and nothing is sent to any server other than the audio requests to everyayah.com.
- Contributions, corrections, and additional surahs are welcome — feel free to open an issue or pull request.
