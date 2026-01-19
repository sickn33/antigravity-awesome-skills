# 🚀 Getting Started with Antigravity Awesome Skills

**New here? This guide will help you understand and use this repository in 5 minutes!**

---

## 🤔 What Are "Skills"?

Think of skills as **specialized instruction manuals** for AI coding assistants. 

**Simple analogy:** Just like you might hire different experts (a designer, a security expert, a marketer), these skills let your AI assistant become an expert in specific areas when you need them.

---

## 📦 What's Inside This Repository?

This repo contains **179 ready-to-use skills** organized in the `skills/` folder. Each skill is a folder with at least one file: `SKILL.md`

```
skills/
├── brainstorming/
│   └── SKILL.md          ← The skill definition
├── stripe-integration/
│   └── SKILL.md
├── react-best-practices/
│   └── SKILL.md
└── ... (176 more skills)
```

---

## 🎯 How Do Skills Work?

### Step 1: Install Skills
Copy the skills to your AI tool's directory:

```bash
# For most AI tools (Claude Code, Gemini CLI, etc.)
git clone https://github.com/sickn33/antigravity-awesome-skills.git .agent/skills
```

### Step 2: Use a Skill
In your AI chat, mention the skill:

```
@brainstorming help me design a todo app
```

or

```
/stripe-integration add payment processing to my app
```

### Step 3: The AI Becomes an Expert
The AI loads that skill's knowledge and helps you with specialized expertise!

---

## 🛠️ Which AI Tools Work With This?

| Tool | Works? | Installation Path |
|------|--------|-------------------|
| **Claude Code** | ✅ Yes | `.claude/skills/` or `.agent/skills/` |
| **Gemini CLI** | ✅ Yes | `.gemini/skills/` or `.agent/skills/` |
| **Cursor** | ✅ Yes | `.cursor/skills/` |
| **GitHub Copilot** | ⚠️ Partial | Copy to `.github/copilot/` |
| **Antigravity IDE** | ✅ Yes | `.agent/skills/` |

---

## 📚 Skill Categories (Simplified)

### 🎨 **Creative & Design** (10 skills)
Make beautiful things: UI design, art, themes, web components
- Try: `@frontend-design`, `@canvas-design`, `@ui-ux-pro-max`

### 🛠️ **Development** (25 skills)
Write better code: testing, debugging, React patterns, architecture
- Try: `@test-driven-development`, `@systematic-debugging`, `@react-best-practices`

### 🛡️ **Security** (50 skills)
Ethical hacking and penetration testing tools
- Try: `@ethical-hacking-methodology`, `@burp-suite-testing`

### 🤖 **AI & Agents** (30 skills)
Build AI apps: RAG, LangGraph, prompt engineering, voice agents
- Try: `@rag-engineer`, `@prompt-engineering`, `@langgraph`

### 📄 **Documents** (4 skills)
Work with Word, Excel, PowerPoint, PDF files
- Try: `@docx-official`, `@xlsx-official`, `@pdf-official`

### 📈 **Marketing** (23 skills)
Grow your product: SEO, copywriting, ads, email campaigns
- Try: `@copywriting`, `@seo-audit`, `@page-cro`

### 🔌 **Integrations** (25 skills)
Connect to services: Stripe, Firebase, Twilio, Discord, Slack
- Try: `@stripe-integration`, `@firebase`, `@clerk-auth`

---

## 🎓 Your First Skill: A Quick Example

Let's try the **brainstorming** skill:

1. **Open your AI assistant** (Claude Code, Cursor, etc.)

2. **Type this:**
   ```
   @brainstorming I want to build a simple weather app
   ```

3. **What happens:**
   - The AI loads the brainstorming skill
   - It asks you questions one at a time
   - It helps you design the app before coding
   - It creates a design document for you

4. **Result:** You get a well-thought-out plan instead of jumping straight to code!

---

## 🔍 How to Find the Right Skill

### Method 1: Browse by Category
Check the [Full Skill Registry](README.md#full-skill-registry-179179) in the main README

### Method 2: Search by Keyword
Use your file explorer or terminal:
```bash
# Find skills related to "testing"
ls skills/ | grep test

# Find skills related to "auth"
ls skills/ | grep auth
```

### Method 3: Look at the Index
Check `skills_index.json` for a machine-readable list

---

## 🤝 Want to Contribute?

Great! Here's how:

### Option 1: Improve Documentation
- Make READMEs clearer
- Add more examples
- Fix typos or confusing parts

### Option 2: Create a New Skill
See our [CONTRIBUTING_GUIDE.md](CONTRIBUTING_GUIDE.md) for step-by-step instructions

### Option 3: Report Issues
Found something confusing? [Open an issue](https://github.com/sickn33/antigravity-awesome-skills/issues)

---

## ❓ Common Questions

### Q: Do I need to install all 179 skills?
**A:** No! Clone the whole repo, and your AI will only load skills when you use them.

### Q: Can I create my own skills?
**A:** Yes! Check out the `@skill-creator` skill or read [CONTRIBUTING_GUIDE.md](CONTRIBUTING_GUIDE.md)

### Q: What if my AI tool isn't listed?
**A:** If it supports the `SKILL.md` format, try `.agent/skills/` - it's the universal path.

### Q: Are these skills free?
**A:** Yes! MIT License. Use them however you want.

### Q: Do skills work offline?
**A:** The skill files are local, but your AI assistant needs internet to function.

---

## 🎉 Next Steps

1. ✅ Install the skills in your AI tool
2. ✅ Try 2-3 skills from different categories
3. ✅ Read [CONTRIBUTING_GUIDE.md](CONTRIBUTING_GUIDE.md) if you want to help
4. ✅ Star the repo if you find it useful! ⭐

---

## 💡 Pro Tips

- **Start with `@brainstorming`** before building anything new
- **Use `@systematic-debugging`** when you're stuck on a bug
- **Try `@test-driven-development`** to write better code
- **Explore `@skill-creator`** to make your own skills

---

**Still confused?** Open an issue and we'll help you out! 🙌

**Ready to dive deeper?** Check out the main [README.md](README.md) for the complete skill list.
