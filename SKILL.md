---
name: interesting
description: Generate minimalist hand-drawn conceptual graphics in the "interesting" visual style from a source image, screenshot, photo, poster, Chinese or English text, abstract idea, product feature, article topic, or presentation concept. When an image is supplied, extract its actual dominant elements, spatial relationships, and repeated motifs before creating a simplified new image; do not invent a hand, character, object, or action that is absent or unnecessary. Produce two selectable colorways by default while preserving one shared composition. Use when the user says "interesting" or "有意思图形", asks to restyle or simplify an image, turn content into this flat-color warm-white geometry and thick black hand-line style, or wants a matching prompt, recolor, or style-consistent variant.
---

# Interesting

Turn the supplied material into one clear visual sentence. When a source image exists, fidelity to its actual subject and composition comes before metaphor. Geometry carries the main forms; existing poses, object relationships, connectors, or optional gestures carry the action.

## Load the visual system

Read [references/style-language.md](references/style-language.md) completely before designing.

When generating an image or delivering a production prompt, also read [references/prompt-and-qa.md](references/prompt-and-qa.md) completely.

For source-image transformation, example selection, or an explanation of the style and its use cases, read [references/style-and-use-cases.md](references/style-and-use-cases.md) completely. Inspect only the one or two closest examples routed there from `assets/examples/`. Treat those screenshots as calibration and workflow examples, never as edit targets or content templates.

When visual calibration is useful, inspect [assets/reference-sheet.png](assets/reference-sheet.png) with the local image viewer. Treat it only as a style reference, never as an edit target or content to reproduce literally.

## Apply defaults

Proceed without clarification unless a missing choice would materially change the result.

- Default deliverable: two generated raster images sharing one composition but using two distinct background colorways.
- Default canvas: landscape 4:3; use square for avatars, stamps, or social-card requests.
- Default text inside image: none.
- Default hand count: zero. Add a hand only when it is present in the source, explicitly requested, or indispensable to the source's central action.
- Default language for the explanation: match the user.
- Default storage: preview inline; save to the requested or current project location when project-bound.
- Default palette: one semantic background color, near-black line, warm-white fill.

If the user asks only for a concept, prompt, or art direction, stop before image generation and provide exactly that artifact.

## Choose the input mode

Use **source-image extraction** whenever the user supplies an image to restyle, simplify, reinterpret, or match. Use **text-to-concept** only when there is no source image or the user explicitly asks to ignore its content.

Use the scene routing in [references/style-and-use-cases.md](references/style-and-use-cases.md) to choose the abstraction density. Treat a triptych, collection, postcard, or framed scene as one semantic core when its identity depends on multiple peer elements.

### Source-image extraction

1. Inspect the source at useful resolution before designing.
2. Record only visible facts:
   - dominant subject;
   - one supporting element if it materially affects recognition;
   - spatial arrangement, scale, crop, and direction;
   - actual interaction or relationship between elements;
   - three to five repeated marks, branches, tiles, windows, dots, or other distinctive rhythm;
   - background mood and whether text or a logo is essential content.
3. Select the one or two elements that make the source recognizable. Preserve their relative position, silhouette, direction, and relationship while simplifying internal detail.
4. Remove photographic texture, lighting, halftone, incidental scenery, and decorative clutter unless one of them is the subject.
5. Do not convert the source into an unrelated metaphor. Do not add a hand, character, prop, arrow, container, or action merely because it belongs to the style vocabulary.
6. Omit text and logos by default. Preserve them only when the user requests them or when removing them would change the subject's identity or message.

If several simplifications are plausible, form up to three extraction candidates and select the one with the strongest source recognition, clearest two-second read, and fewest invented elements.

### Text-to-concept

1. Compress the input into one graphic proposition, no more than 14 Chinese characters or 8 English words.
2. Extract four roles:
   - noun: the core subject;
   - action: what changes, acts, or remains still;
   - relationship: how subjects connect, transform, protect, choose, or grow;
   - emotion: the background-color mood.
3. Form three silent metaphor candidates using only `object + action device + relationship`.
4. Select the candidate with the clearest two-second read, fewest objects, and least cliché.
5. Map it to one standard composition from the style reference.
6. Remove every detail that does not change the main judgment.

An action device may be an existing pose, displacement, deformation, connector, motion path, tool, or hand. Prefer position and object behavior over arrows or words. Keep at most two core objects and one relationship structure.

## Generate the image

Use the built-in image-generation workflow for raster output. Do not substitute SVG, HTML, or generic icon code for the requested final image.

Construct the production prompt from [references/prompt-and-qa.md](references/prompt-and-qa.md). For source-image extraction, explicitly list source facts, elements to preserve, details to remove, composition, exact palette, line behavior, rhythm, and prohibitions against invented content. For text-to-concept, specify the proposition, chosen object, action device, relationship, and the same visual constraints.

Pass the user's source image as a content and composition reference when available. Do not pass the bundled reference sheet as an edit target; it is only for visual calibration.

## Produce two colorways

Choose two semantically appropriate, clearly different background colors from the fixed palette. Keep near-black `#141413` linework and warm-white `#FAF9F6` fills identical in both.

- Preserve the exact same composition, object positions, proportions, linework, and crop across A and B.
- Generate the composition once, then derive the second colorway by deterministic palette replacement whenever possible.
- Do not regenerate the second image independently unless the user asks for different layouts; independent generations make color comparison less useful.
- Prefer color pairs with meaningful contrast, such as terracotta/moss green, fog blue/dusty blush, mint gray/mist lilac, or muted rose/paper cream.
- Avoid nearly identical colors or two variants with different visual content.
- If the user explicitly requests one color or one image, honor that request instead of forcing two.

After generation, inspect the result. Make one targeted iteration when any of these fail:

- a source-image result no longer resembles the source's dominant subject, arrangement, or relationship;
- the result invents a hand, object, character, action, text, or symbol not justified by the input;
- the main relation is not understandable in two seconds;
- more than three colors appear;
- linework becomes thin, clean corporate vector art, or childish doodling;
- gradients, shadows, texture, 3D, realism, text, or decorative clutter appear;
- a hand or gesture is present but decorative rather than necessary.

Preserve successful parts during iteration and change only the failing dimension.

## Deliver

Return:

1. colorway A and colorway B, labeled with color names and hex values;
2. the graphic proposition;
3. a one-sentence extraction mapping for image inputs: `retained elements + retained relationship + removed detail`, or a semantic mapping for text inputs: `object + action device + relationship`;
4. the shared final production prompt;
5. both saved paths for project-bound assets.

Keep the explanation compact. The image is the primary deliverable.
