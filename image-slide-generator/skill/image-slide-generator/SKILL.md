---
name: image-slide-generator
description: create standardized presentation slides as complete generated images using ChatGPT image generation, not traditional PPTX, PDF, document, canvas, or slide tools. Use when the user wants a pitch deck, lesson, webinar, sales deck, training deck, carousel, or visual presentation where every slide must be rendered as one finished image containing its own layout, typography, graphics, and exact slide text. Always guide the user through style, aspect ratio, slide planning, master prompt approval, and sequential image generation. Especially use for presentations built from pasted text, PDFs, notes, transcripts, briefs, or uploaded images that must be preserved faithfully inside image-based slides.
---

# Image Slide Generator

## Non-Negotiable Output Rule

Create presentation slides as final, complete, image-generated slide canvases. Each generated image must be the entire slide, including:

- background
- layout
- title and body text
- typography
- icons, shapes, charts, or visual motifs
- embedded or treated user-provided images
- all final visual composition

Never generate only a decorative illustration, generic AI background, stock-like image, or visual asset to be placed later inside a presentation. The image itself is the slide.

Do not create PowerPoint, Google Slides, PDF, DOCX, HTML, canvas, or traditional slide artifacts unless the user explicitly asks for an additional export after the image slides already exist. If the user mentions that the images will later be combined in an external tool, do not create that external file yourself.

## Required Tool Behavior

Use ChatGPT image generation for the final slide images. Do not use traditional slide/document/PDF tools to lay out text or create a deck.

When generating, make the prompt explicitly request a finished presentation slide image with the approved text rendered inside the image. The image prompt must not ask for a generic illustration about the slide topic.

Use the current conversation to conduct planning and approval. Only generate images after the required approvals have happened.

## Required Workflow With Approval Gates

Follow this workflow in order. Do not skip approval gates unless the user explicitly says to skip approvals, generate directly, or proceed without review.

1. Intake the source material.
2. Ask for or infer the objective, audience, language, and aspect ratio.
3. Propose 2 or 3 complete visual directions if the user has not already defined the style.
4. Get approval for style and aspect ratio.
5. Build a slide-by-slide content plan.
6. Get approval for the slide plan.
7. Create a reusable master prompt record.
8. Get approval for the master prompt.
9. Generate slide images sequentially, one slide at a time.
10. After each image, ask whether to approve, revise, or continue, unless the user explicitly requested batch generation.

If the user starts by uploading a PDF, pasted text, transcript, or rough notes and asks to make a presentation, first extract and structure the content. Do not immediately generate images.

If the user says the skill is selected or asks to use this skill, treat that as a request to run this workflow, not as permission to skip the workflow.

## Step 1: Intake Source Material

Accept any of these inputs:

- PDF containing text
- full presentation text
- rough notes or outline
- sales copy
- training material
- transcript from a call, class, webinar, or meeting
- a partially developed slide list
- uploaded images to include in slides
- a brief topic plus desired outcome

Clarify only what is necessary. At minimum, establish:

- presentation goal
- audience
- output language
- aspect ratio
- desired number of slides, if known
- brand, color, typography, or visual constraints
- whether uploaded images are source images to preserve or only references

If the user does not know the style, suggest options. Do not force the user to define fonts, palettes, and layout systems from scratch.

## Step 2: Propose Style Directions

Based on the material and audience, propose 2 or 3 visual directions. Each option should be concise but operational enough to become a master prompt.

Each option should include:

- visual mood
- typography direction
- color palette
- layout system
- title/header behavior
- body text behavior
- image treatment
- best use case

Example:

```markdown
Opção A: consultoria premium escura
- Fundo: grafite/preto com gradientes sutis
- Tipografia: sans-serif editorial, títulos grandes e fortes, corpo de texto curto e legível
- Paleta: preto, branco, cinza, azul elétrico como acento
- Layout: grid limpo, bastante respiro, poucas frases por slide
- Imagens: recortes limpos, integração com sombras, máscaras e gradientes
- Melhor para: pitch estratégico, proposta executiva, autoridade
```

Ask the user to choose, combine, or modify one direction. Do not generate images before style and aspect ratio are approved.

## Step 3: Build the Slide Plan

Transform the content into a slide-by-slide plan. Adapt the number of slides to preserve legibility.

Rules:

- Prefer more slides with less text over fewer crowded slides.
- Keep each slide focused on one idea.
- Use short titles, strong hierarchy, and minimal body text.
- Split long passages across multiple slides.
- Preserve the user's exact wording when the wording matters.
- Do not invent claims, statistics, names, or data not present in the source unless the user asks for development or copywriting.
- Do not force a rigid slide structure; choose the layout that fits each slide's purpose.

For each slide, list:

- slide number
- slide role or objective
- exact text to appear in the generated image
- visual idea
- image usage, if any
- layout or emphasis notes

Get approval before creating the master prompt.

## Text Density Rules

Image-generated slides become unreliable when overloaded with text. When source material is long:

- split into more slides
- convert paragraphs into concise slide copy
- use hierarchy: title, subtitle, 2 to 4 supporting points
- avoid small labels unless essential
- avoid dense tables and complex diagrams
- warn the user when content should be split

Never silently cram long text into one image.

## Step 4: Create the Master Prompt Record

Create a reusable master prompt for the whole presentation. This is the visual contract for all slide images.

The master prompt must define:

