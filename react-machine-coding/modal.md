---

# Question 18: Build a Modal Component with Outside Click Close

## Problem Statement

Build a **Modal component** in React that appears as an overlay on top of the main content.

The modal should be triggered by a button click and should support the following behaviors:

- Close the modal using a **close button inside the modal**
- Close the modal by **clicking outside the modal area**

---

# Requirements

## 1. Open Modal

There should be a button in the UI that opens the modal.

Example UI:

```
[ Open Modal ]
```

When the user clicks the button:

```
Modal appears
Background content becomes inactive
```

---

# 2. Modal Layout

The modal should appear in the **center of the screen** with a semi-transparent overlay behind it.

Example UI:

```
-------------------------------------
|                                   |
|        (Overlay Background)       |
|                                   |
|        -------------------        |
|        |      Modal Box   |       |
|        |                  |       |
|        |  Modal Content   |       |
|        |                  |       |
|        |     [ Close ]    |       |
|        -------------------        |
|                                   |
-------------------------------------
```

---

# 3. Close Button Inside Modal

The modal should contain a **close button**.

Behavior:

```
User clicks "Close"
→ Modal disappears
```

Example:

```
[ Close ]
```

---

# 4. Close Modal on Outside Click

If the user clicks **outside the modal box (on the overlay area)**, the modal should close.

Example Behavior:

```
User clicks overlay
→ Modal closes
```

Clicks **inside the modal content** should **NOT close the modal**.

---

# Expected UI Behavior

1. Initially, the modal should **not be visible**.
2. Clicking **Open Modal** displays the modal.
3. Clicking **Close button** hides the modal.
4. Clicking **outside the modal** also closes the modal.
5. Clicking **inside the modal content** should not close it.

---

# Example Component Structure

```
App
 ├── Button (Open Modal)
 └── Modal
       ├── Overlay
       └── Modal Content
```

---

# Technical Constraints

- Use **React Functional Components**
- Use **React Hooks**
- Manage modal visibility using state
- Detect **outside click events**
- Prevent closing when clicking inside modal content

---

# React Concepts Expected

The interviewer expects candidates to demonstrate knowledge of:

- `useState`
- Event propagation
- Click event handling
- Conditional rendering
- Overlay UI patterns

---

# Possible Follow-up Enhancements

Interviewers may extend this problem with:

1. Close modal using the **Escape key**.
2. Add **animation when opening and closing** the modal.
3. Implement **focus trapping inside the modal**.
4. Prevent **background scrolling when modal is open**.
5. Render modal using **React Portal**.

---

# Key Concept Being Tested

This problem evaluates the candidate's ability to:

- Build **overlay UI components**
- Handle **outside click detection**
- Manage **component visibility state**
- Implement **interactive modal behavior**
