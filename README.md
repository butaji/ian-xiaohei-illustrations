# Ian Xiaohei Illustrations

> Transform judgments, processes, states, and metaphors from articles into white-background, hand-drawn, absurd but clean article illustrations.
>
> 16:9 horizontal | Xiaohei IP | Pure white hand-drawn | Sparse red/orange/blue annotations | Codex Skill

---

## What is this repo

Ian Xiaohei Illustrations is a Codex Skill designed to guide AI agents in generating article illustrations for posts, blogs, Notion documents, and methodology content.

It's not a generic illustration prompt, nor a PPT infographic template. Its core goal: first understand the cognitive anchors in an article, then transform one judgment, process, structure, state, or metaphor into a memorable 16:9 hand-drawn explanatory illustration.

The default visual IP is "Xiaohei": a solid black creature with white dot eyes, thin legs, and a blank expression. Xiaohei is not a mascot, sticker, or decoration in the corner—it's a bizarre worker seriously participating in the system's operation.

In short: **Get AI to not just "add an illustration" but to draw out a key cognitive action from the article.**

---

## Who it's for

Great for:

- Writing articles and needing body illustrations
- Creating knowledge-based content, methodology content, or AI workflow content
- Wanting to turn abstract judgments into concrete metaphors
- Looking for an illustration style lighter than PPT infographics, more bizarre, with stronger personal recognition
- Using Codex for content production and wanting to consistently reuse a visual language

Not suitable for:

- Wanting commercial illustrations, brand KVs, or refined flat illustrations
- Wanting traditional PPT infographics, complex architecture diagrams, or flowcharts
- Wanting children's cartoons, cute IPs, or meme styles
- Trying to fit large bodies of text, long explanations, or complete course pages into one image
- Needing strictly editable vector source files

---

## What it produces

Default output:

- 16:9 horizontal article illustrations
- A shot list of 4-8 illustrations per article
- Theme, core meaning, structure type, Xiaohei action, and annotation suggestions for each image
- Final PNG images saved to `assets/<article-slug>-illustrations/` in the workspace

Default non-output:

- PPTX / PDF / Keynote
- SVG / HTML / Canvas editable graphics
- Commercial posters or cover KVs
- Text-heavy infographics

---

## Visual style

This skill uses Ian's "Xiaohei Bizarre Article Illustration" style by default:

- Pure white background, no paper texture, off-white, shadows, or gradients
- Black hand-drawn line art, thin lines, slight wobble
- Lots of empty space, main subject takes only about 40%-60% of the canvas
- Sparse red, orange, and blue handwritten annotations
- Each image expresses only one core action, structure, state, or metaphor
- Xiaohei must participate in the core action, not just decorate
- Bizarre, creative, clean, but not childish or cutesy

---

## Example results

### Two Breakpoints

![Two Breakpoints](examples/images/01-two-breakpoints.png)

### Sort by Purpose

![Sort by Purpose](examples/images/02-sort-by-purpose.png)

### One Fish Many Uses

![One Fish Many Uses](examples/images/03-one-fish-many-uses.png)

### Handoff Path

![Handoff Path](examples/images/04-handoff-path.png)

### Information Well

![Information Well](examples/images/05-information-well.png)

### Idea Press

![Idea Press](examples/images/06-idea-press.png)

### Content Fermentation

![Content Fermentation](examples/images/07-content-fermentation.png)

### Trust Bridge

![Trust Bridge](examples/images/08-trust-bridge.png)

These images are style calibration samples, not composition templates. When using, reinvent metaphors from the current article rather than copying objects and compositions from old examples.

---

## Installation

Clone the repo:

```bash
git clone https://github.com/helloianneo/ian-xiaohei-illustrations.git
cd ian-xiaohei-illustrations
```

Copy the skill to Codex skills directory:

```bash
mkdir -p "${CODEX_HOME:-$HOME/.codex}/skills"
cp -R ./ian-xiaohei-illustrations "${CODEX_HOME:-$HOME/.codex}/skills/"
```

After installation, use in Codex:

```text
Use $ian-xiaohei-illustrations to design and generate 5 Xiaohei bizarre article illustrations for this article.
```

---

## How to use

### Planning only

```text
Use $ian-xiaohei-illustrations. Don't generate images yet.
Analyze which parts of this article are worth illustrating and output a shot list of about 5 images.
For each image, specify: where it goes after which paragraph, theme, core meaning, structure type, what Xiaohei is doing, suggested annotation words.

<paste article>
```

