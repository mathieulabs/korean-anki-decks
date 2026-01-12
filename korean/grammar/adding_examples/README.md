# Adding Examples Manually – User Guide

## Table of Contents

1. [Overview](#overview)
2. [How to Add Examples](#how-to-add-examples)
   - [Step-by-Step Instructions](#step-by-step-instructions)
3. [Field Format](#field-format)
   - [Structure of One Example](#structure-of-one-example)
   - [Field Breakdown](#field-breakdown)
4. [Highlighting Grammar Points](#highlighting-grammar-points)
   - [How to Highlight](#how-to-highlight)
   - [Examples](#examples)
   - [Important Notes](#important-notes)
5. [Complete Example](#complete-example)
6. [More Examples](#more-examples)
7. [Priority System (Advanced)](#priority-system-advanced)
8. [Troubleshooting](#troubleshooting)
9. [Tips](#tips)[text](../../../../../Bureau/kimchi-grammar/README_RandomExamplesRaw.md)
10. [Common Mistakes to Avoid](#common-mistakes-to-avoid)
11. [Need Help?](#need-help)

---

## Overview

The `RandomExamplesRaw` field contains all example sentences that can be randomly displayed on the front of your Anki cards. This field is automatically generated when the deck is built, but you can also add or modify examples directly in Anki.

**Note:** This guide is for users who want to add examples directly in Anki. You don't need access to the source code or build scripts.

---

## How to Add Examples

### Step-by-Step Instructions

1. **Open Anki Browser**
   - In Anki, press `B` or go to `Tools` → `Browse`
   
2. **Find Your Card**
   - Search for the grammar point you want to modify
   - Click on the card to select it

3. **Edit the RandomExamplesRaw Field**
   - Click on the `RandomExamplesRaw` field
   - Scroll to the end of the field (or beginning if you prefer)
   - Add your new example following the format below

4. **Save Your Changes**
   - Save
   - Close the browser

---

## Field Format

The `RandomExamplesRaw` field uses special separators to organize multiple examples:

- **Main separator**: `|||$$$|||` (separates different examples)
- **Data separator**: `///$$$///` (separates different parts of one example)
  - **Important:** Always use the complete separator `///$$$///` (three dollar signs `$$$`)
  - When a field is empty, you still write the separator `///$$$///`

### Structure of One Example

Each example follows this format:

```
{krHTML}///$$$///{audioFilename}///$$$///{enText}///$$$///{imageHTML}///$$$///{source}///$$$///{priority}
```

### Field Breakdown

1. **krHTML** - Korean sentence with HTML formatting
   - This is where you put your Korean sentence
   - **Important:** Use HTML tags to highlight the grammar point (see [Highlighting Grammar Points](#highlighting-grammar-points) below)
   - Example: `가족<span class="focus">과</span> 여행을 가고 싶어요.`

2. **audioFilename** - Audio file name (optional)
   - Just the filename, like `example.mp3`
   - Leave empty if no audio: `` (nothing between the separators)
   - Example: `example_audio.mp3` or empty

3. **enText** - English translation
   - The English translation of your Korean sentence
   - Example: `I want to travel with my family.`

4. **imageHTML** - Image HTML (optional)
   - Complete `<img>` tag if you have an image
   - Leave empty if no image: `` (nothing between the separators)
   - Example: `<img src="example.jpg" style="max-width:100%;">` or empty

5. **source** - Where the example comes from
   - Use: `kimchi`, `kgiu`, or `manual` (for examples you add yourself)
   - Must be lowercase
   - Example: `kimchi` or `kgiu` or `manual`

6. **priority** - Display priority (optional, usually leave empty)
   - Most users can leave this empty: `` (nothing between the separators)
   - Advanced: `kgiu_priority` or `kimchi_priority` (see [Priority System](#priority-system) below)
   - Example: empty or `kgiu_priority`

---

## Highlighting Grammar Points

When you add a Korean sentence, you need to highlight the grammar point so it appears in color on the card.

### How to Highlight

Use HTML `<span>` tags with specific classes:

- **`<span class="focus">...</span>`** - Highlights the main grammar point (red/orange color)
- **`<span class="green">...</span>`** - Highlights secondary grammar (green color)  
- **`<span class="blue">...</span>`** - Highlights additional grammar (blue color)

### Examples

**Simple highlighting (most common):**
```
한국어를 공부하고 있어<span class="focus">요</span>.
```
This highlights "요" as the grammar point.

**Multiple highlights:**
```
가족<span class="focus">과</span> <span class="blue">함께</span> 여행을 가고 싶어요.
```
This highlights "과" (main grammar) and "함께" (secondary grammar).

### Important Notes

- **Use double quotes**: `class="focus"` (not single quotes)
- **You must add the tags manually** - there's no automatic highlighting for manually added examples
- The tags will be properly interpreted when the card is displayed (you may see raw HTML in Anki's editor - that's normal)

---

## Complete Example

Here's a complete example you can copy and modify:

```
|||$$$|||새로운 <span class="focus">예문</span>입니다.///$$$//////$$$///This is a new example.///$$$//////$$$///manual///$$$///
```

**Breaking it down:**
- `|||$$$|||` - Separator to add a new example
- `새로운 <span class="focus">예문</span>입니다.` - Korean sentence with highlighted grammar
- `///$$$///` - Data separator (always the complete separator `///$$$///`)
- `` (empty) - No audio file (nothing between separators)
- `///$$$///` - Data separator
- `This is a new example.` - English translation
- `///$$$///` - Data separator
- `` (empty) - No image (nothing between separators)
- `///$$$///` - Data separator
- `manual` - Source (you added this yourself)
- `///$$$///` - Data separator
- `` (empty) - No priority (nothing between separators)

**Important:** Always use the complete separator `///$$$///` (three dollar signs `$$$`). When a field is empty, you still write the separator `///$$$///`.

---

## More Examples

### Example with Audio

```
|||$$$|||한국어를 배우고 있어<span class="focus">요</span>.///$$$///korean_audio.mp3///$$$///I am learning Korean.///$$$//////$$$///manual///$$$///
```

### Example with Image

```
|||$$$|||친구<span class="focus">와</span> 영화를 봤어요.///$$$//////$$$///I watched a movie with my friend.///$$$///<img src="movie.jpg" style="max-width:100%;">///$$$///manual///$$$///
```

### Example with Multiple Highlights

```
|||$$$|||가족<span class="focus">과</span> <span class="blue">함께</span> 여행을 가고 싶어요.///$$$//////$$$///I want to travel with my family.///$$$//////$$$///manual///$$$///
```

---

## Priority System (Advanced)

**Most users can skip this section.** The priority system is only needed for merged cards (cards that have both KGIU and Kimchi content).

### What is Priority?

Priority controls which side (KGIU or Kimchi) an example displays with on merged cards.

- **No priority** (empty) - Example follows the card's default behavior
- **`kgiu_priority`** - Always shows with KGIU side
- **`kimchi_priority`** - Always shows with Kimchi side

### When to Use Priority

You typically don't need to set priority. Only use it if:
- You have a merged card (shows both KGIU and Kimchi content)
- Your example contains words that only make sense with one specific side
- The example isn't displaying with the correct side by default

### Example with Priority

```
|||$$$|||가족<span class="focus">과</span> <span class="blue">함께</span> 여행을 가고 싶어요.///$$$//////$$$///I want to travel with my family.///$$$//////$$$///kgiu///$$$///kgiu_priority
```

---

## Troubleshooting

### My example doesn't appear

**Check:**
-  All separators are present: `|||$$$|||` and `///$$$///`
-  The format is exactly correct (copy from examples above)
-  You saved the card (Ctrl+S or Cmd+S)
-  The `source` field is lowercase: `kimchi`, `kgiu`, or `manual`

### The grammar point isn't highlighted

**Check:**
-  You used `<span class="focus">` (not just `<span>`)
-  You used double quotes: `class="focus"` (not single quotes)
-  The tags are properly closed: `</span>`
-  You can see the raw HTML in Anki's editor (that's normal - it will work on the card)

### Audio doesn't play

**Check:**
-  The filename is correct (just the name, like `audio.mp3`)
-  The audio file exists in Anki's media folder
-  The file is referenced in the card's `MediaReferences` field (Anki should do this automatically when you add media)

### The example shows raw HTML tags

**This is normal!** In Anki's field editor, you'll see the raw HTML tags. When you review the card, the tags will be properly interpreted and the grammar point will be highlighted in color.

---

## Tips

1. **Start simple** - Add one example first, test it, then add more
2. **Copy the format** - Use the examples above as templates
3. **Check your work** - Review a card after adding examples to make sure they appear correctly
4. **Use `manual` as source** - When adding your own examples, use `manual` as the source so you can filter them later if needed
5. **Keep it organized** - Add new examples at the end of the field to keep them organized

---

## Common Mistakes to Avoid

❌ **Missing separators** - Every example needs `|||$$$|||` at the start and `///$$$///` between fields

❌ **Wrong quotes** - Use `class="focus"` not `class='focus'`

❌ **Forgetting to highlight** - Don't forget to add `<span class="focus">` around the grammar point

❌ **Wrong source format** - Use lowercase: `kimchi` not `KIMCHI` or `Kimchi`

❌ **Extra spaces** - Don't add spaces around separators (they should be exactly as shown)

---

## Need Help?

If you're having trouble:
1. Double-check your format against the examples above
2. Make sure all separators are exactly correct
3. Try adding a simple example first (no audio, no image, no priority)

If you have any questions or issues, don't hesitate to contact me on Discord: **mathieu.exe**