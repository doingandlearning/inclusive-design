# Lab: Creating an Accessible Form

## Objective
Participants will create an **accessible HTML form** using best practices for form labels, validation, and usability.

## Instructions

### 1. **Create a New HTML File**
Start by creating an HTML file (`accessible-form.html`).

### 2. **Include the Following Fields**
Your form should include:
- **Full Name** (`text` input)
- **Email Address** (`email` input)
- **Phone Number** (`tel` input)
- **Password** (`password` input)
- **Confirm Password** (`password` input)
- **Date of Birth** (`date` input)
- **Country** (`select` dropdown with at least 3 options)
- **Newsletter Subscription** (`checkbox` input)
- **Submit Button**

### 3. **Ensure Proper Labeling**
- Use **explicit labels** with the `for` attribute.
- Do **not** rely solely on placeholders for field names.

Example:
```html
<label for="full-name">Full Name:</label>
<input type="text" id="full-name" name="full-name" required>
```

### 4. **Implement Accessible Validation**
- Use HTML5 validation attributes (`required`, `pattern`, `minlength`, etc.).
- Provide **clear error messages** (not just color changes).
- Use ARIA attributes for additional accessibility.

Example:
```html
<input type="email" id="email" name="email" required aria-describedby="email-error">
<span id="email-error" role="alert">Please enter a valid email address.</span>
```

### 5. **Test Your Form**
- Use **keyboard navigation** (Tab key) to move through fields.
- Test with **screen readers**.
- Check form validation and error messages.

### 6. **Bonus: Add Fieldset and Legend**
Wrap related fields (like password inputs) inside a `<fieldset>` with a `<legend>` for better grouping.

Example:
```html
<fieldset>
  <legend>Account Information</legend>
  <label for="password">Password:</label>
  <input type="password" id="password" name="password" required>
</fieldset>
```

## Deliverable
Once complete, share your HTML file or a live demo link with the group for feedback!