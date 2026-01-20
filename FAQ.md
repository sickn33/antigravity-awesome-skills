# ❓ Frequently Asked Questions (FAQ)

**Got questions?** You're not alone! Here are answers to the most common questions about Antigravity Awesome Skills.

---

## 🎯 General Questions

### What are "skills" exactly?

Skills are specialized instruction files that teach AI assistants how to handle specific tasks. Think of them as expert knowledge modules that your AI can load on-demand.

**Simple analogy:** Just like you might consult different experts (a lawyer, a doctor, a mechanic), skills let your AI become an expert in different areas when you need them.

---

### Do I need to install all 179 skills?

**No!** When you clone the repository, all skills are available, but your AI only loads them when you explicitly invoke them with `@skill-name` or `/skill-name`.

It's like having a library - all the books are there, but you only read the ones you need.

---

### Which AI tools work with these skills?

These skills work with any AI coding assistant that supports the `SKILL.md` format:

- ✅ **Claude Code** (Anthropic CLI)
- ✅ **Gemini CLI** (Google)
- ✅ **Codex CLI** (OpenAI)
- ✅ **Cursor** (AI IDE)
- ✅ **Antigravity IDE**
- ✅ **OpenCode**
- ⚠️ **GitHub Copilot** (partial support)

---

### Are these skills free to use?

**Yes!** This repository is licensed under MIT License, which means:
- ✅ Free for personal use
- ✅ Free for commercial use
- ✅ You can modify them
- ✅ You can redistribute them

---

### Do skills work offline?

The skill files themselves are stored locally on your computer, but your AI assistant needs an internet connection to function. So:
- ✅ Skills are local files
- ❌ AI assistant needs internet

---

## Installation & Setup

### Where should I install the skills?

The universal path that works with most tools is `.agent/skills/`:

```bash
git clone https://github.com/sickn33/antigravity-awesome-skills.git .agent/skills
```

**Tool-specific paths:**
- Claude Code: `.claude/skills/` or `.agent/skills/`
- Gemini CLI: `.gemini/skills/` or `.agent/skills/`
- Cursor: `.cursor/skills/` or project root
- Antigravity: `.agent/skills/`

---

### Can I install skills in multiple projects?

**Yes!** You have two options:

**Option 1: Global Installation** (recommended)
Install once in your home directory, works for all projects:
```bash
cd ~
git clone https://github.com/sickn33/antigravity-awesome-skills.git .agent/skills
```

**Option 2: Per-Project Installation**
Install in each project directory:
```bash
cd /path/to/your/project
git clone https://github.com/sickn33/antigravity-awesome-skills.git .agent/skills
```

---

### How do I update skills to the latest version?

Navigate to your skills directory and pull the latest changes:

```bash
cd .agent/skills
git pull origin main
```

---

### Can I install only specific skills?

**Yes!** You can manually copy individual skill folders:

```bash
# Clone the full repo first
git clone https://github.com/sickn33/antigravity-awesome-skills.git temp-skills

# Copy only the skills you want
mkdir -p .agent/skills
cp -r temp-skills/skills/brainstorming .agent/skills/
cp -r temp-skills/skills/stripe-integration .agent/skills/

# Clean up
rm -rf temp-skills
```

---

## Using Skills

### How do I invoke a skill?

Use the `@` symbol followed by the skill name:

```
@skill-name your request here
```

**Examples:**
```
@brainstorming help me design a todo app
@stripe-integration add subscription billing
@systematic-debugging fix this test failure
```

Some tools also support `/skill-name` syntax.

---

### How do I know which skill to use?

