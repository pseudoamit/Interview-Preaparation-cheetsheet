---

# Question 3: Build a Configurable Toast Notification System

## Problem Statement

Build a **Toast Notification System in React** that can display different types of notifications such as:

- Success
- Error
- Warning
- Info

The notification system should be **configurable**, allowing the developer to control the **position of the toast container** on the screen.

The goal is to design a **reusable and flexible toast component** that can be triggered from anywhere in the application.

---

## Requirements

1. Create a **Toast component** that displays notification messages.
2. The toast should support **multiple notification types**:
   - Success
   - Error
   - Warning
   - Info
3. Each notification type should have a **distinct visual style** (color or icon).
4. The toast should automatically **disappear after a few seconds**.
5. Multiple toast notifications should be able to **stack together**.
6. The toast system should support **different screen positions**.

---

## Configurable Positions

The toast container should support the following positions:

- `top-left`
- `top-right`
- `bottom-left`
- `bottom-right`

Example configuration:

```javascript
<ToastContainer position="top-right" />
```

---

## Expected UI Behaviour

1. When an action triggers a toast notification, the message should **appear on the screen**.
2. The notification should appear at the **configured position**.
3. If multiple notifications are triggered, they should **stack vertically**.
4. Each toast should **automatically disappear after a specified duration** (for example: 3 seconds).
5. The user should also be able to **manually close the toast**.

---

## Example Usage

Example of triggering different toast notifications:

```javascript
showToast({
  type: "success",
  message: "Data saved successfully",
});

showToast({
  type: "error",
  message: "Failed to save data",
});

showToast({
  type: "warning",
  message: "Please check your input",
});

showToast({
  type: "info",
  message: "New update available",
});
```

---

## Example UI Behaviour

```
Top Right
----------------------------------
✔ Data saved successfully
⚠ Please check your input
ℹ New update available
----------------------------------
```

Each notification will **automatically disappear after a few seconds**.

---

## Technical Constraints

- Use **React Functional Components**
- Use **React Hooks**
- The toast system should be **reusable across the application**
- Avoid unnecessary re-renders
- Ensure multiple notifications can be handled efficiently

---

## Suggested Architecture

A typical implementation may include:

- **ToastContainer**
- **Toast component**
- **Toast context / custom hook**
- **Global state to manage notifications**

Example structure:

```
components/
  ToastContainer.jsx
  Toast.jsx

hooks/
  useToast.js
```

---

## React Concepts Expected

The interviewer expects candidates to demonstrate knowledge of:

- `useState`
- `useEffect`
- `useContext` (optional but recommended)
- Component composition
- State management
- Dynamic rendering of components

---

## Possible Follow-up Enhancements

Interviewers may ask additional improvements such as:

1. Add **animations when toast appears and disappears**.
2. Allow **custom duration per toast**.
3. Add **progress bar for auto-dismiss timer**.
4. Implement **pause on hover**.
5. Prevent too many toasts from appearing simultaneously.

---

## Key Concept Being Tested

This problem evaluates the candidate's ability to:

- Design **reusable UI components**
- Manage **dynamic UI state**
- Implement **configurable UI behavior**
- Structure a **scalable React component system**
