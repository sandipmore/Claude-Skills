---
name: interior-design
description: >
  Create professional interior design deliverables — room layouts, color palettes, mood boards,
  furniture recommendations, and client-ready design concept presentations. Use this skill whenever
  the user mentions interior design, room design, home decor, space planning, room layout,
  color schemes for rooms, furniture selection, mood boards, staging, redesigning a room,
  or wants to produce a design brief, design concept, or design presentation for a client.
  Also trigger when the user uploads a room photo and asks for design advice, wants to visualize
  a room makeover, or mentions terms like "living room", "bedroom", "kitchen design", "office layout",
  "accent wall", "color palette for a space", or "furniture arrangement". Even casual requests like
  "help me redo my living room" or "what would look good in this space" should trigger this skill.
---

# Interior Design Skill

Create polished, client-facing interior design deliverables. This skill helps interior designers
produce professional outputs — from interactive mood boards to formal design briefs and
presentation decks — across any design style.

## When to Use This Skill

- Client wants a design concept for a room or space
- Need to create a mood board or color palette
- Planning furniture layout and space arrangement
- Producing a client-ready design brief (docx) or presentation (pptx)
- Visualizing a design concept as an interactive artifact (HTML/React)
- Giving furniture or decor recommendations with sourcing ideas
- Any room redesign, staging, or makeover request

## Workflow Overview

Every interior design task follows this general flow:

1. **Understand the brief** — Gather room details, client preferences, budget, and constraints
2. **Define the design direction** — Style, color palette, mood, and key inspiration
3. **Develop the concept** — Layout, furniture selections, materials, and accents
4. **Produce the deliverable** — In the format the user needs (artifact, docx, pptx)

## Step 1: Gather the Design Brief

Before producing anything, you MUST collect detailed room information. Do not skip this step or make assumptions — accurate spatial data is the foundation of good design. Ask the user for the following, organized into clear groups:

### Room Basics
- **Room type**: Living room, bedroom, kitchen, office, bathroom, dining room, nursery, studio, etc.
- **Design style**: Modern, minimalist, traditional, bohemian, Scandinavian, industrial, Art Deco, mid-century modern, coastal, rustic, transitional, maximalist, japandi, etc.
- **Color preferences**: Warm, cool, neutral, specific colors, or "surprise me"
- **Budget range**: Luxury, mid-range, budget-friendly, or a specific number
- **Client mood or vibe**: Words like "cozy", "airy", "dramatic", "serene", "playful"

### Room Dimensions & Structure (Critical — always ask)
- **Exact room dimensions**: Length × Width in feet or meters (not just "small/medium/large")
- **Ceiling height**: Standard (~9 ft), tall (~10-12 ft), double-height, vaulted, or sloped
- **Room shape**: Rectangular, L-shaped, open-plan, irregular — note any alcoves, nooks, or bump-outs

### Compass Direction & Natural Light (Critical — affects color and layout)
- **Which direction do the windows face?** North, South, East, West, or combinations
  - North-facing: cooler, diffused light → warmer palette choices help balance
  - South-facing: abundant warm light → can handle cooler or bolder tones
  - East-facing: bright morning light, softer afternoons
  - West-facing: warm afternoon/evening glow, can get hot
- **How much natural light does the room get?** Bright and sunny, moderate, dim/dark
- **Any light obstructions?** Neighboring buildings, trees, overhangs

### Windows & Doors (Critical — defines layout constraints)
- **Number of windows**: How many, and on which walls?
- **Window sizes**: Small, standard, floor-to-ceiling, bay window, skylight
- **Number of doors**: How many, and on which walls? Include closet doors
- **Door types**: Standard swing (which direction?), sliding, pocket, French, archway
- **Any fixed openings?** Pass-throughs to kitchen, open archways to adjacent rooms

### Layout Upload Request
Always ask the user to upload a floor plan or layout sketch if they have one. Phrase it warmly:

