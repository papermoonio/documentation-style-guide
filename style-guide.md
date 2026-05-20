# Developer Documentation Style Guide

This document sets forth the standards and best practices for crafting high-quality technical documentation. It is intended to help you produce clear, consistent, and accessible content. It covers various topics, from writing style and formatting to code examples, images, and more.

The guidelines listed in this document aren't all-inclusive but strive to cover the basics. If this guide does not provide explicit guidance on a particular subject, please default to the [Google developer documentation style guide](https://developers.google.com/style).

> **Authoring with an AI coding agent?** Read [`AGENTS.md`](./AGENTS.md) first. It is the machine-readable companion to this guide and front-loads the rules that LLM-generated output most often violates (list punctuation, bold misuse, em dashes, banned phrases, terminology). The prose guide below remains the source of truth.

## Table of Contents

- [Content Guidelines](#content-guidelines)
  - [Best Practices](#best-practices)
    - [Banned Phrases](#banned-phrases)
  - [Language](#language)
  - [Accessibility](#accessibility)
  - [Terminology](#terminology)
  - [Punctuation](#punctuation)
    - [Em Dash and En Dash](#em-dash-and-en-dash)
  - [Text Formatting](#text-formatting)
    - [Bold](#bold)
    - [Italics](#italics)
    - [Underline](#underline)
    - [Symbols](#symbols)
    - [Numbers](#numbers)
    - [Quotes](#quotes)
    - [Capitalization](#capitalization)
  - [Table Formatting](#table-formatting)
  - [List Formatting](#list-formatting)
    - [List Item Punctuation](#list-item-punctuation)
    - [Description Lists](#description-lists)
  - [Links](#links)

- [Code Guidelines](#code-guidelines)
  - [Code Formatting](#code-formatting)
    - [Code Formatting by Language](#code-formatting-by-language)
    - [Code Identifiers in Prose](#code-identifiers-in-prose)
    - [Identifier Consistency Within a Document](#identifier-consistency-within-a-document)
  - [Variable Conventions](#variable-conventions)
  - [Capturing Terminal Output](#capturing-terminal-output)

- [Structure Guidelines](#structure-guidelines)
  - [Repository Structure](#repository-structure)
    - [Naming Conventions](#naming-conventions) 
  - [Page Structure](#page-structure)
    - [Heading and Titles](#headings-and-titles)
    - [Introductions](#introductions)

- [Visual Aid Guidelines](#visual-aid-guidelines)
  - [Image File Naming](#image-file-naming)
  - [Icons](#icons)
  - [Diagrams](#diagrams)
  - [Screenshots](#screenshots)
  - [Terminal Output](#terminal-output)
 

## Content Guidelines

This section of the document provides guidelines on best practices, language usage, accessibility considerations, terminology standardization, and more.

### Best Practices

- Use a formal tone that conveys confidence. Avoid casual language or slang.
- Keep sentences short and to the point. Avoid unnecessary jargon and ambiguity.
- Maintain a neutral and objective tone. Avoid biases, opinions, or emotional language.
- Provide context. Avoid assuming the reader already knows what you're talking about.
- Stick to the facts. Avoid sales-pitch language and filler phrases. See [Banned Phrases](#banned-phrases) for the explicit list.
- Write timeless documentation that doesn't anchor the content to a specific point in time. Avoid using "at the time of writing," "currently," "as of today," and similar.
- Use bulleted lists for key points and complex information and to break up walls of text (general readability).
- Use numbered lists for step-by-step instructions and sequential items.

#### Banned Phrases

The following phrases are not used in PaperMoon documentation. They are filler, marketing copy, or AI-generated cliché. Rewrite or omit when they appear.

| Banned | Use instead |
|---|---|
| delve into, dive into | (omit, or "explore", "walk through") |
| leverage | use |
| utilize | use |
| seamless, seamlessly | (omit) |
| robust | (omit, or be specific: "production-tested", "fault-tolerant") |
| powerful, cutting-edge, state-of-the-art | (omit) |
| simply, just, easily, obviously | (omit — never describe a step as easy) |
| it's important to note that | (omit — state the thing) |
| it's worth noting that | (omit) |
| in summary, in conclusion | (omit — structure carries it) |
| feel free to | (omit) |
| under the hood | (omit, or "internally") |
| in today's world, in the modern era | (omit) |
| currently, at the time of writing | (omit — write timeless docs) |
| etc. | "and more" or "and so on" |

### Language

- Avoid possessive and first-person plural language, such as "our," "we," and "let's," unless writing an informal tutorial.
- Address the reader as _you_.
- In tutorials and guides, where you're instructing a user to act, use an active voice.
- In conceptual documentation, where you're not instructing a user to act, using a passive voice is permitted.
- Be mindful of pronouns. Avoid unnecessarily gendered language.
- Use contractions sparingly. Default to the expanded form (`do not`, `cannot`, `it is`) in reference and conceptual documentation. Contractions are acceptable in informal tutorials.

### Accessibility

- Headings should follow a hierarchical structure, starting with H1 (`#`).
- Use alt text for all images. The alt text should describe what the image depicts.
- Use descriptive and meaningful link text. Avoid using "here" in link text. If the link points to a specific article, use the title of that article as the link text.
- Avoid directional language, such as "above" or "below".

### Terminology

| Use | Not |
|---|---|
| ERC-20, ERC-721, ERC-1155 | ERC20, ERC 20 |
| JSON-RPC | JSON RPC, JSONRPC |
| dApp | dapp, DApp (DApp is acceptable only at the start of a sentence or in a Chicago title-case heading) |
| TestNet | testnet, test net (unless overridden by a brand-specific guide) |
| MainNet | mainnet, main net |
| smart contract | smart-contract (unless used as a compound adjective: `smart-contract platform`) |
| supermajority | super majority, super-majority |
| and more / and so on | etc. |

For token standards generally, put a dash (`-`) between the standard prefix and the unique identifier.

- Define every acronym on first use in each article.
- Hyphenated identifiers and runtime/network profile names (e.g., `paseo-next`, `westend-next`) keep their canonical casing on every mention. Do not capitalize only the first letter because the identifier starts a sentence — rephrase the sentence so it is not sentence-initial.

### Punctuation

- Use Oxford commas.
- Use colons in lists (instead of dashes).
- For list item punctuation, see [List Formatting](#list-formatting).
- Do not use exclamation marks in formal writing.

#### Em Dash and En Dash

- **Em dash (`—`, U+2014)**: use sparingly to set off a parenthetical aside. Surround with spaces: `text — aside — more text`. At most one em dash per sentence. If a paragraph contains more than one em dash, rewrite using periods or commas.
- **En dash (`–`, U+2013)**: only for numeric ranges (`2024–2025`, `pages 10–14`).
- **Hyphen (`-`)**: compound words and identifiers (`ERC-20`, `kebab-case`).
- Do not substitute two hyphens (`--`) for an em dash. Use the actual `—` character.

Em-dash over-use is a common pattern in AI-generated prose. The pre-publish check is: count the em dashes per paragraph; if more than one, rewrite.

### Text Formatting

#### Bold

- Put bold elements between double asterisks (`**`).
- Use bold **only** for:
  - UI element names (button labels, menu items, field names).
  - The term in a description list: `**Term**: Description.` See [List Formatting](#list-formatting).
- Do not bold for emphasis in prose. Do not bold whole sentences. For emphasis on a specific word or phrase, use italics (see the [Italics](#italics) section). For a stronger callout, use an admonition (`!!! note`, `!!! warning`).

Do:

```markdown
Click **Deploy** to publish the contract.

- **Endpoint**: The URL of the JSON-RPC node.
- **Network**: The chain ID of the target network.

Use _italics_ when you need to draw attention to a single word.
```

Do not:

```markdown
This is **really important** — you **must** save your key.

The contract address is **0xabc...123**.
```

Bold misuse — peppering prose with `**emphasis**` — is a common pattern in AI-generated content. When reviewing, strip bold that isn't either a UI element or a description-list term.

#### Italics

- Put italic elements between single underscores (`_`).
- Use italics when drawing attention to a specific word or phrase, for example, when introducing a new term.

#### Underline

- Do not underline text.

#### Symbols

- Do not use emojis anywhere in documentation — including in headings, prose, bullet markers, callouts, or DO/DON'T markers. This includes ✅, ❌, 🟢, 🔴, ⚠️, 🚀, and similar decorative glyphs.
- Even outside documentation prose (HTML templates, banners, intentional UI elements), never use the rocket emoji (🚀) for blockchain projects — it reads as speculative hype. Prefer a neutral alternative (📣, 📢) or text only.
- For DO/DON'T comparisons, use the text labels `Do:` and `Do not:` instead of colored emoji.
- Do not use ampersands (`&`) unless referring to a UI element that uses them.

#### Numbers

- Spell out numbers zero through nine in prose. Use digits for 10 and above.
- Exceptions — always use digits:
  - Version numbers (`Node.js 18`, `Python 3`).
  - Measurements and units (`4 GB`, `8 cores`, `2 ms`).
  - Code and CLI flags (`--max-count 5`).
  - Inside tables.

#### Quotes

- Use double quotes in regular text.
- Commas and periods go inside quotation marks.
- Single quotes should only be used in code examples, depending on the guidelines in the [Code Formatting By Language](#code-formatting-by-language) section.

#### Capitalization

- Use Chicago title-style capitalization for titles and headings, which capitalizes the first word plus all other significant words.
- Capitalize product names.
- Avoid unnecessary capitalization; before you capitalize a word, think about why and if it should be capitalized.

### Table Formatting

- Use tables to represent sets of related pieces of data in a structured way.
- Table headers and values should be centered.
- Tables should be formatted. You can use a tool to format the tables, like the [Markdown Table Formatter VSCode extension](https://marketplace.visualstudio.com/items?itemName=fcrespo82.markdown-table-formatter).

### List Formatting

- Use ordered (numbered) lists for a sequence of steps.
- Use unordered (bulleted) lists for items that are non-sequential and can be read or completed in any order.
- Maintain consistent grammatical structure across items in a list — all items should start with a verb, or all should be noun phrases.

#### List Item Punctuation

Follow the [Google developer documentation style guide list rules](https://developers.google.com/style/lists). Summary:

- Start each list item with a capital letter, unless case is part of the information conveyed (e.g., a list of `kebab-case` identifiers).
- End each list item with a period or other sentence-ending punctuation, **except**:
  - The item is a single word.
  - The item does not contain a verb.
  - The item is entirely in code font.
  - The item is entirely link text or a document title.
- A numbered step label ending in a colon (e.g., `1. Configure the node:`) already counts as punctuated; do not add a trailing period after the colon.
- If a list ends up inconsistently punctuated, either rewrite for [parallel construction](https://developers.google.com/style/lists#parallel) or add end punctuation to every item for consistency. **Never mix punctuated and unpunctuated items in the same list.**

Do:

_You can do any of the following by using the API:_

- Create an item.
- Replace one item with another.
- Update an item.
- Delete an item.

Do:

_The API supports the following actions:_

- Create
- Replace
- Update
- Delete

Do not (mixed forms in one list):

- Create an item
- Replace one item with another.
- Update.
- Delete an item

#### Description Lists

For description lists, use the format `**Term**: Description.`

- Put the term in bold.
- Capitalize the term.
- Use a colon (`:`) between the term and the description.
- Capitalize the first letter of the description.
- End the description with a period.
- If the description introduces a nested list, restructure the sentence so that only one colon is present at the end.

Example:

- **Endpoint**: The URL of the JSON-RPC node.
- **Network**: The chain ID of the target network.

Do not mix description-list bullets with free-form bullets in the same list. If one item uses `**Term**: Description.`, every item in that list must.

Do not (one item is a description-list bullet; the rest are free-form):

- **Endpoint**: The URL of the JSON-RPC node.
- The chain ID of the target network
- Provide an API key in the header

This section provides only a subset of list formatting guidelines adapted for our documentation. For a complete reference, see the [Google Developer Style Guide on Lists](https://developers.google.com/style/lists#types-of-lists).

### Links

- Use descriptive link text. Avoid `this`, `here`, `click here`, `read more`, and `learn more`. If the link points to a specific article, use the title of that article as the link text.
- Links do not require any in-line formatting, such as bold, italics, or underlining. Depending on the project and the design, links might be underlined, but that will be managed using CSS.
- Opening external links in a new tab is handled automatically by the MkDocs plugin. Do not add `{target=\_blank}` manually.

Do:

```markdown
See the [Moonbase Alpha Faucet](https://faucet.moonbeam.network/) for test tokens.
```

Do not:

```markdown
Get test tokens [here](https://faucet.moonbeam.network/).
```

## Code Guidelines

This section of the document outlines guidelines for code formatting and conventions to adhere to.

### Code Formatting

- Use inline code elements for file names, variable names, function names, or any single line of code that serves as a reference and does not need to be copied.
- For inline code, put code elements in between single backticks (`).
- Use code blocks for multiple lines of code or any code (including single lines) that needs to be copied.
- For code blocks, put code elements in between triple backticks (```).
- Every code block must be assigned a language shortcode, which adds syntax highlighting. For example:
  ```
  ```js
  ```py
  ```solidity
  ```

#### Code Identifiers in Prose

Any reference to a code identifier in prose must be wrapped in backticks. This includes:

- Function and method names: `purgeKeys`, `set_keys`.
- Module, type, and pallet names: `StakingOperator`, `transactionStorage`.
- Variable and parameter names: `keys`, `proof`.
- File paths: `runtime/src/lib.rs`.

Do: `The proxy can call session.purgeKeys to release the deposit.` → write as `` The proxy can call `session.purgeKeys` to release the deposit. ``

Do not: leave identifiers as plain words. AI-generated prose often drops backticks on the second or third mention of an identifier — reviewers flag this consistently.

#### Identifier Consistency Within a Document

When you introduce an identifier or term, use the same form everywhere in the same page:

- If you write `purgeKeys` once, do not switch to `purge_keys` later — pick the form used in the source code and keep it.
- If you describe the role as "staker", do not switch to "validator" or "stash" in the next paragraph unless you have explicitly defined the relationship.
- Spelling, capitalization, and casing of an identifier or term must be identical on every mention.

#### Code Formatting by Language

|    Language     |      JavaScript/TypeScript       |               JSON               |                      Python                      |                                                        Solidity                                                         |
|:---------------:|:--------------------------------:|:--------------------------------:|:------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| Code Formatter  | [Prettier](https://prettier.io/) | [Prettier](https://prettier.io/) | [Black](https://black.readthedocs.io/en/stable/) | [Prettier plugin for Solidity](https://github.com/prettier-solidity/prettier-plugin-solidity?tab=readme-ov-file#vscode) |
|  Indent Style   |              space               |              space               |                      space                       |                                                          space                                                          |
|   Indent Size   |                2                 |                4                 |                        4                         |                                                            4                                                            |
| Max Line Length |                80                |                80                |                        80                        |                                                           80                                                            |
|   Quote Type    |              single              |              double              |                      double                      |                                                         double                                                          |
| Trailing Comma  |               true               |              false               |                       true                       |                                                          false                                                          |
|    Semicolon    |               true               |              false               |                      false                       |                                                          false                                                          |

### Variable Conventions

- For Python, use snake_case.
- For JavaScript, use camelCase.
- Root-level variables should be declared at the top of the code example (after any imports but before any functions).
- Do not use all uppercase letters for variable names unless they are exported constants.

  - Do: `export const PRIVATE_KEY = 'INSERT_PRIVATE_KEY';`
  - Do not: `const PRIVATE_KEY = 'INSERT_PRIVATE_KEY';`
  - Do not: `export const privateKey = 'INSERT_PRIVATE_KEY';`

- When users need to input personalized information, establish a variable to serve as a placeholder. Ensure that placeholder text adheres to the following conventions:
  - It should describe the variable.
  - It should be capitalized in all uppercase letter.
  - Written in snake_case.
  - Start with the keyword `INSERT`.
  - It should not use `HERE` or any other generic keyword aside from `INSERT`.
  - It should be put in quotation marks if the corresponding value requires quotation marks.
 
  See the following examples:

    - Do: `const address = 'INSERT_CONTRACT_ADDRESS';`
    - Do: `const addresses = ['INSERT_X_ADDRESS', 'INSERT_Y_ADDRESS', 'INSERT_Z_ADDRESS'];`
    - Do: `const amount = INSERT_AMOUNT_TO_SEND;`
    - Do not: `const address = 'INSERT-CONTRACT-ADDRESS';`
    - Do not: `const address = 'INSERT_CONTRACT_ADDRESS_HERE';`
    - Do not: `const privateKey = 'insert_privte_key';`

- If you're creating variables for arguments that need to be passed into a function, use the parameter name as the argument variable name. For example, if you have the following function:

  `execute(dest, weight)`

  Do — name the variables after the parameters. For this example, use `dest` and `weight`:
  
    ```js
    const dest = 'INSERT_DEST';
    const weight = 'INSERT_WEIGHT';
    execute(dest, weight);
    ```

  Do not — invent new variable names that do not match the parameters:
  
    ```js
    const xcmDest = 'INSERT_DEST';
    const xcmWeight = 'INSERT_WEIGHT';
    execute(xcmDest, xcmWeight);
    ```

### Capturing Terminal Output

If your code examples need to be run via the command line, you can include a terminal element in the documentation for the command and expected outcome. For more information, please refer to the [Terminal Output] section.

## Structure Guidelines

This section of the document outlines guidelines for repository structure and page structure.

### Repository Structure

- Use snippets for repetitive text or example code.
- Use a dedicated directory for all snippets (text and code should be separated into respective directories).
- Use a dedicated directory for all images.
- Directories for images and snippets should mirror the hierarchical structure of the documentation.

#### Naming Conventions

- Use descriptive names that clearly describe the file's purpose or content.
- Keep names short and concise.
- All directory and file names should use kebab-case (e.g., `hello-world.md`).
- Use lower-case letters in directory and file names.
- Do not use spaces or special characters.
- Always use the correct file extension for the file type (e.g., `.js` for JavaScript, `.py` for Python, `.md` for Markdown).

### Page Structure

- Use a table of contents.
- Most pages will require an introduction, except some reference pages.
- If users need to complete specific tasks or have certain items before going through the page, include a "Check Prerequisites" section.
- Include visual aids to illustrate concepts.

#### Headings and Titles

- Each page should have an H1 title.
- Each page should have a meta title (may be different than the H1 title) and meta description.
- Headings should follow a hierarchical order.
- Headings should not include numbers.
- Use descriptive headings based on the purpose of the section:
   - For task-based content, use a task-based heading (i.e., use "Create an Instance" instead of "Creating an Instance")
   - For a conceptual or non-task-based heading, use a noun phrase that doesn't start with an "-ing" verb (i.e., use "Blockchain Consensus Mechanisms" instead of "Understanding Blockchain Consensus")
- Do not insert a subheading immediately above a list that is already introduced by a lead-in sentence. If the lead-in is "These are the supported extrinsics:", do not add an extra `###` above the list. Replace the would-be subheading with a single sentence, or drop it entirely.

Do not:

```markdown
### Supported Extrinsics

The pallet supports the following extrinsics:

#### Extrinsics

- `store`
- `renew`
```

Do:

```markdown
### Supported Extrinsics

The pallet supports the following extrinsics:

- `store`
- `renew`
```

#### Introductions

When applicable, introductions should follow this recipe:

- Briefly introduce the topic.
- Describe the current standard, including existing methods and their limitations. This should paint a picture of the problem that the topic solves.
- Explain how the new feature addresses these limitations and its benefits.
- Provide a brief overview of the guide's content.

## Visual Aid Guidelines

This section of the document outlines guidelines for visual aids, such as images and diagrams. It is recommended to create templates for visual aids, such as diagrams and icons, to help promote consistency in style and size.

### Image File Naming

Image files must be named `<filename>-<number>.webp`, where `<filename>` matches the page or section the image belongs to and `<number>` is a zero-padded sequence reflecting the image's order on the page. This convention keeps images stable when pages are reorganized.

Do:

- `key-management-01.webp`
- `key-management-02.webp`
- `staking-operator-proxy-01.webp`

Do not:

- `screenshot.webp`
- `image1.webp`
- `polkadot-js-apps-rotate-keys.webp` (no sequence number)
- `Key-Management-01.WEBP` (use kebab-case, lowercase extension)

Image alt text should describe the image in a complete phrase for informative images. For purely decorative images — UI screenshots whose information is already in surrounding text, icons used for visual interest, or images that are not informative on their own — use empty `alt=""` so assistive technologies skip them. See [Google's alt text guidance](https://developers.google.com/style/images#alt-text).

### Icons

- Use icons from the same design system or library.
- Use the same stroke width.
- Use the same fill style (i.e., outline, filled, etc.).
- Use the same dimensions.
- Use the same color scheme.
- Use the same format. Icons should be either `.svg` or `.webp` files.

### Diagrams

- Use a consistent design language.
- Use the same line weight, color, and type (i.e., solid, dashed, etc.). You can use different types and colors, but there should be a valid reason for the difference.
- Use the same font family.
- Use consistent style and size shapes.
- Limit the amount of text in diagrams.
- Check the spacing of elements to ensure all elements are evenly spaced and, where applicable, align horizontally and vertically
- Diagrams should be `.webp` files.

### Screenshots

- Screenshots should be at 150% zoom.
- Resolution: Always use 300 DPI.
- Use the average size of 1510px width (height variable) for most purposes, ensuring that all elements are clear and sharp.
- Take screenshots in light or dark mode to match the theme of the documentation site. If your documentation has both light and dark themes available, take screenshots in dark mode.
- To highlight an item on the screenshot, add arrow(s) to the image.
- If more than one arrow is required, they should be numbered, and the document should have an ordered list that aligns with the numbers in the screenshot.
- Arrows should use the same color scheme.
- Arrows should be a consistent size.
- All screenshots of the browser should include the entire window, including the address bar.
- Images should be `.webp` files.

### Terminal Output

**Note:** This section applies to documentation sites that have implemented the [styled terminals](https://papermoonio.github.io/demo-docs/builders/get-started/features/#terminal-window) provided by PaperMoon. This is highly recommended to improve maintainability.

- Terminal output should be copied and formatted into a "terminal snippet" (see below).
- Show the command that was run.
- Show the output of running that command.
- If the terminal output concludes without requiring user input, returning you to the command prompt to enter the next command, show the blank command prompt.

Terminal snippets are styled HTML elements:

```
<div id="termynal" data-termynal>
  <span data-ty="input"><span class="file-path"></span>INSERT_COMMAND</span>
  <span data-ty>INSERT_OUTPUT</span>
  <span data-ty>INSERT_ADDITIONAL_OUTPUT</span>
  <span data-ty="input"><span class="file-path"></span></span>
</div>
```
