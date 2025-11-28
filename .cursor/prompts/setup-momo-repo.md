Create a monorepo structure with the root of the project:
- Initialize NPM and Git in the root folder / this repo is used to manage the project workspace
- Create the nested repositories:
    - Frontend: React + TypeScript + Webpack in /frontend
    - Backend: Node.js + Koa + TypeScript + Mocha + Chai in /backend
    - Database: MongoDB migrations in /database
- Create the docker-compose configuration for the services at root level (docker-compose.yml)

Include:
- NPM and Git
- NPM scripts for project management (dev, build, test, lint, format)
- Yarn workspaces for package management
- ESLint + Prettier configs shared across packages
- Test folders with placeholder tests for each workspace (using Jest)
- Docker Compose NPM scripts (docker:up, docker:down, docker:build, docker:rebuild, docker:logs, docker:ps, docker:stop, docker:start, docker:restart, docker:clean)
- Root-level README.md with setup instructions
- Individual README.md files for each workspace (frontend, backend, database) describing the project and NPM scripts at that level
