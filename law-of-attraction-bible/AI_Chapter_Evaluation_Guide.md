# AI Chapter Evaluation & Proofreading Master Guide

This guide provides structured frameworks and prompt templates to help you get professional-grade developmental editing, copyediting, and proofreading feedback from advanced AI models on a chapter-by-chapter basis.

---

## 1. Core Framework for AI Chapter Evaluation

To maximize the quality of an AI-generated critique, every chapter submission should follow a structured blueprint. This ensures the AI maintains context across your book and evaluates your writing based on objective storytelling metrics.

```
[System Context & Book Overview]
       │
       ▼
[Chapter-Specific Metadata]
       │
       ▼
[Custom Instructions & Focus Areas]
       │
       ▼
[The Chapter Text]
```

### The Three Golden Rules of AI Critiques
1. **Never Upload Text Without Context:** An AI evaluating a random chapter will flag necessary mysteries as "plot holes" and slow burn pacing as "boring" unless you give it the background framework.
2. **Limit Scope Per Prompt:** Do not ask the AI to check grammar, plot consistency, emotional resonance, and historical accuracy all in one pass. Run separate passes for technical proofreading and creative development.
3. **Use Explicit Personas:** Force the AI into a specific role (e.g., "Line Editor", "Developmental Editor", "Proofreader") to dictate the tone, depth, and harshness of its feedback.

---

## 2. Comprehensive Master Prompts

Copy and paste these exact templates into your AI platform of choice. Replace the bracketed text `[...]` with your book's specific information.

### Prompt 1: The Comprehensive Developmental & Style Critique
*Best for: Early drafts, structural integrity, character voice, and pacing checks.*

```text
Act as an expert, candid, and professional developmental fiction editor. I am writing a book and need a comprehensive chapter critique. Do not sugarcoat your feedback; I want an honest assessment to improve my craft.

Here is the context of my project:
- Title: [Book Title]
- Genre: [e.g., Sci-Fi, Thriller, Romance]
- Target Audience: [e.g., Young Adult, Adult]
- Overall Book Summary: [Provide a 2-3 sentence overview of the main plot]
- Prior Chapter Context: [Provide a brief summary of what happened right before this chapter so the AI understands the continuity]

Please evaluate the chapter text provided below against the following four criteria:
1. Pacing & Momentum: Identify where the narrative drags, where it moves too quickly, and if the scene starts and ends at the right narrative moments.
2. Character Consistency & Voice: Assess whether the characters' actions, dialogue, and internal monologues align with their established personalities. Flag any "out-of-character" moments.
3. Show vs. Tell: Highlight specific instances where I am explaining feelings or background information ("telling") instead of allowing the reader to experience them through action and dialogue ("showing").
4. Dialogue Realism: Evaluate if the dialogue sounds natural, serves a narrative purpose (advancing plot or revealing character), and avoids on-the-nose exposition.

Format your response with clear headers for each of the four categories. Under each header, provide:
- A brief overall diagnostic assessment.
- Bulleted, actionable examples referencing specific lines or moments from the text.
- A concrete recommendation on how to rewrite or fix the flagged issue.

At the very end, provide a "Chapter Scorecard" rating Pacing, Characterization, and Engagement on a scale of 1-10, with a 1-sentence justification for each.

Here is the chapter text to analyze:
[Insert Chapter Text Here]
```

### Prompt 2: The Deep-Dive Line Editor & Proofreader
*Best for: Mid-to-late drafts, flow, syntax, sentence variety, and mechanical grammar checking.*

```text
Act as an elite copyeditor and mechanical proofreader. I want you to review the following chapter for style, rhythm, syntax, and grammatical perfection.

Please analyze the text for the following technical flaws:
1. Redundancies & Filter Words: Eliminate filter phrases that distance the reader from the experience (e.g., "she saw," "he heard," "she felt," "he noticed").
2. Passive Voice: Identify instances of passive construction and suggest active, high-energy verb replacements.
3. Sentence Structure Variety: Flag repetitive sentence structures (e.g., three sentences in a row starting with a noun-verb pattern) and areas where sentence lengths lack rhythmic variety.
4. Absolute Grammar & Typos: Catch misspelled words, missing punctuation, tense inconsistencies, and grammatical errors.

Provide your output in a structured table format with the following columns:
| Original Text Fragment | Issue Identified | Suggested Revision | Technical Reason for Change |

At the bottom of your report, provide a summarized list of my top 3 "crutch words" or mechanical habits discovered in this chapter so I can look out for them in future chapters.

Here is the chapter text to analyze:
[Insert Chapter Text Here]
```

