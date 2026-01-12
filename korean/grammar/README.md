# Korean Grammar Anki Deck - Complete Documentation

## Table of Contents

1. [Introduction](#introduction)
2. [Card Structure](#card-structure)
3. [Card Types](#card-types)
4. [How Cards Work](#how-cards-work)
5. [Tags and Organization](#tags-and-organization)
6. [User Configuration](#user-configuration)
7. [Study Recommendations](#study-recommendations)
8. [Understanding Korean Grammar](#understanding-korean-grammar)
9. [Technical Details](#technical-details)
10. [Getting Help](#getting-help)

---

## Introduction

This Anki deck is designed to help you learn **Korean grammar patterns** systematically. It combines content from two Korean grammar resources:

- **Korean Grammar in Use (KGIU)** - A comprehensive textbook series covering Beginner, Intermediate, and Advanced levels
- **Kimchi Reader Grammar** - An online grammar reference with detailed explanations

The deck contains **428 cards total**, with each card focusing on a specific meaning of a grammar point. If a grammar pattern has multiple meanings, you'll find separate cards for each one.

---

## Card Structure

### Front of the Card

When you see a card, the **front** shows:

1. **A random Korean sentence** - This sentence uses the grammar point you're learning
2. **Random font** - The sentence appears in one of 9 different Korean fonts to help you read various styles
3. **Audio button** (optional) - Click to hear the sentence pronounced
4. **Translation toggle** (optional) - Click to show/hide the English translation

**Why random?** Each time you review a card, you'll see a different example sentence. This helps you understand the grammar pattern in various contexts, not just memorize one example.

### Back of the Card

When you flip the card, you'll see:

1. **Grammar point name** - The name of the grammar pattern
2. **Definition name** - A short label describing this specific meaning (e.g., "Cause and Effect")
3. **English alternatives** - Other English phrases that express similar meanings
4. **Frequency badge** (if available) - Shows how common this grammar point is (this is from Kimchi Reader)
5. **Level badge** (for KGIU side) - Shows the book level: Beginner, Intermediate, or Advanced
6. **The same random sentence** - The sentence you saw on the front, now with its translation visible
7. **Meaning section** - Definiton of the grammar point
8. **All Examples section** - A collapsible list showing ALL example sentences for this grammar point
9. **Details section** - Full lesson content from Korean Grammar in Use / content from Kimchi Reader depending on the side
10. **Related** (if available) - Links to related grammar points

### Interactive Elements

- **Clickable grammar points** - Click any highlighted grammar pattern to open its page on Kimchi Reader or KGIU. Same with the KGIU level badge and Frequency badge.
- **Source switch** (on merged cards) - Toggle between KGIU and Kimchi Reader content

---

## Card Types

The deck contains **three types of cards**. Each type has specific tags that you can use to filter and organize your study (see [Tags and Organization](#tags-and-organization) section).

### 1. Merged Cards

**What they are:** Cards that combine content from both Korean Grammar in Use and Kimchi Reader for the same grammar point.

**How to recognize them:**
- They have a **switch button** at the top (KGIU / Kimchi)
- You can toggle between the two sources
- Both sources share the same example sentences pool

**Why merged?** Some grammar points appear in both resources. Instead of having duplicate cards, they're combined into one card with both explanations.

**Example:** The grammar point "-아/어서" (because, so) appears in both KGIU and Kimchi Reader, so it's a merged card.

### 2. Korean Grammar in Use Only Cards

**What they are:** Grammar points that only appear in the KGIU textbooks, not in Kimchi Reader.

**How to recognize them:**
- No switch button (only one source)
- Have a **level badge** (Beginner/Intermediate/Advanced)
- Include full lesson content in the Details section

**Example:** The grammar point "-(으)ㄴ 끝에" (After a long and difficult process) is an Advanced level pattern from KGIU that isn't covered on Kimchi Reader.

### 3. Kimchi Reader Only Cards

**What they are:** Grammar points that only appear on Kimchi Reader, not in the KGIU textbooks.

**How to recognize them:**
- No switch button (only one source)
- Have a **frequency badge** showing how common they are
- Content comes from Kimchi Reader's grammar section

**Example:** The grammar point "아/어 두다" (Maintain / Prepare) is documented on Kimchi Reader with detailed explanations but doesn't appear in the KGIU textbooks.

---

## How Cards Work

### Random Sentence Selection

**On the front:**
- A random sentence is chosen from the card's sentence pool
- The same sentence appears on the back (synchronized)
- Each review shows a different random sentence

**Why this matters:** You'll see the grammar pattern used in many different contexts, which helps you understand it better than memorizing just one example.

### Font Randomization

Each card displays in one of 9 different Korean fonts to help you read Korean in various styles.

### Audio

Only grammar points from Kimchi Reader contain audio (from the site). This audio is AI-generated. If you don't want it, you can remove it in User Configuration (see [User Configuration](#user-configuration) section).

### Sentence Sources

Each example sentence comes from:
- **Kimchi Reader** examples
- **Korean Grammar in Use** examples
- **Manual examples** (added by me for some points that only had 1 example)

You can see which source a sentence comes from if you enable source badges in the configuration.

---

## Tags and Organization

### Deck Organization

The deck is organized following the **Korean Grammar in Use lesson order**. This means:

1. Cards appear in the same order as the KGIU textbooks
2. Kimchi-only cards are mixed in based on:
   - Their frequency (how common they are)
   - Their relationship to nearby KGIU grammar points

### Tags

Each card has tags that help you organize your study:

#### Level Tags
- `Korean_Grammar::Level::Beginner` - From KGIU Beginner book
- `Korean_Grammar::Level::Intermediate` - From KGIU Intermediate book
- `Korean_Grammar::Level::Advanced` - From KGIU Advanced book

#### Source Tags
- `Korean_Grammar::Type::KGIU_Only` - Only in KGIU, not in Kimchi Reader
- `Korean_Grammar::Type::Kimchi_Only` - Only in Kimchi Reader, not in KGIU
- `Korean_Grammar::Type::Merged` - Appears in both sources

#### Function Tags
Each grammar point has a function tag that describes its grammatical purpose. Examples include:
- `Korean_Grammar::Function::Cause_and_Effect` - Expresses cause and effect relationships
- `Korean_Grammar::Function::Comparison` - Used for comparisons
- `Korean_Grammar::Function::Particle` - Grammatical particles
- `Korean_Grammar::Function::Endings` - Sentence endings
- `Korean_Grammar::Function::Quotations` - Quotation patterns
- `Korean_Grammar::Function::Additional_Information` - Provides additional information
- And more...

#### Relations Tags
- `Korean_Grammar::Relations::Has_Different_Meanings` - Grammar points that have multiple distinct meanings (each meaning has its own card)

### Using Tags

You can use Anki's browser to:
- Filter cards by level (e.g., only show Beginner cards)
- Filter by source (e.g., only show KGIU cards)
- Create custom study sessions
- Suspend cards you don't want to study

**Example:** If you only want to study KGIU content, you can:
1. Hide the Kimchi side on merged cards (see [User Configuration](#user-configuration) section)
2. Suspend all cards with tag `Korean_Grammar::Type::Kimchi_Only`

---

## User Configuration

The deck is highly customizable. You can adjust many settings to match your learning style.

### How to Access Configuration

1. Open a card in Anki
2. Click "Edit" (or press `E`)
3. Look for the **"Front Template"** or **"Back Template"** field
4. Scroll down in the JavaScript code (the configuration is at the beginning of the JavaScript section, but you need to scroll past the initial setup code)
5. Find the section marked `// USER CONFIGURATION AREA` 
6. Modify the settings you want
7. Save the card (this updates all cards in the deck)

### Configuration preview

<img src="screenshots/config1.jpg">

**Note:** Some options are in the Front Template (like autoplay audio, font settings), while others are in the Back Template (like translation modes, section visibility). Check both templates to find all available options.

**CSS Color Customization:** At the top of the CSS section (in the "Styling" field), you can modify all color variables. Look for the section marked `/* COLOR VARIABLES (Light & Dark Mode) */` to customize colors for light mode, dark mode, badges, and other elements.

### Configuration Options

<details>
<summary><strong>Front Template Options</strong> (Click to expand)</summary>

These options are found in the **Front Template** JavaScript section:

**Option 1: AUTOPLAY AUDIO (Front)**
- `true` (default): Audio plays automatically when card appears on the front
- `false`: Audio only plays when you click the button

**Option 2: RANDOM FONT ENABLE**
- `true` (default): Enable random font selection (affects both front and back)
- `false`: Use default font

**Option 3: FONT CONFIGURATION LIST**
- Customize the list of 9 Korean fonts used for random selection
- You can modify font names and scale percentages

**Option 4: HIDE IMAGES ON FRONT**
- `true`: Hide images on front of card
- `false` (default): Show images

**Option 5: IMAGE SIZE ON FRONT**
- Maximum width in pixels for images displayed on the front (default: 180px)

**Option 6: FONT SIZE MULTIPLIER (FRONT ONLY)**
- Adjust font size of random example on front (1.0 = 100%, 1.2 = 120%)

**Option 6.5: TRANSLATION FONT SIZE MULTIPLIER (FRONT ONLY)**
- Adjust font size of translations on front (1.0 = 100%)

**Option 7: SHOW FREQUENCY BADGE ON FRONT**
- `true`: Display frequency badge on front
- `false` (default): Hide frequency badge on front

**Option 8: SHOW KGIU LEVEL BADGE ON FRONT**
- `true`: Display KGIU level badge on front
- `false` (default): Hide KGIU level badge on front

**Option 9: TRANSLATION DISPLAY MODE (FRONT)**
- `0` (default): No translation (completely hidden)
- `1`: Hidden (button) - show with button
- `2`: Visible immediately (no button)

**Option 10: FILTER EXAMPLES BY SOURCE**
- `'all'` (default): Include Kimchi + KGIU + other/manual examples
- `'kimchi+kgiu'`: Include only Kimchi + KGIU examples (exclude other/manual)
- `'kimchi'`: Only Kimchi examples
- `'kgiu'`: Only KGIU examples
- Note: This filter applies to the random example pool on the front

**Option 11: SHOW SOURCE BADGE (FRONT)**
- `true`: Display source badge (KIMCHI/KGIU) on random example
- `false` (default): Hide source badge on front

**Option 12: SHOW AUDIO BUTTON**
- `true` (default): Display audio button
- `false`: Hide audio button

</details>

<details>
<summary><strong>Back Template Options</strong> (Click to expand)</summary>

These options are found in the **Back Template** JavaScript section:

**Option 1: TRANSLATION_MODE (Back)**

Controls when translations are visible:

- `0` (default): Random example translation is hidden (button to show), but "All Examples" translations are visible immediately
- `1`: All translations are hidden (button to show each one)
- `2`: All translations are visible immediately (no buttons)


#### Section Visibility

**Option 2: Default Sections State**

Control which sections are expanded by default:

- `COLLAPSE_ALL_EXAMPLES = true` - "All Examples" section starts collapsed
- `DETAILS_DEFAULT_OPEN = false` - Details section starts collapsed
- `COMPARISON_DEFAULT_OPEN = false` - Comparison section starts collapsed
- `RELATED_DEFAULT_OPEN = false` - Related section starts collapsed
- `MEANING_DEFAULT_OPEN = true` - Meaning section starts expanded

**Recommendation:** Keep `MEANING_DEFAULT_OPEN = true` to always see the meaning. Collapse other sections to reduce clutter.

**Option 3: AUTOPLAY AUDIO (Back)**
- `true`: Audio plays automatically for random sentence on back
- `false` (default): Audio only plays when you click the button

**Option 4 & 5: Font Size Multipliers (Back)**
- `BACK_FONT_SIZE_MULTIPLIER = 1.0` - Size of Korean text on back (1.0 = 100%, 1.2 = 120%)
- `BACK_TRANSLATION_FONT_SIZE_MULTIPLIER = 1.0` - Size of English translations on back

**Option 6: SHOW AUDIO BUTTON (Back)**
- `true` (default): Display audio button
- `false`: Hide audio button

**Option 7: SHOW ENGLISH ALT**
- `true` (default): Display English alternative text
- `false`: Hide English alternatives

**Option 8: SHOW DEFINITION NAME**
- `true` (default): Display definition name
- `false`: Hide definition name

#### Source Control (Merged Cards)

**Option 9: DEFAULT_SOURCE_VIEW**

For merged cards, choose which source shows by default:

- `'kgiu'` (default): Show KGIU content first
- `'kimchi'`: Show Kimchi Reader content first

**Note:** Some cards have a `PrioritizeKimchi` flag that overrides this setting.

**Option 10: OVERRIDE PRIORITIZE KIMCHI**
- `true`: Override PrioritizeKimchi flag and use DEFAULT_SOURCE_VIEW instead
- `false` (default): Respect the PrioritizeKimchi flag from card data
- **Warning:** Not recommended - cards with PrioritizeKimchi are set that way for a reason

**Option 11: OVERRIDE SENTENCE PRIORITIES**
- `true`: Ignore all sentence priorities from raw data (use card's default behavior)
- `false` (default): Use priorities from raw data
- **Note:** Some sentences have priority flags (`kgiu_priority` or `kimchi_priority`) that determine which source they should display with
- **Warning:** Not recommended - sentences with priorities are set that way for a reason

#### Example Filtering

**Option 12: FILTER_ALL_EXAMPLES_SOURCE**

Filter which examples appear in "All Examples" section:

- `'all'` (default): Show all examples from all sources
- `'kimchi+kgiu'`: Show only Kimchi and KGIU examples (hide manual examples)
- `'kimchi'`: Show only Kimchi examples
- `'kgiu'`: Show only KGIU examples

**Option 13: SHOW EXAMPLES SOURCE STATS IN "ALL EXAMPLES"**
- `true`: Display statistics showing how many examples from each source (Kimchi, KGIU, Other) are in "All Examples"
- `false` (default): Don't display statistics

**Option 14: SHOW SOURCE BADGE (BACK)**
- `0` (default): Not displayed
- `1`: Display only on the random example
- `2`: Display only in "All Examples" section (not on random)
- `3`: Display everywhere (random + all examples)

#### Hiding Sections

**Option 15: HIDE_SECTIONS**

Hide entire sections if you don't need them:

- `HIDE_MEANING_SECTION = false` - Hide meaning section
- `HIDE_DETAILS_SECTION = false` - Hide details section
- `HIDE_COMPARISON_SECTION = false` - Hide comparison section
- `HIDE_RELATED_SECTION = false` - Hide related section
- `HIDE_INHERITANCE_SECTION = false` - Hide inheritance section
- `HIDE_ALL_EXAMPLES_BOXES = false` - Hide all example boxes (keep only random example)

**Recommendation:** Don't hide sections unless you're very advanced and don't need the extra information.

#### Source Switch and Badges

**Option 16: SHOW_SOURCE_SWITCH**

- `SHOW_SOURCE_SWITCH = true` - Show the KGIU/Kimchi switch button on merged cards
- `SHOW_FREQUENCY_BADGE = true` - Show frequency badge (#42, etc.)
- `SHOW_KGIU_LEVEL = true` - Show level badge (Beginner/Intermediate/Advanced)

**Recommendation:** Keep all `true` to see all information.

#### Compact View

**Option 17: FORCE_COMPACT_MODE**

- `false` (default): Compact layout (switch and badges below text) only on small screens (< 768px)
- `true`: Always use compact layout, even on large screens

**Recommendation:** Use `false` unless you prefer the compact layout on all devices.

</details>

---

## Study Recommendations

### Daily Study Plan

**Recommended pace:** 2-3 new cards per day


### If You Already Know Some Grammar

If you're already familiar with beginner grammar:

1. **Go through beginner cards quickly** - Review them once and mark as "Easy" if you know them
2. **Suspend known cards** - If you're certain you know a grammar point, suspend it
3. **Focus on your level** - Start learning cards of a certain KGIU level


---

## Technical Details

### Card Fields

Each card contains 12 fields of information:

1. **GrammarPoint** - Name of the grammar pattern (formatted HTML)
2. **DefinitionName** - Short label for this meaning (e.g., "Cause and Effect")
3. **EnglishAlt** - Alternative English phrases
4. **Frequency** - How common this grammar is (ranking number)
5. **Meaning** - Explanation of what it means
6. **Examples** - All example sentences (HTML, collapsible)
7. **Details** - Full detailed explanation (HTML markdown)
8. **RandomExamplesRaw** - Raw data for random sentence selection

<details>
<summary><strong>Adding Manual Examples</strong> (Click to expand)</summary>

> **For a complete guide:** See **[How to add examples](https://github.com/marbaret/anki-decks/blob/main/korean/grammar/adding_examples/README.md)** for detailed instructions, examples, and troubleshooting.

You can add your own examples directly in Anki by editing the `RandomExamplesRaw` field. However, there are important things to know about highlighting grammar points:


**How to highlight the grammar point:**

1. **Use HTML `<span>` tags directly** in the `RandomExamplesRaw` field:
   - `<span class="focus">...</span>` - Highlights the main grammar point (red/orange color)
   - `<span class="green">...</span>` - Highlights secondary grammar (green color)
   - `<span class="blue">...</span>` - Highlights additional grammar (blue color)

2. **Format to follow:**
```
|||$$$|||{krHTML}///$$$///{audioFilename}///$$$///{enText}///$$$///{imageHTML}///$$$///{source}///$$$///{priority}
```

3. **Example of adding:**
```
|||$$$|||새로운 <span class="focus">예문</span>입니다.///$$$//////$$$///This is a new example.///$$$//////$$$///manual///$$$///
```

4. **Important notes:**
   - The HTML tags will be automatically decoded if Anki escapes them (e.g., `&lt;span&gt;` becomes `<span>`)
   - You may see the raw HTML tags in Anki's field editor - this is normal. The tags will be properly interpreted when the card is displayed
   - Make sure to use double quotes for attributes: `class="focus"` (not single quotes)

</details>

### Sentence Synchronization

The same random sentence appears on both front and back because:
- The front and back templates share `sessionStorage`
- When a sentence is selected on the front, its index is stored
- The back template reads the same index to show the same sentence


### Source Priority System

Some sentences have **priority flags** that determine which source (KGIU or Kimchi) they should display with:

- `kgiu_priority` - Always show with KGIU side, even if card defaults to Kimchi
- `kimchi_priority` - Always show with Kimchi side, even if card defaults to KGIU
- No priority - Use card's default behavior

This ensures sentences with source-specific vocabulary or context appear with the correct source.

### Deck Statistics

- **Total cards:** 428
- **Merged cards:** 234 
- **KGIU-only cards:** 89 
- **Kimchi-only cards:** 105 

## Getting Help
---

## Feedback

If you have any questions, suggestions, or issues, don't hesitate to contact me on Discord: **mathieu.exe**

I welcome all suggestions and feedback, and I'll do my best to correct any errors you find.

### Resources


- **Korean Grammar in Use:**
  - [Beginner](https://sayhikorean.blogspot.com/2018/10/korean-grammar-in-use-beginner.html)
  - [Intermediate](https://sayhikorean.blogspot.com/2018/09/korean-grammar-in-use-intermediate.html)
  - [Advanced](https://sayhikorean.blogspot.com/2018/09/korean-grammar-in-use-advanced_10.html)

- **Kimchi Reader Grammar:** [kimchi-reader.app/grammar](https://kimchi-reader.app/grammar)

---

## Conclusion

This deck is designed to be a comprehensive resource for learning Korean grammar. Take your time, study consistently, and don't hesitate to explore the configuration options to customize it to your learning style.

Remember: **Understanding is more important than speed**. It's better to learn 2-3 grammar points well than to rush through many without understanding them.

Good luck with your Korean grammar studies! 화이팅!