**Method 1: Browse the README**
Check the [Full Skill Registry](README.md#full-skill-registry-179179) organized by category

**Method 2: Search by keyword**
```bash
ls skills/ | grep "keyword"
```

**Method 3: Ask your AI**
```
What skills are available for [topic]?
```

---

### Can I use multiple skills at once?

**Yes!** You can invoke multiple skills in the same conversation:

```
@brainstorming help me design this feature

[After brainstorming...]

@test-driven-development now let's implement it with tests
```

---

### What if a skill doesn't work?

**Troubleshooting steps:**

1. **Check installation path**
   ```bash
   ls .agent/skills/
   ```

2. **Verify skill exists**
   ```bash
   ls .agent/skills/skill-name/
   ```

3. **Check SKILL.md exists**
   ```bash
   cat .agent/skills/skill-name/SKILL.md
   ```

4. **Try restarting your AI assistant**

5. **Check for typos in skill name**
   - Use `@brainstorming` not `@brain-storming`
   - Names are case-sensitive in some tools

6. **Report the issue**
   [Open an issue](https://github.com/sickn33/antigravity-awesome-skills/issues) with details

---

## 🤝 Contributing

### I'm new to open source. Can I still contribute?

**Absolutely!** Everyone starts somewhere. We welcome contributions from beginners:

- Fix typos or grammar
- Improve documentation clarity
- Add examples to existing skills
- Report issues or confusing parts

Check out [CONTRIBUTING_GUIDE.md](CONTRIBUTING_GUIDE.md) for step-by-step instructions.

---

### Do I need to know how to code to contribute?

**No!** Many valuable contributions don't require coding:

- **Documentation improvements** - Make things clearer
- **Examples** - Add real-world usage examples
- **Issue reporting** - Tell us what's confusing
- **Testing** - Try skills and report what works

---

### How do I create a new skill?

**Quick version:**

1. Create a folder: `skills/my-skill-name/`
2. Create `SKILL.md` with frontmatter and content
3. Test it with your AI assistant
4. Run validation: `python3 scripts/validate_skills.py`
5. Submit a Pull Request

**Detailed version:** See [CONTRIBUTING_GUIDE.md](CONTRIBUTING_GUIDE.md)

---

### What makes a good skill?

A good skill:
- ✅ Solves a specific problem
- ✅ Has clear, actionable instructions
- ✅ Includes examples
- ✅ Is reusable across projects
- ✅ Follows the standard structure

See [SKILL_ANATOMY.md](docs/SKILL_ANATOMY.md) for details.

---

### How long does it take for my contribution to be reviewed?

Review times vary, but typically:
- **Simple fixes** (typos, docs): 1-3 days
- **New skills**: 3-7 days
- **Major changes**: 1-2 weeks

You can speed this up by:
- Following the contribution guidelines
- Writing clear commit messages
- Testing your changes
- Responding to feedback quickly

---

## Technical Questions

### What's the difference between SKILL.md and README.md?

- **SKILL.md** (required): The actual skill definition that the AI reads
- **README.md** (optional): Human-readable documentation about the skill

The AI primarily uses `SKILL.md`, while developers read `README.md`.

---

### Can I use scripts or code in my skill?

**Yes!** Skills can include:
- `scripts/` - Helper scripts
- `examples/` - Example code
- `templates/` - Code templates
- `references/` - Documentation

Reference them in your `SKILL.md`:
```markdown
Run the setup script:
\`\`\`bash
bash scripts/setup.sh
\`\`\`
```

---

### What programming languages can skills cover?

**Any language!** Current skills cover:
- JavaScript/TypeScript
- Python
- Go
- Rust
- Swift
- Kotlin
- Shell scripting
- And many more...

---

### Can skills call other skills?

**Yes!** Skills can reference other skills:

```markdown
## Workflow

1. First, use `@brainstorming` to design
2. Then, use `@writing-plans` to plan
3. Finally, use `@test-driven-development` to implement
```

---

### How do I validate my skill before submitting?

Run the validation script:

```bash
python3 scripts/validate_skills.py
```

This checks:
- ✅ SKILL.md exists
- ✅ Frontmatter is valid
- ✅ Name matches folder name
- ✅ Description exists

---

## Learning & Best Practices

### Which skills should I try first?

**For beginners:**
- `@brainstorming` - Design before coding
- `@systematic-debugging` - Fix bugs methodically
- `@git-pushing` - Commit with good messages

**For developers:**
- `@test-driven-development` - Write tests first
- `@react-best-practices` - Modern React patterns
- `@senior-fullstack` - Full-stack development

**For security:**
- `@ethical-hacking-methodology` - Security basics
- `@burp-suite-testing` - Web app testing

---

### How do I learn to write good skills?

**Learning path:**

1. **Read existing skills** - Study 5-10 well-written skills
2. **Use skills** - Try them with your AI assistant
3. **Read guides** - Check [SKILL_ANATOMY.md](docs/SKILL_ANATOMY.md)
4. **Start simple** - Create a basic skill first
5. **Get feedback** - Submit and learn from reviews
6. **Iterate** - Improve based on feedback

**Recommended skills to study:**
- `skills/brainstorming/SKILL.md` - Clear structure
- `skills/systematic-debugging/SKILL.md` - Comprehensive
- `skills/git-pushing/SKILL.md` - Simple and focused

---

### Are there any skills for learning AI/ML?

**Yes!** Check out:
- `@rag-engineer` - RAG systems
- `@prompt-engineering` - Prompt design
- `@langgraph` - Multi-agent systems
- `@ai-agents-architect` - Agent architecture
- `@llm-app-patterns` - LLM application patterns

---

## Troubleshooting

### My AI assistant doesn't recognize skills

**Possible causes:**

1. **Wrong installation path**
   - Check your tool's documentation for the correct path
   - Try `.agent/skills/` as the universal path

2. **Skill name typo**
   - Verify the exact skill name: `ls .agent/skills/`
   - Use the exact name from the folder

3. **Tool doesn't support skills**
   - Verify your tool supports the SKILL.md format
   - Check the [Compatibility](#-compatibility) section

4. **Need to restart**
   - Restart your AI assistant after installing skills

---

### A skill gives incorrect or outdated advice

**Please report it!**

1. [Open an issue](https://github.com/sickn33/antigravity-awesome-skills/issues)
2. Include:
   - Which skill
   - What's incorrect
   - What should it say instead
   - Links to correct documentation

We'll update it quickly!

---

### Can I modify skills for my own use?

**Yes!** The MIT License allows you to:
- ✅ Modify skills for your needs
- ✅ Create private versions
- ✅ Customize for your team

**To modify:**
1. Copy the skill to a new location
2. Edit the SKILL.md file
3. Use your modified version

**Consider contributing improvements back!**

---

## Statistics & Info

### How many skills are there?

**179 skills** across 10+ categories as of the latest update.

---

### How often are skills updated?

- **Bug fixes**: As soon as reported
- **New skills**: Added regularly by contributors
- **Updates**: When best practices change

**Stay updated:**
```bash
cd .agent/skills
git pull origin main
```

---

### Who maintains this repository?

This is a community-driven project with contributions from:
- Original creators
- Open source contributors
- AI coding assistant users worldwide

See [Credits & Sources](README.md#credits--sources) for attribution.

---

## Still Have Questions?

### Where can I get help?

- **[GitHub Discussions](https://github.com/sickn33/antigravity-awesome-skills/discussions)** - Ask questions
- **[GitHub Issues](https://github.com/sickn33/antigravity-awesome-skills/issues)** - Report bugs
- **Documentation** - Read the guides in this repo
- **Community** - Connect with other users

---

### How can I stay updated?

- **Star the repository** on GitHub
- **Watch the repository** for updates
- **Subscribe to releases** for notifications
- **Follow contributors** on social media

---

### Can I use these skills commercially?

**Yes!** The MIT License permits commercial use. You can:
- ✅ Use in commercial projects
- ✅ Use in client work
- ✅ Include in paid products
- ✅ Modify for commercial purposes

**Only requirement:** Keep the license notice.

---

## 💡 Pro Tips

- Start with `@brainstorming` before building anything new
- Use `@systematic-debugging` when stuck on bugs
- Try `@test-driven-development` for better code quality
- Explore `@skill-creator` to make your own skills
- Read skill descriptions to understand when to use them

---

**Question not answered?** 

[Open a discussion](https://github.com/sickn33/antigravity-awesome-skills/discussions) and we'll help you out! 🙌
