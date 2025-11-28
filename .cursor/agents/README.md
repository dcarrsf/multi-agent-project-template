# Cursor Agents Configuration

This directory contains configuration and documentation for the 4 specialized agents in this project.

## 🚀 Quick Start

**New to creating agents? Start here:**

👉 **[QUICKSTART.md](./QUICKSTART.md)** - Create all 4 agents in 5 minutes

For detailed step-by-step instructions with troubleshooting, see [SETUP.md](./SETUP.md).

## Agent List

1. **[Backend Developer Agent](./backend-agent.md)** - Node.js/TypeScript API development
2. **[Frontend Developer Agent](./frontend-agent.md)** - React/TypeScript UI development
3. **[DevOps Engineer Agent](./infrastructure-agent.md)** - Infrastructure & Docker management
4. **[Database Architect Agent](./database-agent.md)** - MongoDB schema & migrations

## Quick Reference

**Important:** In Cursor, "New Agent" creates a new chat - that IS your agent. Configure it with an initial message that defines its role, then rename it using the three dots (⋯) menu.

## Using Prompts as Shortcuts

The prompt files in `.cursor/prompts/` serve as **shortcuts** for quick setup:

### 🚀 Agent Setup Shortcuts

Instead of manually typing configuration, reference the prompt files directly:

```
@.cursor/prompts/backend-agent-prompt.md
```

Type `@` in Cursor's chat, then the file path. Cursor will automatically load the prompt content into context.

### 📦 Monorepo Setup Shortcut

To set up your monorepo structure, use:

```
@.cursor/prompts/setup-momo-repo.md
```

This prompt guides setup of the entire monorepo with frontend, backend, database, Docker Compose, and shared configurations.

**Benefits of Prompt Shortcuts:**
- ✅ Centralized configuration in files
- ✅ Easy updates and maintenance
- ✅ Consistent agent setup
- ✅ Quick reuse across conversations

## Agent Files

Each agent has:
- **Definition file** (`.md`) - Contains agent role, responsibilities, and configuration
- **Prompt file** (`.cursor/prompts/{agent-name}-agent-prompt.md`) - Template prompts for the agent (use as shortcuts!)
- **Rule file** (`.cursor/rules/{agent-name}.mdc`) - Development rules and conventions

## Usage

When working with an agent:

1. **Setup**: Use prompt shortcuts - `@.cursor/prompts/{agent-name}-agent-prompt.md`
2. **Reference rules**: `@rules/{agent-name}.mdc` when giving tasks
3. **Assign tasks**: Copy prompt file, replace `${user_input}` with your task
4. The agent will automatically attach relevant files based on its Auto-Attach configuration

## Agent Names for Cursor

When creating agents in Cursor's UI, use these names:

- `Backend Developer` or `Backend API Agent`
- `Frontend Developer` or `React UI Agent`
- `DevOps Engineer` or `Infrastructure & Docker Agent`
- `Database Architect` or `Database & Migrations Agent`

## Available Prompt Shortcuts

### Agent Setup Prompts
- `.cursor/prompts/backend-agent-prompt.md` - Backend Developer Agent
- `.cursor/prompts/frontend-agent-prompt.md` - Frontend Developer Agent
- `.cursor/prompts/infrastructure-agent-prompt.md` - DevOps Engineer Agent
- `.cursor/prompts/database-agent-prompt.md` - Database Architect Agent

### Monorepo Setup Prompt
- `.cursor/prompts/setup-momo-repo.md` - Complete monorepo structure setup

### Other Project Prompts
- `.cursor/prompts/feature-implementation.md` - Feature development
- `.cursor/prompts/review-code.md` - Code review
- `.cursor/prompts/api-change-handoff.md` - API change documentation
- `.cursor/prompts/update-readme.md` - README updates