- aspect ratio and output as a complete slide image
- global visual direction
- typography rules
- color palette
- layout system and grid behavior
- title/header rules
- footer, page number, logo, or recurring elements, if any
- spacing and density rules
- image treatment rules
- icon, illustration, texture, shadow, and gradient rules
- text rendering rules
- negative constraints
- consistency instruction

Show the master prompt to the user in a clearly labeled section so it can be reused later to create additional slides in the same presentation.

Get approval before generating the first slide image.

## Master Prompt Template

Use and adapt this template:

```markdown
MASTER PROMPT DA APRESENTAÇÃO

Crie uma imagem única que seja um slide completo de apresentação em [aspect ratio]. O slide inteiro deve ser renderizado como uma imagem final, incluindo layout, fundo, tipografia, texto, elementos gráficos e imagens integradas. Não crie uma ilustração genérica; crie o slide pronto.

Identidade visual geral:
[estética, atmosfera, sofisticação, referências visuais permitidas]

Tipografia:
[estilo de fonte, pesos, escala de título/subtítulo/corpo, caixa alta/baixa, comportamento de linhas]

Paleta:
- Fundo: [cor/gradiente/textura]
- Texto principal: [cor]
- Texto secundário: [cor]
- Acentos: [cores]
- Elementos gráficos: [cores]

Sistema de layout:
[grid, margens, alinhamento, composição, hierarquia, respiro, densidade máxima]

Cabeçalhos e títulos:
[posição, tamanho, estilo, separadores, numeração, recorrências]

Tratamento de imagens:
[integração com layout, recorte, sombra, gradiente, P&B, duotone, fundo removido, molduras]

Regras de texto:
Renderize dentro da própria imagem somente o texto especificado para o slide. Não adicione texto extra, slogans, marcas d'água, legendas inventadas ou pseudo-texto. Garanta alta legibilidade, contraste e hierarquia. Se o texto estiver longo demais para o slide, não comprima; avise e proponha dividir em mais slides.

Consistência:
Todos os slides devem parecer parte da mesma apresentação. Mantenha a mesma paleta, espaçamento, tipografia, atmosfera, qualidade gráfica e sistema visual.

Evitar:
PowerPoint tradicional, layouts genéricos de template, ilustrações soltas, imagens decorativas sem texto, mockups aleatórios, texto ilegível, pseudo-texto, lorem ipsum, excesso de elementos, ícones inconsistentes, marcas d'água e qualquer arquivo PPTX/PDF/DOCX.
```

## Step 5: Create Slide-Specific Image Prompts

For each slide, combine the approved master prompt with the approved slide-specific content.

Each slide image prompt must include:

- slide number
- slide role
- exact text to render inside the image
- layout composition for this slide
- visual elements and hierarchy
- required image handling instructions
- negative constraints for this slide

Use explicit language like:

```markdown
Gere uma imagem que seja o slide completo, não uma ilustração de apoio. Todo o texto abaixo deve aparecer renderizado dentro da imagem com alta legibilidade.
```

Do not rely on slide 1 as the universal visual reference. The master prompt is the main consistency anchor. Slide 1 may be a cover and may not contain all visual patterns used later.

## Step 6: Generate Images Sequentially

Generate one slide image at a time unless the user explicitly requests batch generation.

Default behavior:

- Generate slide 1 as a complete image slide.
- Ask if the user approves, wants revisions, or wants to continue.
- If revision is requested, revise only that slide while preserving the approved master prompt.
- If approved, continue to the next slide.
- Keep the master prompt active for every slide.

Do not create any presentation file after generating images unless the user explicitly asks for that separate artifact. The default final deliverable is the set of generated slide images only.

## Uploaded Image Handling

Treat user-provided images as source material to preserve unless the user clearly says they are only references.

If the user uploads or attaches an image and does not say it is merely a reference:

- preserve identity, structure, composition, characters, objects, logos, products, screenshots, and key visual details
- do not reinvent, redraw, replace, or create a similar-looking substitute
- use the actual uploaded image as the source to integrate into the slide
- keep people, characters, products, logos, screenshots, and objects faithful to the provided image

Allowed transformations for layout integration:

- crop or reposition
- remove or simplify background
- add gradient overlays
- add shadows, masks, frames, or depth effects
- convert to black and white, duotone, or palette-matched color treatment
- blend into the slide background
- use as a texture or partially transparent visual element

These transformations must support the slide design without changing the image's core subject or identity.

If the user says the image is only a reference, then use it only as stylistic or conceptual inspiration.

## What Not To Do

Never do any of the following unless the user explicitly asks after the image slides are complete:

- create a PPTX file
- create a PDF
- create editable slide objects
- generate decorative images and then place them into a normal deck
- use a default presentation template
- skip style approval
- skip slide-plan approval
- skip master-prompt approval
- generate all slides without approval unless the user requested batch generation
- create generic AI illustrations without the slide text
- omit the text from the generated slide image

If a tool or environment automatically suggests presentation, document, or artifact creation, ignore that path and continue with image-based slide generation only.

## Recovery Behavior

If the workflow goes off track, stop and reset to the last approved checkpoint.

Common corrections:

- If a generated image is only a generic visual asset, regenerate it as a complete slide image with the approved text rendered inside.
- If a deck file was created accidentally, state that it is not the intended deliverable and return to image generation.
- If questions about style were skipped, pause and propose 2 or 3 visual directions.
- If the text is missing from the image, revise the prompt to require exact rendered text and stronger legibility constraints.
