# Question 13: Fetch Data and Implement Debounced Search Filtering

## Problem Statement

Build a **React application** that fetches a list of data from an API and displays it in the UI.

The application should also include a **search input box** that allows users to filter the displayed list.

However, the filtering should **not happen on every keystroke**. Instead, the filtering logic should execute **after a delay of 500 milliseconds** once the user stops typing.

## This behavior is commonly known as **debouncing**.

# Requirements

1. Fetch a **list of items from an API** when the component loads.

Example API:

```
https://jsonplaceholder.typicode.com/users
```

2. Render the fetched data in a **list format**.

Example UI:

```
• John
• Alice
• Robert
• Michael
• Sarah
```

3. Provide a **search input field** above the list.

Example:

```
[ Search user... ]
```

4. When the user types in the input box:

- The list should be **filtered based on the search text**
- Filtering should **not happen immediately**
- Instead, wait **500ms after the user stops typing**

5. If the user continues typing within those **500ms**, the previous filtering operation should be **cancelled**.

---

# Debounce Requirement

The filtering logic must implement **debouncing with a delay of 500 milliseconds**.

Example Behavior:

```
User types: J
(waiting...)

User types: Jo
(waiting...)

User types: Joh
(waiting...)

User stops typing
(after 500ms)

→ Filter results for "Joh"
```

Filtering should occur **only after the user pauses typing for 500ms**.

---

# Expected UI Behavior

1. When the component loads:
   - Fetch data from the API.

2. Display the full list initially.

3. When the user types in the search input:
   - Wait **500ms**
   - Then filter the list.

4. If the input is cleared:
   - Show the **original full list again**.

---

# Example API Response

```json
[
  { "id": 1, "name": "Leanne Graham" },
  { "id": 2, "name": "Ervin Howell" },
  { "id": 3, "name": "Clementine Bauch" }
]
```

---

# Example Filtering

Input:

```
cle
```

Output:

```
• Clementine Bauch
```

---

# Technical Constraints

- Use **React Functional Components**
- Use **React Hooks**
- Implement **debouncing manually**
- Avoid filtering the list on **every keystroke**
- Keep the solution **clean and reusable**

---

# React Concepts Expected

The interviewer expects candidates to demonstrate knowledge of:

- `useState`
- `useEffect`
- Debouncing logic
- Controlled inputs
- Filtering lists
- API handling
- Efficient UI updates

---

# Possible Follow-up Enhancements

Interviewers may ask candidates to extend the solution with:

1. Extract **debounce logic into a reusable custom hook (`useDebounce`)**.
2. Highlight the **matched search text** in results.
3. Add **API-based search instead of local filtering**.
4. Add **loading indicator while fetching data**.
5. Implement **pagination for large datasets**.

---

# Key Concept Being Tested

This problem evaluates the candidate's ability to:

- Fetch and render API data
- Implement **debouncing**
- Optimize UI updates
- Handle **user input efficiently**
- Write clean **React hook-based logic**
