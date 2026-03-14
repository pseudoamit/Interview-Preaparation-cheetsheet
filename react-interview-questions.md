# 1. Must-Know React Fundamentals

1. What is React and why is it used?
2. What is a Single Page Application (SPA)?
3. What is a Multi-Page Application (MPA)?
4. What are controlled components and uncontrolled components?
5. What is the React component lifecycle?
6. What is React Fiber?
7. What are the Render Phase and Commit Phase in React?
8. Why do we need a unique key in lists?
9. What problems occur if keys are not unique?
10. What are React Hooks?
11. What are the most commonly used React hooks?
12. What is a custom hook?
13. How does React differentiate a custom hook from a normal function?
14. What is React Strict Mode?
15. Why does `useEffect` run twice in Strict Mode in development?
16. Why can an infinite loop occur inside `useEffect`?
17. What is automatic batching in React?
18. What are controlled vs uncontrolled form elements?
19. What is component-driven development?

---

# 2. React Hooks (Core + Advanced)

1. What is `useState` and how does it work?
2. What is `useEffect` and when should it be used?
3. What is `useLayoutEffect` and how is it different from `useEffect`?
4. When should you use `useLayoutEffect`?
5. What is `useRef` and when should it be used?
6. What is `useReducer`?
7. When should you use `useReducer` instead of `useState`?
8. How do you implement `useReducer`?
9. What is `useMemo`?
10. When should `useMemo` be used?
11. What is `useCallback`?
12. What is the difference between `useMemo` and `useCallback`?
13. What is `useTransition`?
14. When should `useTransition` be used?
15. What is `useImperativeHandle`?
16. When should `useImperativeHandle` be used?
17. What is the difference between controlled rendering and concurrent rendering?
18. What is `useId`?

---

# 3. State Management (Redux, Context)

1. What is Redux?
2. What problem does Redux solve?
3. What are the core principles of Redux?
4. What is the Redux architecture flow?
5. What is the difference between Redux and Context API?
6. When should you use Context API?
7. When should you use Redux?
8. What is Redux middleware?
9. Why do we need middleware in Redux?
10. How does Redux handle asynchronous actions?
11. What is Redux Thunk?
12. What is Redux Saga?
13. What is the performance issue with `useSelector`?
14. How can you optimize performance when using `useSelector`?

---

# 4. Performance Optimization

1. How do you identify performance issues in a React application?
2. What is React Profiler?
3. How do you detect unnecessary component re-renders?
4. How can you prevent unnecessary re-renders?
5. What are common React performance optimization techniques?
6. What is memoization?
7. How does `React.memo` work?
8. What is debouncing?
9. What is throttling?
10. How do you implement debounce in React?
11. How do you implement throttle in React?
12. What are Web Vitals?
13. How do you measure and improve Core Web Vitals?
14. How can you analyze and reduce bundle size?
15. What is tree shaking?

---

# 5. Code Splitting & Loading Strategies

1. What is code splitting?
2. What is lazy loading?
3. What is the difference between code splitting and lazy loading?
4. What is route-based lazy loading?
5. What is `React.lazy`?
6. What is `Suspense`?
7. What is preload?
8. What is prefetch?
9. What are resource hints?
10. How do you implement prefetch and preload?

---

# 6. React Router

1. What is BrowserRouter?
2. How does routing work in React Router v6+?
3. How do you create nested routes?
4. What is a protected route?
5. How do you implement a protected route?

---

# 7. Rendering Strategies

1. What is Client-Side Rendering (CSR)?
2. What is Server-Side Rendering (SSR)?
3. What is Static Site Generation (SSG)?
4. What is Incremental Static Regeneration (ISR)?
5. What is ISG?
6. What are Server Components?
7. What are Client Components?
8. What is hydration?
9. What is a hydration error?

---

# 8. React 18 & React 19 Features

1. What are the new features introduced in React 18?
2. What are the new features introduced in React 19?
3. What is Concurrent Rendering?
4. What is automatic batching?
5. What is streaming SSR?
6. What are server actions?

---

# 9. Caching & Data Fetching

1. What are different HTTP caching strategies?
2. What is client-side caching?
3. What is server-side caching?
4. What is SWR (stale-while-revalidate)?
5. What is React Query?
6. How does React Query manage caching?
7. How do you use React Query for data fetching?

