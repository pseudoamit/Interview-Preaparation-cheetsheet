---

# Question 15: Build a Resizable Table with Draggable Column Headers

## Problem Statement

Build a **dynamic table component** in React using a given list of:

1. **Column headers**
2. **Table data**
3. **Default column widths**

The table should support **resizable columns**, where users can **drag the edge of a column header to adjust its width**.

Each column must maintain a **minimum width of 50 pixels**.

---

# Requirements

## 1. Render Table from Given Data

You will receive:

- A list of **column headers**
- A dataset containing **rows of data**

Using this information, dynamically render a **table UI**.

Example Column Headers:

```javascript
const columns = ["Name", "Age", "Email"];
```

Example Data:

```javascript
const data = [
  { Name: "John", Age: 25, Email: "john@example.com" },
  { Name: "Alice", Age: 28, Email: "alice@example.com" },
  { Name: "Bob", Age: 30, Email: "bob@example.com" },
];
```

Expected UI:

```
--------------------------------------
| Name  | Age | Email                |
--------------------------------------
| John  | 25  | john@example.com     |
| Alice | 28  | alice@example.com    |
| Bob   | 30  | bob@example.com      |
--------------------------------------
```

---

# 2. Default Column Widths

You will also receive another dataset that specifies the **default width for each column**.

Example:

```javascript
const columnWidths = {
  Name: 150,
  Age: 100,
  Email: 250,
};
```

The table should use these widths when rendering the column headers.

---

# 3. Column Resize (Drag Functionality)

Users should be able to **resize columns by dragging the edge of the column header**.

Example Interaction:

```
| Name | Age | Email |

User drags the border between "Name" and "Age"
→ Column width adjusts dynamically
```

Requirements:

- Dragging should resize the column **horizontally**
- The resize should be **smooth and responsive**
- The width should update **in real time while dragging**

---

# 4. Minimum Column Width

Each column must have a **minimum width of 50 pixels**.

Example:

```
User drags column smaller
↓
If width < 50px
→ Stop resizing
→ Maintain minimum width = 50px
```

---

# Expected UI Behavior

1. Table should render dynamically based on the provided data.
2. Each column should respect its **default width**.
3. Users can **resize columns by dragging the header border**.
4. Column width **cannot be reduced below 50px**.
5. Table layout should update **immediately during resizing**.

---

# Example Data Structure

```javascript
const columns = ["Name", "Age", "Email"];

const columnWidths = {
  Name: 150,
  Age: 100,
  Email: 250,
};

const data = [
  { Name: "John", Age: 25, Email: "john@example.com" },
  { Name: "Alice", Age: 28, Email: "alice@example.com" },
  { Name: "Bob", Age: 30, Email: "bob@example.com" },
];
```

---

# Technical Constraints

- Use **React Functional Components**
- Manage column widths using **React state**
- Implement **drag events (`mousedown`, `mousemove`, `mouseup`)**
- Enforce **minimum column width (50px)**
- Avoid unnecessary re-renders

---

# React Concepts Expected

The interviewer expects candidates to demonstrate knowledge of:

- Dynamic table rendering
- DOM event handling
- Drag interactions
- State management
- Performance considerations
- Controlled UI updates

---

# Possible Follow-up Enhancements

Interviewers may ask candidates to extend the solution with:

1. Add **double-click to auto-fit column width**.
2. Implement **column sorting**.
3. Persist column width in **localStorage**.
4. Add **column reordering (drag-and-drop)**.
5. Support **resizing from both directions**.

---

# Key Concept Being Tested

This problem evaluates the candidate's ability to:

- Build **dynamic table components**
- Implement **drag-based UI interactions**
- Manage **stateful layouts**
- Handle **complex user interactions in React**
