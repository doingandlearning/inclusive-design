# Lab: Enhancing Accessibility with ARIA

## 🧠 Objective
Practice using **ARIA attributes** to improve the accessibility of custom components and dynamic content.

## 🛠 Instructions
Create or enhance the following examples with appropriate ARIA attributes. You may start from scratch or use basic HTML scaffolds.

---

### 1. **Custom Accordion with ARIA**

#### Requirements:
- A toggle button that expands/collapses a hidden panel.
- Use `aria-expanded` and `aria-controls` on the button.
- Use `hidden` attribute for progressive enhancement.

#### Bonus:
- Add keyboard support: Space/Enter toggles, Escape collapses.

---

### 2. **Live Region for Status Updates**

#### Requirements:
- A text input for email and a "Check availability" button.
- Simulate checking (e.g. timeout) and display result in a `<div>`.
- Use `aria-live="polite"` or `aria-live="assertive"` depending on urgency.

#### Bonus:
- Add a loading message that appears while checking.

---

### 3. **Custom Checkbox with ARIA**

#### Requirements:
- Create a `<div>` that looks and behaves like a checkbox.
- Add `role="checkbox"`, `aria-checked`, and manage states via JavaScript.
- Make it keyboard accessible (`Tab`, `Space` to toggle).

---

### 4. **Landmark Navigation**

#### Requirements:
- Create a page with header, main, navigation, and footer.
- Use **ARIA landmark roles** where HTML5 elements aren't used (e.g. `role="main"`, `role="navigation"`).

#### Bonus:
- Add `aria-label` to landmarks to distinguish multiple regions (e.g. two navs).

---

## 🔎 Tips
- Use browser DevTools to inspect ARIA roles and states.
- Test with a screen reader (or screen reader simulation tools).
- Keyboard navigation is critical — ARIA alone won’t manage focus.

---

## ✅ Deliverables
- A set of small HTML files demonstrating:
  - A working accordion
  - A live region example
  - A custom checkbox
  - Page landmarks

Upload or demo your solutions and explain **how ARIA improved the experience**.