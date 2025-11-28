# Agent Setup Guide - Step-by-Step Instructions

This guide provides **accurate, tested instructions** for creating and configuring the 4 specialized agents in Cursor.

## Important Notes

- Clicking "New Agent" creates a new chat window - this is correct behavior
- The agent's identity is established by the initial prompt you give it
- You can rename agents after creation using the three dots menu
- To see multiple agents at once, use "Open as Editor" to create tabs

## Step-by-Step: Creating Your First Agent (Backend Developer)

### Step 1: Create the Agent Chat

1. **Open the Agents Sidebar**
   - Look for the "Agents" button in the left sidebar
   - If you don't see it, click the sidebar icon to expand it
   
2. **Click "New Agent"**
   - This will create a new chat window (this is correct - the agent IS the chat)
   - You should see a new entry in the Agents sidebar

#### Step 2: Configure the Agent's Identity

**Recommended Method (Using Prompt Shortcut):**

In the new chat, send:
```
@.cursor/prompts/backend-agent-prompt.md

Please assume the role described in this prompt file. For the initial setup, confirm you understand your responsibilities as the Backend Developer Agent.
```

**Alternative Method (Manual Configuration):**

If you prefer to type the configuration manually, send:
```
You are the Backend Developer Agent. Your role is to handle all backend-related tasks including API development, database service layer development, and server-side logic.

Please refer to @rules/backend.mdc for backend development standards and conventions.

Your responsibilities include:
- Use Node.js with TypeScript
- Follow RESTful API conventions  
- Validate inputs using Zod
- Implement error handling middleware
- Create unit tests using Mocha and Chai

When working, automatically attach context from /backend/** directories.
```

### Step 3: Rename the Agent

1. **Find the agent in the Agents Sidebar**
   - Look for your newly created agent in the sidebar list
   
2. **Click the three dots (⋯)** next to the agent's name or icon
   
3. **Select "Rename"** from the dropdown menu
   
4. **Enter the name**: `Backend Developer` or `Backend API Agent`
   
5. **Press Enter** to save

### Step 4: (Optional) Open Agent as Editor Tab

To see this agent alongside other agents in tabs:

1. **Click the three dots (⋯)** next to the agent's name again
   
2. **Select "Open as Editor"** or "Open in Tab"
   
3. The agent's chat will now appear as a tab in the editor
   
4. You can switch between agents using these tabs

## Creating the Remaining 3 Agents

Repeat the process above for each agent, using the configurations below:

---

## Frontend Developer Agent

### Step 1: Click "New Agent" in the sidebar

### Step 2: Send this initial message (using prompt shortcut):

```
@.cursor/prompts/frontend-agent-prompt.md

Please assume the role described in this prompt file. For the initial setup, confirm you understand your responsibilities as the Frontend Developer Agent.
```

### Step 3: Rename to: `Frontend Developer` or `React UI Agent`

### Step 4: (Optional) Open as Editor tab

---

## DevOps Engineer Agent

### Step 1: Click "New Agent" in the sidebar

### Step 2: Send this initial message (using prompt shortcut):

```
@.cursor/prompts/infrastructure-agent-prompt.md

Please assume the role described in this prompt file. For the initial setup, confirm you understand your responsibilities as the DevOps Engineer Agent.
```

### Step 3: Rename to: `DevOps Engineer` or `Infrastructure & Docker Agent`

### Step 4: (Optional) Open as Editor tab

---

## Database Architect Agent

### Step 1: Click "New Agent" in the sidebar

### Step 2: Send this initial message (using prompt shortcut):

```
@.cursor/prompts/database-agent-prompt.md

Please assume the role described in this prompt file. For the initial setup, confirm you understand your responsibilities as the Database Architect Agent.
```

### Step 3: Rename to: `Database Architect` or `Database & Migrations Agent`

### Step 4: (Optional) Open as Editor tab

---

## Quick Reference: Agent Names

When you've created all 4 agents, your Agents sidebar should show:

1. **Backend Developer** (or Backend API Agent)
2. **Frontend Developer** (or React UI Agent)
3. **DevOps Engineer** (or Infrastructure & Docker Agent)
4. **Database Architect** (or Database & Migrations Agent)

## Managing Multiple Agents

### View All Agents at Once

1. **Open each agent as an editor tab**:
   - Click three dots (⋯) → "Open as Editor" for each agent
   
2. **Switch between agents**:
   - Click the tabs at the top of the editor
   - Each tab maintains its own conversation history

### Working with Agents in the Sidebar

- **Click an agent name** in the sidebar to open/switch to its chat
- **View agent status** in the sidebar
- **Manage agents** using the three dots menu:
  - Rename
  - Open as Editor
  - Delete (if needed)

## Using Your Agents

### When Working with a Specific Agent:

1. **Click on the agent** in the sidebar (or switch to its tab)
   
2. **Reference relevant files** when asking questions:
   - Example: "Using @rules/backend.mdc, help me create a new API endpoint"
   
3. **The agent will remember its role** from the initial configuration message

### Example Workflow:

**Backend Agent:**
```
Using @rules/backend.mdc, create a new REST endpoint for user profiles.
Validate the input with Zod and include error handling.
```

**Frontend Agent:**
```
Using @rules/frontend.mdc, create a React component for displaying user profiles.
Make it accessible and use TypeScript.
```

**DevOps Agent:**
```
Using @rules/infra.mdc, update the docker-compose.yml to add a new service.
```

**Database Agent:**
```
Using @rules/database.mdc, create a migration to add a profiles table.
```

## Troubleshooting

### "New Agent" just creates a new chat
- ✅ This is correct! The agent IS the chat. Configure it with the initial prompt.

