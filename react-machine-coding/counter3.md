# Question 6: Build a Cyclic Counter (1 to 10 Loop)

## Problem Statement

Build a **React Counter component** that automatically increments numbers starting from **1 up to 10**.

Once the counter reaches **10**, it should **restart from 1 again** and continue the cycle.

This means the counter will **loop continuously between 1 and 10**.

Example sequence:

```
1 → 2 → 3 → 4 → 5 → 6 → 7 → 8 → 9 → 10
↓
Restart
↓
1 → 2 → 3 → ...
```

---

## Requirements

1. The counter should start from **1**.
2. The counter should **increment automatically every second**.
3. The counter should continue increasing until it reaches **10**.
4. When the counter reaches **10**, the next value should reset to **1**.
5. The cycle should **continue indefinitely**.

---

## Example Behavior

Initial state:

```
Counter: 1
```

Running sequence:

```
1
2
3
4
5
6
7
8
9
10
1
2
3
...
```

---

## Expected UI Example

```
Counter: 1
```

The number should update automatically every second.

---

## Visual Flow

```
Start Counter
      ↓
1 → 2 → 3 → 4 → 5 → 6 → 7 → 8 → 9 → 10
      ↓
Reset to 1
      ↓
Repeat cycle
```

---

## Technical Constraints

- Use **React Functional Components**
- Use **React Hooks**
- Use a timer (`setInterval`) to increment values
- Ensure proper **cleanup of intervals**

---

## React Concepts Expected

The interviewer expects candidates to demonstrate knowledge of:

- `useState`
- `useEffect`
- `setInterval` and `clearInterval`
- State updates inside intervals
- Handling cyclic logic in state updates

---

## Possible Follow-up Enhancements

Interviewers may ask additional improvements such as:

1. Add **Start / Pause controls**.
2. Allow the **maximum number to be configurable** instead of fixed at 10.
3. Allow the user to configure the **timer interval**.
4. Add **reverse counting mode (10 → 1)**.
5. Display the counter as a **progress indicator**.

---

## Key Concept Being Tested

This problem evaluates the candidate's ability to:

- Implement **state-based cyclic logic**
- Manage **timers in React**
- Handle **state updates within asynchronous intervals**
