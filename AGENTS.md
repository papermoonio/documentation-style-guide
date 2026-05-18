# AGENTS.md — PaperMoon Documentation Rules for Coding Agents

This file is the **machine-readable** PaperMoon style guide. Coding agents (Claude Code, Cursor, Codex, etc.) load `AGENTS.md` automatically from a repo root. Downstream PaperMoon docs repos should reference this file from their own `AGENTS.md` so these rules apply on every authoring session.

The full prose version lives in [`style-guide.md`](./style-guide.md). If the two ever disagree, **the prose guide wins** — open a PR to reconcile.

---

## How to use this file

If you are an authoring agent generating or editing documentation in a PaperMoon docs repo:

1. Read the rules below **before** producing prose or markdown.
2. Re-check the output against the **Pre-output checklist** at the bottom before returning it to the user.
3. When a rule below is silent on a case, default to the [Google developer documentation style guide](https://developers.google.com/style).

---

## High-friction rules (the ones that get missed)

These are the rules that authoring tools (and humans) violate most often. Treat them as hard constraints.

### 1. List item punctuation

One rule, applied per list:

- If list items are **full sentences or complete thoughts**, end each item with a period.
- If list items are **single words, short fragments, or code tokens**, omit the period.
- A numbered step label ending in a colon (e.g., `1. Configure the node:`) already counts as punctuated — do not add a trailing period after the colon.
- **All items in the same list must follow the same form.** Never mix.

Do:

```markdown
You can do any of the following by using the API:

- Create an item.
- Replace one item with another.
- Update an item.
- Delete an item.
```

```markdown
The API supports the following actions:

- Create
- Replace
- Update
- Delete
```

Don't:

```markdown
- Create an item
- Replace one item with another.
- Update.
- Delete an item
```

### 2. Bold

Use bold **only** for:

- UI element names (button labels, menu items, field names).
- The term in a description list: `**Term**: Description.`

Do **not** bold for emphasis in prose. Do not bold whole sentences. Do not bold to "draw attention" — write a clearer sentence instead.

Do:

```markdown
Click **Deploy** to publish the contract.

- **Endpoint**: The URL of the JSON-RPC node.
- **Network**: The chain ID of the target network.
```

Don't:

```markdown
This is **really important** — you **must** save your key.

The contract address is **0xabc...123**.
```

### 3. Headings — Chicago title case

Capitalize the first word and all other significant words. Articles, coordinating conjunctions, and short prepositions stay lowercase unless they're the first word.

Do:

- `## Deploy a Contract to the Network`
- `### Connect Your Wallet`

Don't:

- `## Deploy a contract to the network` (sentence case)
- `## Deploying a Contract to the Network` (`-ing` form for a task heading — use the imperative)

For task-based headings, use the imperative: **Create an Instance**, not **Creating an Instance**.
For conceptual headings, use a noun phrase: **Blockchain Consensus Mechanisms**, not **Understanding Blockchain Consensus**.

### 4. Numbers

Spell out zero through nine. Use digits for 10 and above.

Exceptions — always use digits:

- Version numbers: `Node.js 18`, `Python 3`.
- Measurements and units: `4 GB`, `8 cores`, `2 ms`.
- Code and CLI flags: `--max-count 5`.
- Inside tables.

Do: `Run the command three times.`
Don't: `Run the command 3 times.`

### 5. Banned words and phrases (AI tells)

Do not emit these. They are filler, marketing copy, or LLM clichés that PaperMoon documentation does not use.

| Banned | Use instead |
|---|---|
| delve into, dive into | (omit, or "explore", "walk through") |
| leverage | use |
| utilize | use |
| seamless, seamlessly | (omit) |
| robust | (omit, or be specific: "production-tested", "fault-tolerant") |
| powerful, cutting-edge, state-of-the-art | (omit) |
| in today's world, in the modern era | (omit) |
| it's important to note that | (omit — just state the thing) |
| it's worth noting that | (omit) |
| in summary, in conclusion | (omit — let the structure carry it) |
| let's, we'll, our | (avoid first-person plural; address the reader as *you*) |
| currently, at the time of writing, as of today | (omit — write timeless docs) |
| etc. | "and more" or "and so on" |
| simply, just, easily, obviously | (omit — never describe steps as easy) |
| feel free to | (omit) |
| under the hood | (omit, or "internally") |

### 6. Em dash and en dash

- **Em dash (`—`, U+2014)**: use sparingly to set off a parenthetical aside. Surround with spaces: `text — aside — more text`. Do not chain em dashes; one per sentence at most.
- **En dash (`–`, U+2013)**: only for numeric ranges: `2024–2025`, `pages 10–14`.
- **Hyphen (`-`)**: compound words and identifiers (`ERC-20`, `kebab-case`).

Do not substitute two hyphens (`--`) for an em dash. Use the actual `—` character.

LLM output tends to over-use em dashes. If your output has more than one em dash per paragraph, rewrite with periods or commas.

### 7. Contractions

Use contractions sparingly. Default to the expanded form (`do not`, `cannot`, `it is`) in reference and conceptual documentation. Contractions are acceptable in informal tutorials.

### 8. Links

- Use descriptive link text. Never use `here`, `this`, `click here`, `read more`, `learn more`.
- External links: append `{target=\_blank}`.
- Internal links to the same page: do **not** append `{target=\_blank}`.
- Do not bold, italicize, or underline links.

Do: `See the [Moonbase Alpha Faucet](https://faucet.moonbeam.network/){target=\_blank} for test tokens.`

Don't: `Get test tokens [here](https://faucet.moonbeam.network/){target=\_blank}.`

### 9. Symbols and emojis

- No emojis in documentation prose, headings, or bullet markers. This includes ✅, ❌, 🟢, 🔴, ⚠️, 🚀, and decorative symbols.
- Even outside documentation prose (HTML templates, banners, UI elements where an emoji is intentional), never use the rocket emoji (🚀) for blockchain projects — it reads as speculative hype. Prefer a neutral alternative (📣, 📢) or text only.
- Use `Do:` / `Don't:` text labels for DO/DON'T comparisons.
- No ampersands (`&`) unless they are in a UI element label or code.
- No exclamation marks.

### 10. Voice and address

- Address the reader as **you**.
- Avoid first-person plural: no `we`, `our`, `let's`.
- Tutorials and guides: active voice (`Deploy the contract.`).
- Conceptual reference: passive is allowed (`The contract is deployed by the runtime.`).
- Do not use unnecessarily gendered language.

### 11. Terminology (PaperMoon-specific)

Always use these spellings:

| Use | Not |
|---|---|
| ERC-20, ERC-721, ERC-1155 | ERC20, ERC 20 |
| JSON-RPC | JSON RPC, JSONRPC |
| dApp | dapp, DApp (DApp is acceptable only at sentence start or in a Chicago title-case heading) |
| TestNet | testnet, test net |
| MainNet | mainnet, main net |
| smart contract | smart-contract (unless used as an adjective: `smart-contract platform`) |
| supermajority | super majority, super-majority |
| and more / and so on | etc. |

- Define every acronym on first use in each article.
- Hyphenated identifiers and runtime/network profile names (e.g., `paseo-next`, `westend-next`) keep their canonical casing on **every** mention. Never capitalize only the first letter because it starts a sentence — rephrase the sentence so the identifier is not sentence-initial.

### 12. Variable placeholders in code examples

Placeholders must:

- Start with `INSERT_`.
- Be `UPPER_SNAKE_CASE`.
- Describe the value (`INSERT_CONTRACT_ADDRESS`, not `INSERT_VALUE`).
- Not end with `HERE` or other generic words.
- Be wrapped in quotes when the value type requires quotes.

Do: `const address = 'INSERT_CONTRACT_ADDRESS';`
Don't: `const address = 'YOUR_ADDRESS_HERE';`
Don't: `const address = '<your-address>';`

### 13. Code blocks

- Every fenced code block declares a language: ` ```js `, ` ```py `, ` ```solidity `, ` ```bash `, ` ```json `.
- Use inline code (single backticks) for filenames, variable names, function names, CLI flags, and single-line code references that are not meant to be copied.
- Use fenced code blocks for anything multi-line or meant to be copied.

### 14. Quotes

- Double quotes in prose.
- Periods and commas go **inside** the closing quote: `He said "yes."`
- Single quotes only inside code, when the language's style guide specifies them (JavaScript: single; JSON/Python: double).

### 15. Punctuation

- Oxford comma, always: `Polkadot, Kusama, and Moonbeam`.
- Use colons (not dashes) to introduce lists.
- No exclamation marks.

### 16. Code identifiers in prose must be in backticks

Every reference to a function name, method, type, module, pallet, variable, parameter, or file path in prose must be wrapped in backticks.

Do: `` The proxy can call `session.purgeKeys` to release the deposit. ``
Don't: `The proxy can call session.purgeKeys to release the deposit.`

This is a recurring reviewer correction — on the second or third mention of an identifier, AI-generated prose often drops the backticks.

### 17. Identifier and term consistency within a document

Once you introduce an identifier or term on a page, use the same form throughout that page:

- Pick one casing for an identifier and keep it (`purgeKeys` everywhere, not `purgeKeys` then `purge_keys`).
- Pick one term for a role and keep it ("staker" everywhere, not "staker" then "validator" then "stash").
- Match what's in the source code or schema. If the code says `purgeKeys`, the docs say `purgeKeys`.

### 18. Image file naming

Image files use the pattern `<topic>-<number>.webp`:

- `key-management-01.webp`, `key-management-02.webp`
- Sequence-numbered so reorganizing a page does not break filename meaning.
- Lowercase kebab-case. Lowercase `.webp` extension.

Don't: `screenshot.webp`, `image1.webp`, descriptive-but-unnumbered names like `polkadot-js-rotate-keys.webp`.

### 19. Don't insert subheadings above lead-in-sentence lists

If a list is introduced by a sentence ending in `:` ("The following extrinsics are supported:"), do not add an extra heading above it. AI-generated content tends to insert a subheading per list; reviewers strip them.

Do:

```markdown
### Supported Extrinsics

The pallet supports the following extrinsics:

- `store`
- `renew`
```

Don't:

```markdown
### Supported Extrinsics

The pallet supports the following extrinsics:

#### Extrinsics

- `store`
- `renew`
```

### 20. Do not mix description-list and free-form bullets

If one bullet in a list uses `**Term**: Description.`, every bullet in that list must. If you can't write all of them in that form, drop the description-list format entirely and use plain bullets.

---

## Pre-output checklist (run before returning prose to the user)

Mentally scan the draft for each item. Fix any miss.

- [ ] Every list has consistent end-punctuation (all periods or none).
- [ ] No bold used for emphasis in prose — only UI elements and description-list terms.
- [ ] Every heading is Chicago title case; task headings use imperative form.
- [ ] No banned phrases ("delve", "leverage", "seamless", "it's important to note", "let's", "currently", "simply", "etc.").
- [ ] Single-digit numbers (0–9) spelled out in prose; digits used for versions, units, and code.
- [ ] At most one em dash per paragraph; en dash used only for ranges.
- [ ] Address the reader as "you"; no "we" / "our" / "let's".
- [ ] All external links append `{target=\_blank}`; link text is descriptive (no "here", "this", "click here").
- [ ] No emojis anywhere — including ✅ / ❌ / 🟢 / 🔴.
- [ ] Every code block has a language tag.
- [ ] Placeholders are `INSERT_UPPER_SNAKE_CASE` and describe the value.
- [ ] Terminology: `ERC-20`, `JSON-RPC`, `dApp`, `TestNet`, `MainNet`.
- [ ] Oxford commas present.
- [ ] Every code identifier in prose is in backticks — including the second and third mention.
- [ ] Identifiers and role terms are spelled the same on every mention in the page.
- [ ] Image files follow `<topic>-<number>.webp`; alt text is non-empty.
- [ ] No subheading sits directly above a list that already has a lead-in sentence.
- [ ] Description-list bullets are not mixed with free-form bullets in the same list.

---

## Linting

This repo ships a starter [Vale](https://vale.sh) configuration in [`.vale.ini`](./.vale.ini) and [`styles/PaperMoon/`](./styles/PaperMoon/). Downstream repos should adopt it so the banned-phrase, terminology, and emoji rules are enforced mechanically rather than in prose review.

Run locally:

```bash
vale .
```

---

## How a downstream docs repo wires this in

Add an `AGENTS.md` at the root of the downstream repo containing at least:

```markdown
# AGENTS.md

This repo follows the [PaperMoon Documentation Style Guide](https://github.com/papermoonio/documentation-style-guide/blob/main/AGENTS.md). Read it before generating or editing any documentation in this repository.

Project-specific overrides:

- (list any deviations here, with rationale)
```

Coding agents that respect the `AGENTS.md` convention will load both files automatically.
