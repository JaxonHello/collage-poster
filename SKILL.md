---
name: collage-poster
description: Create ultra-wide experimental editorial collage posters from simple subject or scene descriptions. Use when the user asks to generate a character poster, event poster, battle poster, sports poster, narrative key visual, anime/game editorial poster, or similar visual using dense interlocked collage, Japanese contemporary graphic design, Swiss typography, asymmetric grids, and controlled negative space.
---

# Collage Poster

## Goal

Turn a minimal user description such as:

- "原神 Furina"
- "One Piece 路飞大战凯多"
- "国安大战鲁能，标题京鲁大战，人物张稀哲和王大雷"
- "悲剧英雄"
- "EVA Asuka"

into a finished ultra-wide experimental editorial poster.

## Canonical prompt contract

Before generating an image, read
[references/poster-style.md](references/poster-style.md) in full.

That file is the canonical, previously tested image-generation prompt. Use its
complete text for every generation.

- Replace only the [SCENE OR SUBJECT DESCRIPTION] placeholder with the user's
  actual description.
- Do not summarize, shorten, paraphrase, translate, reorder or reconstruct the
  canonical prompt.
- Do not reduce it to a list of style keywords.
- Preserve its repeated constraints, quantitative ranges, hierarchy, negative
  constraints and capitalization. The repetition is intentional.
- If the user explicitly overrides a title, person, location, time, palette,
  aspect ratio, typography, object or mood, preserve that value as a hard
  constraint and change only the directly conflicting value in the template.
- When the user supplies an exact title, state inside the substituted subject
  description that it must be reproduced exactly as the primary title.
- When the user does not supply a title, retain the template's conceptual-title
  system unchanged.

## Workflow

1. Parse the user's subject and explicit constraints.
2. Read the canonical prompt in full.
3. Substitute the user's description into its single placeholder.
4. Verify that no canonical section or sentence was omitted or rewritten.
5. Generate the image directly with the completed prompt.

The user should not need to fill a template. Infer missing subject knowledge
through the canonical prompt rather than rewriting the prompt around the
subject.

## Output behavior

Use image generation directly when the user asks to create the poster.

Do not expose the internal prompt unless the user explicitly asks for it.
