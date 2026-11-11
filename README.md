# Bilingual Paper Annotator

A Codex skill that turns an English academic paper into a standalone HTML reader. It keeps the original English text and places the Korean translation directly below each paragraph. An annotation card explains what the paragraph does, how it supports the argument, and where the reasoning may be weak.

## Install

Clone the repository with a GitHub account that has access, then move the `bilingual-paper-annotator` folder into your Codex `skills` directory. The default location is `~/.codex/skills/` (`%USERPROFILE%\.codex\skills\` on Windows). Keep `SKILL.md`, `agents/`, `assets/`, and `references/` together.

```sh
git clone https://github.com/n01r1r/bilingual-paper-annotator.git
```

## Use

Attach an English paper or give Codex a path to it. Then invoke the skill with a request like this.

```text
$bilingual-paper-annotator Convert the attached paper into a standalone
English–Korean HTML reader with paragraph-level argument annotations.
```

Open the resulting `.html` file in a browser. The reader has English, bilingual, and Korean modes. It highlights the thesis in yellow, key concepts in red, evidence in blue, concessions and rebuttals in green, and methods and assumptions in purple. An overview at the end traces the paper’s argument and identifies its strongest and weakest points.

See [SKILL.md](SKILL.md) for the full workflow, including how the skill handles equations, figures, tables, and citations.

## Attribution

The two-column layout, paragraph annotations, and five-color legend draw on Whisper’s prompt. [Original X post](https://x.com/Whisperrrrr66/status/2120024993287536934) · [Public copy with the full prompt and examples](https://meppp.com/entry/27f9d062-ab66-4d6b-a1ff-fb1a79d4dea0/)
