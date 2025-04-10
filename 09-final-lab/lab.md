## 🧪 Final Lab: Accessibility Fix-Up

### **Lab Idea:**  
Provide participants with a purposefully **inaccessible webpage** — one that visually looks fine but breaks multiple accessibility rules in HTML, CSS, and JavaScript.

### 🔍 Problems might include:
#### 💡 Design
- Poor colour contrast (text/background)
- Interactive elements with tiny touch targets
- Fonts in all caps or poor spacing
- Colour used as the only indicator (e.g. “red = error”)

#### 🧱 Markup
- No semantic structure (just `<div>`s and `<span>`s)
- Missing or incorrect `<label>` elements
- Inaccessible form validation (just coloured borders)
- Incorrect or overused ARIA roles

#### 🔄 Behaviour
- Keyboard traps
- JavaScript modals with no focus management
- Custom buttons/links that aren’t focusable or actionable by keyboard
- Live updates that aren’t announced to screen readers

---

## 🛠️ Learner Task

1. **Audit the Page**  
   - Use **keyboard navigation**, **screen reader testing**, and **Axe DevTools**
   - Make a checklist of accessibility violations

2. **Fix the Issues**  
   - Update **HTML**: Use semantic elements, proper form structure, valid ARIA roles only where needed  
   - Update **CSS**: Improve contrast, touch targets, focus styles, avoid inaccessible layouts  
   - Update **JavaScript**: Ensure keyboard access, add focus management, announce changes with ARIA

3. **Re-Test**  
   - Re-run the tools and screen reader check after fixes
   - Compare your accessibility score before/after

4. **Reflect and Share**  
   - What were the hardest problems to fix?
   - What would you change in your own code going forward?

---

## 🧩 Extras (Optional)
- You could give **one version per group**, each with different issues (e.g., one form-focused, one interaction-focused, one layout-focused).
- Bonus for teams who write their **own accessibility statement** for the fixed version.

---