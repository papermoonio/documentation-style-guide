# Documentation checklist

Before requesting a PR review, please check your work against this list of commonly missed items from the style guide. 

Guidance for Grammarly, Screenshots, and Diagrams can be found in the internal Docs Standards. 

- [ ] Check your lists
    - [ ] Ensure lists requiring a specific order (step-by-step instructions, etc.) are numbered
    - [ ] Use bullets for lists that can be in any order (list of features, etc.)
    - [ ] Check your formatting for list items - they should look like:
	    - Item name - copy about the item/description
		    - [ ] Item name capitalized
		    - [ ] space, dash, space between item name and description
		    - [ ] the description starts with a lowercase letter
		    - [ ] there is no punctuation at the end of the description
- [ ] Check your links
	- [ ] Ensure all links are followed by `{target=\_blank}` so they will open in a new tab when selected
		- Example link -`[Link text](link url){target=\_blank}`
	- [ ] Use descriptive and meaningful link text
		- Recommended -  "You can get DEV tokens for testing on Moonbase Alpha once every 24 hours from the [Moonbase Alpha Faucet](https://faucet.moonbeam.network/){target=\_blank}." 
		- Not Recommended -  "You can get DEV tokens for testing on Moonbase Alpha [here](url){target=\_blank}."
- [ ] Check your images
	- [ ] All browser screenshots should have the browser window in them
	- [ ] All images should be sized - Width: 756px, Height: variable
	- [ ] All images should have alt text for accessibility
		- Example image with alt text - `![Alt text in here](/path/to/image/goes/here)`
- [ ] Check your code snippets
	- [ ] Did you use inline code elements (between single backticks) for file names, variable names, function names, or any single line of code that serves as a reference and does not need to be copied?
	- [ ] Did you use code blocks for multiple lines of code or any code that needs to be copied?
		- [ ] All code blocks put code elements between triple backticks 
		- [ ] All code blocks include a language shortcode for syntax highlighting
		- [ ] Did you run Prettier or Black to format your code blocks?
- [ ] Check your headings
	- [ ] Headings should follow a hierarchical structure, starting with H1 (`#`)
	- [ ] You should be able to understand the main points of your content using only the headings. Do they make sense? Are they in a logical order that flows well?
- [ ] Check your industry-specific words 
	- [ ] For token standards, put a dash (`-`) between the standard prefix and the unique identifier for the standard. For example, ERC-20 instead of ERC20
	- [ ] Use JSON-RPC instead of JSON RPC
	- [ ] Use dApp instead of dapp.  
		- DApp is ok at the beginning of a sentence or when capitalizing for a title or heading
	- [ ] Use TestNet instead of testnet or test net
- [ ] Check for bold formatting on UI elements 
	- [ ] Example - "Click `**Deploy**` to deploy your smart contract"