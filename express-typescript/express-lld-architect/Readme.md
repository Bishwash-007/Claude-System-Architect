# Express LLD Architect

A Claude Code skill package.

## Requirements

Before installing, ensure you have:

* Claude Code installed
* Node.js 20+ (recommended)
* Git

Verify your installation:

```bash
claude --version
node --version
git --version
```

---

# Installation

## Option 1: Install for a Single Project

Create the skill directory:

```bash
mkdir -p .claude/skills/express-lld-architect
```

Copy the skill files:

```bash
cp -R express-lld-architect/* .claude/skills/express-lld-architect/
```

Project structure:

```text
my-project/
├── .claude/
│   └── skills/
│       └── express-lld-architect/
│           ├── SKILL.md
│           ├── index.md
│           └── ...
├── src/
└── package.json
```

---

## Option 2: Install Globally

Create the global skills directory:

```bash
mkdir -p ~/.claude/skills
```

Copy the skill:

```bash
cp -R express-lld-architect ~/.claude/skills/
```

Result:

```text
~/.claude/
└── skills/
    └── express-lld-architect/
        ├── SKILL.md
        ├── README.md
        └── ...
```

The skill will now be available across all Claude Code projects.

---

# Installation from GitHub

Clone directly into your Claude skills directory:

```bash
git clone https://github.com/your-org/express-lld-architect.git \
~/.claude/skills/express-lld-architect
```

Or for a single project:

```bash
git clone https://github.com/your-org/express-lld-architect.git \
.claude/skills/express-lld-architect
```

---

# Verifying Installation

Navigate to any Claude Code project:

```bash
cd my-project
claude
```

List available skills:

```text
/help
```

or invoke the skill directly:

```text
/express-lld-architect
```

If installed correctly, Claude Code should recognize and load the skill.

---

# Updating

If installed via Git:

```bash
cd ~/.claude/skills/express-lld-architect
git pull
```

For project-local installations:

```bash
cd .claude/skills/express-lld-architect
git pull
```

---

# Uninstalling

## Global Installation

```bash
rm -rf ~/.claude/skills/express-lld-architect
```

## Project Installation

```bash
rm -rf .claude/skills/express-lld-architect
```

---

# Local Development

Make changes to the skill files:

```text
express-lld-architect/
├── SKILL.md
├── README.md
├── docs/
├── templates/
└── examples/
```

Restart Claude Code after modifying the skill:

```bash
claude
```

or restart the current Claude session.

---

# Development Workflow

Create a feature branch:

```bash
git checkout -b feature/my-change
```

Commit changes:

```bash
git add .
git commit -m "Add improvement"
```

Push:

```bash
git push origin feature/my-change
```

---

# Running Examples

Open Claude Code inside any project:

```bash
cd my-project
claude
```

Run the skill:

```text
/express-lld-architect
```

Example usage:

```text
Design a backend for an e-commerce platform.
```

```text
Create a scalable notification service.
```

```text
Generate a TypeScript Express architecture for a booking system.
```

```text
Design a payment processing backend.
```

```text
Create an API architecture for a chat application.
```

---

# Packaging for Distribution

Create a release archive:

```bash
zip -r express-lld-architect.zip express-lld-architect
```

Verify contents:

```bash
unzip -l express-lld-architect.zip
```

Expected structure:

```text
express-lld-architect/
├── SKILL.md
├── README.md
├── LICENSE
├── docs/
├── examples/
└── templates/
```

---

# Publishing a Release

Tag a version:

```bash
git tag v1.0.0
git push origin v1.0.0
```

Create a GitHub Release and upload:

```text
express-lld-architect.zip
```

as the release artifact.

---

# Troubleshooting

## Skill Not Found

Verify the directory exists:

```bash
ls ~/.claude/skills/
```

or

```bash
ls .claude/skills/
```

Ensure:

```text
SKILL.md
```

exists at the root of the skill directory.

---

## Changes Not Appearing

Restart Claude Code:

```bash
claude
```

or start a new session.

---

## Invalid Skill Structure

Correct:

```text
express-lld-architect/
├── SKILL.md
└── README.md
```

Incorrect:

```text
express-lld-architect/
└── nested/
    └── SKILL.md
```

The `SKILL.md` file must be located at the root of the skill directory.

---

# License

MIT
