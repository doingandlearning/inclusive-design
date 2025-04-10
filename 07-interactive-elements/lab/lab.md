## 🧪 Observational Lab: Real-World Interactive Accessibility

### 🎯 Objective  
Build your *critical eye* by identifying how well (or poorly) real websites implement accessible interactive elements — **without writing code**.

---

### 🗺️ Instructions

1. **Choose a website** to audit:  
   - You can pick from the list below or choose one you visit regularly.
   - Prefer sites with menus, tabs, modals, accordions, or form elements.

2. **Explore with your keyboard**  
   - Use `Tab`, `Enter`, `Esc`, and arrow keys to navigate.
   - Can you **access every interactive element**?
   - Is the **focus visible**?

3. **Check accessibility with browser tools**
   - Use DevTools (Elements → Accessibility tree)
   - Are interactive roles and states present (e.g. `aria-expanded`, `role="button"` on non-buttons)?

4. **Take notes on what’s working and what’s not**
   - Good example: Native `<button>` with `aria-expanded`, focus styles, toggles a panel.
   - Bad example: Clickable `<div>` with no focus style or keyboard support.

5. (Optional) **Try a screen reader**  
   - Even a quick test with macOS VoiceOver or NVDA is eye-opening.

---

### 🔍 Things to Look For

| ✅ Good Practices | ❌ Bad Practices |
|------------------|-----------------|
| Native `<button>` and `<a>` elements | Clickable `<div>` with no `tabindex` or `role` |
| Clear visual focus indicators | Focus ring removed or invisible |
| ARIA state attributes (like `aria-expanded`) | No feedback for state changes |
| Keyboard accessibility (`Tab`, `Enter`, `Esc`) | Requires mouse or touchscreen only |

---

### 🌐 Suggested Sites to Explore

| Site | Why It’s Interesting |
|------|----------------------|
| [GOV.UK](https://www.gov.uk) | Consistently accessible layout and navigation using semantic HTML. |
| [Apple](https://www.apple.com) | Slick UI — test if styling comes at the cost of accessibility. |
| [Medium](https://www.medium.com) | Interactive components like menus and tooltips worth inspecting. |
| [Booking.com](https://www.booking.com) | Complex forms and calendars — great for testing keyboard access. |
| [GitHub](https://github.com) | Keyboard-friendly UI with clear focus states; lots of live regions. |
| [The Guardian](https://www.theguardian.com) | Rich content layout, dynamic sections, and good ARIA usage. |
| [BBC News](https://www.bbc.co.uk/news) | Public broadcaster — generally solid accessibility practices. |
| [Stack Overflow](https://stackoverflow.com) | Great test case for modals, focus traps, and alert regions. |
| [Target](https://www.target.com) | Previously involved in a major accessibility lawsuit — look at improvements. |
| [Coursera](https://www.coursera.org) | Educational platform with video, quizzes, tabs, and menus. |
| [Can I Use](https://caniuse.com) | Simple, data-heavy site with toggleable panels and filters. |


---

### ✍️ Deliverable

Write up (or share aloud):
- **One good example** and why it worked well.
- **One bad example** and how it could be improved.

You can even paste a snippet or screenshot if it helps.
