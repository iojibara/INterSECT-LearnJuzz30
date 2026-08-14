# Juzz 30 — Complete Learning System

A single-file, offline-friendly web app for studying, reciting, memorizing, and understanding **all of Juz 30** — every one of its 37 surahs, plus Al-Fatihah — combining Arabic text, English translation, key-word breakdowns, Tajweed rules, Tafsir Ibn Kathir summaries, and recitation audio by **Sheikh Ibrahim Akhdar**.

No build step, no server, no dependencies — it's one self-contained `.html` file that runs entirely in the browser. An optional backend microservice can be connected for full tajweed-rule assessment (see below).

## Features

- **38 surahs, 571 ayahs** — the complete Juz 30 (surahs 78–114) plus Al-Fatihah  
- **Four learning modes** per surah: Understand, Key Words, Recite, Memorize  
- **Key-word breakdowns** on every ayah (1,919 entries total):  
  - Contextual, hand-written notes on the pedagogically important words in each verse (root letters, grammatical notes, nuance)  
  - Plus **supplementary high-frequency vocabulary entries** sourced from a Quranic word-frequency corpus, showing how often each word appears across the whole Quran and its part of speech — giving a sense of which words are worth memorizing first  
  - Numbering follows the natural right-to-left reading order of the Arabic text, matched left-to-right in the English tag list below it  
- **Tajweed throughout**:  
  - Every ayah is tagged with the Tajweed rules it contains (10 rules: Ghunnah, Izhaar, Idghaam, Iqlaab, Ikhfaa, Qalqalah, Madd, Tafkheem, Meem Sakinah, Waqf)  
  - **"Tajweed in Ayah"** — a focused breakdown of just the rules in that one verse, with the ayah's own text colour-coded per rule  
  - **"Tajweed in Surah"** — a full breakdown of every rule found anywhere in the surah, with examples from that surah  
  - A global reference modal covering all 10 rules in depth  
- **Tafsir of Surah** *(new)* — a paginated summary of Tafsir Ibn Kathir for every one of the 38 surahs:  
  - Broken into a handful of pages per surah (3 to 11, always an odd number), sized to how much genuine commentary a surah actually has rather than to its length — a 4-ayah surah like Al-Ikhlas gets 7 pages given its outsized theological weight, while some 20+ ayah surahs get 5  
  - Each page covers a specific ayah range with a title, the summarized commentary, and — where relevant — a note flagging historical context or a scholarly caveat (e.g. hadith authenticity, variant readings)  
  - Navigate with **Next / Back** buttons or the page dots  
  - This is a careful summary in plain English, not a verbatim translation of any published edition — it preserves Ibn Kathir's actual interpretive points (which hadith he cites, where he flags scholarly disagreement) without the full chains of narration of the complete work. For serious study or teaching, cross-check against the original.  
- **Surah Overview**: a Key Themes summary for every surah — the main ideas and message at a glance  
- **Recitation audio**: play any individual ayah, or hit **Play All** to recite an entire surah start to finish with the view auto-scrolling to follow along  
- **Record & Rate**: record your own recitation and get feedback —  
  - Always available: an on-device rhythm/timing comparison against the reference recitation (no server required)  
  - Optional: connect a backend microservice (see `TAJWEED_API_BASE` below) for full per-rule tajweed correctness scoring (madd length, qalqalah, etc.)  
- **Works offline**: all text, translations, Tajweed data, and Tafsir content are embedded in the page — only audio playback (and the optional Record & Rate backend) need an internet connection

## Surahs Included

