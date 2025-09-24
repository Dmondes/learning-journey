This repo documents my learning journey as I study and practice software testing, focusing on both **manual** and **automation** testing.
The goal: to clearly understand each concept, write notes in my own words, and track progress.

---

## Concept 1: The Fundamental Role of a Tester

**Analogy:**
- Developers = engineers building a car.
- Testers = drivers testing the car before customers use it.

**Main Goal of a Tester:**
- Verify the product works as expected.
- Find problems (bugs).
- Ensure quality before release.

**Developer vs Tester:**
- Developer = **Maker** (builds the product).
- Tester = **Checker** (validates the product).

**Key Idea:**
- It’s not "maker vs checker," but a **partnership** to deliver high-quality products.
- This process is called **Quality Assurance (QA)**.

💡 **Checkpoint:**
- In your own words: What is the main goal of a software tester?
- How is the role of a tester different from a developer?

---

## Concept 2: Two Ways of Testing (Manual vs Automation)

### Manual Testing
- Done **by hand** (like driving the car yourself).
- Examples: clicking buttons, checking features one by one, exploratory testing.
- **Best for:**
  - New features
  - UI/UX judgment
  - Creative bug-hunting

### Automation Testing
- Writing **scripts** that act like robots to run tests repeatedly.
- Fast, consistent, and reduces human error.
- **Best for:**
  - Regression testing (re-checking old features after updates)
  - Repetitive and predictable tasks

💡 **Checkpoint:**
- If you want to confirm the **Login button still works** → Automation (Regression Test).
- If you want to check if the **Login page design is clear** → Manual (UI Testing).

# Concept 3: The Automation "Toolbox" (Frameworks & Languages)

You can’t build a robot out of thin air. You need **parts, tools, and an instruction manual**.
In software automation, these are programming languages and frameworks.

---

### 1. The Programming Language (The Robot’s Language)
- The language you use to write instructions for your automation robot.
- Examples: **Java, Python, C#**.
- Just like humans speak English or Spanish, a computer "understands" Java or Python.

**Example instruction in Python:**
```python
if button.color == 'blue':
    button.click()
