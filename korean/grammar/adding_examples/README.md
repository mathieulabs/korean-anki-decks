# Adding Examples Manually – User Guide

> [!IMPORTANT]
> **Migration Notice:** This guide describes the **new JSON format** introduced in the latest update.
> If you are using an older version of the deck (where fields use `|||$$$|||` separators), you **must update your deck** to use this feature.
>
> ⚠️ **Important:** When updating your deck, **do not open the Browse window**.  
> Stay on Anki’s **main screen immediately after launching the app**, otherwise the cards you’re currently viewing **will not be updated correctly**.
>> **How to update:** Simply download the latest `.apkg` version of the deck and double-click it to import. Select **'Merge Note Types'**. Anki will update the card templates automatically.

> **Note:** The `AllExamples` field is no longer used. After updating, you can safely delete it from your note type if you wish to clean up.
>
> **Don't worry:** Re-importing the deck **preserves your progress and scheduling**. You won't lose any reviews!


## Table of Contents

1. [Overview](#overview)
2. [How to Add Examples](#how-to-add-examples)
3. [JSON Field Format](#json-field-format)
   - [Structure](#structure)
   - [Field Breakdown](#field-breakdown)
4. [Highlighting Grammar Points](#highlighting-grammar-points)
   - [How to Highlight](#how-to-highlight)
   - [Escaping Quotes (Critical!)](#escaping-quotes-critical)
5. [Complete Examples](#complete-examples)
6. [Troubleshooting](#troubleshooting)
7. [Need Help?](#need-help)

---

## Overview

The `RandomExamplesRaw` field contains all example sentences for the card. **This field is now formatted as standard JSON.**

Instead of using special separators like `|||$$$|||`, you must now provide a valid JSON array of objects.

---

## How to Add Examples

1. **Open Anki Browser** (Press `B`)
2. **Select the Card**
3. **Find `RandomExamplesRaw`** field
4. **Edit the JSON array**:
   - The field starts with `[` and ends with `]`
   - Each example is an object inside curly braces `{ ... }`
   - Objects are separated by commas `,`
5. **Add your new example object** to the list (don't forget the comma after the previous object!)

---

## JSON Field Format

### Structure

The field must look like this:

```json
[
  {
    "kr": "Existing sentence...",
    "en": "Existing translation...",
    "source": "kimchi"
  },
  {
    "kr": "YOUR NEW SENTENCE HTML",
    "en": "YOUR NEW TRANSLATION",
    "source": "manual",
    "audio": "optional_filename.mp3",
    "img": "optional_image_html"
  }
]
```

### Field Breakdown

Each example object can have the following properties:

1. **`"kr"` (Required)**
   - The Korean sentence with HTML highlighting.
   - Example: `"kr": "한국어를 <span class=\"focus\">공부해요</span>."`

2. **`"en"` (Required)**
   - English translation.
   - Example: `"en": "I study Korean."`

3. **`"source"` (Required)**
   - Use `"manual"` for your own examples.
   - Example: `"source": "manual"`

4. **`"audio"` (Optional)**
   - Filename of the audio file in your collection.media folder.
   - Example: `"audio": "my_audio_file.mp3"`

5. **`"img"` (Optional)**
   - Image HTML tag.
   - Example: `"img": "<img src=\"my_image.jpg\">"`

6. **`"priority"` (Optional)**
   - Usually empty for manual examples.
   - Example: `"priority": ""`

---

## Priority System (Advanced)

**Most users can leave the `"priority"` field empty.**

### What is it?
This setting is **only for Merged Cards** (cards that contain both KGIU and Kimchi Reader content). It controls which "side" of the card is shown when this specific example is displayed.

- **Empty (`""`)**: The card uses its default behavior (usually showing KGIU first, or remembering your last choice).
- **`"kgiu_priority"`**: Forces the card to switch to the **KGIU view** when this example is shown.
- **`"kimchi_priority"`**: Forces the card to switch to the **Kimchi Reader view** when this example is shown.

### Why use it?
Sometimes an example sentence uses specific vocabulary or grammar nuances that are only explained in one of the two sources.

For example, if KGIU explains a grammar point's formal usage, and Kimchi Reader explains its casual usage:
- You might tag a formal sentence with `"kgiu_priority"` so the user sees the formal KGIU explanation with it.
- You might tag a casual sentence with `"kimchi_priority"` so the user sees the casual Kimchi explanation with it.

This ensures the example sentence always matches the context of the explanation shown.

---

## Highlighting Grammar Points

### How to Highlight

Use HTML `<span>` tags within the `"kr"` string:

- **`<span class=\"focus\">...</span>`** - Main grammar point (Required)
- **`<span class=\"green\">...</span>`** - Secondary grammar
- **`<span class=\"blue\">...</span>`** - Additional grammar

### Escaping Quotes (Critical!)

Because you are inside a JSON string (which is already wrapped in double quotes `"`), **you MUST escape internal double quotes** with a backslash `\`.

❌ **WRONG:**
```json
"kr": "한국어를 <span class="focus">공부해요</span>."
```
*(Result: Invalid JSON, will break the card)*

✅ **CORRECT:**
```json
"kr": "한국어를 <span class=\"focus\">공부해요</span>."
```

---

## Complete Examples

### Simple Example
```json
{
  "kr": "저는 <span class=\"focus\">학생</span>입니다.",
  "en": "I am a student.",
  "source": "manual"
}
```

### Example with Audio
```json
{
  "kr": "한국어를 <span class=\"focus\">배워요</span>.",
  "audio": "korean_sentence_01.mp3",
  "en": "I learn Korean.",
  "source": "manual"
}
```

### Example with Image
```json
{
  "kr": "사과가 <span class=\"focus\">이/가</span> 있어요.",
  "en": "There is an apple.",
  "img": "<img src=\"apple.jpg\">",
  "source": "manual"
}
```

### Full Field Example

If your field already has one example, adding a new one looks like this:

```json
[
  {
    "kr": "Existing sentence...",
    "en": "Existing translation...",
    "source": "kimchi"
  },
  {
    "kr": "NEW SENTENCE <span class=\"focus\">HERE</span>.",
    "en": "NEW TRANSLATION.",
    "source": "manual"
  }
]
```

**Note the comma `,` after the first closing brace `}`!**

---

## Troubleshooting

### Card shows "JSON PARSING ERROR"
This means you made a syntax error. Check:
1. **Commas**: Did you forget a comma between objects? Or did you add an extra comma after the last object?
2. **Quotes**: Did you forget to escape quotes inside strings (`\"` instead of `"`)?
3. **Brackets**: Does the field start with `[` and end with `]`?

### Example doesn't show up
- Ensure `"source"` is set.
- Check if you filtered sources in the card configuration.

---

## Need Help?

If you're stuck, use a [JSON Validator](https://jsonlint.com/) to check your syntax.

Contact: **mathieu.exe** on Discord.