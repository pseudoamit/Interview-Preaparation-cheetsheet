# Question 5: Build a Configurable Countdown Timer

## Problem Statement

Build a **Countdown Timer component in React** that starts from a **specific initial number** and **counts down to zero**.

The starting number should be **configurable**, meaning the timer may start from values like:

- 60
- 55
- 58
- Any other positive number

The timer should **decrease by 1 every second** until it reaches **0**.

Once the counter reaches **0**, it should **automatically stop**, and no further increment or decrement should occur.

---

## Requirements

1. The counter should **start from a configurable initial value**.
2. The counter should **decrement automatically every second**.

Example:

```
60 → 59 → 58 → 57 → ...
```

3. Provide controls for the timer:
   - **Start**
   - **Pause**
   - **Reset**

---

## Start Behaviour

- When the **Start button** is clicked, the countdown begins.
- The value should **decrease by 1 every second**.

Example:

```
Initial value: 60

Start clicked

60 → 59 → 58 → 57
```

---

## Pause Behaviour

- When **Pause** is clicked, the timer should **stop decreasing**.
- The value should remain at the **current number**.

Example:

```
Current value: 45

Pause clicked

Counter stays at: 45
```

If the user clicks **Start again**, the timer should **resume from the paused value**.

---

## Reset Behaviour

- When **Reset** is clicked:
  - The timer should **stop**
  - The value should return to the **initial starting value**

Example:

```
Initial value: 60

Current value: 32

Reset clicked

Counter becomes: 60
```

---

## Zero Condition

When the timer reaches **0**:

- The timer should **automatically stop**
- No further decrement should occur

Example:

```
3 → 2 → 1 → 0

Timer stops
```

---

## Expected UI Example

```
Countdown Timer: 60

[ Start ]   [ Pause ]   [ Reset ]
```

Running state:

```
Countdown Timer: 34
```

---

## Visual Flow

```
Initial State
Counter = 60

Start Clicked
↓
Counter decreases every second

Pause Clicked
↓
Counter stops at current value

Start Clicked Again
↓
Counter resumes

Counter reaches 0
↓
Timer automatically stops
```

---

## Technical Constraints

- Use **React Functional Components**
- Use **React Hooks**
- Ensure **intervals are properly cleared**
- Avoid **multiple intervals running simultaneously**

---

## React Concepts Expected

The interviewer expects candidates to demonstrate knowledge of:

- `useState`
- `useEffect`
- `useRef`
- `setInterval` and `clearInterval`
- Managing timers in React

---

## Possible Follow-up Enhancements

Interviewers may ask additional improvements such as:

1. Allow the user to **enter the starting number dynamically**.
2. Display the timer in **MM:SS format**.
3. Add an **alert when the timer reaches zero**.
4. Disable **Start button when the timer reaches zero**.
5. Add **sound notification on completion**.

---

## Key Concept Being Tested

This problem evaluates the candidate's ability to:

- Implement a **countdown timer**
- Manage **timer lifecycle in React**
- Handle **pause, resume, and reset functionality**
- Properly stop execution when a **terminal condition (0) is reached**
