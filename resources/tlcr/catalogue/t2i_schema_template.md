Here is my Prompt:



---

Here is my template:

# 🎨 T2I Schema Template — <% tp.file.title %>

> This document standardizes your text-to-image prompt 
> into structured nodes for most vision models.

---

## 🧠 **1. Rendered Table**

> The **Rendered Table** is a visual, human-readable breakdown of your prompt.  

| **Node Category**                                 | **Keywords / Elements**        | **Tags**                                                  |
| ------------------------------------------------- | ------------------------------ | --------------------------------------------------------- |
| 🧠 **WHO — The Cast / Node**                      | - {{who_elements}}             | #actor, #subject                                          |
| 🧍‍♀️ **FOCUS CHARACTER — Main Character / Node** | - {{focus_character_elements}} | #appearance, #face, #hair, #eyes, #body, #clothing, #pose |
| 🎬 **WHAT — Activity / Node**                     | - {{what_elements}}            | #pose, #camera, #action                                   |
| 🌆 **WHERE — Location Setting / Node**            | - {{where_elements}}           | #environment, #background, #time                          |
| 💭 **WHY — Catalyst / Node**                      | - {{why_elements}}             | #mood, #lighting, #emotion, #tone                         |
| 🎥 **SCENE SETTING — Render Style / Node**        | - {{scene_elements}}           | #render, #lighting, #camera, #style, #quality             |
| 🧩 **LORA / MODEL INFLUENCE — Node**              | - {{lora_elements}}            | #model, #style, #lighting                                 |

---

## 🧱 **2. Structured Prompt**
> A prompt with a hippo as a super hero.

```markdown
Hippo, superhero, funny animal, animal, flying hero [BREAK]

dressed as a superhero, flying over a city skyline, selfie, looks directly in cam, fish eye view, funny pose, funny, weird, head slightly tilted, sitting on traffic light [BREAK]

flying over city, taking selfie, sitting on traffic light, head slightly tilted, funny pose [BREAK]

city skyline, urban scene, high above ground, traffic light setting [BREAK]

funny, weird, playful, humorous, creative, cartoonish energy [BREAK]

Hyper-realistic, 16k resolution, intricate details, (masterpiece, award winning artwork), many details, extreme detailed, full of details, Wide range of colors, high Dynamic, dynamic lighting [BREAK]

<lora:ral-drp:0.35> ral-drp <lora:WildcardX-XL-Detail-Enhancer:0.95> <lora:xl_more_art-full_v1:0.285> <lora:zavy-bcklt-sdxl:0.25> zavy-bcklt <lora:RMSDXL_Creative:0.24> <lora:add-detail-xl:1> <lora:MJ52:0.285>
```


---

Acknowledge this instruction and wait for further input!