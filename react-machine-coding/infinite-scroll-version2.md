---
# Question 2: Implement Infinite Data Loading (Row-by-Row API Fetch)

## Problem Statement

Build a React component that **continuously fetches and displays records from an API as the user scrolls**.

The API initially returns **10 records**, and once the **last record is rendered on the screen**, the application should automatically **request the next record from the API**.

This process should continue **until the API stops returning data**.

The goal is to create a **progressive data loading system** that dynamically loads records as the user reaches the bottom of the list.
---

## Requirements

1. When the component loads, fetch the **first 10 records** from the API.
2. Render the records in a **list format** on the screen.
3. Detect when the **last rendered record becomes visible in the viewport**.
4. When the last record is visible:
   - Fetch the **next record(s)** from the API.
5. Append the newly fetched data to the **existing list without refreshing the page**.
6. Continue fetching data until the **API stops returning new records**.
7. Prevent **duplicate API calls while a request is already in progress**.
8. Show a **loading indicator while fetching additional data**.

---

## Example API Behavior

Initial request:

```
GET /api/data?limit=10
```

Response:

```json
[
  { "id": 1, "name": "Item 1" },
  { "id": 2, "name": "Item 2" },
  ...
  { "id": 10, "name": "Item 10" }
]
```

When the **10th item becomes visible**, the application should fetch the next data.

Example:

```
GET /api/data?offset=10
```

Response:

```json
{ "id": 11, "name": "Item 11" }
```

Then:

```
GET /api/data?offset=11
```

Response:

```json
{ "id": 12, "name": "Item 12" }
```

And so on.

---

## Expected UI Behaviour

1. The UI initially shows **10 records**.
2. When the user scrolls to the bottom and the **last item becomes visible**, the application should fetch the next item.
3. The list should **keep growing dynamically**.
4. The process should stop when the API returns **no more records**.

---

## Visual Flow

```
Initial Load
     ↓
Fetch first 10 items
     ↓
Render items on screen
     ↓
User scrolls down
     ↓
Last item becomes visible
     ↓
Trigger API request
     ↓
Fetch next item
     ↓
Append to list
     ↓
Repeat until API returns no data
```

---

## Technical Constraints

- Use **React Functional Components**
- Use **React Hooks**
- Use **Intersection Observer API** to detect the last visible element
- Avoid using **scroll event listeners**
- Prevent **multiple simultaneous API calls**

---

## React Concepts Expected

The interviewer expects candidates to demonstrate knowledge of:

- `useState`
- `useEffect`
- `useRef`
- Intersection Observer API
- Pagination / incremental API loading
- Efficient list rendering
- Handling asynchronous operations

---

## Possible Follow-up Enhancements

Interviewers may ask candidates to extend the solution with:

1. Add a **loading spinner** when fetching new data.
2. Handle **API failure scenarios**.
3. Implement **retry logic** if API fails.
4. Add a **"No more records available"** indicator.
5. Optimize performance using **React memoization techniques**.

---

## Key Concept Being Tested

This problem tests the candidate's ability to:

- Implement **dynamic data loading**
- Handle **incremental API pagination**
- Efficiently detect **viewport visibility using Intersection Observer**
- Manage **state updates and asynchronous API calls in React**
