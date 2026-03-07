# React Machine Coding Interview Questions

This document contains **React machine coding questions** that were asked during technical interviews.  
Each problem includes the **problem statement, requirements, and expected behavior**.

---

# Question 1: Implement Infinite Scroll Using Intersection Observer

## Problem Statement

Build an **Infinite Scroll component in React** that loads additional data automatically when the user reaches the bottom of the list.

The implementation must use the **Intersection Observer API** instead of scroll event listeners.

The goal is to **detect when the last element becomes visible in the viewport** and trigger an API request to load more data.

---

## Requirements

1. Display a list of items fetched from an API.
2. Initially load the **first set of items** when the component mounts.
3. When the user scrolls and the **last item becomes visible in the viewport**, fetch the next set of items.
4. Newly fetched items should be **appended to the existing list**.
5. Continue loading data until the API has no more items.
6. Show a **loading indicator** while new data is being fetched.
7. Prevent **duplicate API calls** while a request is already in progress.

---

## Example API

Example API endpoint:

```
https://jsonplaceholder.typicode.com/posts?_limit=10&_page=1
```

Pagination parameters:

| Parameter | Description              |
| --------- | ------------------------ |
| `_limit`  | Number of items per page |
| `_page`   | Current page number      |

---

## Example Data Response

```json
[
  {
    "userId": 1,
    "id": 1,
    "title": "Post title",
    "body": "Post description"
  }
]
```

---

## Expected UI Behaviour

1. When the page loads, the **first set of items is displayed**.
2. As the user scrolls down, when the **last item becomes visible**, the next page should be fetched automatically.
3. The list should **grow continuously without refreshing the page**.
4. When there is **no more data**, the loading should stop.

---

## Visual Flow

```
Initial Load
     ↓
Display first 10 items
     ↓
User scrolls
     ↓
Last item enters viewport
     ↓
Intersection Observer triggers
     ↓
Fetch next page
     ↓
Append items to list
     ↓
Repeat until no more data
```

---

## Technical Constraints

- Use **React Functional Components**
- Use **React Hooks**
- Use **Intersection Observer API**
- Avoid using **scroll event listeners**
- Prevent unnecessary re-renders

---

## React Concepts Expected

The interviewer expects candidates to demonstrate knowledge of:

- `useState`
- `useEffect`
- `useRef`
- Intersection Observer API
- API calls
- State updates and list rendering
- Handling asynchronous operations

---

## Bonus Improvements (Follow-up Questions)

Interviewers may ask additional enhancements:

1. Add a **loader skeleton** while fetching data.
2. Implement **error handling** for failed API requests.
3. Add **debouncing or throttling** if needed.
4. Add a **"No more items" indicator** when data ends.
5. Implement **virtualization for performance** (optional advanced solution).

---

## Key Concept Being Tested

The primary concept being evaluated is the **efficient implementation of infinite scrolling using the Intersection Observer API instead of scroll event listeners**.
