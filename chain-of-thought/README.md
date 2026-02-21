# 🔗 Chain of Thought (CoT)

> "Let's think step by step."

The most powerful prompt engineering technique for enabling AI reasoning.

---

## What is Chain of Thought?

Chain of Thought prompting encourages the AI to show its reasoning process before giving the final answer.

---

## The Magic Phrase

```
"Let's think step by step."
```

This simple addition can improve accuracy by **40-80%** on complex tasks.

---

## Before vs After

### ❌ Without CoT
```
Q: "If I have 3 apples and buy 5 more, then give away 2, 
    then triple what's left, how many do I have?"
A: "18 apples"
```

### ✅ With CoT
```
Q: "If I have 3 apples and buy 5 more, then give away 2, 
    then triple what's left, how many do I have?"

A: "Let's think step by step:
    1. Start with 3 apples
    2. Buy 5 more: 3 + 5 = 8 apples
    3. Give away 2: 8 - 2 = 6 apples
    4. Triple what's left: 6 × 3 = 18 apples
    Answer: 18 apples"
```

---

## Production Roadmap

| Phase | Task | Deliverable |
|-------|------|-------------|
| 1 | Basic CoT prompts | Simple step-by-step templates |
| 2 | Domain-specific CoT | Math, science, coding examples |
| 3 | Verification steps | Self-check prompts |
| 4 | Complex multi-step | Advanced reasoning chains |

---

## Templates

### Basic Template
```
[Problem statement]

Let's think step by step:
1. [First step]
2. [Second step]
3. [Continue until complete]
Answer: [Final answer]
```

### Advanced Template
```
[Problem statement]

To solve this, I'll:
1. First, [identify what we know]
2. Then, [identify what we need]
3. Apply [relevant rules/principles]
4. Calculate [intermediate results]
5. Verify [against constraints]

Step 1: ...
Step 2: ...
...

Final Answer: [answer with units]

Verification: [check work]
```

---

## Best Practices

1. **Always show work** - Even for simple problems
2. **Number each step** - Makes it scannable
3. **Label intermediate results** - "Step 3 result: 42 VA"
4. **Verify at the end** - Check against constraints
5. **Use units** - Always include units in calculations

---

*"The journey is the destination. Show the path, not just the destination."*
