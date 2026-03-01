---
name: project-organizer
description: |
  Project file organization and management skill. Enforces structured folder conventions
  to keep project workspaces clean, consistent, and navigable across all projects.
  Use when: starting a new project, creating new files during any task, organizing an
  existing messy folder, or whenever the user mentions "organize", "clean up", "tidy",
  "file structure", "folder structure", or "project setup". Also activate at the START
  of any multi-file task to establish folder conventions before generating files.
---

# Project Organizer

Enforce structured file organization in every project to prevent clutter.

## Core Rules (Apply Always)

### 1. On First File Creation -- Establish Structure

Before creating the first output file in any project, check if a folder structure exists. If not, propose and create one:

```
project-name/
  README.md           -- Project description, status, conventions
  drafts/             -- Working drafts, iterative versions
  figures/            -- Images, charts, diagrams
  scripts/            -- Code that generates outputs
  references/         -- Source materials, templates, examples
  output/             -- Final deliverables only
  archive/            -- Superseded versions (not deleted, moved here)
```

Adapt folder names to the project domain but keep the separation principle: **inputs vs. process vs. outputs**.

### 2. File Naming Convention

| Rule | Example |
|------|---------|
| Use `_v1`, `_v2` version suffixes | `draft_v2.md`, `report_v3.docx` |
| Add dates for milestones | `submission_20260226.docx` |
| Never use `_final`, `_new`, `_copy` | BAD: `report_final_really_final.docx` |
| Use lowercase + underscores for scripts | `generate_figures.py` |
| Prefix figures with sequence numbers | `fig1_trust_curve.png` |

### 3. File Placement Rules

| File Type | Target Folder | Examples |
|-----------|--------------|---------|
| Working drafts, iterative text | `drafts/` | `section1.md`, `intro_v2.md` |
| Generated images/charts | `figures/` | `fig1_model.png` |
| Code scripts (generators, tools) | `scripts/` | `build_docx.mjs`, `plot.py` |
| Reference/source materials | `references/` | `template.pdf`, `style_guide.md` |
| Final outputs for delivery | `output/` | `submission.docx` |
| Old superseded versions | `archive/` | moved from other folders |
| Temporary/scratch files | `/tmp/` or `archive/tmp/` | one-off extractions, test files |

### 4. Cleanup Checkpoints

Every 3-5 tool calls that create files, briefly audit:
- Move any misplaced files to correct folders
- Archive superseded versions (do not delete, move to `archive/`)
- Remove empty directories

### 5. README.md Convention

Maintain a `README.md` at project root with:

```markdown
# Project: [Name]
**Status**: [Current phase]
**Target**: [Goal, e.g., journal name]

## Folder Structure
- `drafts/` -- ...
- `output/` -- ...

## Current Task
[What is being worked on]

## Version History
- v3 (2026-02-27): Final submission version
- v2 (2026-02-26): Added numerical analysis
- v1 (2026-02-25): Initial framework
```

## When the User Starts a New Project

1. Ask what the project primary output is (paper, app, report, etc.)
2. Propose a folder structure tailored to that output type
3. Create the structure and `README.md` before any content generation
4. State the convention to the user: "All new files will follow this structure."

## When Organizing an Existing Messy Folder

1. Scan all files with `list_dir` and `find_by_name`
2. Categorize every file by type (draft, figure, script, output, temp, reference)
3. Propose the target structure to the user
4. Execute moves in batches, reporting each batch
5. Verify final structure is clean (no loose files at top level)
6. Update or create `README.md`

## Domain-Specific Templates

### Academic Paper Project
```
paper-project/
  README.md
  drafts/          -- section-by-section markdown drafts
  figures/         -- paper figures (fig1_xxx.png)
  scripts/         -- figure generation, docx builders, data processing
  references/      -- template papers, style guides, literature
  output/          -- final submission files ONLY
  archive/         -- old versions, intermediate outputs
```

### Web Application Project
```
webapp-project/
  README.md
  src/             -- source code
  public/          -- static assets
  scripts/         -- build/deploy scripts
  docs/            -- documentation
  dist/            -- build output
```

### Data Analysis Project
```
analysis-project/
  README.md
  data/            -- raw and processed data
  notebooks/       -- Jupyter/analysis notebooks
  scripts/         -- processing scripts
  figures/         -- output visualizations
  output/          -- final reports/deliverables
  archive/         -- old versions
```
