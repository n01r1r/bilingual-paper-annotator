---
name: bilingual-paper-annotator
description: Convert a supplied English academic paper into a standalone English–Korean HTML reader with paragraph-aligned translations, color-coded argument annotations, and an argument overview. Use when the user requests an interactive bilingual edition for close reading or critical study.
---

# Bilingual Paper Annotator

Produce one complete, standalone `.html` file from the supplied paper. Use English as the primary language and Korean as the secondary language. Keep the original English wording, paragraph boundaries, section order, and heading hierarchy.

## Workflow

1. Inventory the full source before drafting. Identify paragraphs, headings, equations, definitions, citations, references, footnotes, figures, and tables. Check ambiguous PDF extraction against the visible pages, especially reading order, symbols, line-wrap hyphens, and figure captions. If material is missing or unreadable, request the affected pages or text before claiming completeness.
2. Assign stable IDs to sections and paragraphs. For each paragraph, keep the exact English text, place the full Korean translation below it, and pair both with one annotation card containing paragraph function, logical role, and critical commentary in both languages. Connect analytical claims to the relevant paragraph IDs or numbered source material.
3. Map the paper's reasoning in its actual order. At the bottom, include the reasoning path, the central thesis in one sentence, and the strongest and weakest arguments the evidence supports. Describe the limits of the assessment where the paper leaves a question open.
4. Use [the HTML template](assets/paper-reader.html) and [the assembly contract](references/html-reader.md) for the desktop and mobile layouts, legend, navigation, and three language modes. Read [the analysis and fidelity guide](references/analysis-and-fidelity.md) when drafting and reviewing the bilingual content.
5. Compare the final English text and paragraph inventory with the source. Check Korean completeness and analytical equivalence, the argument map, citations, equations, and other source objects. Open the finished HTML locally and exercise the three language modes, translation toggle, and section links. Check desktop alignment and mobile reading order. Deliver the single HTML file and report any unresolved source or verification limitations.

## Language modes

- **English — Primary.** Default. Show the English original and English analysis. Let the reader show or hide Korean translations.
- **English + Korean — Bilingual.** Show each English paragraph followed by its Korean translation. Show English annotations and overview text followed by their Korean equivalents.
- **Korean — Secondary.** Keep the English original above the Korean translation. Show Korean annotations, navigation labels, and overview text with the same analytical detail as the English versions.

## Attribution

The dual-column layout, paragraph annotations, and five-color legend draw on a prompt shared by Whisper (@Whisperrrrr66).

- [Original post on X](https://x.com/Whisperrrrr66/status/2120024993287536934)
- [Public copy with the full prompt and examples](https://meppp.com/entry/27f9d062-ab66-4d6b-a1ff-fb1a79d4dea0/)