### Can't find the rename option
- Look for three dots (⋯) next to the agent name in the sidebar
- If you don't see it, try right-clicking on the agent name
- The rename option might be under "More" or "Settings"

### Want to see multiple agents at once
- Use "Open as Editor" option from the three dots menu
- This creates tabs you can switch between
- CMD+T/Ctrl+T won't create agent tabs - that's for file tabs

### Agent not remembering its role
- Re-send the initial configuration message
- Or reference the rule file: `@rules/backend.mdc` (or appropriate file)
- Agents maintain context through the conversation

## Using Prompts as Shortcuts (Recommended Method)

The prompt files in `.cursor/prompts/` can be used as **shortcuts** to quickly configure agents and set up your monorepo. This is faster and more reliable than copying/pasting content.

### How Prompt Shortcuts Work

In Cursor, you can reference files directly using the `@` symbol:

1. **Type `@`** in the chat input
2. **Start typing the file path** - Cursor will autocomplete
3. **Select the prompt file** from the dropdown
4. **Cursor automatically loads the file content** into the conversation context

### Agent Setup Using Prompt Shortcuts

Instead of copying prompt content, simply reference the prompt file:

**For Backend Agent:**
```
@.cursor/prompts/backend-agent-prompt.md

Please assume the role described in this prompt file. For the initial setup, confirm you understand your responsibilities as the Backend Developer Agent.
```

**For Frontend Agent:**
```
@.cursor/prompts/frontend-agent-prompt.md

Please assume the role described in this prompt file. For the initial setup, confirm you understand your responsibilities as the Frontend Developer Agent.
```

**For DevOps Engineer Agent:**
```
@.cursor/prompts/infrastructure-agent-prompt.md

Please assume the role described in this prompt file. For the initial setup, confirm you understand your responsibilities as the DevOps Engineer Agent.
```

**For Database Architect Agent:**
```
@.cursor/prompts/database-agent-prompt.md

Please assume the role described in this prompt file. For the initial setup, confirm you understand your responsibilities as the Database Architect Agent.
```

### Monorepo Setup Using Prompt Shortcuts

To set up your monorepo structure, use the monorepo setup prompt:

**In any agent or Cursor chat, send:**
```
@.cursor/prompts/setup-momo-repo.md

Please follow the instructions in this prompt to set up the monorepo structure.
```

This will guide the agent to:
- ✅ Initialize NPM and Git in the root
- ✅ Create frontend, backend, and database directories
- ✅ Set up Docker Compose configuration at root level
- ✅ Configure Yarn workspaces for package management
- ✅ Set up shared ESLint + Prettier configs
- ✅ Create test folders with Jest placeholders
- ✅ Add Docker Compose NPM scripts
- ✅ Create README files for root and each workspace

### Benefits of Using Prompt Shortcuts

1. **No Copy-Pasting**: Direct file references are cleaner
2. **Always Current**: Changes to prompt files are automatically used
3. **Autocomplete**: Cursor's `@` autocomplete makes it fast
4. **Centralized**: All configuration lives in prompt files
5. **Reusable**: Same prompts can be used across conversations
6. **Maintainable**: Update once, use everywhere

### Alternative: Copy-Paste Method

If you prefer to copy the prompt content directly:

1. Open the prompt file: `.cursor/prompts/backend-agent-prompt.md` (or appropriate file)
2. Copy the contents
3. For setup: Replace `${user_input}` with a confirmation message
4. For tasks: Replace `${user_input}` with your actual task
5. Send it to the agent

## File Structure Reference

```
.cursor/
├── agents/
│   ├── backend-agent.md          # Agent definition & details
│   ├── frontend-agent.md         # Agent definition & details
│   ├── infrastructure-agent.md   # Agent definition & details
│   ├── database-agent.md         # Agent definition & details
│   ├── SETUP.md                  # This file
│   └── README.md                 # Quick reference
├── prompts/
│   ├── backend-agent-prompt.md   # Prompt template
│   ├── frontend-agent-prompt.md  # Prompt template
│   ├── infrastructure-agent-prompt.md  # Prompt template
│   └── database-agent-prompt.md  # Prompt template
└── rules/
    ├── backend.mdc               # Backend development rules
    ├── frontend.mdc              # Frontend development rules
    ├── infra.mdc                 # Infrastructure rules
    └── database.mdc              # Database rules
```

## Setting Up Your Monorepo

Once your agents are configured, you can use the monorepo setup prompt to initialize your project structure:

**In any agent (or main Cursor chat), send:**
```
@.cursor/prompts/setup-momo-repo.md

Please follow the instructions in this prompt to set up the monorepo structure.
```

The agent will:
- Initialize NPM and Git in the root
- Create frontend, backend, and database workspaces
- Set up Docker Compose configuration
- Configure Yarn workspaces
- Add shared ESLint/Prettier configs
- Create README files
- Add NPM scripts for project management

**Tip:** Use the **DevOps Engineer Agent** for monorepo setup, as it's most suited for infrastructure tasks.

## Summary

### Creating Agents
1. **Click "New Agent"** → Creates a new chat (this IS the agent)
2. **Use prompt shortcut** → `@.cursor/prompts/{agent-name}-agent-prompt.md` + setup instruction
3. **Rename the agent** → Click three dots (⋯) → Rename → Enter name
4. **(Optional) Open as Editor** → Creates a tab for easy switching

### Setting Up Monorepo
1. **Use prompt shortcut** → `@.cursor/prompts/setup-momo-repo.md` + setup instruction
2. **Let the agent execute** → It will create the full monorepo structure
3. **Review and customize** → Adjust configurations as needed

Repeat for all 4 agents, set up your monorepo, and you're ready to go!