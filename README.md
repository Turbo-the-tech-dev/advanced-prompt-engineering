# 🧠 Advanced Prompt Engineering Techniques

> "The prompt is the new code. Master it, and you master the AI."

A comprehensive repository of advanced prompt engineering techniques for maximizing AI performance, accuracy, and reasoning capabilities.

---

## 📁 Directory Structure

```
advanced-prompt-engineering/
├── role-packaging/           # Framing the AI's role
├── persona-assignment/       # Giving the AI a character
├── specific-knowledge/       # Domain expertise injection
├── tone/                     # Voice and mood control
├── style/                    # Writing style specification
├── tasks/                    # Task decomposition
├── few-shot/                 # Few-shot learning patterns
├── examples/                 # Worked examples
├── shots/                    # Single/multi-shot techniques
├── designed-input-format/    # Structured input templates
├── data-classification/      # Categorization prompts
├── chain-of-thought/         # CoT reasoning
├── complex-reasoning/        # Multi-step logic
├── step-by-step/             # Sequential processing
├── show-its-work/            # Explicit reasoning display
├── accuracy/                 # Precision optimization
├── mastering-techniques/     # Advanced mastery
├── transition/               # Smooth topic shifts
└── prompt-solving-partner/   # Collaborative prompting
```

---

## 🎯 Technique Overview

| Technique | Purpose | Difficulty | Impact |
|-----------|---------|------------|--------|
| **Role Packaging** | Frame the AI's identity | ⭐ | High |
| **Persona Assignment** | Give character traits | ⭐ | High |
| **Specific Knowledge** | Inject domain expertise | ⭐⭐ | Very High |
| **Tone Control** | Set voice/mood | ⭐ | Medium |
| **Style Specification** | Define writing style | ⭐ | Medium |
| **Task Decomposition** | Break into subtasks | ⭐⭐ | High |
| **Few-Shot Learning** | Provide examples | ⭐⭐⭐ | Very High |
| **Chain of Thought** | Enable reasoning | ⭐⭐⭐ | Critical |
| **Complex Reasoning** | Multi-step logic | ⭐⭐⭐⭐ | Critical |
| **Step-by-Step** | Sequential processing | ⭐⭐ | High |
| **Show Its Work** | Explicit reasoning | ⭐⭐ | High |
| **Accuracy Optimization** | Precision focus | ⭐⭐⭐ | Critical |

---

## 🎭 1. Role Packaging

**What it is:** Framing the AI's role to optimize responses.

```
❌ Weak: "Tell me about electricity."

✅ Strong: "You are a Master Electrician with 20 years 
           of commercial installation experience. Explain 
           conduit bending techniques."
```

**Why it works:**
- Activates relevant training data
- Sets expertise expectations
- Filters inappropriate responses

**Template:**
```
You are a [ROLE] with [EXPERIENCE] specializing in [DOMAIN].
Your task is to [OBJECTIVE].
```

---

## 🎪 2. Persona Assignment

**What it is:** Giving the AI a character with traits.

```
❌ Weak: "Explain this code."

✅ Strong: "You are a patient, encouraging coding mentor 
           who breaks down complex concepts into simple 
           analogies. You celebrate small wins and never 
           make the student feel stupid."
```

**Key Elements:**
- Personality traits (patient, encouraging)
- Teaching style (analogies, celebration)
- Emotional guardrails (never condescending)

---

## 📚 3. Specific Knowledge

**What it is:** Injecting domain-specific information.

```
❌ Weak: "What's the load calculation?"

✅ Strong: "Using NEC 2023 Article 220, calculate the 
           feeder load for a 2,500 sq ft residential 
           dwelling with the following appliances:
           - Range: 12 kW
           - Dryer: 5 kW
           - HVAC: 3 tons, 240V"
```

**Why it works:**
- References specific standards
- Provides exact parameters
- Enables precise calculations

---

## 🎨 4. Tone Control

**What it is:** Setting the voice and mood.

```
Tone Options:
• Professional/Formal
• Casual/Friendly
• Urgent/Emergency
• Encouraging/Supportive
• Authoritative/Direct
• Poetic/Philosophical
```

**Example:**
```
"Respond in a calm, reassuring tone suitable for 
explaining technical concepts to anxious homeowners."
```

---

## ✍️ 5. Style Specification

**What it is:** Defining the writing style.

```
Style Options:
• Bullet points for quick scanning
• Numbered steps for procedures
• Tables for comparisons
• Code blocks for technical content
• Analogies for complex concepts
```

**Example:**
```
"Use short paragraphs. Include one real-world analogy 
per concept. End with a summary table."
```

---

## 📋 6. Task Decomposition

**What it is:** Breaking complex tasks into subtasks.

```
❌ Weak: "Design this electrical system."

✅ Strong: "Complete these steps in order:
1. Calculate total connected load (VA)
2. Apply demand factors per NEC 220.42
3. Determine service conductor size
4. Select main breaker rating
5. Verify voltage drop < 3%"
```