### Prompt 3: The Continuous Continuity & Plot Hole Tracker
*Best for: Multi-chapter check-ins to make sure you aren't dropping plot threads.*

```text
Act as a continuity editor and line producer for a long-form novel. Your job is to make sure this chapter aligns perfectly with the established rules, setup, and world-building of my book.

Here is my current master story bible context:
- Magic/Tech System Rules: [e.g., Magic requires physical exhaustion, faster-than-light travel strains fuel supplies]
- Main Character Profiles & Physical Descriptions: [e.g., John has a scar on his left hand; Sarah speaks with a slight formal cadence]
- Unresolved Subplots Heading Into This Chapter: [e.g., The missing key from chapter 3; Sarah's distrust of the mentor]

Analyze the chapter below specifically for:
1. Contradictions: Did a character do or know something they shouldn't? Did a physical attribute or setting detail accidentally shift?
2. Dropped Threads: Did an urgent plot thread or character motivation from the setup disappear completely from this scene without reason?
3. Setup Tracking: Did I naturally advance the unresolved subplots listed above, or did this chapter stall the main narrative?

Provide a bulleted list of any logical inconsistencies found, ranked by severity (High, Medium, Low). If no major contradictions are found, provide a "Continuity Health Check" confirming alignment with the story bible.

Here is the chapter text to analyze:
[Insert Chapter Text Here]
```

---

## 3. Comparative Matrix of Leading AI Platforms

Not all AI models are built the same for creative writing workflows. Choose your platform based on your manuscript's length and your specific feedback goals.

| Platform | Strengths for Authors | Weaknesses | Ideal Use Case | Memory Capacity |
| :--- | :--- | :--- | :--- | :--- |
| **Claude (Anthropic)** | Exceptional grasp of subtext, emotional resonance, voice, and literary nuances. Writes and edits with the most natural human cadence. | Occasionally overly polite unless explicitly instructed to be harsh/candid. | **Developmental Pass & Dialogue Editing:** Best for analyzing character depth and style. | Huge (Can hold multiple chapters or an entire novella background). |
| **ChatGPT Plus (OpenAI)** | Highly analytical, structured, excellent at building complex tables and tracking strict logic or world rules. | Creative output can sometimes feel formulaic, predictable, or overly cliché. | **Proofreading & Continuity Tracking:** Best for structural outlines, spotting plot holes, and technical line-editing tables. | Large (Easily manages current chapter + full story bible context). |
| **DeepSeek** | Highly cost-effective or free tiers, excellent analytical frameworks, strong logical reasoning. | Creative stylistic adjustments can sometimes feel rigid or dry compared to literary-tuned models. | **Budget-Friendly Mechanical Proofreading:** Great for running highly systematic grammar and filter-word sweeps. | Standard to Large (Varies by interface; generally excellent for single-chapter passes). |

---

## 4. How to Handle and Implement AI Feedback

Receiving an automated report can be overwhelming. Follow this structural triage process to implement edits without ruining your unique creative voice.

```
                  [Receive AI Report]
                          │
                          ▼
             [Filter Out Platform Biases]
           (Ignore generic "make it punchier"
            if it ruins your stylistic voice)
                          │
                          ▼
            [Triage Structural Issues First]
            (Fix plot holes, pacing gaps,
             and character contradictions)
                          │
                          ▼
             [Execute Technical Copyedits]
           (Apply line-by-line grammar fixes
            and fix repetitive sentence flow)
                          │
                          ▼
            [Protect Your Creative Voice]
            (Do a final human pass to read
             the text aloud for rhythm)
```

### Actionable Triage Steps
1. **The 24-Hour Rule:** If the AI flags a major issue in your plot or pacing, do not immediately rewrite it. Step away for an hour to determine if the AI genuinely caught a structural weakness or if it simply lacked a piece of future context you haven't written yet.
2. **Beware of Homogenization:** AI models love clean, standardized, simple writing. If your style relies on poetic run-on sentences, stream-of-consciousness, or intentional fragments, the AI will try to correct it. **Reject edits that strip away your personal flavor.**
3. **The Read-Aloud Test:** After applying technical fixes suggested by an AI, read the revised paragraphs out loud. If your tongue trips or it sounds like a corporate textbook, discard the AI's phrasing and rewrite the correction in your own voice.

---
This guide is compiled for informational and structural support for independent authors. All prompt frameworks are optimized for modern large language models as of 2026.