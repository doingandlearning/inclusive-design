## ✅ Sample ARIA Examples (Different from Labs)

---

### 🧩 1. **ARIA Accordion (Read-Only Sample)**

A simplified FAQ accordion that’s keyboard-expandable but doesn't use hidden content.

```html
<h2>FAQ</h2>
<div>
  <button aria-expanded="false" aria-controls="faq1" onclick="toggleFaq(this)">What is accessibility?</button>
  <p id="faq1" hidden>Accessibility means designing for everyone, including users with disabilities.</p>
</div>

<script>
function toggleFaq(btn) {
  const target = document.getElementById(btn.getAttribute("aria-controls"));
  const expanded = btn.getAttribute("aria-expanded") === "true";
  btn.setAttribute("aria-expanded", !expanded);
  target.hidden = expanded;
}
</script>
```

---

### 🔔 2. **ARIA Live Region – Notifications**

Minimal notification bar using `aria-live="assertive"` for high-priority alerts.

```html
<h2>System Status</h2>
<div>
  <button onclick="showAlert()">Trigger Alert</button>
  <div id="alert-region" aria-live="assertive" role="alert"></div>
</div>

<script>
function showAlert() {
  document.getElementById("alert-region").textContent = "Connection lost. Trying to reconnect…";
}
</script>
```

---

### ☑️ 3. **ARIA Checkbox (Read-Only Preview)**

Custom checkbox *disabled*, just to demonstrate states — doesn't need keyboard support.

```html
<h2>Preferences</h2>
<div role="checkbox" aria-checked="true" aria-disabled="true" tabindex="0" style="padding: 0.5rem; border: 1px solid #888;">
  Enable Dark Mode
</div>
```

---

### 🗺️ 4. **Landmark Roles with Multiple Navs**

Demonstrates distinct `aria-label`s for multiple `role="navigation"` elements.

```html
<header role="banner">
  <h1>My News Site</h1>
</header>

<nav role="navigation" aria-label="Main menu">
  <ul><li><a href="#">Home</a></li><li><a href="#">World</a></li></ul>
</nav>

<main role="main">
  <h2>Today's Headlines</h2>
  <p>Top stories updated every hour.</p>
</main>

<nav role="navigation" aria-label="Social links">
  <ul><li><a href="#">Twitter</a></li><li><a href="#">LinkedIn</a></li></ul>
</nav>
```

---

## 🧠 Purpose of These Samples

These are meant to be:
- **Reference examples** shown before or during teaching
- Clear and focused (not too interactive)
- Different in structure and complexity from labs
- Easily copy-pastable into browser/CodePen to demo concepts
