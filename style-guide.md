# Developer Documentation Style Guide

This document sets forth the standards and best practices for crafting high-quality technical documentation. It is intended to help you produce clear, consistent, and accessible content. It covers various topics, from writing style and formatting to code examples, images, and more.

The guidelines listed in this document aren't all-inclusive but strive to cover the basics. If this guide does not provide explicit guidance on a particular subject, please default to the [Google developer documentation style guide](https://developers.google.com/style).

## Table of Contents

- [Content Guidelines](#content-guidelines)
  - [Best Practices](#best-practices)
  - [Language](#language)
  - [Accessibility](#accessibility)
  - [Terminology](#terminology)
  - [Punctuation](#punctuation)
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
  - [Links](#links)

- [Code Guidelines](#code-guidelines)
  - [Code Formatting](#code-formatting)
    - [Code Formatting by Language](#code-formatting-by-language)
  - [Variable Conventions](#variable-conventions)
  - [Capturing Terminal Output](#capturing-terminal-output)

- [Structure Guidelines](#structure-guidelines)
  - [Repository Structure](#repository-structure)
    - [Naming Conventions](#naming-conventions) 
  - [Page Structure](#page-structure)
    - [Heading and Titles](#headings-and-titles)
    - [Introductions](#introductions)

- [Visual Aid Guidelines](#visual-aid-guidelines)
  - [Icons](#icons)
  - [Diagrams](#diagrams)
  - [Screenshots](#screenshots)
  - [Terminal Output](#terminal-output)
 

## Content Guidelines

This section of the document provides guidelines on best practices, language usage, accessibility considerations, terminology standardization, and more.

### Best Practices

- Use a formal tone that conveys confidence. Avoid casual language or slang
- Keep sentences short and to the point. Avoid unnecessary jargon and ambiguity
- Maintain a neutral and objective tone. Avoid biases, opinions, or emotional language
- Provide context. Avoid assuming the reader already knows what you're talking about
- Stick to the facts. Avoid sounding like a sales pitch
- Write timeless documentation that doesn't anchor the content to a specific point in time. Avoid using "at the time of writing," "currently," etc.
- Use bulleted lists for key points and complex information and to break up walls of text (general readability)
- Use numbered lists for step-by-step instructions and sequential items

### Language

- Avoid possessive language, such as "our," "we," etc., unless writing an informal tutorial
- Address the reader as _you_
- In tutorials and guides, where you're instructing a user to act, use an active voice
- In conceptual documentation, where you're not instructing a user to act, using a passive voice is permitted
- Be mindful of pronouns. Avoid unnecessarily gendered language

### Accessibility

- Headings should follow a hierarchical structure, starting with H1 (`#`)
- Use alt text for all images. The alt text should describe what the image depicts
- Use descriptive and meaningful link text. Avoid using "here" in link text. If the link points to a specific article, use the title of that article as the link text
- Avoid directional language, such as "above" or "below"

### Terminology

- For token standards, put a dash (`-`) between the standard prefix and the unique identifier for the standard. For example, ERC-20 instead of ERC20
- Use JSON-RPC instead of JSON RPC
- Use dApp instead of dapp or DApp (except at the beginning of a sentence)
- Use "and more" or "and so on" instead of "etc."

### Punctuation

- Use Oxford commas
- Use dashes in lists (instead of colons)
- Do not put periods at the end of a list item
- Do not use exclamation marks in formal writing

### Text Formatting

#### Bold

- Put bold elements between double asterisks (`**`)
- Use bold formatting for:
  - When referencing UI elements
  - List items where we're listing out terms with a description. The term will be in bold. See [List Formatting](#list-formatting) for an example
  - Sparingly can be used to highlight can't-miss, important things

#### Italics

- Put italic elements between single underscores (`_`)
- Use italics when drawing attention to a specific word or phrase, for example, when introducing a new term

#### Underline

- Do not underline text

#### Symbols

- Do not use emojis
- Do not use ampersands (`&`) unless referring to a UI element that uses them

#### Numbers

- Spell out numbers as words for numbers zero through nine

#### Quotes

- Use double quotes in regular text
- Commas and periods go inside quotation marks
- Single quotes should only be used in code examples, depending on the guidelines in the [Code Formatting By Language](#code-formatting-by-language) section

#### Capitalization

- Use Chicago title-style capitalization for titles and headings, which capitalizes the first word plus all other significant words
- Capitalize product names
- Avoid unnecessary capitalization; before you capitalize a word, think about why and if it should be capitalized

### Table Formatting

- Use tables to represent sets of related pieces of data in a structured way
- Table headers and values should be centered
- Tables should be formatted. You can use a tool to format the tables, like the [Markdown Table Formatter VSCode extension](https://marketplace.visualstudio.com/items?itemName=fcrespo82.markdown-table-formatter)

### List Formatting

- Use ordered (numbered) lists for a sequence of steps
- Use unordered (bulleted) lists for items that are non-sequential and can be read or completed in any order
- For description lists, use the following formatting: `**term** - description`
  - Put the term in bold
  - Use a dash (`-`) between the term and the description
  - Do not capitalize the first word in the description, unless it's an acronym or product name that should be capitalized
- Do not add punctuation at the end of each list item

### Links

- Add `{target=\_blank}` to all links, except links to other sections on the same page
- Use descriptive link text; avoid using "this", "here", and other generic words in the link text
- Links do not require any in-line formatting, such as bold, italics, or underlining. Depending on the project and the design, links might be underlined, but that will be managed using CSS

## Code Guidelines

This section of the document outlines guidelines for code formatting and conventions to adhere to.

### Code Formatting

- Use inline code elements for file names, variable names, function names, or any single line of code that serves as a reference and does not need to be copied
- For inline code, put code elements in between single backticks (`)
- Use code blocks for multiple lines of code or any code (including single lines) that needs to be copied
- For code blocks, put code elements in between triple backticks (```)
- Every code block must be assigned a language shortcode, which adds syntax highlighting. For example:
  ```
  ```js
  ```py
  ```solidity
  ```

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

- For Python, use snake_case
- For JavaScript, use camelCase
- Root-level variables should be declared at the top of the code example (after any imports but before any functions)
- Do not use all uppercase letters for variable names unless they are exported constants

  - 🟢 `export const PRIVATE_KEY = 'INSERT_PRIVATE_KEY';`
  - 🔴 `const PRIVATE_KEY = 'INSERT_PRIVATE_KEY';`
  - 🔴 `export const privateKey = 'INSERT_PRIVATE_KEY';`

- When users need to input personalized information, establish a variable to serve as a placeholder. Ensure that placeholder text adheres to the following conventions:
  - It should describe the variable
  - It should be capitalized in all uppercase letters
  - Written in snake_case
  - Start with the keyword `INSERT`
  - It should not use `HERE` or any other generic keyword aside from `INSERT`
  - It should be put in quotation marks if the corresponding value requires quotation marks
 
  See the following examples:

    - 🟢 `const address = 'INSERT_CONTRACT_ADDRESS';`
    - 🟢 `const addresses = ['INSERT_X_ADDRESS', 'INSERT_Y_ADDRESS', 'INSERT_Z_ADDRESS'];`
    - 🟢 `const amount = INSERT_AMOUNT_TO_SEND;`
    - 🔴 `const address = 'INSERT-CONTRACT-ADDRESS';`
    - 🔴 `const address = 'INSERT_CONTRACT_ADDRESS_HERE';`
    - 🔴 `const privateKey = 'insert_privte_key';`

- If you're creating variables for arguments that need to be passed into a function, use the parameter name as the argument variable name. For example, if you have the following function:

  `execute(dest, weight)`

  🟢 You should name the variables after the parameters. For this example, you would use dest and weight:
  
    ```js
    const dest = 'INSERT_DEST';
    const weight = 'INSERT_WEIGHT';
    execute(dest, weight);
    ```

  🔴 This is as opposed to doing something like this:
  
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

- Use snippets for repetitive text or example code
- Use a dedicated directory for all snippets (text and code should be separated into respective directories)
- Use a dedicated directory for all images
- Directories for images and snippets should mirror the hierarchical structure of the documentation

#### Naming Conventions

- Use descriptive names that clearly describe the file's purpose or content
- Keep names short and concise
- All directory and file names should use kebab-case (e.g., `hello-world.md`)
- Use lower-case letters in directory and file names
- Do not use spaces or special characters
- Always use the correct file extension for the file type (e.g., `.js` for JavaScript, `.py` for Python, `.md` for Markdown)

### Page Structure

- Use a table of contents
- Most pages will require an introduction, except some reference pages
- If users need to complete specific tasks or have certain items before going through the page, include a "Check Prerequisites" section
- Include visual aids to illustrate concepts

#### Headings and Titles

- Each page should have an H1 title
- Each page should have a meta title (may be different than the H1 title) and meta description
- Headings should follow a hierarchical order
- Headings should not include numbers
- Use descriptive headings based on the purpose of the section:
   - For task-based content, use a task-based heading (i.e., use "Create an Instance" instead of "Creating an Instance")
   - For a conceptual or non-task-based heading, use a noun phrase that doesn't start with an "-ing" verb (i.e., use "Blockchain Consensus Mechanisms" instead of "Understanding Blockchain Consensus")

#### Introductions

When applicable, introductions should follow this recipe:

- Briefly introduce the topic
- Describe the current standard, including existing methods and their limitations. This should paint a picture of the problem that the topic solves
- Explain how the new feature addresses these limitations and its benefits
- Provide a brief overview of the guide's content

## Visual Aid Guidelines

This section of the document outlines guidelines for visual aids, such as images and diagrams. It is recommended to create templates for visual aids, such as diagrams and icons, to help promote consistency in style and size.

### Icons

- Use icons from the same design system or library
- Use the same stroke width
- Use the same fill style (i.e., outline, filled, etc.)
- Use the same dimensions
- Use the same color scheme
- Use the same format. Icons should be either `.svg` or `.webp` files

### Diagrams

- Use a consistent design language
- Use the same line weight, color, and type (i.e., solid, dashed, etc.). You can use different types and colors, but there should be a valid reason for the difference
- Use the same font family
- Use consistent style and size shapes
- Limit the amount of text in diagrams
- Check the spacing of elements to ensure all elements are evenly spaced and, where applicable, align horizontally and vertically
- Diagrams should be `.webp` files

### Screenshots

- Screenshots should be at 150% zoom
- Resolution: Always use **300 DPI**.
- Use the average size of 1510px width (height variable) for most purposes, ensuring that all elements are clear and sharp.
- Take screenshots in light or dark mode to match the theme of the documentation site. If your documentation has both light and dark themes available, take screenshots in dark mode
- To highlight an item on the screenshot, add arrow(s) to the image
- If more than one arrow is required, they should be numbered, and the document should have an ordered list that aligns with the numbers in the screenshot
- Arrows should use the same color scheme
- Arrows should be a consistent size
- All screenshots of the browser should include the entire window, including the address bar
- If editing the screenshot in any way, make sure to keep an SVG of the modified image in a directory accessible to the rest of the team
- Images should be `.webp` files
- Image Placement (Moonbeam - Tanssi):
  - Upload all image copies to the corresponding Drive folder following the same path as the technical document.
  - Inside the Drive folder, create a subfolder called `crop` containing the **unedited SVG** version of the image.
  - Ensure the **edited image** used in the technical document is outside the `crop` folder, resized to the appropriate dimensions.

### Terminal Output

**Note:** This section applies to documentation sites that have implemented the [styled terminals](https://papermoonio.github.io/demo-docs/builders/get-started/features/#terminal-window) provided by PaperMoon. This is highly recommended to improve maintainability.

- Terminal output should be copied and formatted into a "terminal snippet" (see below)
- Show the command that was run
- Show the output of running that command
- If the terminal output concludes without requiring user input, returning you to the command prompt to enter the next command, show the blank command prompt

Terminal snippets are styled HTML elements:

```
<div id="termynal" data-termynal>
  <span data-ty="input"><span class="file-path"></span>INSERT_COMMAND</span>
  <span data-ty>INSERT_OUTPUT</span>
  <span data-ty>INSERT_ADDITIONAL_OUTPUT</span>
  <span data-ty="input"><span class="file-path"></span></span>
</div>
```
