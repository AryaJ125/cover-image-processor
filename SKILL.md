---
name: cover-image-processor
description: "Turn uploaded real photos of 3D-printed models or products into polished studio-style cover images and related marketing visuals. Use when the user says phrases such as 按封面处理这几张图片, 按封面处理, 做封面, 优化成封面图, 生成标题图, 继续做场景图, 胸针穿戴图, or otherwise wants a reusable 3D-print product-cover workflow. Default cover behavior includes a pure white background, premium real-product studio photography, soft directional light, natural grounding shadow, preserved 3D-print texture, 4:3 aspect ratio, and separate output for each uploaded image unless the user explicitly requests a collage or other layout. The workflow can extend from cover cleanup into title covers, lifestyle/wearing images, and detail showcase images."
---

Apply this workflow to uploaded product or 3D-printed model photos.

## What this skill does

This skill is not only for white-background cleanup. It is a reusable **3D print product-cover workflow** with four layers:

1. **Base cover cleanup**  
   Convert a real product photo into a clean premium studio-style cover image.
2. **Title cover generation**  
   Build a finished cover with headline text and layout.
3. **Lifestyle / wearing scene generation**  
   Place the product into a realistic usage context while keeping the product faithful.
4. **Detail showcase generation**  
   Present structure, components, accessories, assembly, or back-side details clearly.

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

## Output modes

### Mode A. Base cover cleanup

Use this when the user says things like:

- 按封面处理这几张图片
- 按封面处理
- 做封面
- 优化成封面图

Behavior:

1. Apply the default cover preset.
2. Treat every uploaded image as an independent edit target unless the user wants a combined layout.
3. Generate one result per source image.
4. Keep the visual treatment consistent across the set.
5. Do not create a collage unless explicitly requested.

### Mode B. Title cover generation

Use this when the user asks for:

- 标题图
- 标题封面
- 加标题
- 生成封面标题

Rules:

- Use the cleaned cover image or the uploaded subject as the main visual.
- Preserve the object faithfully.
- Add a clear, readable headline.
- Favor large title text, cute or product-appropriate typography, and supportive color blocks when suitable.
- Keep the layout clean and commercially usable.
- Do not let decorations overpower the product.
- If the user provides exact title text, render that exact text.
- If the user only says “加标题”, infer a concise product title from context.

### Mode C. Lifestyle / wearing scene generation

Use this when the user asks for:

- 场景图
- 穿戴图
- 佩戴效果图
- 使用场景图

Rules:

- Preserve the product itself, including shape, color, structure, and material feel.
- Place it into a realistic scene appropriate to the product type.
- For brooches or wearable pieces, default to gentle modern everyday clothing unless told otherwise.
- Keep the outfit natural, soft, and contemporary rather than formal costume-heavy styling.
- Avoid obviously artificial background lighting unless the user explicitly wants a dramatic setup.
- Let the scene support the product rather than distract from it.

### Mode D. Detail showcase generation

Use this when the user asks for:

- 细节图
- 展示图
- 装配图
- 零件图
- 背针图

Rules:

- Show components, structure, attachment methods, accessories, or important features clearly.
- Prefer clean white or simple backgrounds.
- Keep product fidelity high.
- Use a neat, commercial presentation style.
- If the user wants multiple angles or a layout showing parts, create a tidy composition that clearly separates and labels visual priorities.

## Workflow chaining

When the user asks for a broader workflow such as:

- 按封面流程处理
- 按封面处理，并继续生成标题图和场景图
- 先按封面处理，再做标题图/穿戴图/细节图

Interpret this as a chained workflow:

1. First create the cleaned studio-style base cover.
2. Then use that result as the visual anchor for later outputs.
3. Extend into any requested title cover, lifestyle image, or detail showcase.
4. Keep the object identity, colors, and overall look consistent across the series.

## Overrides

Honor explicit user instructions first. Common overrides include:

- different background color or gradient
- horizontal, vertical, 1:1, 3:4, or another ratio
- keep the hand, clothing, or environment
- add or remove title text
- warmer or cooler lighting
- preserve the original composition exactly
- modern gentle casual outfit for lifestyle images
- no obvious spotlight or stage lighting
- left-side title layout / centered layout / blank title area

Keep all non-conflicting default rules.

## Prompt pattern

### Base cover prompt pattern

Use wording equivalent to:

“Reference the uploaded real photo. Preserve the model/product itself, including its shape, colors, structure, proportions, and key features. Do not redesign or randomly alter the object. Change the background to pure white and optimize the image into a premium studio product-photo look. Preserve real material detail, visible 3D-print texture, and natural shadow information. Use soft directional lighting, a clean composition, a natural ground-to-background transition, and a soft grounding shadow. Keep the result bright, tidy, realistic, and faithful to the source. Use a 4:3 aspect ratio.”

### Title cover prompt pattern

Use wording equivalent to:

“Use the cleaned cover image or uploaded subject as the main product visual. Preserve the product faithfully. Create a polished title cover with clean commercial layout and clear hierarchy. Add the exact title text provided by the user. Make the title large and readable. Use a cute or product-appropriate style, optional supportive color blocks, and minimal decorative elements that match the product. Keep the composition clean and suitable for a product cover.”

### Lifestyle / wearing prompt pattern

Use wording equivalent to:

“Place the product into a realistic lifestyle or wearing scene while preserving the product itself faithfully. Keep the object’s shape, colors, structure, and texture consistent with the source. Use a gentle modern everyday outfit and a soft unobtrusive background unless the user specifies otherwise. Avoid dramatic visible lighting effects. Make the scene feel natural, warm, and commercially appealing.”

### Detail showcase prompt pattern

Use wording equivalent to:

“Create a detail showcase image for this product. Preserve the product faithfully. Clearly show the important structure, components, accessories, or back-side details. Keep the composition clean and easy to read, with a simple background and a polished product-presentation style.”

## Multi-image handling

For multiple uploaded images:

- edit each image separately for base cover cleanup unless asked to combine them
- preserve the original view and subject arrangement of each source unless asked otherwise
- maintain consistent white balance, lighting softness, background treatment, and overall finish across the set
- if the user asks for a series of follow-up outputs, use the strongest cleaned image as the anchor when needed for consistency

## Recommended user commands

Examples of natural-language triggers this skill should handle well:

- 按封面处理这几张图片
- 按封面处理，并生成标题图
- 先按封面处理，再做穿戴图
- 做一个标题封面，标题是“猫耳马蹄莲胸针”
- 继续生成胸针穿戴图，现代温柔一点
- 再做一张细节展示图，把零件和背针展示清楚
- 这一组图按封面流程全做：白底封面、标题图、场景图、细节图

## Quality check

Before finalizing, verify:

- no important model parts changed unexpectedly
- colors still match the real object
- print texture is not over-smoothed
- shadows look physically plausible
- the object feels photographed, not re-rendered from scratch
- output ratio matches the requested ratio
- title text, if requested, is correct and readable
- scene images support the product instead of overpowering it
- detail images clearly show the intended parts or features
