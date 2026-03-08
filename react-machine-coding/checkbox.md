# Question 8: Build a Checkbox Selection Component

## Problem Statement

Build a **Checkbox Selection Component in React** where a user can select **multiple options at the same time** from a list.

Unlike radio buttons (where only one option can be selected), checkboxes allow **multiple selections simultaneously**.

## The component should manage the **selected options using React state** and update the UI accordingly.

## Requirements

1. Display a list of **checkbox options**.
2. Users should be able to **select multiple options simultaneously**.
3. When a checkbox is selected:
   - The option should become **checked**.
4. When a checkbox is unchecked:
   - The option should be **removed from the selected list**.
5. The selected values should be **stored in React state**.
6. The UI should always reflect the **currently selected options**.

---

## Example Options

Example list of checkbox options:

```javascript
const options = ["React", "Angular", "Vue", "Svelte"];
```

---

## Expected UI Example

```
Select your preferred frameworks:

[ ] React
[ ] Angular
[ ] Vue
[ ] Svelte
```

User selects **React and Vue**:

```
[x] React
[ ] Angular
[x] Vue
[ ] Svelte
```

---

## Expected Behavior

- Users can **select multiple options**.
- Each option should **toggle between checked and unchecked** when clicked.
- Selected options should be stored in a **list/array in state**.

Example selected values:

```javascript
["React", "Vue"];
```

---

## Visual Flow

```
User sees list of checkbox options
        ↓
User selects one or more options
        ↓
React state updates with selected items
        ↓
Checkbox UI reflects the selected state
```

---

## Technical Constraints

- Use **React Functional Components**
- Use **React Hooks**
- Manage selected options using **state**

---

## React Concepts Expected

The interviewer expects candidates to demonstrate knowledge of:

- `useState`
- Controlled form components
- Handling arrays in state
- Event handling (`onChange`)
- Conditional rendering

---

## Possible Follow-up Enhancements

Interviewers may ask additional improvements such as:

1. Add a **"Select All" checkbox**.
2. Add a **"Clear Selection" button**.
3. Disable certain checkbox options.
4. Fetch options **dynamically from an API**.
5. Display the **selected options summary**.

---

## Key Concept Being Tested

This problem evaluates the candidate's ability to:

- Implement **controlled checkbox inputs**
- Manage **array-based state updates**
- Handle **multiple selections in React**
