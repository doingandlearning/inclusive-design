## ✅ Semantic HTML – Sample Snippets

---

### 1. **Basic Page Structure**

```html
<header>
  <h1>Inclusive Recipes</h1>
</header>

<nav>
  <ul>
    <li><a href="#">Home</a></li>
    <li><a href="#">Browse</a></li>
    <li><a href="#">Contact</a></li>
  </ul>
</nav>

<main>
  <section>
    <h2>Featured Recipes</h2>
    <div>
      <h3>Chickpea Stew</h3>
      <p>A hearty, vegan dish perfect for winter evenings.</p>
    </div>
  </section>
</main>

<footer>
  <p>&copy; 2025 Inclusive Recipes</p>
</footer>
```

✅ **Why it’s useful**: Clear demonstration of common semantic layout (`header`, `nav`, `main`, `section`, `article`, `footer`).

---

### 2. **Less Common Elements in Context**

```html
<article>
  <h2>Accessible Web Tips</h2>
  <p><mark>Tip:</mark> Use semantic HTML wherever possible.</p>

  <aside>
    <p><strong>Note:</strong> This article was first published in 2022.</p>
  </aside>

  <figure>
    <img src="https://picsum.photos/200/300" alt="Diagram showing keyboard navigation flow">
    <figcaption>Keyboard navigation structure for a menu.</figcaption>
  </figure>
</article>
```

✅ **Why it’s useful**: Shows how `mark`, `aside`, `figure`, and `figcaption` provide **additional meaning and context** to content.

---

### 3. **Unusually Useful Elements in Action**

```html
<details>
  <summary>What devices support screen readers?</summary>
  <p>Most modern operating systems have built-in screen readers: VoiceOver on Mac/iOS, NVDA on Windows, TalkBack on Android.</p>
</details>

<p>The next webinar is on <time datetime="2025-04-18T15:00">April 18th at 3pm</time>.</p>

<p>We follow <abbr title="Web Content Accessibility Guidelines">WCAG</abbr> standards.</p>

<address>
  Contact us at: <a href="mailto:info@example.com">info@example.com</a><br>
  123 Web Street, London, UK
</address>
```

✅ **Why it’s useful**: Introduces rarely used tags (`details`, `summary`, `time`, `abbr`, `address`) that offer strong **semantic clarity** with little visual disruption.

---

### 4. **“Bad Example” for Comparison**

```html
<div class="top">Welcome to our site</div>
<div class="menu">Home | About | Blog</div>
<div class="main-content">
  <div class="block">
    <h2>New Post</h2>
    <div>We just launched a new product!</div>
  </div>
</div>
<div class="bottom">Copyright 2025</div>
```

❌ **Why it’s useful**: This “div soup” can spark a great discussion. It looks fine visually, but **offers no structure or meaning** for screen readers, search engines, or assistive tech.

---
