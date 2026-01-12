# Korean Anki Decks

## Table of Contents

- [Download](#-download)
- [Korean Grammar Deck](#korean-grammar-deck)
- [Hanja Deck](#hanja-deck)
- [User Configuration](#user-configuration)
  - [Optional Glassmorphism (CSS)](#optional-glassmorphism-css)
- [Credits](#credits)
- [Feedback](#feedback)
- [License](#license)

##  Download

* **Grammar Deck**: <a href="">Download</a>
* **Hanja Deck**: <a href="https://drive.google.com/file/d/1HcRvRjV2Y_nGwVnRZi_7GW7-3k8zzrQf/view?usp=drive_link">Download</a>

## Korean Grammar Deck

### Card previews

**Front example**

<table>
  <tr>
    <img src="korean/grammar/screenshots/altfront1.png">
  </tr>
</table>

**Back example**

<table>
  <tr>
    <img src="korean/grammar/screenshots/altback1.png">

  </tr>
</table>

This deck focuses on **Korean grammar patterns**.

It contains **every grammar point from _Korean Grammar in Use (KGIU)_**, as well as **additional points from the Kimchi Reader Grammar section**.

Each time a card appears, the **front** shows a **random example sentence** chosen from the card’s sentence pool, displayed with a **randomly selected font**.  
On the **back**, the same randomly selected sentence appears at the top, together with the **focused grammar point and its meaning**, while all other available sentences are listed in the **“All examples”** section.

For the **Korean Grammar in Use** side, **the full lesson content** is included in the **Details** section, along with additional sections such as **related grammar points** and **comparisons**.
Each card also has a **tag indicating its book level**: *Beginner*, *Intermediate*, or *Advanced*.

For the **Kimchi Reader** side, all the grammar point from Kimchi reader site is included.

The pool of sentence includes all exmaples sentences from both  sources.

You can **click on any highlighted grammar point**, which will take you directly to the corresponding **[Kimchi Reader grammar page](https://kimchi-reader.app/grammar)** or **[Korean Grammar in Use page](https://sayhikorean.blogspot.com/2018/10/korean-grammar-in-use-beginner.html)** 

There is **one card per meaning**.  
So if a grammar point has **three different meanings**, the deck contains **three separate cards**, each with its own specific set of example sentences.

Common grammar points from **Korean Grammar in Use** and **Kimchi Reader** are merged into the same cards.  
As a result, there are **three types of cards**:

- **Merged**
- **Korean Grammar in Use only**
- **Kimchi Reader only**

If you want to use **only one source**, you can hide one side on the merged cards and **suspend the “Only” cards** from the source you don’t want (see the [User Configuration](#user-configuration) section).


The deck is ordered following the **Korean Grammar in Use lesson order**.  
**Kimchi Reader–only cards** that are not covered in the books are **mixed into the KGIU lesson order**, and placed based on a combination of **frequency** and **their relation to KGIU grammar points**.


## Study recommendation

My **personal recommendation** is to study **no more than 2–3 new cards per day**, alongside your normal reviews.  
At this pace, you will finish the deck in approximately **143–214 days** (**428 cards total**).

If you already know the early grammar points, I recommend going through them **quickly during the first few days** or **suspending them**.

There are many more details about this deck, including **tags, user configuration, structure, and how it was built**.  
For full documentation, see the dedicated README:  
👉 **[Deck README](https://github.com/marbaret/anki-decks/blob/main/korean/grammar/README.md)**
👉 **[How to add examples](https://github.com/marbaret/anki-decks/blob/main/korean/grammar/adding_examples/README.md)**



## Hanja Deck

### Card previews

**Front example**

<table>
  <tr>
    <img src="korean/hanja/screenshots/front1.png">
  </tr>
</table>

**Back example**

<table>
  <tr>
    <td><img src="korean/hanja/screenshots/back1.png"></td>
    <td><img src="korean/hanja/screenshots/back2.png"></td>
  </tr>
</table>

This deck helps build **recognition and understanding of commonly used Hanja** and their usage in Korean.
  
It contains **multiple sections** that can be easily **enabled or disabled** to suit individual preferences directly in the **HTML** (see the [**User Configuration**](#user-configuration) section below).
 
It is **ordered by 한자능력검정 급수** (8급, 7급, etc.).
 
My personal recommendation is to study **no more than 5 cards per day**, alongside your usual reviews.   
With this pace, you will finish the deck in **about one year** (**1,948 cards total**).

<p><strong>For more details about this deck</strong> (tags, structure, and how it was built), <strong><a href="https://github.com/marbaret/anki-decks/blob/main/korean/hanja/README.md">see the dedicated README here</a></strong>.</p>

## User Configuration

Both decks include a <strong>USER CONFIGURATION AREA</strong> directly inside the <strong>Front</strong> and <strong>Back</strong> JavaScript of the cards.

This section allows you to customize the deck behavior and appearance (for example: display options, fonts, or other variables) <strong>without touching the core logic</strong>.

To modify it:

1. Open Anki
2. Go to <strong>Browse</strong> → select the deck
3. Click <strong>Cards…</strong>
4. Edit the values inside the <strong>USER CONFIGURATION AREA</strong> in the Front and/or Back JavaScript

### Configuration preview

<img src="korean/grammar/screenshots/config1.jpg">

### Optional Glassmorphism (CSS)

The card styling includes an <strong>optional glassmorphism effect</strong> that can be enabled or adjusted directly in the <strong>CSS</strong>.  
It can look great when used with a background image.

To configure it:

1. Open <strong>Cards…</strong> in Anki
2. Go to the <strong>Styling (CSS)</strong> section
3. Delete start and end comment in the first section <em>GLASSMORPHISM OPTION</em>

<strong>How to configure</strong>

<img src="korean/grammar/screenshots/config2.jpg">

<strong>Visual result (with external background)</strong>

<img src="korean/grammar/screenshots/glassmorphism.png">


## Credits

### Grammar Deck

This deck has been created using the GitHub repo from **[Kimchi Reader's](https://kimchi-reader.app/grammar) grammar section**.  
And all the lesson from Korean Grammar in Use books.

**I strongly encourage you to try out [Kimchi Reader](https://kimchi-reader.app/) !**  
It's the most amazing tool I've used to learn Korean and the best way to build a vocab deck using its sentence mining feature. There is a 1-week free trial, so honestly just give it a try.  

There is an amazing **[Discord server](https://discord.gg/abRkZ2hhSA)** with people who will help you if you have any questions.

- **[Kimchi Reader Grammar page](https://kimchi-reader.app/grammar)**  
- **[Kimchi Reader Grammar GitHub repo](https://github.com/Alaanor/kimchi-grammar)**

**Disclaimer**

I am **not** the creator of Kimchi Reader, and the Grammar page was **not** originally created to serve as a structured language course or a series of lessons.


The [Kimchi Reader Grammar GitHub repo](https://github.com/Alaanor/kimchi-grammar) was created by amazing contributors, and a huge thanks goes to all of them, but keep in mind that there might be some typos or minor issues.  
For every update of the repo, I’ll update the Grammar deck, so you’ll just have to download it again to have the latest version.

If you have the knowledge and time to do so, I really encourage you to **contribute** to the [repo](https://github.com/Alaanor/kimchi-grammar).  
For example, there are points with only **one example sentence**, and it would be amazing to have **multiple examples** for the **random sentence feature** of the deck.


### Hanja Deck

This deck was created by merging **Retro's Hanja deck**, which can be found **[here](https://drive.google.com/drive/folders/1FemoEaheHiJy2eEtTQXGU_bNj8yQipjo?usp=sharing)**  
and another deck that I unfortunately can’t find again on AnkiWeb.  

I also added fields with data scraped from **[Wiktionary](https://en.wiktionary.org/wiki/Wiktionary:Main_Page)**.  

All credits go to Retro and to the creator of the other deck.  

Find **Retro's Blog site** **[here](https://retrolearnskorean.blogspot.com/)**.

### Feedback

If you have any questions, suggestions, or issues, don’t hesitate to contact me on Discord: **mathieu.exe**

I welcome all suggestions and feedback, and I'll do my best to correct any errors you find.

## License

This project is licensed under <strong>Creative Commons Attribution 4.0 International (CC BY 4.0)</strong>.  
See the <code>LICENSE</code> file for full details.
