---
# Question 17: Build an Autocomplete Search Component

## Problem Statement

Build an **Autocomplete (Typeahead) component** in React that suggests results to the user while typing in an input field.

As the user types, the component should display a **list of matching suggestions** based on the input.

Users should also be able to **select a suggestion**, which will populate the input field.
---

# Requirements

## 1. Search Input Field

The UI should contain a **text input field** where the user can type.

Example UI:

```
[ Search... ]
```

---

# 2. Display Suggestions

As the user types into the input field, display a **dropdown list of suggestions** that match the entered text.

Example Dataset:

```javascript
const suggestions = [
  "Apple",
  "Banana",
  "Orange",
  "Mango",
  "Pineapple",
  "Grapes",
  "Strawberry",
];
```

Example Behavior:

Input:

```
ap
```

Dropdown Suggestions:

```
Apple
Pineapple
Grapes
```

---

# 3. Select a Suggestion

Users should be able to **click on a suggestion** from the dropdown list.

Behavior:

```
User clicks "Apple"
→ Input field value becomes "Apple"
→ Suggestions dropdown disappears
```

---

# 4. Hide Suggestions

The suggestion list should disappear when:

- A suggestion is selected
- The input field is cleared
- The user clicks outside the component

---

# Expected UI Behavior

1. Initially, the suggestions dropdown should **not be visible**.
2. When the user types in the input field:
   - Filter the suggestions based on the input text.
3. Display the filtered results in a **dropdown list**.
4. Clicking a suggestion should:
   - Populate the input field
   - Close the dropdown.

---

# Example Data Structure

```javascript
const suggestions = [
  "Apple",
  "Banana",
  "Orange",
  "Mango",
  "Pineapple",
  "Grapes",
  "Strawberry",
];
```

---

# Technical Constraints

- Use **React Functional Components**
- Use **React Hooks**
- Implement **controlled input fields**
- Filter suggestions dynamically
- Handle dropdown visibility properly

---

# React Concepts Expected

The interviewer expects candidates to demonstrate knowledge of:

- `useState`
- Controlled components
- Event handling
- Conditional rendering
- Filtering lists
- Managing UI state

---

# Possible Follow-up Enhancements

Interviewers may extend this problem with:

1. Add **keyboard navigation (Arrow Up / Arrow Down)**.
2. Highlight the **matched text in suggestions**.
3. Fetch suggestions **from an API instead of static data**.
4. Implement **debounced API calls**.
5. Handle **large datasets efficiently**.

---

# Key Concept Being Tested

This problem evaluates the candidate's ability to:

- Build **search-driven UI components**
- Implement **dynamic suggestion lists**
- Manage **user input efficiently**
- Handle **interactive dropdown behavior**
