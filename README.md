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

# Part 2: convert the paper
Now convert my paper into the template you just profiled.

Attached: my paper's source zip (Overleaf export). My author/affiliation information is [attached as image/text below / already in the .tex, use that].

Follow these rules exactly.

CONTENT
- Do not change my wording, numbers, equations, citations, table data or figure captions. Only change what the new template forces (layout, macros, packages).
- Do not delete content silently. Anything you can't place goes into a "% TODO" comment at the right spot and into your report.
- Replace ALL template sample content (title, authors, abstract, sections, figures, references, acknowledgements).

FRONT MATTER
- Use my author list exactly as given, in my order. Apply the template's macros for authors, affiliations, emails, corresponding-author markers.
- Corresponding authors: keep those marked in my paper or list unless I say otherwise.
- Do not invent anything: no equal-contribution notes, ORCIDs, addresses, or funding. If a number is skipped in my list, an email domain doesn't match the affiliation, or an abbreviation was expanded, flag it.

CONVERSION
- Keep the template's class, class options (drop unused ones), preamble structure and bibliography style, unless I say otherwise.
- Remove packages, fonts and macros that belong to my old class or template (e.g. old front-matter macros, history/DOI commands, old font packages). Keep only what my paper actually uses; keep needed patches (e.g. algorithm float/vertical-rule) and load their dependencies.
- Follow the template's rules (e.g. single .tex file: no \input; inline anything needed).
- If the column layout changes (one <-> two column): fix figure* / table*, re-size figure widths, and re-fit wide tables. If the class wraps tables in a way that breaks \resizebox/\scalebox, use explicit column widths (p{} columns, \small/\footnotesize, \tabcolsep) instead.
- Copy only figures that are actually referenced; rename files to have no spaces or special characters; update all paths; put them in Figures/.
- Bibliography: keep my .bib, use the template's style, check every \cite key exists in the .bib, list uncited entries, and flag entries that look suspicious (placeholder IDs, mismatched topic).
- Declarations: map my ethics, funding, acknowledgement, competing-interest, data-availability and author-contribution text to the template's sections. Flag contradictions between sections (e.g. funding footnote vs "no sponsorship") and stale statements (e.g. names of people no longer authors). Leave those as TODO, don't guess.
- If I ask for custom margins: do NOT stack \geometry margins on top of the class's text block (that causes "over-specification" warnings). Override with explicit textwidth/textheight (plus one margin per axis) so the layout matches what I asked for.

VERIFY (do all of it, don't skip)
1. Full compile cycle (pdflatex, bibtex, pdflatex x2). Target: 0 errors, 0 undefined references, 0 undefined citations.
2. Go through every warning. Fix the fixable ones (unused class options, unused packages, unused theorem styles, geometry over-specification, missing font sizes via lmodern, overfull boxes). For any you can't fix, tell me why in one line.
3. Render and look at the key pages: title page (authors/affiliations/abstract), every table, the algorithm, at least one figure. Fix what looks wrong.

DELIVER
- A zip (main .tex, class, .bst, .bib, Figures/) plus a preview PDF, and the main .tex separately.
- A short final report with: (a) what you changed, (b) a numbered list of things that need MY decision or correction, most important first. No padding, no repeating what I already know.

If something blocks you, make the most reasonable assumption, state it in the report, and continue. Ask me only if you truly can't proceed.
