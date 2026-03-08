# PocketBase Go Skill

This skill provides a robust, atomic, and type-safe workflow for managing PocketBase backends in Go projects. It automates schema migration, code generation, and environment setup.

## Archive Notice

This repository is archived and kept as a read-only reference.

The active copy of this skill lives in the `mrchypark/skills` monorepo at:

- `pocketbase-go/`
- [https://github.com/mrchypark/skills/tree/main/pocketbase-go](https://github.com/mrchypark/skills/tree/main/pocketbase-go)

If you are adopting this skill now, use the monorepo path above.
Do not start new setup from this standalone repository unless you specifically need the archived snapshot.

## Recommended Path

Use the monorepo version if you want:

- the location that will continue to be organized with other personal skills
- a single repository for installing and managing multiple `mrchypark` skills
- the latest documentation layout used in the active skills repository
- the path that will receive future organization and updates

## Migration

If you previously used this standalone repository, move to:

```bash
git clone https://github.com/mrchypark/skills.git mrchypark-skills
cd mrchypark-skills/pocketbase-go
```

Or copy only the skill directory you need:

```bash
mkdir -p ~/.codex/skills
git clone https://github.com/mrchypark/skills.git mrchypark-skills
cp -R mrchypark-skills/pocketbase-go ~/.codex/skills/pocketbase-go
```

## Legacy Standalone Installation

The installation methods below are preserved only for users who need the archived standalone layout.
For new setups, use the monorepo path described above instead.

### Option 1: Manual Installation (Git Submodule)
Legacy standalone installation as a git submodule in your project's `skills/` directory:

```bash
mkdir -p skills
git submodule add https://github.com/mrchypark/pocketbase-go-skill.git skills/pocketbase-go
```

### Option 2: Clone Directly
Legacy standalone installation by cloning this repository directly:

```bash
git clone https://github.com/mrchypark/pocketbase-go-skill.git skills/pocketbase-go
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
