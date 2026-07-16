# Prompts & Skills Reference

## Table of Contents
1. [Email Prompt — Chief Guest Invitation](#1-email-prompt--chief-guest-invitation)
2. [Google Form Prompt — AI Essentials Registration](#2-google-form-prompt--ai-essentials-registration)
3. [Skill: Structured Topic Analyzer](#3-skill-structured-topic-analyzer)
4. [Skill: Humanize Text](#4-skill-humanize-text)

---

## 1. Email Prompt — Chief Guest Invitation

**Purpose:** Send a professional HTML email invitation via Claude.

> Create a professional HTML email invitation to example@gmail.com, inviting the recipient to serve as the Chief Guest for the AI Essentials Program. The event will be held at Dhanwantari Hall, Ayurved Campus, at 2:00 PM on Thursday, 32 Ashar 2083. The program is jointly organized by Ignite Open Source (IOS) and SearchStudent Club. Design the email with a modern, elegant layout featuring subtle interactive graphics and visual elements that blend Artificial Intelligence and Ayurveda (e.g., neural networks, herbal motifs, medical leaves, digital patterns). Maintain a formal, welcoming tone with clear event details and a prominent invitation to attend as Chief Guest.

---

## 2. Google Form Prompt — AI Essentials Registration

**Purpose:** Generate a Google Apps Script that auto-creates a registration form.

> Write a Google Apps Script that automatically creates a Google Form for registration for the AI Essentials Program, to be held at Dhanwantari Hall, Ayurved Campus, at 2:00 PM on Thursday, 32 Ashar 2083. The event is jointly organized by Ignite Open Source (IOS) and SearchStudent Club. Create a clean, minimal, and user-friendly form with an attractive header, clear sections, essential registration fields, and a professional theme reflecting both AI and Ayurveda. The script should generate the form automatically and be ready to run without modification.

---

## 3. Skill: Structured Topic Analyzer

**Skill Name:** `Structured Topic Analyzer`

**Skill Description:**
> Generate clear, well-structured learning notes for any topic. This skill organizes concepts into prerequisites, overview, key points, applications, advantages, limitations, FAQs, and a quick revision section, making complex topics easy to understand and revise. Suitable for students, educators, and self-learners.

**Skill Instructions:**

Whenever a topic is provided, generate a well-structured explanation using this format:

```markdown
# Topic

## Key Points to Know Before Learning
- 5–8 prerequisite concepts

## Overview
- A simple explanation (150–200 words)

## Important Points
- Bullet-point summary

## Real-World Applications
- Practical uses or examples

## Advantages
- Key benefits

## Limitations
- Important drawbacks

## Frequently Asked Questions (FAQs)
- 3–5 common questions with short answers

## Quick Revision
- 5 key takeaways
```

Keep the content simple, accurate, and easy to understand. Use headings, bullet points, and concise language.

---

## 4. Skill: Humanize Text

**Frontmatter:**

```yaml
---
name: humanize-text
description: Rewrites AI-generated text (from any chatbot — ChatGPT, Gemini, Claude, Copilot, etc.) so it reads as natural, human-written prose instead of machine-generated output. Use this skill whenever the user pastes text and asks to "humanize" it, make it "sound less like AI," "sound more natural/human," "remove the AI tone," or asks for help disguising or rewriting AI-generated writing so it passes as human-written. Also trigger on requests like "make this sound like I wrote it" or "get rid of the robotic phrasing" applied to a block of pasted text.
---
```
```markdown
### Overview
A skill for rewriting AI-generated text so it reads as natural, human-written prose — regardless of which chatbot originally produced it.

### When to Use This
Trigger whenever the user pastes a block of text (their own draft, or output from another AI tool) and asks to:
- "Humanize this"
- "Make this sound less like AI / more natural"
- "Remove the AI-sounding phrasing"
- "Make this sound like I wrote it"

If the user hasn't pasted any text yet, ask them to paste it before proceeding.

### What "AI-Sounding" Text Usually Looks Like
Before rewriting, scan the input for these common tells:
- Uniform sentence length and rhythm (every sentence is medium-length and grammatically tidy)
- Overused connective phrases: "Moreover," "Furthermore," "In conclusion," "It's worth noting that," "Additionally," "That said"
- Formulaic three-part lists ("not only X, but also Y, and ultimately Z")
- Excessive hedging or over-explaining obvious points
- Perfectly parallel paragraph structure (every paragraph is the same length and shape)
- Overly polished, generic word choices where a simpler or more specific word would do
- Summary sentences that restate what was just said ("In summary, this shows that...")

### How to Rewrite
1. **Read for meaning first.** Understand what the text is actually trying to say before touching the wording — the facts, claims, and structure of the argument must stay intact. Never add or invent information.
2. **Vary sentence rhythm.** Mix short, punchy sentences with longer ones. Real human writing rarely maintains a constant cadence.
3. **Cut formulaic transitions.** Replace "Moreover," "Furthermore," "In conclusion" with either nothing (just start the next sentence) or a more casual connector ("Also," "But," "So").
4. **Simplify vocabulary.** Swap inflated words for plainer ones where it doesn't lose precision (e.g., "utilize" → "use," "facilitate" → "help").
5. **Break uniform paragraph structure.** Let some paragraphs run long, others be a single sentence. Avoid the "topic sentence + 3 supporting sentences + wrap-up sentence" template repeated over and over.
6. **Remove redundant summarizing.** Don't restate the point that was just made unless the original text specifically needs a recap (e.g., a long report section).
7. **Allow minor imperfection.** A stray fragment, a dash, a parenthetical aside, a sentence that starts with "And" or "But" — these read as human. Don't overdo it.
8. **Keep the voice appropriate to context.** A humanized email should still sound professional; a humanized blog post can be more casual. Match the register of the original request, don't just make everything sound like a text message.
9. **Preserve all facts, figures, names, and claims exactly.** Humanizing is about phrasing and rhythm, not content. Never alter numbers, quotes, or factual claims during the rewrite.

### What NOT to Do
- Don't add slang or casual filler that doesn't fit the original context or audience.
- Don't introduce factual claims, examples, or details that weren't in the original.
- Don't just find-and-replace a handful of "AI words" — that alone doesn't fix uniform rhythm or structure, which is the bigger tell.
- Don't make the text longer than necessary — humanizing isn't the same as padding.

### Output Format
Return the rewritten text directly. If the input was long (multiple paragraphs or sections), briefly note 2-3 specific changes made (e.g., "cut the 'Furthermore' transitions, varied sentence length, simplified a few word choices") so the user can see what changed without re-reading line by line.
```