**Why it works:**
- Reduces cognitive load
- Ensures complete coverage
- Enables verification at each step

---

## 🎯 7. Few-Shot Learning

**What it is:** Providing examples to guide output.

```
Example Format:

Input: "What size wire for 100A service?"
Thought: "NEC 310.16, 75°C column, copper THHN..."
Output: "3 AWG copper"

Input: "What size wire for 200A service?"
Thought: "NEC 310.16, 75°C column, copper THHN..."
Output: "3/0 AWG copper"

Input: "What size wire for 60A service?"
Thought: [AI completes this]
Output: [AI generates answer]
```

**Types:**
- **Zero-shot:** No examples
- **One-shot:** One example
- **Few-shot:** 2-5 examples
- **Many-shot:** 5+ examples

---

## 📖 8. Examples (Worked)

**What it is:** Complete worked solutions.

```
Problem: Calculate the minimum service size for a 
1,800 sq ft home with 12 kW range and 5 kW dryer.

Solution:
1. General Lighting: 1,800 × 3 VA = 5,400 VA
2. Small Appliance: 2 × 1,500 VA = 3,000 VA
3. Laundry: 1 × 1,500 VA = 1,500 VA
4. Total General: 9,900 VA
5. Apply demand (220.42): 
   - First 3,000 VA @ 100% = 3,000 VA
   - Remainder 6,900 VA @ 35% = 2,415 VA
6. Range (220.55): 8 kW = 8,000 VA
7. Dryer (220.54): 5 kW = 5,000 VA
8. Total Load: 3,000 + 2,415 + 8,000 + 5,000 = 18,415 VA
9. Service Current: 18,415 VA ÷ 240V = 76.7A
10. Minimum Service: 100A (next standard size)
```

---

## 🎬 9. Shots (Single/Multi)

**What it is:** Controlling example quantity.

| Type | Examples | Use Case |
|------|----------|----------|
| Zero-shot | 0 | Simple, well-known tasks |
| One-shot | 1 | Pattern demonstration |
| Few-shot | 2-5 | Complex pattern learning |
| Multi-shot | 5+ | Nuanced task mastery |

---

## 📐 10. Designed Input Format

**What it is:** Structured input templates.

```
Template:
┌─────────────────────────────────────┐
│ TASK: [What needs to be done]       │
│ CONTEXT: [Background information]   │
│ CONSTRAINTS: [Limitations/rules]    │
│ OUTPUT FORMAT: [Expected structure] │
│ EXAMPLES: [Reference solutions]     │
└─────────────────────────────────────┘
```

**Example:**
```
TASK: Calculate conduit fill
CONTEXT: 4 x 12 AWG THHN in 1/2" EMT
CONSTRAINTS: NEC Chapter 9, Table 1 (40% fill)
OUTPUT FORMAT: Step-by-step with table
EXAMPLES: [See examples/ directory]
```

---

## 🗂️ 11. Data Classification

**What it is:** Categorization and labeling prompts.

```
Prompt:
"Classify each electrical load as:
- CONTINUOUS (3+ hours): Multiply by 125%
- NON-CONTINUOUS (< 3 hours): 100%

Loads:
1. General lighting in dwelling
2. Store lighting
3. Water heater
4. EV charger
5. Security system"

Expected Output Format:
| Load | Classification | Multiplier |
|------|---------------|------------|
| ...  | ...           | ...        |
```

---

## 🔗 12. Chain of Thought (CoT)

**What it is:** Enabling explicit reasoning.

```
❌ Weak: "What's 8 ÷ 2(2+2)?"

✅ Strong: "Solve this step by step. Show your 
           reasoning at each stage before giving 
           the final answer."

Output:
Step 1: Evaluate parentheses: (2+2) = 4
Step 2: Rewrite: 8 ÷ 2 × 4
Step 3: Left-to-right: 8 ÷ 2 = 4
Step 4: Continue: 4 × 4 = 16
Answer: 16
```

**Magic Phrase:**
> "Let's think step by step."

**Why it works:**
- Forces sequential processing
- Makes errors visible
- Improves accuracy 40-80%

---

## 🧩 13. Complex Reasoning

**What it is:** Multi-step logical deduction.

```
Structure:
1. State the problem
2. Identify known information
3. Identify unknown information
4. List relevant rules/principles
5. Apply rules to knowns
6. Derive intermediate conclusions
7. Combine for final answer
8. Verify against constraints
```

**Example (Electrical):**
```
"Design a feeder for a 50 HP motor:
1. Problem: Size conductors and OCPD
2. Known: 50 HP, 480V, 3-phase, Design B
3. Unknown: FLA, conductor size, breaker size
4. Rules: NEC 430.6, 430.22, 430.52, Table 310.16
5. Apply: FLA from Table 430.250 = 65A
6. Conductor: 65A × 1.25 = 81.25A → 4 AWG
7. Breaker: 65A × 2.5 = 162.5A → 175A
8. Verify: Voltage drop < 3% at 100 ft ✓"
```

