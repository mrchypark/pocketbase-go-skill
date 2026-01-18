# PocketBase Go Skill

This skill provides a robust, atomic, and type-safe workflow for managing PocketBase backends in Go projects. It automates schema migration, code generation, and environment setup.

## Installation

### Option 1: Manual Installation (Git Submodule)
The recommended way to install this skill is as a git submodule in your project's `skills/` directory.

```bash
mkdir -p skills
git submodule add https://github.com/your-username/pocketbase-go-skill.git skills/pocketbase-go
```

### Option 2: Clone Directly
If you are not using git submodules, you can simply clone the repository:

```bash
git clone https://github.com/your-username/pocketbase-go-skill.git skills/pocketbase-go
```

## Usage

1.  **Load the Skill**: Tell your AI agent "Use the PocketBase Go skill".
2.  **Initialize**: The agent will run `make init` to setup the environment.
3.  **Manage Schema**: Ask the agent to "Create a posts collection" or "Add a title field to posts".
4.  **Sync**: The agent will run `make sync` to update `pb_schema.json` and generate Go code.

## Requirements

*   **Go 1.21+**: Required for `pbc-gen`.
*   **Python 3**: Required for the migration script.
*   **Make**: Required for the build system.
*   **Docker**: (Optional) For containerized deployment.

## Repository Structure

```text
pocketbase-go/
├── SKILL.md            # Entry point for the AI agent
├── README.md           # This file
└── resources/          # Helper scripts and configuration
    ├── Makefile
    ├── pb_migrate_ops.py
    └── Dockerfile
```
