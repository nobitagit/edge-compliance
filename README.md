# Edge Compliance Playground

A browser-based flashcard game for learning medical device classification rules. Each round presents 5 randomly selected questions — swipe right for Yes, swipe left for No. At the end you get a score and a full recap of every question, including the correct category and the reasoning behind it.

## Running the project

Open `index.html` directly in a browser. No build step or server required.

## Skills

Skills are AI-executable workflows stored in `.ai/skills/`. To run one, open this project in an AI coding assistant (such as OpenCode) and tell it:

> "Run the `<skill-name>` skill"

The assistant will read the skill file and follow its steps.

### Available skills

| Skill | File | What it does |
|---|---|---|
| update-cards | `.ai/skills/update-cards.md` | Parses `data.csv` from the project root and replaces the `CARDS` array in `index.html` with the converted data. |