---

## 📝 14. Step-by-Step

**What it is:** Sequential processing enforcement.

```
Prompt Pattern:
"Complete this task one step at a time.
After each step, pause and verify correctness
before proceeding to the next step."

Benefits:
• Reduces errors
• Enables debugging
• Shows reasoning process
• Builds confidence
```

---

## 🔍 15. Show Its Work

**What it is:** Explicit reasoning display.

```
❌ Weak: "What's the answer?"

✅ Strong: "Show all your work. Include:
1. Formulas used
2. Intermediate calculations
3. Unit conversions
4. Final answer with units"
```

**Why it matters:**
- Errors become visible
- Learning is enabled
- Verification is possible
- Trust is built

---

## 🎯 16. Accuracy Optimization

**What it is:** Precision-focused prompting.

```
Techniques:

1. **Self-Verification:**
   "After solving, review your answer and check 
   for errors. List any assumptions you made."

2. **Confidence Scoring:**
   "Provide a confidence level (0-100%) for 
   your answer and explain why."

3. **Alternative Methods:**
   "Solve this two different ways to verify 
   the answer."

4. **Constraint Checking:**
   "Verify your answer against these constraints:
   - NEC 210.19(A)(1)
   - Voltage drop < 3%
   - Temperature correction"
```

---

## 🎓 17. Mastering Techniques

**What it is:** Combining all techniques.

```
The Master Prompt:

"You are a Master Electrician preparing for 
NEC certification exam (ROLE + PERSONA).

Using NEC 2023 Articles 210-220, calculate 
the service load for this dwelling (SPECIFIC 
KNOWLEDGE).

Show your work step by step, explaining each 
calculation (CHAIN OF THOUGHT + SHOW WORK).

Use this format (DESIGNED INPUT):
┌────────────────────────┐
│ Step | Calculation    │
│------|----------------│
│  1   | ...            │
└────────────────────────┘

After solving, verify against code requirements 
(ACCURACY + SELF-VERIFICATION).

Tone: Professional but educational (TONE).
Include one analogy for each major concept (STYLE)."
```

---

## 🔄 18. Transition

**What it is:** Smooth topic shifts.

```
Transition Phrases:
• "Now that we've established X, let's consider Y..."
• "Building on that foundation..."
• "This leads us to the next question..."
• "With that understood, we can now..."

Why it matters:
• Maintains context
• Reduces confusion
• Creates narrative flow
• Enables complex multi-part tasks
```

---

## 🤝 19. Prompt Solving Partner

**What it is:** Collaborative AI interaction.

```
Mindset Shift:
❌ AI as oracle (one-shot Q&A)
✅ AI as partner (iterative collaboration)

Pattern:
1. State the problem
2. AI proposes approach
3. You review and refine
4. AI executes
5. You verify
6. Iterate until complete

Example:
"Let's work through this together. I'll provide 
the problem, you suggest the approach, and we'll 
solve it step by step. Ready?"
```

---

## 📊 Production Roadmap

| Phase | Techniques | Deliverable | Timeline |
|-------|------------|-------------|----------|
| **1** | Role, Persona, Tone | Basic prompt templates | Week 1 |
| **2** | Few-shot, Examples, Shots | Example library | Week 2 |
| **3** | CoT, Step-by-step, Show Work | Reasoning templates | Week 3 |
| **4** | Complex Reasoning, Accuracy | Advanced patterns | Week 4 |
| **5** | All Combined | Master prompt system | Week 5 |

---

## 🛠️ Quick Reference Card

```
┌─────────────────────────────────────────────────────────┐
│  PROMPT ENGINEERING CHEAT SHEET                         │
├─────────────────────────────────────────────────────────┤
│                                                         │
│  1. ROLE: "You are a..."                                │
│  2. PERSONA: "You are patient, thorough..."             │
│  3. KNOWLEDGE: "Using [standard]..."                    │
│  4. TONE: "Respond in a... tone"                        │
│  5. STYLE: "Use bullet points, tables..."               │
│  6. TASK: "Complete these steps..."                     │
│  7. EXAMPLES: Provide 2-3 worked examples               │
│  8. FORMAT: "Output as a table with columns..."         │
│  9. CoT: "Think step by step, show your work"           │
│ 10. VERIFY: "Check your answer against..."              │
│                                                         │
└─────────────────────────────────────────────────────────┘
```

---

## 📚 Resources

| Resource | Type | Link |
|----------|------|------|
| Anthropic Prompt Engineering | Guide | docs.anthropic.com |
| OpenAI Prompt Engineering | Guide | platform.openai.com |
| Learn Prompting | Course | learnprompting.org |
| Prompt Engineering Guide | Repo | github.com/dair-ai |

---

*"Master the prompt, master the AI. Master the AI, master any domain."*
