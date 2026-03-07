---

# Question 4: Build a Counter with Start, Pause, and Reset Controls

## Problem Statement

Build a **Counter component in React** that can be controlled using three buttons:

- Start
- Pause
- Reset

The counter should **increment automatically at a fixed interval (every second)** when started.

The key requirement is that the **counter should resume from the same value after being paused**, instead of restarting from zero.

---

## Requirements

1. Display a **counter value** on the screen.
2. Initially, the counter value should be **0**.
3. Provide three buttons:
   - **Start**
   - **Pause**
   - **Reset**

### Start Button

- When the user clicks **Start**, the counter should begin incrementing:

```
1 → 2 → 3 → 4 → ...
```

- The counter should increment **every second**.

---

### Pause Button

- When the user clicks **Pause**, the counter should **stop incrementing**.
- The current counter value should **remain unchanged**.

Example:

```
Counter running:
1 → 2 → 3 → 4

Pause clicked

Counter stops at: 4
```

---

### Resume Behavior

If the user clicks **Start again after pausing**, the counter should **resume from the paused value**, not restart from zero.

Example:

```
Counter paused at: 4

Start clicked again

Counter continues:
5 → 6 → 7
```

---

### Reset Button

- When the user clicks **Reset**, the counter should:
  - Stop the timer
  - Reset the value to **0**

Example:

```
Counter: 7

Reset clicked

Counter becomes:
0
```

---

## Expected UI Example

```
Counter: 0

[ Start ]   [ Pause ]   [ Reset ]
```

While running:

```
Counter: 5
```

---

## Visual Flow

```
Initial State
Counter = 0

Start Clicked
↓
Counter increments every second

Pause Clicked
↓
Counter stops at current value

Start Clicked Again
↓
Counter resumes from previous value

Reset Clicked
↓
Counter becomes 0
Timer stops
```

---

## Technical Constraints

- Use **React Functional Components**
- Use **React Hooks**
- Avoid creating multiple intervals accidentally
- Ensure proper **cleanup of timers**

---

## React Concepts Expected

The interviewer expects candidates to demonstrate knowledge of:

- `useState`
- `useEffect`
- `useRef` (recommended for interval management)
- Timer functions (`setInterval`, `clearInterval`)
- Managing component lifecycle

---

## Possible Follow-up Enhancements

Interviewers may ask additional improvements such as:

1. Allow the user to **configure the interval duration**.
2. Add a **maximum counter limit**.
3. Disable **Start button when already running**.
4. Display **formatted time (HH:MM:SS)** instead of numbers.
5. Convert the counter into a **countdown timer**.

---

## Key Concept Being Tested

This problem evaluates the candidate's ability to:

- Manage **timers and intervals in React**
- Control **state transitions**
- Handle **pause and resume behavior correctly**
- Prevent **memory leaks by cleaning up intervals**
