# 🛠️ Claude Code Skills

## 1. Directory Structure (Folder Kaise Banega)
Claude Code (CLI) mein skills hamesha filesystem par base karti hain. Har skill ka apna ek folder hota hai:

```
.claude/
└── skills/
    └── [skill-name]/            <-- Sirf lowercase, numbers, aur hyphens
        ├── SKILL.md             <-- Main entry point (Zaroori hai)
        ├── logic-script.py      <-- Optional: Automation scripts
        └── reference-docs.md    <-- Optional: Extra details (One level deep) 
        ```
## 2. SKILL.md ka Structure

Har SKILL.md file ke shuru mein YAML Frontmatter hona lazmi hai taake Claude use "Discover" kar sake.
```
---
name: your-skill-name        <-- Max 64 chars, no reserved words like 'claude'
description: Brief summary   <-- Claude ise parh kar faisla karta hai ke kab use karna hai
---

# Skill Title

## Instructions
[Step-by-step rules jo Claude ko follow karni hain]

## Examples
[Concrete examples of how to use this skill]

## Scripts (Optional)
[References to other files in the folder]
---

## 3. Best Practices (Professional Patterns)
Aapne jo patterns parhe hain, unka nichor ye hai:

Progressive Disclosure: Claude ko shuru mein sirf SKILL.md ki basic info dikhayi jati hai. Wo gehri details (jaise nested files) tabhi parhta hai jab zaroorat ho.

One-Level Deep Rule: Saari extra files (reference, examples, logs) ka link seedha SKILL.md se hona chahiye. File ke andar file ka link (Deep nesting) Claude ko confuse kar deta hai.

Domain Isolation: Agar project bada hai, toh har domain (UI, Database, API) ki alag skill banayein taake context focused rahe.

## 4. Claude Code vs API Differences
Claude Code: Skills ko Full Network Access hota hai aur wo aapke computer par scripts chala sakti hain.

Claude API: Skills ka network access nahi hota aur wo pre-installed packages tak limited hoti hain.

## Skill Banane ka Process (Manual Step-by-Step)
Analyze: Pehle dekhein ke kya ye kaam baar-baar ho raha hai? (Jaise Figma to Tailwind calculation).

Define: Aik unique name aur clear description sochein.

Draft: SKILL.md likhein jisme clear constraints hon (e.g., "Always use Poppins font").

Reference: Agar documentation lambi hai, toh use alag files mein baant kar SKILL.md se link kar dein.