| \# | Surah | Meaning | Ayahs | Tafsir Pages | Type |
| :---- | :---- | :---- | :---- | :---- | :---- |
| 1 | Al-Fatihah | The Opening | 7 | 7 | Meccan |
| 78 | An-Naba | The Tidings | 40 | 9 | Meccan |
| 79 | An-Nazi'at | Those Who Drag Forth | 46 | 9 | Meccan |
| 80 | Abasa | He Frowned | 42 | 9 | Meccan |
| 81 | At-Takwir | The Overthrowing | 29 | 7 | Meccan |
| 82 | Al-Infitar | The Cleaving | 19 | 5 | Meccan |
| 83 | Al-Mutaffifin | The Defrauders | 36 | 7 | Meccan |
| 84 | Al-Inshiqaq | The Sky Splitting Open | 25 | 5 | Meccan |
| 85 | Al-Burooj | The Great Stars | 22 | 7 | Meccan |
| 86 | At-Tariq | The Morning Star | 17 | 5 | Meccan |
| 87 | Al-A'la | The Most High | 19 | 5 | Meccan |
| 88 | Al-Ghashiyah | The Overwhelming | 26 | 7 | Meccan |
| 89 | Al-Fajr | The Dawn | 30 | 9 | Meccan |
| 90 | Al-Balad | The City | 20 | 5 | Meccan |
| 91 | Ash-Shams | The Sun | 15 | 5 | Meccan |
| 92 | Al-Lail | The Night | 21 | 5 | Meccan |
| 93 | Ad-Duha | The Morning Brightness | 11 | 5 | Meccan |
| 94 | Ash-Sharh | The Relief / The Expansion | 8 | 3 | Meccan |
| 95 | At-Tin | The Fig | 8 | 3 | Meccan |
| 96 | Al-Alaq | The Clinging Clot | 19 | 11 | Meccan |
| 97 | Al-Qadr | The Night of Decree | 5 | 5 | Meccan |
| 98 | Al-Bayyinah | The Clear Proof | 8 | 5 | Medinan |
| 99 | Az-Zalzalah | The Earthquake | 8 | 5 | Medinan |
| 100 | Al-'Adiyat | The Charging Steeds | 11 | 5 | Meccan |
| 101 | Al-Qari'ah | The Striking Calamity | 11 | 5 | Meccan |
| 102 | At-Takathur | Rivalry in Worldly Increase | 8 | 5 | Meccan |
| 103 | Al-'Asr | Time / The Declining Day | 3 | 3 | Meccan |
| 104 | Al-Humazah | The Slanderer | 9 | 5 | Meccan |
| 105 | Al-Fil | The Elephant | 5 | 5 | Meccan |
| 106 | Quraysh | Quraysh | 4 | 3 | Meccan |
| 107 | Al-Ma'un | Assistance / Small Kindnesses | 7 | 5 | Meccan |
| 108 | Al-Kawthar | Abundance | 3 | 3 | Meccan |
| 109 | Al-Kafirun | The Disbelievers | 6 | 3 | Meccan |
| 110 | An-Nasr | Divine Support | 3 | 3 | Medinan |
| 111 | Al-Masad | The Palm Fibre Rope | 5 | 5 | Meccan |
| 112 | Al-Ikhlas | Sincerity / Purity of Faith | 4 | 7 | Meccan |
| 113 | Al-Falaq | The Daybreak | 5 | 5 | Meccan |
| 114 | An-Nas | Mankind | 6 | 5 | Meccan |

*Al-Alaq (96) — the first surah ever revealed — carries the maximum 11 pages, opening with the authentic account of the first revelation in the Cave of Hira before working through its verses.*

## Getting Started

### Option 1 — Just open it

Download `juzz30_learning_system_12.html` and open it directly in any modern browser (Chrome, Safari, Firefox, Edge). That's it.

### Option 2 — Host it with GitHub Pages

1. Rename the file to `index.html`  
2. Push it to a GitHub repository  
3. Go to **Settings → Pages**, and set the source to your main branch  
4. Your app will be live at `https://<your-username>.github.io/<repo-name>/`

Note: microphone recording (for Record & Rate) requires a secure context — it works once hosted over HTTPS (like GitHub Pages) or on localhost, but may be blocked if the file is opened directly via `file://`.

## Connecting the Tajweed Assessment microservice

The **Record & Rate** feature works out of the box using on-device rhythm comparison, and by default is already pointed at a deployed assessment service for full per-rule tajweed correctness scoring (madd length, qalqalah, etc.):

const TAJWEED\_API\_BASE \= 'https://inter-sect-learnjuz30tajweed.onrender.com';

If you deploy your own instance of the microservice (see its own `README.md` for setup and deployment), update this line near the top of the `<script>` block to point at your own URL, then re-upload the file. If the service is ever unreachable, Record & Rate automatically falls back to on-device rhythm comparison — no functionality is lost.

## Attribution

- Recitation audio: Sheikh Ibrahim Akhdar, streamed from [everyayah.com](https://everyayah.com)  
- Arabic text: cross-verified against the Tanzil.net Uthmani Quran text (Tanzil Project, Copyright © 2008–2010, [tanzil.net](https://tanzil.net))  
- Word-frequency data (supplementary vocabulary notes): derived from a Quranic word-frequency corpus (based on data from [corpus.quran.com](http://corpus.quran.com))  
- Tajweed rule annotations: cross-referenced against open tajweed annotation datasets  
- Tafsir summaries: based on Tafsir Ibn Kathir, one of the most widely referenced classical Sunni exegetical works — summarized in plain English for this app rather than quoted verbatim from any specific published translation  
- Translations, key-word notes, and surah overviews compiled for educational use, cross-referenced against real Quranic datasets where possible

## Notes

- This is a static, front-end-only project — no data is collected, and nothing is sent to any server other than audio requests to everyayah.com and, by default, the Tajweed assessment microservice above.  
- Given the scale of this project (571 ayahs' worth of translations, keyword notes, and 210 pages of tafsir summaries), treat the content the way you would any large first draft: solid and internally consistent, having been through multiple rounds of cross-checking against authoritative sources, but still worth spot-checking against a trusted mushaf and the original tafsir before relying on it for formal teaching.  
- Contributions, corrections, and improvements are welcome — feel free to open an issue or pull request.

