# Question 11: Build a Master–Child Checkbox Selection System

## Problem Statement

Build a **checkbox selection system in React** where there is:

- One **Master Checkbox**
- Multiple **Child Checkboxes**

The master checkbox controls the **selection and deselection of all child checkboxes**.

Additionally, the state of the **master checkbox should automatically update based on the selection state of the child checkboxes**.

This problem tests the ability to **synchronize parent and child state relationships**.

---

## Requirements

1. Display one **Master Checkbox** at the top.
2. Display multiple **Child Checkboxes** below it.
3. When the **Master Checkbox is selected**:
   - All child checkboxes should become **selected**.
4. When the **Master Checkbox is deselected**:
   - All child checkboxes should become **deselected**.

---

## Child Checkbox Behavior

The system should also work **in reverse**.

1. If **any child checkbox is selected**, the **master checkbox should automatically become selected**.
2. If **all child checkboxes are deselected**, the **master checkbox should also become deselected**.

---

## Example Options

Example list of child checkboxes:

```javascript
const options = ["Option 1", "Option 2", "Option 3", "Option 4"];
```

---

## Expected UI Example

Initial state:

```
[ ] Select All

[ ] Option 1
[ ] Option 2
[ ] Option 3
[ ] Option 4
```

---

### When Master Checkbox is Selected

```
[x] Select All

[x] Option 1
[x] Option 2
[x] Option 3
[x] Option 4
```

---

### When a Child Checkbox is Selected

```
[x] Select All

[x] Option 1
[ ] Option 2
[ ] Option 3
[ ] Option 4
```

---

### When All Child Checkboxes Are Deselected

```
[ ] Select All

[ ] Option 1
[ ] Option 2
[ ] Option 3
[ ] Option 4
```

---

## Visual Flow

```
User selects Master Checkbox
        ↓
All Child Checkboxes become selected

User deselects Master Checkbox
        ↓
All Child Checkboxes become deselected

User selects a Child Checkbox
        ↓
Master Checkbox becomes selected

User deselects all Child Checkboxes
        ↓
Master Checkbox becomes deselected
```

---

## Technical Constraints

- Use **React Functional Components**
- Use **React Hooks**
- Manage checkbox states using **React state**
- Ensure parent-child state synchronization

---

## React Concepts Expected

The interviewer expects candidates to demonstrate knowledge of:

- `useState`
- Managing arrays in state
- Controlled form components
- Event handling (`onChange`)
- Parent–child state relationships
- Conditional state updates

---

## Possible Follow-up Enhancements

Interviewers may ask candidates to extend the solution with:

1. Add an **indeterminate state** to the master checkbox when **some but not all children are selected**.
2. Allow child checkboxes to be **dynamically loaded from an API**.
3. Add a **Select All / Clear All button**.
4. Display the **count of selected checkboxes**.
5. Convert the component into a **reusable checkbox group component**.

---

## Key Concept Being Tested

This problem evaluates the candidate's ability to:

- Synchronize **parent and child component state**
- Implement **Select All / Deselect All logic**
- Manage **dynamic checkbox selections**
- Handle **bidirectional state updates**
