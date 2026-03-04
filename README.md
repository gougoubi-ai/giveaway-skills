# giveaway-skills

`giveaway-skills` is a BSC on-chain giveaway (red packet) contract skill repository for AI Agents.  
It is built around `contracts/contracts/Giveaway.sol` and provides standardized call descriptions and best practices to help Agents safely and reliably create giveaways, claim giveaways, manage whitelists, and withdraw expired giveaways under natural-language instructions.

---

## About this repository

This repository contains the Skill definition and documentation related to the **Giveaway contract**, with the main goals:

- **Unified specification**: define the contract address, core method signatures, parameter meanings, and return value explanations.
- **Lower integration barrier**: provide reusable call templates for scripts, frontends, and workflows (such as OpenClow).
- **Serve Agents**: enable various AI Agents (regardless of framework) to access BSC giveaway capabilities with minimal configuration.

The core description and usage conventions are centralized in `SKILL.md`; it is recommended to read it fully before integrating.

---

## Use cases

Use this Skill when you need to perform the following operations on the **BSC network**:

- **Create giveaway**: create an on-chain giveaway that can be claimed once or multiple times.
- **Claim giveaway**: claim assets based on a giveaway ID.
- **Whitelist management**: maintain an allowlist of addresses for specific campaigns.
- **Withdraw expired**: withdraw unclaimed giveaway balance after the campaign ends or expires.

Whether you are using scripts (Node.js/TS), a frontend DApp, or a workflow engine (such as OpenClow), you can follow the conventions in `SKILL.md` and use libraries like `ethers` / `viem` / `web3` to interact with this contract.

---

## Directory overview

- **`contracts/contracts/Giveaway.sol`**: core implementation of the giveaway contract.
- **`SKILL.md`**: Skill metadata, call conventions, and examples (the main entry document for AI Agent integration).
- Other scripts or config files: to be added as needed (e.g., deployment scripts, test examples, etc.).

The concrete file structure may evolve over time; always refer to the latest version in the repository.

---

## Contribution guide

Contributions and PRs to improve this Skill are welcome, including but not limited to:

- Adding or correcting documentation (parameter descriptions, code examples, edge cases).
- Adding examples in different languages/frameworks (such as Python, Go, different frontend stacks).
- Improving test cases or local development scripts.

Recommended workflow:

1. **Create a branch**
   ```bash
   git checkout -b feature/<your-change>
   ```
2. **Complete your changes and pass local tests.**
3. **Open a Pull Request**, explaining the motivation and impact of your changes.

---

## Disclaimer

This repository and its Skill configurations, contract examples, and documentation are for technical research and reference only.  
They do **not** constitute any investment, financial, or trading advice, nor any guarantee of returns.  
On-chain operations carry high risk, including but not limited to contract risk, private key/mnemonic leakage, and market volatility.

Before using any content from this repository with real funds, you should:

- Fully understand the contract logic and call risks;
- Verify the correctness of the flow with small amounts and in test environments;
- Make prudent decisions based on your own situation and bear all consequences yourself.

The maintainers of this repository do not bear legal responsibility for any loss or liability arising from the use of this repository.
