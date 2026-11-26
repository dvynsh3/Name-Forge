## [Unreleased]

---

## [v0.4.0] - 2026-11-26
First GitHub-ready build, renamed from "Arcane Name Forge" to **Name Forge**. Builds on [v0.3.0](#v030---2026-09-04).
### Added
- **Favourites.** Star any name (in the last-generated list, the full history, Related Names, or the current name) and download it as a Markdown table row. A save dialog sets the vault folder hint and filename, with a live path preview. The first download after a page load includes the table header.
- **Likes and Related Names.** Heart a name and the Related Names panel suggests words with similar sounds. Likes are session-only and reset on Clear All.
- **Star Names** generation method, using real named stars.
- **Select All / Unselect All** control for the Generation Methods list.
- **Spacebar** refreshes all tabs when focus is not in a text field.
- **Click to copy** on names in the history, Related Names and Favourites, with a confirmation toast.
- **Repetition avoidance:** the generator retries up to 8 times to avoid names already seen this session.
- Like and favourite buttons directly under the current name on each tab.
- Repository package: README with screenshots, MIT licence and `.gitignore`.

### Changed
- Renamed from "Arcane Name Forge" to **Name Forge** (page title and header).
- Fiction Names pool thinned of anime-style names and extended with other fantasy names.

---

## [v0.3.0] - 2026-09-04
Two new generation methods and a slower default auto-refresh, on top of [v0.2.0](#v020---2026-08-02).
### Added
- **Add / Remove Letter** generation method, separate from Letter Mutation. Instead of swapping a letter, it inserts a random letter at an internal position (*Storm* → *Stoarm*) or removes one (*Riven* → *Rien*). Uses the seed word when one is given and scales with word count.
- **Multilingual Words** generation method with 10 language pools: Japanese, Italian, French, Korean, Arabic, Spanish, Greek, Hindi, Chinese and Norse. Each pool has real names plus evocative common words, romanised (e.g. *Akira Nyx*, *Fuoco Kaito*). Multi-word names can mix languages, and the method badge shows which language was drawn.
- Both new methods are selectable in the Generation Methods list (on by default), favoured when a seed word is set, and weighted by the Randomness slider.
- All multilingual words are browsable in the Dictionary under per-language headings.

### Changed
- Default **Auto Speed** lowered from 5 to **1** (slowest), so Auto Refresh no longer blasts through names the moment it is started.

---

## [v0.2.0] - 2026-08-02
Selectable methods, a seed word that is always used, an All tab and full history. Built on [v0.1.0](#v010---2026-06-29).
### Added
- **All tab** at the start of the tab strip, showing a current name for every type (People, Titles, Places, Tools, Abilities) in a two-column card grid. Updates on every refresh, including Auto Refresh.
- **"See all ▾"** button next to "Last Generated" on each type's tab. It opens a scrollable panel listing every name generated that session for that type, numbered newest first. The last-3 strip is unchanged.

### Changed
- **Generation Methods** is now a checkbox-style list in the sidebar (replacing the pill buttons). Click anywhere on a row to toggle it; only selected methods are used. All are selected by default.
- **Seed word is now used by every generator**, where in [v0.1.0](#v010---2026-06-29) it was applied only occasionally:
  - English Roots: slots the seed into the name structure.
  - Letter Mutation: the seed is always the base word, and gets a second, softer mutation when word count is above 1.
  - Hindi Numbers: fuses the seed with a number word.
  - Compound: the seed replaces the element/subject slot.
  - Fiction Names: joins the seed to the drawn name.
- With a seed set, Mutation, Compound and English Roots are favoured when picking a method.
- Full session history is now kept for every type, not just the last 3 (v1 trimmed history to 3 during Auto Refresh).

---

## [v0.1.0] - 2026-06-29
First working build, named **Arcane Name Forge**. A single HTML file, fully offline, with no AI and no external dependencies apart from the Google Fonts import.
### Added
- Five name types, each in its own tab and generated together on every refresh: **People**, **Titles**, **Places**, **Tools**, **Abilities**.
- Five generation methods, toggled as pills in the sidebar:
  - **English Roots**: syllable-stitched fantasy names and name-like English words.
  - **Letter Mutation**: swaps vowels or consonants in a base word, driven by the Letter Chaos slider.
  - **Hindi Numbers**: 1-100 in English transliteration, blended with roots for longer names.
  - **Compound Structure**: "Fire Mage of Thornfield, Grimwater" style, appearing at higher word counts.
  - **Fiction Names**: a library of about 120 names from Tolkien, A Song of Ice and Fire, Harry Potter, Naruto, Dragon Ball, The Witcher and others.
- Controls: **Words** (1-5), **Seed Word**, **Randomness**, **Letter Chaos** and **Auto Speed** (about 2 s down to 200 ms).
- **Refresh** and **Auto Refresh** buttons, which show the last 3 names while running, with a pulse animation on each new name.
- **Clear All**, which wipes the session and stops Auto Refresh.
- **Dictionary** modal for browsing every stored word pool, grouped by category.
- Per-session counters in the sidebar.
- Dark teal and gold interface using Cinzel, Share Tech Mono and Inter.

### Known limitations
- The seed word is only applied some of the time (fixed in [v0.2.0](#v020---2026-08-02)).
- Methods cannot be selectively turned off with a list (fixed in [v0.2.0](#v020---2026-08-02)).
- No combined view and no full session history (both added in [v0.2.0](#v020---2026-08-02)).