> "If you have a floor plan, blueprint, or even a rough hand-drawn sketch of the room showing where the doors and windows are, please upload it — it'll help me create a much more accurate layout for you. A photo of the room also works great."

If the user uploads a floor plan or photo:
- Analyze it carefully for wall positions, door swings, window placements, and any fixed elements
- Note the scale if provided, or ask the user to confirm key measurements
- Identify existing furniture or built-ins visible in photos
- Note natural light direction from shadows or window brightness in photos

If no upload is available, ask the user to describe the wall-by-wall layout:
> "No worries! Can you walk me through the room wall by wall? For example: 'The north wall has two standard windows and the main entry door on the left. The east wall is solid with a built-in bookshelf...'"

### Existing Elements & Lifestyle
- **Existing elements to keep**: Flooring type, built-ins, fireplace, specific furniture pieces
- **Flooring**: Hardwood, tile, carpet, concrete, laminate — color/tone
- **Lifestyle needs**: Kids, pets, work-from-home, entertaining, accessibility requirements
- **Things to avoid**: Any colors, styles, materials, or items the client dislikes

## Step 2: Design Direction

### Color Palette

Build a cohesive palette with 5-7 colors:

- **Primary** (walls/large surfaces): 1-2 colors, typically neutral or soft
- **Secondary** (furniture/rugs): 1-2 colors that complement the primary
- **Accent** (pillows, art, decor): 1-2 pops of contrast or vibrancy
- **Metallic/finish**: Gold, brass, chrome, matte black, or natural wood tone

Provide exact hex codes and color names. Explain the emotional effect of the palette (e.g., "This sage and terracotta combination creates warmth while keeping the space grounded and natural").

### Style Definition

For each design style, consider these hallmarks:

- **Modern/Minimalist**: Clean lines, monochromatic, functional, negative space, low-profile furniture
- **Traditional/Classic**: Symmetry, rich fabrics, dark wood, ornate details, layered textures
- **Bohemian/Eclectic**: Mixed patterns, global influences, layered textiles, plants, vintage finds
- **Scandinavian**: Light wood, white/gray palette, hygge comfort, simple forms
- **Industrial**: Exposed materials, metal/wood, open layouts, utilitarian aesthetics
- **Mid-Century Modern**: Organic curves, teak/walnut, retro colors, iconic furniture silhouettes
- **Coastal**: Blue/white/sand palette, natural textures, airy and relaxed
- **Japandi**: Japanese minimalism meets Scandinavian warmth, wabi-sabi, natural materials
- **Art Deco**: Geometric patterns, rich jewel tones, luxe materials, dramatic lighting
- **Transitional**: Traditional meets modern, neutral palette, balanced ornamentation

## Step 3: Develop the Concept

### Room Layout & Space Planning

When creating a layout:

- Consider traffic flow — main pathways should be 36+ inches wide
- Anchor the room with the largest piece first (sofa, bed, dining table)
- Create zones in open-plan spaces using rugs, lighting, or furniture groupings
- Balance visual weight across the room
- Account for window/door placement and natural light direction
- Leave breathing room — not every wall needs furniture against it

For the interactive artifact output, create a top-down room layout visualization using SVG or canvas showing furniture placement, dimensions, and zones.

### Furniture & Decor Recommendations

For each recommended piece, provide:

- **Item name and type** (e.g., "Curved sectional sofa, 3-seat, bouclé fabric")
- **Approximate dimensions** — ensure it fits the space
- **Material and color** — tied to the palette
- **Price range** — aligned with budget tier
- **Sourcing suggestions** — mention realistic retailers/brands appropriate to the budget:
  - Luxury: Restoration Hardware, B&B Italia, Holly Hunt, 1stDibs
  - Mid-range: West Elm, CB2, Article, Pottery Barn, Crate & Barrel
  - Budget: IKEA, Target (Threshold/Studio McGee), Wayfair, H&M Home
- **Why it works** — brief design rationale

