---
# Question 19: Build a Multi-Step Form with Validation

## Problem Statement

Build a **Multi-Step Form** in React that divides a form into **three separate steps (tabs)**.

Users should be able to navigate through the steps and fill in the required information.

The **Submit button will only appear on the final step**, and submission should only be allowed if **all required fields from Step 1 and Step 2 are completed**.
---

# Requirements

## 1. Three-Step Form Layout

The form should contain **three steps** displayed as tabs.

Example UI:

```
[ Step 1 ]  [ Step 2 ]  [ Step 3 ]
```

Each step should display different form inputs.

Example:

```
Step 1 → Personal Information
Step 2 → Contact Details
Step 3 → Review & Submit
```

---

# 2. Step Navigation

Users should be able to navigate between steps using **Next** and **Previous** buttons.

Example:

```
Step 1
[ Next ]

Step 2
[ Previous ] [ Next ]

Step 3
[ Previous ] [ Submit ]
```

---

# 3. Required Field Validation

Certain fields in **Step 1 and Step 2** should be marked as **required**.

Example:

### Step 1 (Required Fields)

```
First Name *
Last Name *
```

### Step 2 (Required Fields)

```
Email *
Phone Number *
```

---

# 4. Submit Button Behavior

The **Submit button should appear only on Step 3**.

However, the form should only be submitted if:

- All **required fields in Step 1 are filled**
- All **required fields in Step 2 are filled**

If required fields are missing:

```
Submit should be disabled
OR
Show validation errors
```

---

# Example UI Flow

```
Step 1
----------------
First Name *
Last Name *
[ Next ]
```

```
Step 2
----------------
Email *
Phone *
[ Previous ] [ Next ]
```

```
Step 3
----------------
Review Information
[ Previous ] [ Submit ]
```

---

# Expected UI Behavior

1. The form should start at **Step 1**.
2. Users can move to the **next step** after filling required fields.
3. The **Submit button appears only in Step 3**.
4. Submission should only occur if **Step 1 and Step 2 validations pass**.
5. Users should be able to **navigate back to previous steps**.

---

# Example Form Data Structure

```javascript
const formData = {
  firstName: "",
  lastName: "",
  email: "",
  phone: "",
};
```

---

# Technical Constraints

- Use **React Functional Components**
- Use **React Hooks**
- Maintain form data using state
- Implement **basic validation logic**
- Prevent submission if required fields are missing

---

# React Concepts Expected

The interviewer expects candidates to demonstrate knowledge of:

- `useState`
- Controlled form inputs
- Conditional rendering
- Form validation
- Multi-step UI flows
- State management across steps

---

# Possible Follow-up Enhancements

Interviewers may extend this problem with:

1. Add **progress indicator for steps**.
2. Persist form state using **localStorage**.
3. Allow **direct navigation between tabs**.
4. Add **field-level validation messages**.
5. Implement **dynamic steps**.

---

# Key Concept Being Tested

This problem evaluates the candidate's ability to:

- Build **multi-step forms**
- Manage **form state across multiple components**
- Implement **form validation**
- Handle **conditional submission logic**
