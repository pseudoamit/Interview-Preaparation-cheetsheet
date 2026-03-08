# Question 14: Build a VS Code-Style Folder Explorer

## Problem Statement

Build a **file explorer UI similar to VS Code** that displays a hierarchical folder structure.

Users should be able to:

- Expand or collapse folders
- View files inside folders
- Add new files or folders inside any folder

The UI should behave like a **tree structure**, where each folder can contain **files or other folders**.

---

# Requirements

## 1. Folder Expansion and Collapse

The folder structure should be displayed in a **tree format**.

Users should be able to:

- Click on a **folder**
- Expand the folder to see its contents
- Collapse the folder to hide its contents

Example UI:

```
📁 src
   📁 components
      📄 Button.js
      📄 Modal.js
   📁 hooks
      📄 useFetch.js
   📄 App.js
```

When collapsed:

```
📁 src
```

---

## 2. Nested Folder Support

Folders can contain:

- Files
- Other folders

Example structure:

```
src
 ├── components
 │    ├── Button.js
 │    └── Modal.js
 ├── hooks
 │    └── useFetch.js
 └── App.js
```

The tree should support **unlimited nesting levels**.

---

## 3. Add New File

Users should be able to **add a new file inside any folder**.

Example:

User clicks **Add File** inside `components`.

Result:

```
📁 components
   📄 Button.js
   📄 Modal.js
   📄 NewFile.js
```

---

## 4. Add New Folder

Users should also be able to **create a new folder inside an existing folder**.

Example:

User adds a folder inside `src`.

Result:

```
📁 src
   📁 components
   📁 hooks
   📁 utils
   📄 App.js
```

---

# Expected UI Behavior

1. Folder icons should indicate expandable items.
2. Clicking a folder toggles **expand/collapse**.
3. Users can **add files or folders inside any folder**.
4. Newly added items should appear immediately in the tree.

---

# Example Initial Data Structure

```javascript
const explorer = {
  name: "root",
  isFolder: true,
  items: [
    {
      name: "src",
      isFolder: true,
      items: [
        {
          name: "components",
          isFolder: true,
          items: [
            { name: "Button.js", isFolder: false },
            { name: "Modal.js", isFolder: false },
          ],
        },
        {
          name: "hooks",
          isFolder: true,
          items: [{ name: "useFetch.js", isFolder: false }],
        },
        { name: "App.js", isFolder: false },
      ],
    },
  ],
};
```

---

# Technical Constraints

- Use **React Functional Components**
- Use **recursive rendering** for nested folders
- Maintain folder expand/collapse state
- Dynamically update the structure when adding files or folders

---

# React Concepts Expected

The interviewer expects candidates to demonstrate knowledge of:

- Recursive components
- `useState`
- Tree data structures
- Dynamic rendering
- Component composition
- Immutable state updates

---

# Possible Follow-up Enhancements

Interviewers may extend this problem by asking candidates to:

1. Implement **delete file/folder** functionality.
2. Add **rename file/folder** feature.
3. Implement **drag-and-drop file movement**.
4. Add **icons for file types**.
5. Persist data using **localStorage**.

---

# Key Concept Being Tested

This problem evaluates the candidate's ability to:

- Work with **tree data structures**
- Implement **recursive UI components**
- Manage **nested state updates**
- Build **interactive file explorer interfaces**