Group recommendations by category: seating, tables, storage, lighting, textiles, wall decor, plants/accessories.

### Materials & Textures

Suggest a mix of textures to add depth:
- Hard: wood, stone, metal, glass, ceramic
- Soft: velvet, linen, wool, cotton, leather, bouclé
- Natural: rattan, jute, sisal, terracotta, marble

Explain the tactile balance (e.g., "Pairing a velvet sofa with a jute rug and marble side table creates rich contrast between soft and hard, warm and cool").

## Step 4: Produce the Deliverable

### Output Format: Interactive Artifact (HTML/React)

Create a visually polished React artifact that includes:

- **Mood Board Panel**: A grid layout showcasing the color palette (rendered as swatches with hex codes), texture/material references (described visually), and key design keywords
- **Room Layout View**: A simplified top-down SVG floor plan showing furniture placement with labeled pieces and approximate dimensions
- **Furniture Picks Section**: Cards for each recommended item with name, description, price range, and suggested source
- **Color Palette Bar**: Horizontal strip of the full palette with names and hex codes
- **Style Summary**: A short paragraph capturing the overall concept narrative

Use Tailwind CSS for styling. Make it feel like a professional design tool — clean, elegant, with good typography. Use a neutral background (white or very light gray) so colors and content pop. Include tab navigation between sections.

Read the frontend-design skill at `/mnt/skills/public/frontend-design/SKILL.md` before building the artifact for best UI practices.

### Output Format: Design Brief (Word Document)

Create a polished .docx with:

1. **Cover page** — Project title, client name (if provided), date, designer branding
2. **Design Concept Overview** — 1-2 paragraphs capturing the vision and mood
3. **Color Palette** — Swatches (colored table cells) with hex codes and color names
4. **Room Layout Description** — Written description of the spatial plan with zones
5. **Furniture & Decor Schedule** — Table with item, description, dimensions, price range, source
6. **Materials & Finishes** — Table listing recommended materials, where they're used, and why
7. **Implementation Notes** — Practical tips, phasing suggestions, contractor notes
8. **Budget Summary** — Estimated total broken into categories

Read the docx skill at `/mnt/skills/public/docx/SKILL.md` before creating the document.

### Output Format: Client Presentation (PowerPoint)

Create a professional .pptx with:

1. **Title slide** — Project name, room, client name, date
2. **Design Vision** — Concept statement with mood keywords
3. **Color Palette slide** — Visual palette with named colors
4. **Mood & Inspiration slide** — Description of the mood and design references
5. **Floor Plan / Layout slide** — Description or simplified diagram of the layout
6. **Furniture Selections** — 2-3 slides with key pieces, organized by category
7. **Materials & Textures** — Slide showing the material palette
8. **Budget Overview** — High-level cost breakdown
9. **Next Steps** — Timeline or action items

Read the pptx skill at `/mnt/skills/public/pptx/SKILL.md` before creating the presentation.

## Tone & Language

This is client-facing work, so the tone should be:

- **Confident and knowledgeable** — speak like a professional designer
- **Warm but not casual** — approachable without being overly chatty
- **Specific and visual** — use concrete descriptions ("warm cognac leather" not just "brown")
- **Narrative** — tell the story of the space: why choices work together, what feeling they create

Avoid generic filler. Every recommendation should feel intentional and considered. The client should read the deliverable and feel like they hired a talented designer who truly understands their space.

## Quick Reference: Design Principles

- **60-30-10 Rule**: 60% dominant color, 30% secondary, 10% accent
- **Rule of Three**: Group decor items in odd numbers for visual interest
- **Scale & Proportion**: Mix furniture heights and sizes; avoid everything being the same scale
- **Layered Lighting**: Combine ambient (overhead), task (desk/reading), and accent (decorative) lighting
- **Focal Point**: Every room needs one — fireplace, statement wall, view, art piece
- **Visual Flow**: The eye should move naturally through the room without dead zones
