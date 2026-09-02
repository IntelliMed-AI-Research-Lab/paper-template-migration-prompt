I need to convert my paper from one LaTeX template/journal format into another.

I am attaching two files:
1. My current paper's full .tex file, written in the ---------- [current template/journal name, e.g. "PLOS One"] format.
2. The target template's .tex file (currently containing placeholder/dummy content) for ---------- [target template/journal name, e.g. "IEEE Access"], which I need to convert my paper into.

Please do the following:

1. First, read and fully understand my current paper from the attached file — all sections, tables, figures, equations, algorithms, and citations — before making any changes.

2. Take the exact preamble, package imports, and structural conventions (title/author/abstract commands, section formatting, bibliography style, etc.) from the target template file, and port my paper's full content into that structure.

3. Preserve all of the following exactly, without summarizing, shortening, or paraphrasing:
   - All section and subsection content, in the same order
   - All tables, with their data intact
   - All figures and their \includegraphics calls, captions, and labels
   - All equations and their numbering
   - All algorithms/pseudocode blocks
   - All in-text citations (\cite{} keys unchanged)
   - Any tracked-edit formatting (e.g. \textcolor{blue}{...}) I have in the current draft — carry it over as-is unless I say otherwise

4. Adapt only what differs structurally between the two formats, such as:
   - Section header commands (e.g. \section* → \section, or vice versa)
   - Abstract/keywords environment syntax
   - Author/affiliation block formatting
   - Bibliography style and \bibliography{} command (tell me if the .bib filename needs to change or be recreated)
   - Any front-matter-specific commands unique to one template that don't exist in the other (tell me explicitly if you drop a section like this, and why)

5. Do NOT introduce any new claims, reword scientific content, or "fix" anything unless I've separately asked you to — this is a structural port only, not a content edit pass.

6. After conversion, give me:
   - The complete converted .tex file, ready to paste directly into the new template's main.tex
   - A short list of anything I need to do manually afterward (e.g. renaming/uploading a .bib file, re-uploading figure files, installing a missing package, class file requirements)
   - A short list of anything you dropped, merged, or restructured because it had no equivalent in the target template, so I know to check it

Target template name: ----------
Current format name: ----------
Any special instructions (e.g. "keep tracked-changes coloring", "strip all colors for final submission", "use this specific bibliography filename: ----------"): ----------
