# Claude Code Skills

A collection of custom skills for [Claude Code](https://claude.ai/code) — focused on writing,
career content, and professional communication for tech professionals.

## Skills

| Skill | Invoke with | Description |
|-------|-------------|-------------|
| [humanizer](humanizer/SKILL.md) | `/humanizer` | Remove AI writing patterns to make text sound natural and human |
| [linkedin](linkedin/SKILL.md) | `/linkedin` | Write LinkedIn posts, about sections, headlines, and connection messages |
| [linkedin-expert](linkedin-expert/SKILL.md) | `/linkedin-expert` | Full LinkedIn strategy for tech professionals — profile optimization, job search, recruiter outreach, and ATS tailoring |
| [resume](resume/SKILL.md) | `/resume` | Write and polish resumes for tech roles — ATS optimization, CAR-format bullets, tailoring to job descriptions, and section-by-section rewrites |


## Installation

Skills live in your Claude Code skills directory. Pick one of the methods below.

### Option 1 — Clone the whole repo (recommended)

Clone directly into your Claude Code skills folder:

```bash
# macOS / Linux
git clone https://github.com/your-username/skills ~/.claude/skills

# Windows (PowerShell)
git clone https://github.com/your-username/skills "$env:USERPROFILE\.claude\skills"
```

All skills are immediately available. Pull to get updates:

```bash
git -C ~/.claude/skills pull          # macOS / Linux
git -C "$env:USERPROFILE\.claude\skills" pull   # Windows
```

### Option 2 — Copy a single skill

If you only want one skill, copy its folder into your Claude Code skills directory:

```bash
# macOS / Linux — example: adding the resume skill
cp -r resume ~/.claude/skills/resume

# Windows (PowerShell)
Copy-Item -Recurse resume "$env:USERPROFILE\.claude\skills\resume"
```

### Where is the skills directory?

| Platform | Path |
|----------|------|
| macOS / Linux | `~/.claude/skills/` |
| Windows | `%USERPROFILE%\.claude\skills\` |

Each skill is a subfolder containing a `SKILL.md` file. The folder name is the invoke name.

```
~/.claude/skills/
  humanizer/
    SKILL.md
  linkedin/
    SKILL.md
  linkedin-expert/
    SKILL.md
  resume/
    SKILL.md
```


## Usage

Once installed, invoke any skill from the Claude Code chat by typing its slash command:

```
/humanizer
/linkedin
/linkedin-expert
/resume
```

You can pass context inline:

```
/resume rewrite my experience section — here's my current version: [paste]

/humanizer here's a blog post draft I need cleaned up: [paste]

/linkedin-expert write me 3 headline options, I'm a senior .NET engineer targeting architect roles

/resume tailor this resume to the following job description: [paste JD]
```

Claude will read the skill file and apply its instructions to your request.


## Keeping skills up to date

If you cloned the repo, just pull:

```bash
git -C ~/.claude/skills pull
```

If you copied individual folders, re-copy them after pulling the source.


## License

MIT
