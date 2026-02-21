# 🎯 Few-Shot Learning

> "Show, don't just tell."

Providing examples to guide the AI's output pattern.

---

## What is Few-Shot Learning?

Giving the AI 2-5 examples of input-output pairs to demonstrate the desired pattern.

---

## Types of Shots

| Type | Examples | Use Case |
|------|----------|----------|
| Zero-shot | 0 | Simple, well-known tasks |
| One-shot | 1 | Pattern demonstration |
| Few-shot | 2-5 | Complex pattern learning |
| Many-shot | 5+ | Nuanced mastery |

---

## Example: Wire Sizing

```
Example 1:
Input: "What size copper THHN for 100A at 75°C?"
Thought: "NEC 310.16, 75°C column, 100A rating"
Output: "3 AWG copper THHN"

Example 2:
Input: "What size copper THHN for 200A at 75°C?"
Thought: "NEC 310.16, 75°C column, 200A rating"
Output: "3/0 AWG copper THHN"

Example 3:
Input: "What size copper THHN for 60A at 75°C?"
Thought: [AI completes]
Output: [AI generates]
```

---

## Why It Works

1. **Pattern recognition** - AI learns the format
2. **Quality control** - Examples set the standard
3. **Edge cases** - Show how to handle exceptions
4. **Consistency** - All outputs follow the same structure

---

## Production Roadmap

| Phase | Task | Deliverable |
|-------|------|-------------|
| 1 | Collect examples | 10-20 worked examples per domain |
| 2 | Categorize | Organize by difficulty/topic |
| 3 | Template creation | Reusable few-shot templates |
| 4 | Quality review | Verify all examples are correct |

---

## Best Practices

1. **Use 2-5 examples** - Enough to show pattern, not overwhelming
2. **Vary the inputs** - Show different scenarios
3. **Include edge cases** - Demonstrate exception handling
4. **Show reasoning** - Include the "Thought:" step
5. **Keep consistent format** - Same structure for all examples

---

*"Examples are the shadows of truth. Cast the right shadows."*
