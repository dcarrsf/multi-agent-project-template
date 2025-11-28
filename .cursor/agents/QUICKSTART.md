# Quick Start: Create 4 Agents in 5 Minutes

## The Simple Truth

**Agents in Cursor are chats with a defined role.** Here's how to create them using the prompt files we've set up.

## Step-by-Step Process

For each agent, use the prompt files in `.cursor/prompts/`. You have two options:

**Method 1 (Recommended):** Copy the prompt file content, remove the `${user_input}` placeholder, and send it  
**Method 2:** Reference the prompt file directly using the quick alternatives below

---

## Quick Copy-Paste Setup Messages

### Option A: Using Prompt Files (Easiest)

For each agent, simply send this message (replace `{agent-name}` with the appropriate file):

```
@.cursor/prompts/{agent-name}-agent-prompt.md - Please assume this role. Replace ${user_input} with: "Please confirm your role and that you understand your responsibilities."
```

### Option B: Full Setup from Prompt Files

Open each prompt file, copy the entire content, replace `${user_input}` with "Please confirm your role and that you understand your responsibilities.", then send.

---

### 1. Backend Developer Agent

1. Click **"New Agent"** in the Agents sidebar (this opens a new chat - that's your agent!)
2. **Open**: `.cursor/prompts/backend-agent-prompt.md`
3. **Copy the entire contents** and paste it into the new chat
4. **Remove or replace** the `## Task\n${user_input}` section with: `## Task\nPlease confirm your role and that you understand your responsibilities.`
5. **Send the message**
6. Click **three dots (⋯)** next to the agent in sidebar → **"Rename"** → Type: `Backend Developer`
7. (Optional) Click **three dots (⋯)** → **"Open as Editor"** to create a tab

**Quick Alternative:** Just send:
```
@.cursor/prompts/backend-agent-prompt.md

Please assume the role described in this prompt file. For the initial setup, confirm you understand your responsibilities as the Backend Developer Agent.
```

---

### 2. Frontend Developer Agent

1. Click **"New Agent"** 
2. **Open**: `.cursor/prompts/frontend-agent-prompt.md`
3. **Copy the contents**, remove/replace the `${user_input}` section, and paste into chat
4. **Send the message**
5. **Rename** → `Frontend Developer`
6. (Optional) **"Open as Editor"** for tab

**Quick Alternative:**
```
@.cursor/prompts/frontend-agent-prompt.md

Please assume the role described in this prompt file. For the initial setup, confirm you understand your responsibilities as the Frontend Developer Agent.
```

---

### 3. DevOps Engineer Agent

1. Click **"New Agent"**
2. **Open**: `.cursor/prompts/infrastructure-agent-prompt.md`
3. **Copy the contents**, remove/replace the `${user_input}` section, and paste into chat
4. **Send the message**
5. **Rename** → `DevOps Engineer`
6. (Optional) **"Open as Editor"** for tab

**Quick Alternative:**
```
@.cursor/prompts/infrastructure-agent-prompt.md

Please assume the role described in this prompt file. For the initial setup, confirm you understand your responsibilities as the DevOps Engineer Agent.
```

---

### 4. Database Architect Agent

1. Click **"New Agent"**
2. **Open**: `.cursor/prompts/database-agent-prompt.md`
3. **Copy the contents**, remove/replace the `${user_input}` section, and paste into chat
4. **Send the message**
5. **Rename** → `Database Architect`
6. (Optional) **"Open as Editor"** for tab

**Quick Alternative:**
```
@.cursor/prompts/database-agent-prompt.md

Please assume the role described in this prompt file. For the initial setup, confirm you understand your responsibilities as the Database Architect Agent.
```

---

## Done! ✅

Your Agents sidebar should now show 4 agents:
- Backend Developer
- Frontend Developer  
- DevOps Engineer
- Database Architect

## Using Your Agents

1. **Click an agent name** in the sidebar to switch to it
2. **Ask questions** - the agent remembers its role
3. **Reference rules**: "Using @rules/backend.mdc, help me..."
4. **Use the prompt files** when assigning tasks:
   - Copy content from `.cursor/prompts/{agent-name}-agent-prompt.md`
   - Replace `${user_input}` with your actual task
   - Send it to the agent

## View Multiple Agents at Once

- Click **three dots (⋯)** → **"Open as Editor"** on each agent
- They'll appear as tabs at the top
- Switch between tabs to see different agents

## Common Questions

**Q: Why does "New Agent" just open a chat?**  
A: That's correct! The agent IS the chat with a configured role.

**Q: How do I rename agents?**  
A: Click three dots (⋯) next to agent name → "Rename"

**Q: CMD+T doesn't create agent tabs?**  
A: Correct - use "Open as Editor" from the three dots menu instead.

**Q: How do I see all agents at once?**  
A: Use "Open as Editor" on each agent to create tabs.

---

## Using Prompts as Shortcuts

The prompt files serve as **shortcuts** for quickly configuring agents and setting up your monorepo. Here's how to use them:

### Prompt Shortcuts for Agent Setup

Instead of manually typing configuration messages, you can reference the prompt files directly. Cursor will automatically load and use the prompt content.

**Quick Shortcut Method:**

For each agent, simply type `@` followed by the prompt file path in Cursor's chat:

- Backend: `@.cursor/prompts/backend-agent-prompt.md`
- Frontend: `@.cursor/prompts/frontend-agent-prompt.md`
- Infrastructure: `@.cursor/prompts/infrastructure-agent-prompt.md`
- Database: `@.cursor/prompts/database-agent-prompt.md`

Then add: "Please assume this role and confirm you understand your responsibilities."

**Example for Backend Agent:**
```
@.cursor/prompts/backend-agent-prompt.md

Please assume the role described in this prompt file. For the initial setup, confirm you understand your responsibilities as the Backend Developer Agent.
```

### Prompt Shortcuts for Monorepo Setup

You can use the monorepo setup prompt as a shortcut to initialize your project structure:

**In any agent chat (or Cursor chat), send:**
```
@.cursor/prompts/setup-momo-repo.md

Please follow the instructions in this prompt to set up the monorepo structure.
```

This will guide the agent to:
- Initialize NPM and Git in the root
- Create frontend, backend, and database directories
- Set up Docker Compose configuration
- Configure Yarn workspaces
- Set up shared ESLint/Prettier configs
- Create README files
- Add NPM scripts for project management

### How Prompt Shortcuts Work in Cursor

1. **Type `@`** in the chat to trigger file/context selection
2. **Type the file path** or select from autocomplete
3. **Cursor loads the file content** into the conversation context
4. **Add your instruction** to tell the agent how to use the prompt

This approach:
- ✅ Keeps configuration centralized in prompt files
- ✅ Makes it easy to update agent configurations
- ✅ Allows quick reuse across different conversations
- ✅ Ensures consistency when setting up multiple agents

---

## Prompt Files Reference

Each agent has a corresponding prompt file in `.cursor/prompts/`:

- **Backend**: `.cursor/prompts/backend-agent-prompt.md`
- **Frontend**: `.cursor/prompts/frontend-agent-prompt.md`
- **Infrastructure**: `.cursor/prompts/infrastructure-agent-prompt.md`
- **Database**: `.cursor/prompts/database-agent-prompt.md`
- **Monorepo Setup**: `.cursor/prompts/setup-momo-repo.md`

These prompts include the agent's role, guidelines, and expected deliverables. Use them when:
1. **Setting up the agent** (initial configuration) - use prompt shortcuts
2. **Assigning tasks** (replace `${user_input}` with your task) - copy and customize
3. **Setting up the monorepo** - reference the setup-momo-repo.md prompt

---

For more details, see [SETUP.md](./SETUP.md)
