# 7. Interactive Elements

Interactive elements include buttons, links, menus, sliders, and custom widgets that users interact with via mouse, touch, or keyboard. Designing these accessibly ensures a smoother experience for users with motor disabilities, screen reader users, and anyone relying on keyboard navigation.

## Why This Matters
- Many custom controls (e.g. JavaScript-based buttons or menus) are not keyboard accessible by default.
- Inaccessible interactive elements break the user journey — a single missing keyboard focus can prevent form submission or navigation.

## Core Principles

### 1. **Use Native HTML Elements When Possible**
- `<button>` is better than a clickable `<div>`.
- `<a href="...">` is better than `onclick` on a `<span>`.
- Native elements come with keyboard interaction and accessibility built-in.

### 2. **Ensure Keyboard Accessibility**
- All interactive components should be operable using `Tab`, `Enter`, and arrow keys.
- Use `tabindex="0"` to make custom elements focusable.
- Avoid `tabindex="-1"` unless managing focus manually.

### 3. **Provide Visual Focus Styles**
- Focus styles must be visible.
- Don’t remove outlines unless replacing them with a clear alternative (e.g. `outline: 2px solid #007acc`).

### 4. **Use ARIA When Necessary (but Prefer Native)**
- Use `role="button"` with `aria-pressed`, `aria-expanded`, etc., when creating custom controls.
- Remember to add `aria-disabled`, `aria-haspopup`, etc., to convey states.
- Avoid using ARIA to override native semantics.

### 5. **Manage State and Feedback**
- Ensure that screen readers are informed of state changes (e.g. "expanded", "selected").
- Use `aria-live` or update `aria-*` attributes dynamically when a user acts on a control.

## Common Mistakes
- Using `<div>` or `<span>` as buttons without keyboard events or role attributes.
- Forgetting to manage focus when showing/hiding content.
- Creating modals, tabs, or menus without announcing their roles or states.

## Tips
- Use the [Accessibility Object Model](https://developer.mozilla.org/en-US/docs/Web/API/Accessibility_Object_Model) for complex interactions.
- Test with keyboard alone: can you tab through and activate every control?
- Try your page with a screen reader (VoiceOver, NVDA, or Narrator).

