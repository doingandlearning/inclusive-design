## ✅ Accessible Forms – Sample Snippets

---

### 1. **Explicit Label with Input (Minimal Example)**

```html
<form>
  <label for="username">Username</label>
  <input type="text" id="username" name="username">
</form>
```

✅ **Why it’s useful**: Great for showing the **minimum required** for screen reader-friendly form inputs.

---

### 2. **Visually Hidden Label with Placeholder**

```html
<form>
  <label for="search" class="visually-hidden">Search</label>
  <input type="search" id="search" name="search" placeholder="Search…">
</form>

<style>
.visually-hidden {
  position: absolute;
  width: 1px;
  height: 1px;
  margin: -1px;
  overflow: hidden;
  clip: rect(0, 0, 0, 0);
  white-space: nowrap;
  border: 0;
}
</style>
```

✅ **Why it’s useful**: Shows how to **keep visual design clean** while maintaining accessibility. Use this as a talking point around screen reader testing and placeholder misuse.

---

## ✅ Why It’s Best Practice

### 1. **Accessibility without Breaking Semantics**
The goal is to:
- Remove visual clutter for sighted users
- Retain important information for screen reader users

This allows content like labels, headings, or descriptions to:
- Stay part of the accessibility tree
- Be read aloud in screen readers
- Be focusable or referenced with ARIA (e.g., `aria-describedby`)

---

### 2. **Avoids `display: none` and `visibility: hidden`**
Those styles **completely remove elements from the accessibility tree**, which is not what we want if the content is meant to assist or describe something.

---

### 3. **Supports Reflow and Layout Stability**
It keeps the element technically in the DOM and **outside of layout flow** without disrupting other elements. This helps in responsive designs and in debugging.

---

## 🧪 Common Use Cases

- Hidden `<label>`s when a visual placeholder is used
- Descriptive text for form fields (e.g. ARIA references)
- Skip-to-content links for keyboard users
- Headings for screen reader-only navigation
- Tooltips or modals meant only for non-visual users

---

## 🧬 Canonical Version (used by GOV.UK, Bootstrap, etc.)

```css
.visually-hidden {
  position: absolute;
  width: 1px;
  height: 1px;
  padding: 0;
  margin: -1px;
  overflow: hidden;
  clip: rect(0, 0, 0, 0);
  white-space: nowrap;
  border: 0;
}
```

> ⚠️ This style does not remove the element from the DOM. It’s still focusable and screen reader-accessible — which is **exactly** what we want for accessibility support.

---

### 3. **Validation with ARIA Descriptions**

```html
<form>
  <label for="email">Email</label>
  <input
    type="email"
    id="email"
    name="email"
    required
    aria-describedby="email-help email-error"
  >
  <div id="email-help">We'll never share your email.</div>
  <div id="email-error" role="alert" style="color: red; display: none;">
    Please enter a valid email address.
  </div>
</form>
```

✅ **Why it’s useful**: Demonstrates how to use `aria-describedby` to link **both help and error messages** to a field, including a `role="alert"`.

---

### 4. **Inline Radio Group with Fieldset and Legend**

```html
<form>
  <fieldset>
    <legend>Preferred Contact Method</legend>

    <label>
      <input type="radio" name="contact" value="email"> Email
    </label>

    <label>
      <input type="radio" name="contact" value="phone"> Phone
    </label>
  </fieldset>
</form>
```

✅ **Why it’s useful**: Shows how to group related controls **semantically** and use a `<legend>` for better screen reader context.

---

### 5. **Bad Practice Comparison**

```html
<!-- ❌ Only uses placeholder -->
<form>
  <input type="text" placeholder="Your name">
</form>
```

✅ **Why it’s useful**: Quick demo of what **not** to do. Placeholder-only inputs offer no support to screen readers, break when cleared, and don’t help autofill.

---

### 6. **Keyboard-Focusable Custom Button (vs. `div`)**

```html
<!-- ✅ Good -->
<button type="submit">Send</button>

<!-- ❌ Bad -->
<div onclick="submitForm()">Send</div>
```

✅ **Why it’s useful**: A `<button>` gets keyboard focus, can be activated with Enter/Space, and is announced properly by screen readers — unlike a generic `<div>`.

---

### 7. **Accessible Inline Validation (ARIA + JavaScript)**

```html
<label for="username">Username</label>
<input
  type="text"
  id="username"
  name="username"
  aria-describedby="username-error"
  aria-invalid="true"
/>
<span id="username-error" role="alert" style="color: red;">
  Username is required and must be at least 3 characters.
</span>
```

✅ **Why it’s useful**: Combines `aria-describedby`, `aria-invalid`, and `role="alert"` for a robust, screen reader-friendly inline validation pattern.

---

### 8. **Toggle Button with ARIA State**

```html
<button
  aria-expanded="false"
  aria-controls="more-info"
  onclick="togglePanel(this)"
>
  Show more
</button>

<div id="more-info" hidden>
  This is additional content.
</div>

<script>
  function togglePanel(button) {
    const expanded = button.getAttribute("aria-expanded") === "true";
    button.setAttribute("aria-expanded", !expanded);
    document.getElementById("more-info").hidden = expanded;
  }
</script>
```

✅ **Why it’s useful**: Demonstrates an ARIA state (`aria-expanded`) that updates with user interaction. Screen readers will announce “collapsed” / “expanded” context.

---

### 9. **Skip Link for Keyboard Users**

```html
<a href="#main" class="visually-hidden focusable">Skip to main content</a>

<style>
.visually-hidden.focusable:focus {
  position: static;
  width: auto;
  height: auto;
  margin: 0;
  overflow: visible;
  clip: auto;
  white-space: normal;
}
</style>
```

✅ **Why it’s useful**: A real-world use case of `.visually-hidden`, enhanced with a `.focusable` modifier for skip-links.

---

### 10. **Descriptive Grouped Checkbox Fields**

```html
<fieldset>
  <legend>Select your interests</legend>

  <label>
    <input type="checkbox" name="interests" value="accessibility">
    Accessibility
  </label>

  <label>
    <input type="checkbox" name="interests" value="design">
    Design
  </label>

  <label>
    <input type="checkbox" name="interests" value="performance">
    Performance
  </label>
</fieldset>
```

✅ **Why it’s useful**: When multiple checkboxes relate to the same topic, grouping them in a `fieldset` with a `legend` helps users understand the relationship.
