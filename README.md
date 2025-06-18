# 🧠 Vibe Coding OS

## What is the Vibe Coding OS?

The Vibe Coding OS (Operating System) is a systematic and self-evolving framework for software development with Large Language Models (LLMs). It transforms the development process from a series of disconnected prompts into an intelligent, stateful workflow.

It's designed to solve the biggest challenges of working with LLMs: their limited context windows and lack of persistent memory. It does this by creating a resilient, documentation-driven system where the LLM's "thinking" is captured, organized, and reused.

## Core Principles: THINK → ACT → LEARN → EVOLVE

This entire OS is built around a simple, powerful feedback loop:

1.  **THINK**: Understand requirements, context, and architecture *before* writing code.
2.  **ACT**: Execute tasks with clear guidance from established standards and patterns.
3.  **LEARN**: Capture every decision, failure, and success as structured knowledge.
4.  **EVOLVE**: Use that captured knowledge to make the system itself smarter for the next interaction.

## 🚀 Quick Start

1.  **Copy this project structure** to your new repository.
2.  **Open the project in Cursor.** The OS will activate automatically.
3.  **Start the discovery process by editing `vibe_docs/task_on_hand.md`**.
4.  **Converse with the LLM.** It will read the `task_on_hand.md` and our core rules to begin asking clarifying questions.
5.  **Watch the documentation and the system evolve** as your project takes shape.

## 📁 System Architecture

The OS consists of two main components that work together: the Brain and the Memory.

### 🧠 `.cursor/rules/` (The Brain)

This is the intelligent engine of the OS. It's a set of modular rules that tell the LLM *how* to think and act based on the current context.

-   **`core.mdc`**: The kernel of the OS. It's **always active** and contains the core principles, auto-creation protocols, and the conflict resolution hierarchy.
-   **`design.mdc`**: A specialist for architectural thinking. Invoked manually with **`@design`**.
-   **`implement.mdc`**: A specialist for code quality. Activates **automatically** when you edit source code files.
-   **`debug.mdc`**: A specialist for troubleshooting. Invoked manually with **`@debug`**.

### 📚 `vibe_docs/` (The Memory)

This is the persistent knowledge base of the project. It's where the "thinking" from the Brain gets stored.

-   **`task_on_hand.md`**: The main working document for the current session's goals and progress.
-   **`development_log.md`**: An append-only log of all decisions and actions.
-   **`project_context.md`** & **`technical_details.md`**: Store the long-term strategic and technical knowledge of the project.
-   **Auto-Created Documents**: Files like `troubleshooting_runbook.md` and `coding_standards.md` are created **on-demand** by the OS the first time they are needed.

## 🔄 How It Works: The Process in Action

### 1. The Core Loop (Always-On)

The `core.mdc` rule is always running. It ensures that every session starts with a clear understanding of the current task and that the "THINK BEFORE CODE" philosophy is always enforced.

### 2. On-Demand Documentation (Auto-Creation)

You don't need to create every file upfront. The OS is smart. When a rule needs to document a failure, it checks for `troubleshooting_runbook.md`. If it doesn't exist, the **`Auto-Creation Protocol`** from the core rule creates it with the correct template.

### 3. Invoking Specialists (Manual & Automatic)

When you need to shift context, you invoke a specialist:

-   **Making a big decision?** Start your prompt with `@design` to load the architectural thinking module.
-   **Hitting a tough bug?** Start your prompt with `@debug` to load the systematic troubleshooting module.
-   **Writing code?** The `implement` module activates automatically, ensuring you adhere to project standards.

### 4. Conflict Resolution

If multiple rules ever give conflicting advice, the **`Rule Conflict Resolution`** hierarchy in `core.mdc` ensures a predictable outcome. The highest priority is always **Human Override**, guaranteeing you are in control.

## 💡 Key Benefits

1.  **No Context Loss**: All critical information is persisted in `vibe_docs`.
2.  **Self-Healing & Resilient**: The system can create missing documents and handle rule conflicts gracefully.
3.  **Intelligent Automation**: The system automates documentation, enforces standards, and guides the development process.
4.  **Systematic Approach**: Ensures no important details are missed during any phase of development.
5.  **Self-Improving**: The entire system—rules and documentation—evolves and gets smarter with every interaction.

## 📝 Example Usage

```
You: "Okay, I'm ready to figure out the database schema."

LLM: "Understood. What are your thoughts on the schema?"

You: "@design I need to decide between a relational (SQL) or NoSQL database for this project. Can you help me weigh the pros and cons based on our project context?"

LLM: *Reads the design.mdc rule and your project_context.md file*
"Of course. Let's analyze this from an architectural perspective. Given that our project requires [requirement from project_context], here are the key considerations..."
```

## 🔧 Customization

Feel free to:

- Add more template documents
- Modify the question categories
- Adjust the process to your workflow
- Add project-specific sections

The key is maintaining the core principle: **Document everything for context preservation**.

## 🤝 Contributing

If you develop improvements to the vibe coding system:

1. Document what worked well
2. Note what could be improved
3. Share your enhanced templates
4. Help evolve the methodology

---

**Remember**: The goal is a sustainable development flow that works *with* an LLM's strengths while systematically overcoming its weaknesses.