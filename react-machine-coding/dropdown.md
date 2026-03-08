# Question 9: Build a Dropdown Selection Component (Single Select)

## Problem Statement

Build a **Dropdown Selection Component in React** that allows a user to **select one value from a list of options**.

The dropdown should display a list of values when opened, and when a user selects an option, that value should become the **currently selected value**.

Only **one option can be selected at a time**.

## The goal is to implement a **controlled dropdown component using React state**.

## Requirements

1. Display a **dropdown input field**.
2. When the user clicks the dropdown, a **list of options should appear**.
3. The user should be able to **select only one option** from the list.
4. Once an option is selected:
   - The dropdown should **display the selected value**.
   - The dropdown list should **close**.
5. The selected value should be **stored in React state**.
6. The UI should always reflect the **currently selected value**.

---

## Example Options

Example list of dropdown options:

```javascript
const options = ["React", "Angular", "Vue", "Svelte"];
```

---

## Expected UI Example

Initial state:

```
Select a framework ▼
```

Dropdown opened:

```
Select a framework ▼

React
Angular
Vue
Svelte
```

After selecting **Vue**:

```
Vue ▼
```

---

## Expected Behavior

- Only **one option can be selected at a time**.
- The selected value should **update the dropdown label**.
- The dropdown list should **close automatically after selection**.

---

## Visual Flow

```
User clicks dropdown
        ↓
Options list appears
        ↓
User selects an option
        ↓
React state updates
        ↓
Selected value displayed in dropdown
        ↓
Dropdown closes
```

---

## Technical Constraints

- Use **React Functional Components**
- Use **React Hooks**
- Manage selected value using **component state**
- Handle dropdown open/close state properly

---

## React Concepts Expected

The interviewer expects candidates to demonstrate knowledge of:

- `useState`
- Controlled form components
- Event handling (`onClick`, `onChange`)
- Conditional rendering
- Managing UI state

---

## Possible Follow-up Enhancements

Interviewers may ask additional improvements such as:

1. Add **keyboard navigation (arrow keys + enter)**.
2. Add **searchable dropdown functionality**.
3. Close dropdown when clicking **outside the component**.
4. Allow **dynamic options from an API**.
5. Support **default selected value**.

---

## Key Concept Being Tested

This problem evaluates the candidate's ability to:

- Implement a **controlled dropdown component**
- Manage **UI state transitions**
- Handle **user interaction and conditional rendering in React**
