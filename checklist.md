# Documentation Checklist

Before requesting a PR review, please check your work against this list of commonly missed items from the style guide.

If you authored this content with an AI coding agent (Claude Code, Cursor, Codex, etc.), the [`AGENTS.md`](./AGENTS.md) rule set should already be loaded by the agent. Even so, _always_ run through this checklist before requesting review — these are the items reviewers most frequently flag.

Guidance for Grammarly, screenshots, and diagrams can be found on the internal Docs Standards page in the Wiki.

- [ ] Check your lists:
    - [ ] Ensure lists requiring a specific order (step-by-step instructions, etc.) are numbered.
    - [ ] Use bullets for lists that can be in any order (list of features, etc.).
    - [ ] Check your formatting for list items. They should look like:
	    - **Item name**: Copy about the item/description.
		    - [ ] Item name capitalized and in bold.
		    - [ ] Space, colon, space between item name and description.
		    - [ ] The description starts with a lowercase letter.
		    - [ ] Punctuation at the end of the description.
- [ ] Check your links:
	- [ ] Opening external links in a new tab is handled automatically by the MkDocs plugin. Do not add `{target=\_blank}` manually.
	- [ ] Use descriptive and meaningful link text:
		- **Recommended**: "You can get DEV tokens for testing on Moonbase Alpha once every 24 hours from the [Moonbase Alpha Faucet](https://faucet.moonbeam.network/)." 
		- **Not recommended**: "You can get DEV tokens for testing on Moonbase Alpha [here](url)."
- [ ] Check your images:
  - [ ] All browser screenshots should have the browser window in them, showing the URL.
  - [ ] For full page screenshots, they should have a minimum width of 1510px.
  - [ ] Ensure 300 DPI for clarity.
  - [ ] Images should have alt text for accessibility purposes, with some exceptions, as outlined in the [Google Developer Documentation Style Guide](https://developers.google.com/style/images#alt-text).
    - **Example**: `![Alt text in here](/path/to/image/goes/here)`
- [ ] Check your code snippets:
	- [ ] Did you use inline code elements (between single backticks) for file names, variable names, function names, or any single line of code that serves as a reference and does not need to be copied?
	- [ ] Did you use code blocks for multiple lines of code or any code that needs to be copied?
		- [ ] All code blocks put code elements between triple backticks.
		- [ ] All code blocks include a language shortcode for syntax highlighting.
		- [ ] Did you run Prettier or Black to format your code blocks?
- [ ] Check your headings:
	- [ ] Headings should follow a hierarchical structure, starting with H1 (`#`).
	- [ ] You should be able to understand the main points of your content using only the headings. Do they make sense? Are they in a logical order that flows well?
- [ ] Check your industry-specific words:
	- [ ] For token standards, put a dash (`-`) between the standard prefix and the unique identifier for the standard. For example, ERC-20 instead of ERC20.
	- [ ] Use JSON-RPC instead of JSON RPC.
	- [ ] Use dApp instead of dapp. DApp is ok at the beginning of a sentence or when capitalizing for a title or heading.
	- [ ] Use TestNet instead of testnet or test net, unless otherwise specified per brand-specific guidelines.
- [ ] Check for bold formatting on UI elements:
	- [ ] Example: "Click `**Deploy**` to deploy your smart contract"
	- [ ] Bold is not used for emphasis in prose. For emphasis on a specific word or phrase, use italics (`_word_`). For a stronger callout, use an admonition (`!!! note`, `!!! warning`).
- [ ] Check for code identifiers in backticks:
	- [ ] Every function, method, type, pallet, module, variable, parameter, and file path reference in prose is wrapped in backticks — on the first mention AND every subsequent mention.
- [ ] Check identifier and term consistency within the page:
	- [ ] An identifier is spelled the same on every mention (e.g., `purgeKeys` everywhere, not switching to `purge_keys`).
	- [ ] A role or term is named the same on every mention (e.g., "staker" everywhere, not switching between "staker", "validator", and "stash").
- [ ] Check image filenames:
	- [ ] Image files follow `<filename>-<number>.webp` (lowercase kebab-case, sequence-numbered).
- [ ] Check structure for AI-generated redundancy:
	- [ ] No subheading sits directly above a list that's already introduced by a lead-in sentence ending in `:`.
	- [ ] No mixed description-list and free-form bullets in the same list.
- [ ] Check for AI-generated tells:
	- [ ] No banned phrases ("delve", "leverage", "seamless", "robust", "it's important to note", "in summary", "feel free to", "currently", "etc.", "simply", "just", "easily").
	- [ ] At most one em dash per paragraph.
	- [ ] Address the reader as "you" — no "we", "our", "let's" (except in informal tutorials).
