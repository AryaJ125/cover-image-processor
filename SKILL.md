---
name: cover-image-processor
description: "Turn uploaded real photos of 3D-printed models or products into polished cover images while faithfully preserving the subject. Use when the user says phrases such as 按封面处理这几张图片, 按封面处理, 做封面, 优化成封面图, or otherwise asks to convert existing photos into clean studio-style cover images. Default behavior includes a pure white background, premium real-product studio photography, soft directional light, natural grounding shadow, preserved 3D-print texture, 4:3 aspect ratio, and separate output for each uploaded image unless the user explicitly requests a collage or other layout."
---

Apply this workflow to uploaded product or 3D-printed model photos.

## Default cover preset

Unless the user overrides a setting:

- Preserve the model/product shape, proportions, structure, colors, assembly relationships, and main features.
- Do not invent, remove, redesign, or simplify subject details.
- Preserve real material appearance and visible 3D-print/FDM layer texture where present.
- Replace the background with pure white.
- Produce a premium studio product-photo look rather than a pure CGI render.
- Use soft directional lighting with controlled highlights.
- Keep the floor and background naturally continuous.
- Preserve or add a soft natural grounding shadow.
- Keep the composition clean and minimal.
- Use 4:3 by default.

## Shorthand behavior

When the user says “按封面处理这几张图片” or an equivalent shorthand:

1. Apply the default cover preset.
2. Treat every uploaded image as an independent edit target.
3. Generate one result per source image.
4. Keep the visual treatment consistent across the set.
5. Do not create a collage unless explicitly requested.

## Overrides

Honor explicit user instructions first. Common overrides include:

- different background color or gradient
- horizontal, vertical, 1:1, 3:4, or another ratio
- keep the hand, clothing, or environment
- add or remove title text
- warmer or cooler lighting
- preserve the original composition exactly

Keep all non-conflicting default rules.

## Prompt pattern

For a normal white-background cover edit, use wording equivalent to:

“Reference the uploaded real photo. Preserve the model/product itself, including its shape, colors, structure, proportions, and key features. Do not redesign or randomly alter the object. Change the background to pure white and optimize the image into a premium studio product-photo look. Preserve real material detail, visible 3D-print texture, and natural shadow information. Use soft directional lighting, a clean composition, a natural ground-to-background transition, and a soft grounding shadow. Keep the result bright, tidy, realistic, and faithful to the source. Use a 4:3 aspect ratio.”

## Multi-image handling

For multiple uploaded images:

- edit each image separately
- preserve the original view and subject arrangement of each source unless asked otherwise
- maintain consistent white balance, lighting softness, background treatment, and overall finish across the set

## Quality check

Before finalizing, verify:

- no important model parts changed unexpectedly
- colors still match the real object
- print texture is not over-smoothed
- shadows look physically plausible
- the object feels photographed, not re-rendered from scratch
- output ratio matches the requested ratio