---

# 10. Browser Internals & JavaScript Concepts

1. What are microtasks and macrotasks?
2. When does the browser render during the event loop?
3. What is a race condition?
4. What is AbortController?
5. What are Web Workers?
6. How do Web Workers work?
7. What is WebSocket?
8. How does WebSocket communication work?

---

# 11. Security in React Applications

1. What are common security risks in React applications?
2. How can you protect a React application from XSS attacks?
3. What is CSRF?
4. What is a CSRF token?
5. How do you implement CSRF protection?
6. How do you secure API communication?

---

# 12. Architecture & System Design

1. What is Micro Frontend Architecture?
2. Why use Micro Frontends?
3. What is a host application?
4. What is a remote application?
5. Can a remote application run standalone?
6. What is Module Federation?
7. Why is Module Federation used?
8. How do you share components between micro frontends?
9. How do you share global state between micro frontends?
10. How do you pass data between micro frontends?
11. What happens if micro frontends use different React versions?
12. How do you enforce the same React version across applications?
13. How does the browser know multiple micro frontends are running?

---

# 13. Build Tools & Infrastructure

1. What is Webpack?
2. What is a bundler?
3. What are build tools?
4. Why do we need build tools in modern web development?
5. What is Vite?
6. What is Babel?
7. What is tree shaking in bundlers?

---

# 14. Service Workers & PWA

1. What is a Progressive Web App (PWA)?
2. What is a Service Worker?
3. How does a Service Worker work?
4. What are offline caching strategies in PWAs?

---

# 15. Debugging & Production Issues

1. What is a memory leak in React?
2. How do memory leaks happen?
3. How do you detect memory leaks in production?
4. How do you debug production issues in React?

---

# 16. Testing React Applications

1. What testing libraries have you used in React?
2. What is React Testing Library?
3. What is the difference between `getBy`, `queryBy`, and `findBy`?
4. What is the difference between `jest.fn()` and `jest.spyOn()`?
5. Why do we use `waitFor` in tests?
6. How do you test a component that receives props?
7. How do you mock an API response in React tests?

---

# 17. Real-Time Data & Communication

1. How do you implement real-time data updates in React?
2. How do you sync real-time data across multiple browser tabs?
3. What technologies can be used for real-time updates?

---

# 18. Backend for Frontend (BFF)

1. What is the Backend for Frontend (BFF) pattern?
2. Why is BFF used in frontend architectures?
3. How does BFF improve security and performance?

## 19. React Design Pattern – Compound Component Pattern

Design a **Compound Component Pattern** in React.

The Compound Component Pattern allows multiple related components to **share implicit state and behavior** through a parent component, while giving consumers a **flexible and declarative API**.

### Problem Statement

Create a component system for a **Dropdown** using the Compound Component Pattern.

The API should look like this:

```jsx
<Dropdown>
  <Dropdown.Trigger>Open Menu</Dropdown.Trigger>

  <Dropdown.Menu>
    <Dropdown.Item>Profile</Dropdown.Item>
    <Dropdown.Item>Settings</Dropdown.Item>
    <Dropdown.Item>Logout</Dropdown.Item>
  </Dropdown.Menu>
</Dropdown>
```

### Requirements

- `Dropdown` should manage the **open / close state** internally.
- `Dropdown.Trigger` should **toggle the dropdown menu**.
- `Dropdown.Menu` should render its children **only when the dropdown is open**.
- `Dropdown.Item` should represent **individual menu items**.
- All child components should **share state from the parent component**.

### Expected Behavior

1. Initially the menu should be **closed**.
2. Clicking **Trigger** should open the menu.
3. Clicking **Trigger again** should close the menu.
4. Menu items should only be visible when the dropdown is open.

### Example Usage

```jsx
function App() {
  return (
    <Dropdown>
      <Dropdown.Trigger>Open Menu</Dropdown.Trigger>

      <Dropdown.Menu>
        <Dropdown.Item>Profile</Dropdown.Item>
        <Dropdown.Item>Settings</Dropdown.Item>
        <Dropdown.Item>Logout</Dropdown.Item>
      </Dropdown.Menu>
    </Dropdown>
  );
}
```

### Expected UI Behavior

```
Initial State:
[Open Menu]

After Click:
[Open Menu]

Profile
Settings
Logout
```
