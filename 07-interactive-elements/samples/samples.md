## ✅ Sample Snippets for Interactive Elements

---

### 1. ✅ **Use Native Elements**

```html
<!-- ✅ Native button -->
<button type="button">Submit</button>

<!-- ❌ Don’t do this -->
<div onclick="submitForm()">Submit</div>
```

> ✅ Use native HTML elements whenever possible — they’re focusable, keyboard accessible, and screen reader friendly by default.

---

### 2. 🔀 **Keyboard Accessible Custom Control**

```html
<div
  role="button"
  tabindex="0"
  aria-pressed="false"
  onclick="toggle(this)"
  onkeydown="if(event.key === 'Enter' || event.key === ' ') toggle(this)"
>
  Toggle setting
</div>

<script>
function toggle(el) {
  const isPressed = el.getAttribute("aria-pressed") === "true";
  el.setAttribute("aria-pressed", !isPressed);
}
</script>
```

> ✅ Shows how to make a custom control that is focusable, toggleable, and screen reader friendly.

---

### 3. 🔍 **Focusable Custom Element with Visible Focus**

```html
<style>
.custom-link {
  display: inline-block;
  padding: 0.5rem;
  border: 2px solid transparent;
}
.custom-link:focus {
  border-color: #00f;
  outline: none;
}
</style>

<a href="#" class="custom-link">Learn more</a>
```

> ✅ Emphasises styling focus in a way that is visible and consistent with brand design.

---

### 4. 📣 **Live Region for Dynamic Feedback**

```html
<p>
  <button onclick="announce()">Check for updates</button>
</p>

<div id="status" role="status" aria-live="polite"></div>

<script>
function announce() {
  document.getElementById("status").textContent = "You are up to date.";
}
</script>
```

> ✅ This provides feedback for screen readers without needing manual focus. Use for non-critical notifications.

---

### 5. 🗂 **Custom Tab Interface with ARIA**

```html
<div role="tablist">
  <button role="tab" aria-selected="true" aria-controls="panel1" id="tab1">Overview</button>
  <button role="tab" aria-selected="false" aria-controls="panel2" id="tab2">Details</button>
</div>

<div role="tabpanel" id="panel1" aria-labelledby="tab1">Content for Overview</div>
<div role="tabpanel" id="panel2" aria-labelledby="tab2" hidden>Content for Details</div>
```

> ✅ Good for advanced examples — can show how roles, labels, and keyboard interaction work together in components like tabs or accordions.
