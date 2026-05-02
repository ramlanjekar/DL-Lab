# VLM GEval Image-Centric Report

_Last updated: 2026-04-15T23:06:08_

## Image 1: f244.png

**Actual answer:** Somewhat. The front wheel appears distorted and unnaturally angled, and the reflection on the car’s door is inconsistent with the background, making the image look slightly unrealistic.

| Model | Model Answer | Image GEval Score | Model Overall GEval | Model Variance | GEval Reasoning |
|---|---|---:|---:|---:|---|
| InternVL3-14B | No, the image appears realistic with natural reflections and details typical of a high-quality photograph of a car. | 1.200 | 3.102 | 2.771 | The verdicts are opposite (Somewhat vs No), and VLM fails to identify the distorted wheel and reflection inconsistency. |
| InternVL3-14B-FT | Somewhat. The car's wheels and side mirrors appear slightly distorted and unnatural, and the transition between the car and the background is not smooth, suggesting possible digital manipulation. | 4.300 | 3.906 | 1.362 | The verdicts agree, and the VLM identifies the wheel distortion, though mentions side mirrors as an extra artifact, resulting in a high score. |

## Image 2: f126.png

**Actual answer:** No, there is nothing unrealistic in this image. The leaf and the background both appear natural and visually consistent.

| Model | Model Answer | Image GEval Score | Model Overall GEval | Model Variance | GEval Reasoning |
|---|---|---:|---:|---:|---|
| InternVL3-14B | No, the leaf and background appear natural with realistic lighting and texture. | 4.100 | 3.102 | 2.771 | The verdicts agree, and the VLM correctly identifies the leaf and background as natural with realistic features. |
| InternVL3-14B-FT | No, there is nothing unrealistic in this image. The leaf and background appear natural and well-rendered. | 5.000 | 3.906 | 1.362 | Both the human and VLM agree that there is nothing unrealistic in the image, and they both mention the leaf and background, leading to a perfect score. |

## Image 3: r3.png

**Actual answer:** No, there is nothing unrealistic in this image. All objects, people, and buildings appear normal and proportionate, with smooth transitions and no obvious distortions.

| Model | Model Answer | Image GEval Score | Model Overall GEval | Model Variance | GEval Reasoning |
|---|---|---:|---:|---:|---|
| InternVL3-14B | No, the image appears to be a realistic urban scene with no obvious signs of artificiality or anomalies. | 4.100 | 3.102 | 2.771 | The verdicts agree, and the VLM correctly identifies the urban scene as realistic with no anomalies. |
| InternVL3-14B-FT | Somewhat. The transition between the sidewalk and the street appears unnatural, with an abrupt change in texture and color, and the street markings look oddly distorted. | 2.600 | 3.906 | 1.362 | The verdicts disagree (No vs. Somewhat); VLM identifies a different artifact (sidewalk and street transition) which is not what the human identified as unrealistic, incurring a penalty. |

## Image 4: f145.png

**Actual answer:** Somewhat. The crowd in the background looks blurry and unnaturally merged together, and some people's faces and bodies lack clear details or appear distorted.

| Model | Model Answer | Image GEval Score | Model Overall GEval | Model Variance | GEval Reasoning |
|---|---|---:|---:|---:|---|
| InternVL3-14B | No, the image appears to be a natural scene with people and trees, showing no obvious signs of artificiality or unrealistic elements. | 1.200 | 3.102 | 2.771 | The verdicts are opposite (Somewhat vs No), and the VLM fails to identify the blurry and distorted crowd. |
| InternVL3-14B-FT | No, there is nothing unrealistic in this image. The scene appears natural, with people, trees, and buildings all proportionate and consistent with a real park setting. | 1.300 | 3.906 | 1.362 | The verdicts directly contradict (Somewhat vs. No); since the verdicts are opposite, the score is low. |

## Image 5: f170.png

**Actual answer:** Yes. The giraffe's neck is unusually long and distorted, making the proportions unrealistic compared to a real giraffe; its body-to-neck transition is not smooth.

| Model | Model Answer | Image GEval Score | Model Overall GEval | Model Variance | GEval Reasoning |
|---|---|---:|---:|---:|---|
| InternVL3-14B | No, the image appears natural with realistic lighting and texture on the giraffe and background. | 1.200 | 3.102 | 2.771 | The verdicts are opposite (Yes vs No), and VLM fails to identify the giraffe's unnatural neck proportions. |
| InternVL3-14B-FT | No, there is nothing unrealistic in this image. The giraffe and its surroundings appear natural and consistent with a typical savanna environment. | 1.200 | 3.906 | 1.362 | The verdicts contradict (Yes vs No) and the VLM misses the core artifact; therefore, a low score is given. |

