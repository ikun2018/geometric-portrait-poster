---
name: geometric-portrait-poster
description: Create clean, high-contrast geometric portrait posters from an uploaded portrait or a text-only character description. Use when the user asks for an angular polygon portrait, WPAP-inspired poster, faceted vector-style avatar, or a portrait in selectable color palettes such as 色卡 01 / 色卡 02 / 如图.
---

# Geometric Portrait Poster

Create a graphic portrait made of deliberate, flat, hard-edged polygon facets. Preserve the subject's recognizable face, pose, accessories, and clothing silhouette; make the facets explain the form rather than obscure it.

## Input modes

### Uploaded portrait

Treat the supplied image as the identity and composition reference. Preserve age, gender presentation, facial proportions, hairstyle, eyewear, facial hair, and defining accessories. Use a head-and-shoulders crop unless the user requests another framing.

If the user has not already specified a color treatment, respond with the short palette menu below and wait for their choice. Do not generate yet.

> 选一个色卡：01 紫蓝霓虹（如图）、02 复古暖色、03 青橙电影感、04 黑白编辑感、05 从原图提取配色。也可以告诉我“如图”或自定义颜色。

Map “如图”, “参考图那样”, or “第一张那样” to 色卡 01, unless the user clearly indicates another image.

### Text-only generation

Use the user's character description as the identity brief. If they did not choose a palette, use 色卡 01 by default and state that choice concisely before generating.

## Palette menu

Read [references/palettes.md](references/palettes.md) before generating. Keep the palette deliberately limited: 5–8 dominant colors plus near-black shadows and a white contour where applicable.

## Generation rules

Use image generation. Write a compact, precise prompt that includes the following.

1. **Geometry:** large-to-medium irregular polygons with straight hard edges; a few small facets only at high-information features such as the eyes, nose, mouth, glasses, and hairline.
2. **Structure:** organize facets along facial planes, not in a random mosaic. Keep the eye line, nose bridge, mouth shape, jaw, and neck readable at thumbnail size.
3. **Graphic finish:** flat vector-like fills; no gradients, watercolor, airbrush, texture, grain, photoreal skin, or 3D low-poly rendering.
4. **Outline:** use a thick, clean white outer contour for 色卡 01 or when requested. Keep internal linework minimal and near-black.
5. **Composition:** use a black or otherwise solid background; allow a three-quarter portrait by default. Crop intentionally at the shoulders or chest.
6. **Control:** avoid arbitrary triangles, fragmented facial features, duplicated glasses, melted hands, illegible clothing, text, logos, and AI color blotches.

For an uploaded photo, explicitly say: “preserve the subject's exact recognizable identity and pose from the reference image.”

## Prompt skeleton

Adapt this rather than copying it blindly:

```text
Create a clean graphic geometric portrait poster of [subject]. Preserve [identity details and pose] from the reference. Three-quarter head-and-shoulders composition on a solid [background] background. Render the face, hair, glasses/accessories, neck, and jacket as intentional flat irregular polygon facets that follow real facial planes. Use [palette]. Keep high information around the eyes, nose bridge, mouth, hairline, and jaw; use larger calm facets elsewhere. [Use a bold clean white exterior contour.] Crisp vector-poster finish, hard edges, no gradients, no texture, no random mosaic, no low-poly 3D, no text, no logo, no color noise.
```

## After generating

Present the image without a long explanation. If the user asks for a revision, retain the established identity, framing, and palette unless they explicitly request a change. Translate common requests as follows:

- “更像本人” → reduce face fragmentation; strengthen eye, nose, mouth, jaw, hairstyle, and glasses landmarks.
- “不要那么乱” → use fewer, larger facets across cheeks, jacket, and background.
- “更有冲击力” → raise contrast only at focal features; do not add random colors.
- “更像矢量” → remove shading artifacts and gradients; enforce clean flat fills.
