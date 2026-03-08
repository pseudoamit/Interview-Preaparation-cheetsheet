# Question 10: Build a Multi-Select Searchable Dropdown Component

## Problem Statement

Build a **Multi-Select Searchable Dropdown Component in React** that allows users to:

- Select **multiple options**
- **Search/filter options** inside the dropdown
- Display the **selected items**

Unlike a normal dropdown where only one option can be selected, this component should allow the user to **select multiple values from the list**.

The dropdown should also include a **search input field** to filter options dynamically as the user types.

---

## Requirements

1. Display a **dropdown input field**.
2. When the user clicks the dropdown, a **list of options should appear**.
3. The dropdown should include a **search input** at the top.
4. As the user types in the search field:
   - The list should **filter matching options**.
5. The user should be able to **select multiple options**.
6. Selected options should appear:
   - Inside the dropdown input
   - Or as **tags/chips** above the dropdown.
7. The user should be able to **deselect/remove selected options**.
8. The dropdown should **remain open while selecting multiple values**.

---

## Example Options

Example list of dropdown options:

```javascript
const options = ["React", "Angular", "Vue", "Svelte", "Next.js", "Node.js"];
```

---

## Expected UI Example

Initial state:

```
Select frameworks ▼
```

Dropdown opened:

```
Select frameworks ▼

[ Search... ]

[ ] React
[ ] Angular
[ ] Vue
[ ] Svelte
[ ] Next.js
[ ] Node.js
```

User selects **React and Vue**:

```
Selected: React, Vue

[ Search... ]

[x] React
[ ] Angular
[x] Vue
[ ] Svelte
[ ] Next.js
[ ] Node.js
```

---

## Expected Behavior

- Users can **select multiple options**.
- Selected options should **remain checked** in the list.
- Users can **search/filter options dynamically**.
- Users should be able to **remove selections**.

Example selected values stored in state:

```javascript
["React", "Vue"];
```

---

## Visual Flow

```
User clicks dropdown
        ↓
Options list appears
        ↓
User types in search field
        ↓
Options get filtered
        ↓
User selects multiple options
        ↓
Selected values stored in state
        ↓
Selected options displayed in UI
```

---

## Technical Constraints

- Use **React Functional Components**
- Use **React Hooks**
- Manage dropdown state properly
- Avoid unnecessary re-renders
- Ensure smooth search filtering

---

## React Concepts Expected

The interviewer expects candidates to demonstrate knowledge of:

- `useState`
- `useEffect`
- Handling arrays in state
- Controlled input components
- Filtering data dynamically
- Event handling
- Conditional rendering

---

## Possible Follow-up Enhancements

Interviewers may ask additional improvements such as:

1. Add **"Select All" option**.
2. Add **"Clear All" button**.
3. Show selected items as **removable tags/chips**.
4. Implement **keyboard navigation**.
5. Close dropdown when **clicking outside**.
6. Fetch dropdown options **from an API**.

---

## Key Concept Being Tested

This problem evaluates the candidate's ability to:

- Build a **complex reusable UI component**
- Manage **multiple selections and filtered data**
- Handle **dynamic user interaction**
- Structure scalable **React component logic**
