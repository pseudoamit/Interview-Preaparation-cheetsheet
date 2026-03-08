# Question 7: Build a Radio Selection Component

## Problem Statement

Build a **Radio Selection Component in React** where a user can select **only one option at a time** from a list of available choices.

This component should behave like a **standard radio button group**, meaning that when a user selects a new option, the **previously selected option should automatically be deselected**.

## The goal is to implement **controlled radio inputs using React state**.

## Requirements

1. Display a list of **radio options** to the user.
2. The user should be able to **select only one option at a time**.
3. When a user selects an option:
   - That option should become **active/checked**.
   - Any previously selected option should be **automatically unselected**.
4. The selected value should be **stored in React state**.
5. The UI should reflect the **currently selected option**.

---

## Example Options

Example list of radio options:

```javascript
const options = ["React", "Angular", "Vue", "Svelte"];
```

---

## Expected UI Example

```
Select your preferred framework:

( ) React
( ) Angular
( ) Vue
( ) Svelte
```

When the user selects **React**:

```
(●) React
( ) Angular
( ) Vue
( ) Svelte
```

If the user then selects **Vue**:

```
( ) React
( ) Angular
(●) Vue
( ) Svelte
```

---

## Expected Behavior

- Only **one radio option can be selected at a time**.
- Selecting a new option should **replace the previous selection**.

---

## Visual Flow

```
User sees multiple radio options
        ↓
User selects one option
        ↓
React state updates
        ↓
Selected radio button becomes checked
        ↓
Previous selection is automatically deselected
```

---

## Technical Constraints

- Use **React Functional Components**
- Use **React Hooks**
- Manage the selected option using **component state**

---

## React Concepts Expected

The interviewer expects candidates to demonstrate knowledge of:

- `useState`
- Controlled form components
- Event handling (`onChange`)
- Conditional rendering based on state

---

## Possible Follow-up Enhancements

Interviewers may ask candidates to extend the solution with:

1. Allow **dynamic options from an API**.
2. Display the **currently selected option below the list**.
3. Allow a **default selected option**.
4. Convert it into a **reusable radio group component**.
5. Support **disabled options**.

---

## Key Concept Being Tested

This problem evaluates the candidate's ability to:

- Implement **controlled form inputs in React**
- Manage **state-based UI updates**
- Ensure **mutually exclusive selection behavior**