### Direct generation

```text
Use $ian-xiaohei-illustrations to generate 4 Xiaohei bizarre article illustrations from this article.
Requirements: 16:9 horizontal, pure white background, black hand-drawn line art, sparse red/orange/blue handwritten annotations.

<paste article>
```

### Single concept

```text
Use $ian-xiaohei-illustrations to generate one article illustration for "Trust isn't shouted out—it's paved over one piece of evidence at a time."
The scene should be bizarre but clean, with Xiaohei taking on the core action.
```

### Remove titles or errors

```text
Use $ian-xiaohei-illustrations to edit this image. Remove the "Flowchart" title in the top-left corner, keep everything else unchanged.
```

More examples in [examples/prompts.md](examples/prompts.md).

---

## Workflow

The skill's process is:

1. Read articles, Markdown, Notion content, screenshots, or user-provided topics
2. Extract core viewpoints, cognitive turning points, process structures, and passages suitable for visualization
3. First output shot list: select only one cognitive anchor per image
4. Choose structure type for each image: Workflow, system partial, before/after comparison, role state, concept metaphor, method layers, map route, or mini-comic panels
5. Reinvent a low-tech, bizarre but valid physical metaphor
6. Have Xiaohei take on the core action
7. Generate each image separately via image model
8. Check against QA checklist: white background, empty space, Xiaohei action, annotations, not PPT-like, not old case recreation
9. Save final PNGs and report usage and paths

---

## Directory structure

```text
.
├── README.md
├── LICENSE
├── NOTICE.md
├── assets/
│   └── ian-wechat-qr.jpg
├── examples/
│   ├── images/
│   │   ├── 01-two-breakpoints.png
│   │   ├── 02-sort-by-purpose.png
│   │   └── ...
│   └── prompts.md
└── ian-xiaohei-illustrations/
    ├── SKILL.md
    ├── agents/
    │   └── openai.yaml
    ├── assets/
    │   └── examples/
    └── references/
        ├── style-dna.md
        ├── xiaohei-ip.md
        ├── composition-patterns.md
        ├── prompt-template.md
        └── qa-checklist.md
```

The actual installation for Codex is the subdirectory:

```text
ian-xiaohei-illustrations/
```

Root-level README, LICENSE, NOTICE, and examples are for GitHub sharing documentation.

---

## Notes

- Shorter text in images is more stable.
- Each image should explain only one core structure, don't turn the article into an instruction manual.
- Xiaohei must take on the core action; if the image still works completely without Xiaohei, then Xiaohei is too decorative.
- Example images are only for calibrating line density, white space, color restraint, and Xiaohei's participation—not for recreating compositions.
- AI image models may produce typos, hallucinated labels, style drift, or extra titles; check after generation.
- If typos in annotations are severe, prioritize reducing annotation words and regenerating.

---

## Related projects

- [Ian Handdrawn PPT](https://github.com/helloianneo/ian-handdrawn-ppt) — Hand-drawn technical PPT-style page illustration generation Skill
- [Awesome Claude Code Skills](https://github.com/helloianneo/awesome-claude-code-skills) — Curated collection of Claude Code Skills / Agents / Plugins
- [Obsidian + Claude AI Second Brain](https://github.com/helloianneo/obsidian-ai-second-brain) — Obsidian + Claude AI personal knowledge base setup guide

---

## About the author

**Ian** — Product Designer / Solo Company Practitioner / AI Builder

Building a solo company with AI teams.

- GitHub: [helloianneo](https://github.com/helloianneo)
- X/Twitter: [@ianneo_ai](https://x.com/ianneo_ai)
- Website: [www.ianneo.xyz](https://www.ianneo.xyz)
- WeChat: `ianneoxyz`
- Email: hello.neoc@gmail.com

---

## Continue exploring

This Xiaohei illustration skill is just one tool in my AI-powered personal production system.

If you're also using AI for content, knowledge bases, workflows, or products, check out my website: [www.ianneo.xyz](https://www.ianneo.xyz).

Just want to observe first? Follow my [X/Twitter](https://x.com/ianneo_ai).

Interested in Indie Builders Club? Add me on WeChat: `ianneoxyz`, note "OPC".

<p>
  <img src="assets/ian-wechat-qr.jpg" alt="Ian WeChat QR Code" width="120">
</p>

Can't scan? Search WeChat: `ianneoxyz`.

---

## License

MIT License. See [LICENSE](LICENSE).
