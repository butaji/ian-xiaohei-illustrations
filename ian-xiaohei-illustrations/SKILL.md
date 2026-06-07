---
name: ian-xiaohei-illustrations
description: Generate Ian-style article illustrations. For tasks where users request "bizarre", "Xiaohei", "hand-drawn", "article illustration", "body image", "illustration suggestions", "shot list", "remove title/edit image" for articles, posts, blogs, Notion documents, workflow documents, methodology, processes, structures, states, metaphors, or viewpoints; defaults to Xiaohei IP, pure white hand-drawn style, sparse red/orange/blue annotations, clean but imaginative visual style.
---

# Ian Xiaohei Bizarre Article Illustrations

## Core positioning

Design and generate 16:9 horizontal article illustrations. The goal is not commercial illustration, PPT infographics, or cute cartoons—it's transforming key judgments, processes, structures, states, or metaphors into clean, bizarre, creative, readable but non-instructional hand-drawn explanatory illustrations.

The default visual IP is "Xiaohei": solid black, white dot eyes, thin legs, blank expression, seriously doing something absurd but valid. Xiaohei must participate in the image's core action, not just stand beside as decoration.

## Read these references first

Read based on task needs, don't flood the context all at once:

- `references/style-dna.md`: Style DNA, colors, text, and prohibitions.
- `references/xiaohei-ip.md`: Xiaohei IP's appearance, personality, action library, and prohibitions.
- `references/composition-patterns.md`: Structure types, original metaphor methods, and anti-pattern rules.
- `references/prompt-template.md`: Single image generation prompt template.
- `references/qa-checklist.md`: Post-generation checking and iteration rules.
- `assets/examples/`: For low-frequency visual calibration only, not part of the default generation path. Do not copy compositions, objects, or annotations from these examples.

## Workflow

### 1. Digest the content

First read the text, links, Notion pages, Markdown files, or screenshots provided by the user. Extract:

- What is the core viewpoint
- Which paragraphs carry cognitive turning points
- Which content is suitable for visual explanation
- Which places are text-only and don't need images

Don't distribute illustrations evenly. Prioritize "cognitive anchors" such as: core judgments, two breakpoints, input-output loops, diversions, before/after comparisons, one fish many uses, handoff paths, common pitfalls, role state changes.

### 2. Output illustration strategy first

If the user only says "analyze how to illustrate / think about which parts need images," provide a shot list first. For each image, clearly state:

- After which paragraph it goes
- Theme
- Core meaning
- Structure type
- What Xiaohei is doing in the image
- Suggested elements
- Suggested annotation words

Default 4-8 images. 1-3 for very short articles; don't easily exceed 9 even for long articles. Enough is enough—avoid turning articles into picture books.

### 3. Single image generation

If the user explicitly asks to "generate / output / create / help me generate," don't stop to wait for confirmation; generate each image separately using the built-in `image_gen`. Don't combine multiple images into one.

Each image explains only one core structure. Prompts must include:

- 16:9 horizontal article illustration
- Pure white background
- Black hand-drawn line art
- Sparse red/orange/blue handwritten annotations
- Lots of empty white space
- Xiaohei as the core action subject
- No PPT, commercial illustration, childish cuteness, complex architecture, or type titles in top-left corner

Don't recreate past cases. Examples only provide style density and Xiaohei participation methods—don't directly reuse "conveyor breakpoints / Xiaohei pulling lines / material fish / stamp toolbox / common pitfalls path" and other existing compositions unless the user explicitly requests recreating a specific image. Always reinvent a bizarre but valid metaphor from the current article.

### 4. Check and iterate

After generation, check `references/qa-checklist.md`. If the following issues occur, prioritize regenerating or local editing:

- Xiaohei is just decoration
- Image is too full
- Too much like a flowchart/PPT
- Too much text or severe typos
- "Common pitfalls / Flowchart / System Architecture" titles appear in top-left
- Style is too cute, childish, or rigid
- Background is not clean white

### 5. Save and deliver

If the user is working in workspace, copy final images to:

```text
assets/<article-slug>-illustrations/
```

Name sequentially:

```text
01-topic-name.png
02-topic-name.png
```

Keep original generated files; don't overwrite existing assets unless the user explicitly requests replacement.

## Output guidelines

Pre-generation strategy output should be short and precise. Post-generation delivery should include:

- How many images were generated
- Purpose of each image
- Save paths
- Which images are most stable, which are optional

Don't write long explanations of style theory; let the images speak for themselves.
