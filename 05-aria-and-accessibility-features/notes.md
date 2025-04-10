# ARIA and Accessibility Features – Notes

## 💡 What is ARIA?
**ARIA** stands for **Accessible Rich Internet Applications**. It's a set of HTML attributes that:
- Describe the **roles**, **states**, and **properties** of UI elements.
- Enhance accessibility when native HTML falls short.

> ARIA doesn’t make inaccessible things accessible. It makes custom elements understandable to assistive tech.

---

## 🔧 When to Use ARIA (and When Not To)

### ✅ Use ARIA when:
- You’re building **custom interactive widgets** (e.g. tabs, modals, sliders) that don’t exist in native HTML.
- You want to expose **state information** (e.g. `aria-expanded`, `aria-checked`).
- You need to define **landmarks** for assistive tech (e.g. `role="navigation"`).

### ❌ Avoid ARIA when:
- **Native HTML** already does the job (e.g. use `<button>` instead of `role="button"`).
- You're using ARIA without understanding its **impact on keyboard and screen reader users**.

> Rule of thumb: **First use semantic HTML**, then ARIA **only if you have to**.

---

## 🔑 Key ARIA Roles and Attributes

### 🔹 Landmarks
- `role="navigation"`, `role="banner"`, `role="main"`, `role="complementary"`
- Helps screen reader users skip to key areas.

### 🔹 States & Properties
- `aria-expanded="true|false"`: For dropdowns, collapsible sections.
- `aria-checked="true|false"`: For custom checkboxes/switches.
- `aria-disabled="true"`: Marks a control as visually disabled.
- `aria-hidden="true"`: Hides content from screen readers (use with caution).

### 🔹 Widgets
- `role="tablist"`, `role="tab"`, `role="tabpanel"`
- `role="dialog"`, `role="alert"`, `role="tooltip"`

---

## 💬 Examples

### 1. **Custom Accordion**
```html
<button aria-expanded="false" aria-controls="section1" id="toggle1">
  Show details
</button>
<div id="section1" hidden>
  ...content...
</div>
```

### 2. **Live Region for Updates**
```html
<div aria-live="polite" id="announcement">
  New message received.
</div>
```

> Live regions help announce dynamic content changes (e.g. chat apps, form errors).

---

## 🧪 Testing ARIA Features
- **Use a screen reader** (VoiceOver, NVDA) to confirm the ARIA behaviour.
- Inspect ARIA attributes using **browser DevTools Accessibility pane**.
- Don’t forget to **test keyboard navigation** — ARIA can describe but not fix focus!

---

## 🛠 Best Practices
- Prefer native HTML.
- Use ARIA landmarks and roles to **enhance clarity**, not patch poor structure.
- Test regularly with assistive tech.
- Avoid `aria-hidden` unless absolutely necessary.
- Don't apply ARIA roles to elements that already have semantics (e.g. `role="button"` on `<button>` is redundant).

---

## 🔗 Further Reading
- [ARIA in HTML – web.dev](https://web.dev/learn/accessibility/aria-html)
- [MDN ARIA Guide](https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA)
- [WAI ARIA Authoring Practices](https://www.w3.org/WAI/ARIA/apg/)
- [Can I Use ARIA](https://caniuse.com/?search=aria)

---

