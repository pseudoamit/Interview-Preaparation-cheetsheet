# Question 16: Build a Multi-Expand Accordion Component

## Problem Statement

Build an **Accordion component** in React that displays a list of sections. Each section contains:

- A **header**
- Associated **content**

Users should be able to **expand or collapse sections** by clicking on the header.

Unlike a traditional accordion, this component should allow **multiple sections to be open at the same time**.

---

# Requirements

## 1. Render Accordion Sections

You will receive a list of sections where each section contains:

- `title` (header)
- `content` (body text)

Example Data:

```javascript
const accordionData = [
  {
    title: "What is React?",
    content: "React is a JavaScript library for building user interfaces.",
  },
  {
    title: "What are Hooks?",
    content:
      "Hooks allow you to use state and other React features in functional components.",
  },
  {
    title: "What is Virtual DOM?",
    content:
      "Virtual DOM is a lightweight copy of the real DOM used to improve performance.",
  },
];
```

---

# 2. Expand and Collapse Sections

Users should be able to **click on a header to toggle the section**.

Behavior:

```
Click Header → Show Content
Click Again → Hide Content
```

Example UI:

```
▶ What is React?
▶ What are Hooks?
▶ What is Virtual DOM?
```

After clicking **What is React**:

```
▼ What is React?
React is a JavaScript library for building user interfaces.

▶ What are Hooks?
▶ What is Virtual DOM?
```

---

# 3. Multiple Sections Open Simultaneously

Unlike a traditional accordion, **multiple sections can remain open at the same time**.

Example:

```
▼ What is React?
React is a JavaScript library for building user interfaces.

▼ What are Hooks?
Hooks allow you to use state and other React features in functional components.

▶ What is Virtual DOM?
```

There should be **no restriction on the number of open sections**.

---

# Expected UI Behavior

1. Initially, all sections should be **collapsed**.
2. Clicking a header **toggles** the visibility of its content.
3. Users can **open multiple sections at once**.
4. Clicking an already open section should **collapse it**.

---

# Technical Constraints

- Use **React Functional Components**
- Use **React Hooks**
- Maintain the open/close state for each section
- Avoid unnecessary re-renders

---

# React Concepts Expected

The interviewer expects candidates to demonstrate knowledge of:

- `useState`
- Event handling
- Conditional rendering
- Component reusability
- Dynamic UI rendering

---

# Possible Follow-up Enhancements

Interviewers may ask candidates to extend the solution with:

1. Add **animation when expanding/collapsing**.
2. Add a **single-open mode** (only one section open at a time).
3. Add **keyboard accessibility**.
4. Persist accordion state using **localStorage**.
5. Add **icons for expand/collapse**.

---

# Key Concept Being Tested

This problem evaluates the candidate's ability to:

- Build **interactive UI components**
- Manage **component state**
- Handle **dynamic user interactions**
- Implement **expand/collapse behavior**
