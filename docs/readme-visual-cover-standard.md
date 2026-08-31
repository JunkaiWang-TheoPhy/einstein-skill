# README Visual Cover Standard

## When To Use It

Use a visual cover when the user explicitly requests one or when the repository's subject gains real meaning from a visual opening. Do not add generated artwork as a default decoration to every repository.

## Placement and Asset Rules

- Store the final raster asset inside the repository, normally under `assets/`.
- Place the image below the centered language switcher and evidence-backed badge row, before the story or overview.
- Reuse the same asset and placement in `README.md` and `README.zh.md`.
- Add descriptive alt text in the language of each README.
- Avoid text, logos, watermarks, fake citations, and visual claims that the repository cannot support.
- Prefer a composition that remains legible at README width and does not compete with the opening narrative.

## Verification

Inspect the generated image before committing. Check its dimensions, file type, local relative path, both README references, remote asset existence, and `git diff --check`. Keep the generation prompt and image provenance in the task record when the asset is consequential.

## Boundary

Generated artwork communicates a theme; it does not establish a scientific claim. Historical figures and scientific scenes should be described as illustrative unless the image is a verified archival source.
