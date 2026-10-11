# Float Reader dictionaries

Offline dictionaries for the [Float Reader](https://play.google.com/store/apps/details?id=com.rufatapps.floatreader)
e-book app. There is one pack per language (German, French, Spanish, …), each with English definitions, word
forms and grammar.

The app downloads these packs itself. You don't need to download anything from
here.

## Source and licence

The data comes from [Wiktionary](https://en.wiktionary.org/), through the
machine-readable extraction by [kaikki.org](https://kaikki.org/) (Wiktextract,
Tatu Ylonen).

**Licence: [CC BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0/)
and [GFDL](https://www.gnu.org/licenses/fdl-1.3.html)**, the same as
Wiktionary. Wiktionary contributors are the authors of the content.

You may share and adapt these packs, including commercially, as long as you
credit Wiktionary and share your adaptations under the same licence.

## Changes made

The packs were converted to compact SQLite files.

- Definitions are limited to the first ten senses per word.
- Example sentences longer than 180 characters are left out.
- Word forms are stored in a compact automaton (format "schema 3").
- Multi-word forms are dropped, except particle verbs.

The conversion tool is part of the Float Reader source (`tools/dict_builder`).

## Files

- `manifest.json`: the list of packs, with sizes and SHA-256 checksums.
- `<language>-en.sqlite.gz`: one pack per language.
