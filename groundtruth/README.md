# groundtruth

Hand-corrected transcriptions of sampled pages, against which Bron measures OCR. Each page is corrected by a named reader from the scan, then checked again blind wherever an OCR engine read something different. The figures these pages produce are in `bron/docs/research/`.

| Path | Holds |
|---|---|
| `bavinck/gd/ed2/print2/` | One file per sampled page of the second printing (Delpher, VU copy), `v<volume>-p<page>.gt.txt` |
| `bavinck/gd/ed2/print4/variants.yaml` | Places where the fourth printing prints something else, confirmed by the reader on its scan |
| `bavinck/gd/ed2/rounds/` | Every check round's items and answers, as they came back |

The sample itself, with the source of every page and its hashes, is `ocr/bavinck/gd/ed2/m2-sample/manifest.yaml`.

**Rights.** The pages transcribe a public-domain work: Bavinck died in 1921. They carry the Public Domain Mark, and any rights Bron or the reader might hold in them are waived under CC0 1.0 (`../LICENSE-CC0`).

## Transcription rules

These rules are what the reader follows, and what every OCR engine is asked to follow too. They follow OCR-D's ground-truth guidelines, level 2.

Save plain UTF-8 text without tabs. Keep the identifying `#` header unchanged.

**What to type**

1. **Type what is printed.** Keep the spelling, capitals, punctuation, quotation marks („ " ' ') and dashes (— –, -) exactly as the page prints them, even where they look wrong. Do not modernize, and do not correct the printer.
2. **One text line for each printed line.** Keep the line breaks of the page. If the pre-filled text joins two printed lines or splits one, fix it so they match. If a printed line is missing, type it in its place. Delete lines that the page does not print.
3. **Keep line-end hyphens.** A word broken at the end of a line keeps its hyphen, and its second part starts the next line.
4. **Letters, not ligatures.** Type printing ligatures as separate letters (fi, fl, ff). Type the Dutch ĳ as the two letters `ij`.
5. **Greek and Hebrew in full.** Type Greek with every accent and breathing, and Hebrew with every vowel point and accent the page prints. Type them in the order you read them; Hebrew runs right to left as usual.
6. **No formatting.** Do not mark italics, letter-spacing (spatiëring), bold or small capitals. Small capitals are typed as the capital and lower-case letters they stand for.
7. **Spaces.** One space between words. Before a punctuation mark, type a space only where the page clearly leaves a full space (as in a Bible reference printed `2 : 8`).
8. **Footnote numbers.** Type a footnote number as it is printed, as a plain digit, with its bracket: `1)`.

**Tags at the start of a line**

9. `@head` marks running-head and page-number lines. The pre-filled text tags the running head; check it. If the page number appears on a separate line, tag that line `@head` too. Put one space between a tag and the printed text.
10. `@note` marks every line of a footnote, at the foot of the page, in small type. Tag each footnote line yourself.
11. A line starting with `#` names the page. Leave it as it is.

**When you cannot read it**

12. For each character you cannot read, type `□` (one per character). Do not guess. This placeholder is excluded from scoring; every other character is counted as read.

**Time**

13. Write down in `minutes.txt` how many minutes each page took, rounded to five.

## Reader and rounds

Filled in when the ground truth is committed: the reader's name (with their consent), the dates of each round, and the minutes per page.

No human-corrected pages have been collected yet. Reader: —. Round dates and minutes per page: —.

The reader corrects the Delpher pre-fill against the scan in round 1. In round 2, they read blind crops wherever any engine disagrees, including candidate fourth-printing differences. In round 3, they settle disagreements between their own readings. Record minutes per page in every round. Fourth-printing ground truth is derived from the corrected second-printing text and only reader-confirmed differences.

After this sample and these rules merge, rebuild the round-1 packet from the committed rules before handing it to the reader. Trial packets are not the final handover.

These instructions are documentation under CC BY 4.0, attributed to Bron contributors (see `../LICENSE`). The public-domain/CC0 statement above applies to the transcribed text.
