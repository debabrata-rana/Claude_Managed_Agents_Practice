# Claude Managed Agents Practice

This repository is a hands-on collection of Jupyter notebooks for experimenting with Anthropic's Claude Managed Agents capabilities. Instead of a traditional application, the project focuses on live API patterns for creating agents, attaching tools, orchestrating multi-agent workflows, connecting to MCP servers, and persisting context through memory and vaults.

## What is implemented

The project includes working examples for the following:

- Basic agent creation, environment setup, and session management
- Multi-agent orchestration with specialized researcher/writer/coordinator roles
- Custom skills for domain-specific behavior
- External tool access through MCP servers
- PDF document analysis with uploaded files
- Persistent memory stores for user context and profile data
- Vault-based secret management for GitHub access

## Repository structure

- `managed_agents.ipynb` — basic setup and first agent session
- `multi_agent.ipynb` — orchestrated collaboration between multiple agents
- `agent_skills.ipynb` — custom skill creation and attachment to an agent
- `mcp_connector.ipynb` — connecting an agent to an external MCP server
- `pdf_analysis.ipynb` — uploading and analyzing a PDF file
- `persistent_memory.ipynb` — creating and using memory stores
- `vaults.ipynb` — creating vaults and registering credentials
- `skills/marketing-review/` — reusable marketing-review skill assets
- `Docs/Travel_guide_for_India.pdf` — sample PDF used for document-analysis demos

## Skill example

The repository includes a custom marketing-review skill in `skills/marketing-review/`:

- `SKILL.md` — skill instructions
- `brand-guidelines.md` — brand rules to apply
- `marketing-checklist.md` — review checklist
- `linkedin-template.md` — LinkedIn post structure

This is used in the notebook workflow to review and improve marketing copy using a consistent brand and checklist.

## Setup

1. Create a Python environment and install the required libraries:

```bash
pip install anthropic python-dotenv
```

2. Configure your environment variables in a `.env` file at the project root:

```env
ANTHROPIC_API_KEY=your_anthropic_api_key
CLAUDE_MODEL=claude-sonnet-5-5
GITHUB_ACCESS_TOKEN=your_github_token_if_needed
```

3. Open the notebooks in VS Code or Jupyter and run the cells in order.

## Notes

- The notebooks are designed as practical examples and references for Claude Managed Agents features.
- Several examples rely on Anthropic beta APIs and therefore may require access to the appropriate API version or model availability.
- The `vaults` example uses a GitHub credential and is intended for secure integration scenarios.

## Typical workflow

The repo demonstrates a pattern like this:

1. Create an Anthropic client
2. Set up environment and model configuration
3. Create an agent or multiple agents
4. Attach tools, skills, memory, or MCP servers
5. Start a session and interact with the agent(s)
6. Persist context or credentials via memory stores and vaults

This project is best used as a learning and prototyping sandbox for Claude-managed agent architectures.
