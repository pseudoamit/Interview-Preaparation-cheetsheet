# Question 12: Fetch Data from Multiple APIs and Render Dynamic UI (List, Table, Cards)

## Problem Statement

Build a **React application** that fetches data from different APIs and renders the response in **different UI formats** depending on the type of data returned.

The application should use a **custom React hook** to fetch API data.

The same hook should support rendering the data in different UI layouts such as:

- List View
- Table View
- Card View

The UI should dynamically adapt depending on the **structure or type of response received from the API**.

---

# Requirements

1. Create a **custom React hook** responsible for fetching API data.

Example:

```javascript
const { data, loading, error } = useFetch(apiUrl);
```

2. The hook should handle:

- API requests
- Loading state
- Error handling
- Returning the fetched data
- **Handling race conditions when multiple API calls are triggered**

---

# Race Condition Requirement

Your API fetching logic must handle **race conditions**.

Race conditions can occur when:

- Multiple API requests are triggered rapidly
- A previous request resolves **after** a newer request
- The UI mistakenly renders **stale data**

Example Scenario:

```
User selects API A
Request A is sent

Before A finishes, user selects API B
Request B is sent

If Request A finishes AFTER Request B
→ UI should NOT render A's response
→ Only the latest request (B) should update the UI
```

The custom hook should ensure that:

- **Only the latest API response updates the state**
- Previous or outdated responses are ignored or cancelled

Possible approaches include:

- `AbortController`
- Request ID tracking
- Cleanup functions inside `useEffect`

---

# Scenario 1: Render Data as a List

If the API returns a **simple list of items**, the application should render them as a **list view**.

Example API Response:

```json
["Apple", "Banana", "Orange", "Grapes"]
```

Expected UI:

```
• Apple
• Banana
• Orange
• Grapes
```

---

# Scenario 2: Render Data in Table Format

If the API returns **structured objects**, the application should render the data in a **tabular format**.

Example API Response:

```json
[
  { "id": 1, "name": "John", "age": 25 },
  { "id": 2, "name": "Alice", "age": 28 },
  { "id": 3, "name": "Bob", "age": 30 }
]
```

Expected UI:

```
---------------------------------
| ID | Name  | Age              |
---------------------------------
| 1  | John  | 25               |
| 2  | Alice | 28               |
| 3  | Bob   | 30               |
---------------------------------
```

---

# Scenario 3: Render Data as Cards

If the API returns data suitable for a **card layout**, the application should display the data as **cards**.

Each row should display **a maximum of 3 cards**.

Example API Response:

```json
[
  { "title": "Product 1", "price": "$20" },
  { "title": "Product 2", "price": "$30" },
  { "title": "Product 3", "price": "$40" },
  { "title": "Product 4", "price": "$50" }
]
```

Expected UI:

```
[Card 1]   [Card 2]   [Card 3]

[Card 4]
```

Each card may contain information such as:

- Title
- Description
- Price
- Image

---

# Custom Hook Requirement

You must create a **reusable custom hook** to fetch API data.

Example structure:

```
hooks/
  useFetch.js
```

Example usage:

```javascript
const { data, loading, error } = useFetch(apiUrl);
```

The hook should manage:

- API request
- Loading state
- Error handling
- Returning the fetched data
- Preventing **race condition issues**

---

# Expected UI Behavior

1. When the component loads:
   - The API should be called using the **custom hook**.

2. While the data is being fetched:
   - A **loading indicator** should be displayed.

3. Once the data is received:
   - The UI should render the data according to its **format type**.

4. If the API request fails:
   - An **error message** should be displayed.

5. If multiple API calls occur:
   - Only the **latest response** should update the UI.

---

# Visual Flow

```
Component Loads
        ↓
Custom Hook calls API
        ↓
Loading State
        ↓
Data Received
        ↓
Determine Data Type
        ↓
Render UI

List → List View
Objects → Table View
Card Data → Card Layout
```

---

# Technical Constraints

- Use **React Functional Components**
- Use **React Hooks**
- Create a **custom hook for API fetching**
- Handle **race conditions**
- Ensure components are **reusable**
- Handle **loading and error states properly**

---

# React Concepts Expected

The interviewer expects candidates to demonstrate knowledge of:

- Custom Hooks
- `useState`
- `useEffect`
- API handling
- Race condition handling
- Conditional rendering
- Dynamic UI generation
- Component reusability

---

# Possible Follow-up Enhancements

Interviewers may ask candidates to extend the solution with:

1. Add **pagination support**.
2. Add **sorting functionality in table view**.
3. Add **responsive grid layout for cards**.
4. Add **loading skeletons** instead of a simple loader.
5. Add **API caching** inside the custom hook.

---

# Key Concept Being Tested

This problem evaluates the candidate's ability to:

- Create **reusable custom React hooks**
- Handle **race conditions in API requests**
- Handle **API-driven UI rendering**
- Build **dynamic UI layouts**
- Write **scalable component architecture**
