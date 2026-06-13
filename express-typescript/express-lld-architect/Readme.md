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
cp -R claude-skills/express-typescript/express-lld-architect/* \
.claude/skills/express-lld-architect/
```

Project structure:

```text
my-project/
├── .claude/
│   └── skills/
│       └── express-lld-architect/
│           ├── SKILL.md
│           ├── README.md
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
cp -R \
claude-skills/express-typescript/express-lld-architect \
~/.claude/skills/
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

Clone the repository:

```bash
git clone https://github.com/Bishwash-007/Claude-System-Architect.git
```

Install globally:

```bash
cp -R \
claude-skills/express-typescript/express-lld-architect \
~/.claude/skills/
```

Or install into a specific project:

```bash
mkdir -p .claude/skills/express-lld-architect

cp -R \
claude-skills/express-typescript/express-lld-architect/* \
.claude/skills/express-lld-architect/
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

If installed from the repository:

```bash
cd claude-skills
git pull
```

Reinstall the latest version:

```bash
cp -R \
express-typescript/express-lld-architect \
~/.claude/skills/
```

For project-local installations:

```bash
cp -R \
express-typescript/express-lld-architect/* \
your-project/.claude/skills/express-lld-architect/
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

Repository structure:

```text
claude-skills/
└── express-typescript/
    └── express-lld-architect/
        ├── SKILL.md
        ├── README.md
        ├── docs/
        ├── templates/
        └── examples/
```

Make changes to the skill files and reinstall if necessary.

Restart Claude Code after modifying the skill:

```bash
claude
```

or start a new session.

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

---

# Packaging for Distribution

Create a release archive:

```bash
cd express-typescript

zip -r \
express-lld-architect.zip \
express-lld-architect
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

exists at the root of the installed skill directory.

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
~/.claude/skills/
└── express-lld-architect/
    ├── SKILL.md
    └── README.md
```

Incorrect:

```text
~/.claude/skills/
└── express-lld-architect/
    └── nested/
        └── SKILL.md
```

The `SKILL.md` file must be located at the root of the installed skill directory.

---

# License

MIT
