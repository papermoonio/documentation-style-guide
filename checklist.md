# Documentation Checklist

Before requesting a PR review, please check your work against this list of commonly missed items from the style guide. 

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
	- [ ] Ensure all external links are followed by `{target=\_blank}` so they will open in a new tab when selected. For internal links, use your best judgment (i.e., links at the end of the page where we direct users to the next page do not need to open in a new tab).
		- **Example**: `[Link text](link url){target=\_blank}`
	- [ ] Use descriptive and meaningful link text:
		- **Recommended**: "You can get DEV tokens for testing on Moonbase Alpha once every 24 hours from the [Moonbase Alpha Faucet](https://faucet.moonbeam.network/){target=\_blank}." 
		- **Not recommended**: "You can get DEV tokens for testing on Moonbase Alpha [here](url){target=\_blank}."
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
	- [ ] **Example**: "Click `**Deploy**` to deploy your smart contract"
