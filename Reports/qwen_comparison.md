# VLM GEval Image-Centric Report

_Last updated: 2026-05-02T20:47:50_

## Image 1: f244.png

**Actual answer:** Somewhat. The front wheel appears distorted and unnaturally angled, and the reflection on the car’s door is inconsistent with the background, making the image look slightly unrealistic.

| Model | Model Answer | Image GEval Score | Model Overall GEval | Model Variance | GEval Reasoning |
|---|---|---:|---:|---:|---|
| Qwen3-VL-8B-Thinking | No, the image appears to be a realistic photograph of a car with natural lighting, detailed reflections, and plausible background elements like a crowd and grassy area without obvious AI artifacts. | 1.100 | 3.483 | 2.006 | The verdicts are opposite (Somewhat vs No); the human identifies distortion of the front wheel and inconsistent reflection, while the VLM claims natural lighting and detailed reflections, indicating a significant disagreement. |
| Qwen3-VL-8B-Thinking-FT | No, the car's body and wheel details appear realistic with plausible reflections and shadows, indicating a genuine photograph. | 3.800 | 3.734 | 1.886 | The verdicts disagree on the realism of the car image, but the human's identified distortion in the wheel and reflection inconsistency are not acknowledged by the VLM which identifies the image as realistic. |

## Image 2: f126.png

**Actual answer:** No, there is nothing unrealistic in this image. The leaf and the background both appear natural and visually consistent.

| Model | Model Answer | Image GEval Score | Model Overall GEval | Model Variance | GEval Reasoning |
|---|---|---:|---:|---:|---|
| Qwen3-VL-8B-Thinking | No, the leaf’s natural texture, realistic vein patterns, and organic interaction with the wooden surface all indicate a genuine photograph without AI-generated artifacts. | 4.100 | 3.483 | 2.006 | The verdicts agree, and the VLM identifies the realistic texture, veins, and interaction with the surface, covering the core artifacts mentioned by the human. |
| Qwen3-VL-8B-Thinking-FT | No, the image shows a naturally occurring maple leaf with realistic vein patterns, natural color gradients, and organic textures on wooden surface, lacking any telltale signs of artificial manipulation. | 4.800 | 3.734 | 1.886 | The verdicts align on the realism of the leaf image, with the VLM accurately identifying realistic leaf vein patterns, natural colors, and textures, matching the human's assessment of naturalness. |

## Image 3: r3.png

**Actual answer:** No, there is nothing unrealistic in this image. All objects, people, and buildings appear normal and proportionate, with smooth transitions and no obvious distortions.

| Model | Model Answer | Image GEval Score | Model Overall GEval | Model Variance | GEval Reasoning |
|---|---|---:|---:|---:|---|
| Qwen3-VL-8B-Thinking | No, the cobblestone pattern in the foreground is too uniform and lacks natural irregularities typical of realworld stone paving. | 3.000 | 3.483 | 2.006 | The verdicts agree, but the VLM identifies the cobblestone pattern as unrealistic due to uniformity, while the human states all objects appear normal, disagreeing on the artifact. |
| Qwen3-VL-8B-Thinking-FT | No, the image depicts a realistic urban scene with no obvious AI-generated artifacts such as inconsistent textures, unnatural perspective, or repetitive elements. | 4.800 | 3.734 | 1.886 | The verdicts align on the realism of the urban scene, with the VLM correctly identifying the absence of AI artifacts such as inconsistent textures or unnatural perspectives, matching the human's judgment. |

## Image 4: f145.png

**Actual answer:** Somewhat. The crowd in the background looks blurry and unnaturally merged together, and some people's faces and bodies lack clear details or appear distorted.

| Model | Model Answer | Image GEval Score | Model Overall GEval | Model Variance | GEval Reasoning |
|---|---|---:|---:|---:|---|
| Qwen3-VL-8B-Thinking | No, the scene maintains natural human diversity and consistent environmental details, with no obvious signs of artificial repetition or structural inconsistencies. | 1.100 | 3.483 | 2.006 | The verdicts are opposite (Somewhat vs No); the human notes blurry crowd, distorted faces/bodies, while the VLM claims natural diversity and consistent details, leading to a strong disagreement. |
| Qwen3-VL-8B-Thinking-FT | No, the scene appears naturally composed with realistic human activity and natural elements. | 3.900 | 3.734 | 1.886 | The verdicts disagree on the realism of the image with a crowd, and VLM does not address the blurriness and distortion noted in the human explanation. |

## Image 5: f170.png

**Actual answer:** Yes. The giraffe's neck is unusually long and distorted, making the proportions unrealistic compared to a real giraffe; its body-to-neck transition is not smooth.

| Model | Model Answer | Image GEval Score | Model Overall GEval | Model Variance | GEval Reasoning |
|---|---|---:|---:|---:|---|
| Qwen3-VL-8B-Thinking | No, the giraffe’s natural proportions, consistent spot pattern, and realistic integration with the savanna environment suggest it is a genuine photograph. | 1.100 | 3.483 | 2.006 | The verdicts are opposite (Yes vs No); the human mentions the giraffe’s unusually long and distorted neck, whereas the VLM finds natural proportions and a consistent spot pattern, representing a significant disagreement. |
| Qwen3-VL-8B-Thinking-FT | No, the giraffe's natural patterns and proportions appear realistic, with no obvious signs of artificial artifacts. | 2.300 | 3.734 | 1.886 | The verdicts are contradictory about the giraffe image; the human identified an unusually long and distorted neck, while the VLM claimed natural proportions and no artifacts, thus disagreeing on the single subject's critical attribute. |
