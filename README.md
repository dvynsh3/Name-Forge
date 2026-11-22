# Name Forge

An offline, rule-based random name generator for worldbuilding. Single-file, vanilla HTML/CSS/JavaScript: no dependencies, no APIs, no AI models. Just open `index.html` in a browser.

## Features

- **Five name types** generated in parallel, each in its own tab plus a combined **All** view: People, Titles, Places, Tools, Abilities
- **Eight generation methods**, individually toggleable (with Select All / Unselect All):
  - English Roots: name-like English words and syllable-stitched names
  - Letter Mutation: swap letters in a base word
  - Add / Remove Letter: insert or delete a single letter
  - Hindi Numbers: 1-100 transliterated into English
  - Compound: structures like "Fire Mage of Thornfield"
  - Fiction Names: commonly used names from fantasy fiction
  - Multilingual Words: names and words from 10 languages
  - Star Names: real named stars
- **Controls**: word count (1-5), randomness, letter chaos, auto-refresh speed
- **Seed word**: every generated name incorporates your word
- **Auto Refresh** with the last 3 names shown, plus a full session history dropdown
- **Spacebar** refreshes all tabs
- **Click any name** to copy it
- **Likes** (session-only) bias the Related Names suggestions
- **Favourites** export to a Markdown table with a configurable vault path and filename, for use in Obsidian
- **Dictionary** browser for all stored word pools
- **Repetition avoidance** within a session

## Usage

Open `index.html` directly in any modern browser. No build step or server needed.

To use it inside Obsidian, point a plugin such as Custom Frames at the local `index.html` file.

## Favourites and Obsidian

Browsers can't write to arbitrary folders, so favourites download as a `.md` file. The vault subfolder and filename you set in the save dialog are embedded as a path hint in the file. Move the downloaded file into your vault, or paste new rows at the bottom of your existing table.

## Notes

The generator itself uses no AI. The code was developed with AI assistance.
