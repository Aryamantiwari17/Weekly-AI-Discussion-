# What is a Head?

Before learning **Attention**, **Query**, **Key**, or **Value**, let's understand one simple idea:

> **What is a Head?**

A **Head** is simply an **independent worker** inside a Transformer.

Each head receives the **same input**, but each is free to process it in its own way.

---

## Think of a Team

Imagine your manager gives the same document to four employees.

Employee 1 looks for grammar mistakes.

Employee 2 checks the facts.

Employee 3 summarizes the document.

Employee 4 looks for security issues.

Everyone starts with the **same document**.

But each employee focuses on something different.

```
                Same Input
                     │
        ┌────────────┼────────────┐
        │            │            │
      Head 1      Head 2      Head 3      Head 4
        │            │            │            │
   Own Analysis Own Analysis Own Analysis Own Analysis
        └────────────┼────────────┘
                     │
             Combined Output
```

A **Head** works exactly like one of these employees.

---

# Why Multiple Heads?

Suppose you only had **one employee**.

That employee would have to:

- understand grammar
- find important information
- summarize
- detect errors

all at the same time.

Instead, we split the work across multiple independent heads.

Each head becomes good at discovering different patterns.

---

# Important Property

Every head:

- Receives the same input
- Has its own parameters (weights)
- Learns independently
- Produces its own output

No one tells a head what to learn.

During training, each head naturally specializes in different patterns because that helps solve the task.

---

# Real-Life Analogy

Imagine watching a football match.

One commentator watches only the striker.

Another watches the goalkeeper.

Another watches the defenders.

Another watches team formations.

Everyone is watching **the same game**.

But each notices different things.

A **Head** works the same way.

---

# Another Analogy

Imagine looking at a city.

One photographer captures:

- Buildings

Another captures:

- Roads

Another captures:

- People

Another captures:

- Nature

Same city.

Different perspectives.

Each perspective is like one **Head**.

---

# What Does a Head Actually Do?

A head is simply an independent computation unit.

You can think of it as:

```
Input
   │
   ▼
 Head
   │
   ▼
Output
```

How the head performs this computation depends on the model.

In a Transformer, it uses **Attention**.

But the concept of a **Head** exists independently of understanding attention.

---

# Head vs Attention

These two terms are often confused.

| Head | Attention |
|------|-----------|
| An independent processing unit | The mechanism used by a head to process information |
| Represents a perspective | Represents the computation performed |
| Multiple heads can exist | Each head performs its own attention computation |

A simple way to remember it:

> **Head = Who is doing the work.**  
> **Attention = How the work is being done.**

---

# Key Takeaways

- A **Head** is an independent processing unit.
- Every head receives the same input.
- Different heads learn different patterns.
- Their outputs are combined to build a richer representation.
- Attention is **what happens inside a head**, not what a head is.
