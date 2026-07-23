# Production prompt and QA

## Prompt template

```text
Use case: stylized-concept
Asset type: conceptual editorial illustration / visual icon
Input mode: {source-image extraction | text-to-concept}
Input image role: {content and composition reference; omit when no image}
Primary request: Compress "{graphic proposition}" into one text-free conceptual image.
Source facts: {dominant subject, supporting element, spatial arrangement, actual interaction, repeated motif; omit for text-only input}.
Preserve: {recognizable silhouettes, relative positions, scale, direction, crop, actual relationship}.
Simplify/remove: {photographic texture, lighting, incidental scenery, nonessential text/logo, clutter}.
Subject: {one or two core elements}; use {existing pose, position, deformation, connector, motion path, tool, or justified hand} to express "{core relationship}".
Style/medium: minimalist thick-line hand-drawn graphic; restrained, intelligent, human; neither a children's doodle nor a polished corporate vector icon.
Composition/framing: {source-preserving or standard composition}; retain the source's dominant arrangement when an image is supplied; main subject fills 55%–75% of the canvas; generous quiet margin; make the original subject or core relationship readable at a glance.
Color palette: one perfectly flat {background name} background {HEX}; near-black #141413 linework; warm-white #FAF9F6 solid geometric masses; three colors maximum.
Colorway delivery: render this exact composition as A using {background A name} {HEX A}, then derive B by replacing only the background with {background B name} {HEX B}; keep every object, line, proportion, and crop identical.
Line language: stroke width about 1.4%–2.2% of the short edge; rounded caps and joins; controlled natural wobble; nearly constant width; continuous one-stroke feeling.
Shape language: reduce the source to circles, squares, triangles, steps, irregular paper shapes, simplified silhouettes, dots, and connectors; use a soft hand gesture only when justified.
Rhythm: one large mass, one medium relationship, and three to five small repeated units; information density 25%–40%.
Constraints: do not invent a hand, character, object, action, arrow, text, or symbol absent from or unnecessary to the input; no text unless explicitly required; no gradients; no shadows; no texture; no 3D; no realistic perspective; no decorative mini-icons; use no more than two semantic cores and one relationship system, while preserving a necessary source collection or framed scene as one core; no watermark.
Avoid: unrelated metaphors, content drift from the source, perfect vector geometry, thin corporate line icons, glossy UI style, photorealism, childish doodles, decorative clutter, random symbols.
```

Use the user's exact concept; do not add unrelated characters, objects, slogans, brands, or narrative beats.

## Selection examples

### Source image: dithered snowy landscape with one tree and a four-square mark

- Proposition: Preserve the solitary tree inside a simplified snow field.
- Retain: the tree as dominant subject, snow as the surrounding mass, the four-square motif, and the source's left/right balance.
- Remove: halftone, photographic lighting, distant incidental scenery, and nonessential text.
- Action device: none; the source does not require a hand or invented action.
- Template/color: Source-preserving; fog blue `#7497B9`.

### "AI makes complex work simple"

- Proposition: Compress complexity into clear modules.
- Object: a dense five-node network and two warm-white paper blocks.
- Action device: a narrowing connector turns the network into an ordered pair.
- Relationship: dense network becomes clear modules.
- Template/color: Transform; fog blue `#7497B9`.

### "Slow is fast"

- Proposition: Patient steps create durable progress.
- Object: three warm-white steps.
- Action device: a looping line lands on successive steps.
- Relationship: three controlled arcs land on successive steps.
- Template/color: Transform; moss green `#7D8C63`.

### "Build trust"

- Proposition: Two sides create one reliable connection.
- Object: two warm-white nodes.
- Action device: the nodes move into alignment.
- Relationship: a single short black link forms between them.
- Template/color: Co-create; dusty blush `#E6D0CF`.

### "Protect your attention"

- Proposition: Keep one focus safe from outside noise.
- Object: one warm-white circle inside a house or bracket.
- Action device: the bracket closes the vulnerable side.
- Relationship: outside node lines stop at the boundary.
- Template/color: Container; mist lilac `#CBCAD9`.

## QA checklist

- One dominant judgment is visible.
- For source-image work, the dominant subject, direction, relative positions, and relationship remain recognizable.
- No hand, character, object, action, text, or symbol has been invented without justification.
- Comparison-board labels, logos, split bars, watermarks, and explanatory overlays from calibration assets have not leaked into the output.
- The palette has no more than three colors and uses exact system colors.
- Colorways A and B share identical geometry and differ only in their clearly distinct background colors.
- The background is perfectly flat and texture-free.
- Lines are thick, near-black, round-ended, and slightly imperfect.
- Geometry and simplified source silhouettes carry the subject; an optional action device carries only a real or requested action.
- Any hand present is necessary, meaningful, and consistent with the source or explicit concept.
- Three to five repeats create rhythm.
- The main subject, margins, and negative space follow the style guide.
- No text, gradient, shadow, 3D, realism, or decorative clutter appears.
- The relation remains understandable when the title is hidden.

Reject a result that matches the palette and line style but changes the source's actual subject, arrangement, or relationship. Also reject a text-only result whose core relationship is unclear.

## Iteration guidance

Change one variable at a time:

- weak source recognition → restore the dominant silhouette, position, direction, or repeated motif;
- invented content → remove the unsupported hand, character, object, action, text, or symbol;
- unclear meaning → simplify the metaphor or strengthen the actual object relationship;
- decorative hand → remove it; retain it only when it performs a source-grounded or explicitly requested action;
- visual clutter → remove secondary objects and relationship systems;
- corporate vector look → increase controlled wobble and continuous curves;
- childish look → reduce exaggeration and random irregularity;
- weak rhythm → introduce one repeated unit three to five times;
- wrong palette → restore exact background, line, and fill colors.
