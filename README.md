# Part 1: teach the AI the target template
I am going to convert my research paper into a journal/conference LaTeX template. This message is only about the TEMPLATE. Do NOT convert anything yet; my paper comes in the next message.

Attached: the target template (zip).

Do this:
1. List the zip contents (don't blindly extract everything). Identify: main .tex, document class file, bibliography style files (.bst), sample .bib, sample figures, user manual.
2. Read the main .tex fully and build a "template profile":
   - documentclass and its options (which are valid, which are just leftovers)
   - single- or double-column, text width/height, page size
   - front-matter macros: title, authors (with corresponding-author marker), affiliations, emails, abstract, keywords, any extra required fields
   - required or forbidden things stated in comments (e.g. "no \input", "single .tex file", figure format rules)
   - bibliography style and how citations are made
   - how the class redefines table/figure/float environments (check the .cls for wrappers such as threeparttable that can break \resizebox/\scalebox)
   - which declaration sections it expects (funding, ethics, competing interests, data availability, author contributions, acknowledgements)
   - packages already loaded
3. Identify what in the template is SAMPLE CONTENT (placeholder title, authors, abstract, sections, figures, references) that must be removed later.
4. Compile the template untouched (pdflatex/bibtex cycle) and record its baseline warnings, so we know which are pre-existing.
5. Reply with a SHORT profile (bullet points) plus a list of risks or quirks I should know about for the conversion. No conversion yet, no long explanations. Then wait for my next message.

Keep this profile in mind; the next message refers to it.
