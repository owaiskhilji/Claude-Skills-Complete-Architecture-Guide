🛠️ Claude Code Skills: Master Architecture GuideYe guide Claude Code mein Custom Skills banane aur unhein organize karne ka official aur professional tareeqa batati hai.📂 1. Directory StructureClaude Code filesystem-based skills use karta hai. Har skill ko ek makhsoos folder mein hona chahiye.Bash.claude/
└── skills/
    └── [skill-name]/            # Sirf lowercase, numbers, aur hyphens
        ├── SKILL.md             # Main entry point (Required)
        ├── automation-script.py # Optional: Python/Bash scripts
        └── reference-docs.md    # Optional: Level 1 reference files
📝 2. SKILL.md TemplateHar skill file ke shuru mein YAML Frontmatter hona lazmi hai taake Claude use automatically "Discover" kar sake.Markdown---
name: my-custom-skill
description: Detailed description of when Claude should trigger this skill.
---

# Skill Title

## 🚀 Instructions
- Step-by-step guidance for Claude.
- Clear constraints and rules (e.g., Coding standards).

## 💡 Examples
- Provide concrete examples of inputs and expected outputs.

## 🔗 References
- [Advanced Docs](reference-docs.md)
- [Implementation Examples](examples.md)
🎯 3. Core Principles (Best Practices)PrincipleDescriptionProgressive DisclosureClaude pehle sirf metadata parhta hai, gehri details tabhi load hoti hain jab zaroorat ho.One-Level Deep RuleSaari extra files ka link direct SKILL.md mein hona chahiye. Nested links (link ke andar link) avoid karein.Domain IsolationHar domain (UI, API, DB) ki alag skill banayein taake context focused rahe.Naming ConventionMax 64 characters. "anthropic" ya "claude" jaise reserved words use na karein.⚙️ 4. Product Surface ComparisonClaude Code: Full network access aur computer par scripts execute karne ki ijazat.Claude API: No network access aur sirf pre-installed packages use kar sakta hai.🛠️ 5. Step-by-Step Creation ProcessIdentify: Dekhein kaunsa task repetitive hai (e.g., Figma calculations).Naming: Aik unique lowercase name aur clear description chunein.Drafting: SKILL.md likhein aur YAML header lazmi dalein.Linking: Agar info zyada hai toh use alag files mein baant kar SKILL.md se link karein (One-level deep).Activation: Terminal mein project folder se Claude run karein, wo automatically .claude/skills/ scan kar lega.
