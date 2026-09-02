# blog-preview-card
This is a solution for the Blog preview card challenge on Frontend Mentor.

## Table of contents

- [blog-preview-card](#blog-preview-card)
  - [Table of contents](#table-of-contents)
  - [Overview](#overview)
    - [The challenge](#the-challenge)
    - [Screenshot](#screenshot)
    - [Links](#links)
  - [My process](#my-process)
    - [Built with](#built-with)
    - [What I learned](#what-i-learned)
    - [Continued development](#continued-development)
    - [Useful resources](#useful-resources)
  - [Author](#author)

## Overview

### The challenge

Users should be able to:
- See hover and focus states for all interactive elements on the page

### Screenshot

![](./screenshot.png)

### Links

- Solution URL: [rizanne-f/blog-preview-card](https://github.com/rizanne-f/blog-preview-card)
- Live Site URL: [rizanne-f.github.io/blog-preview-card/](https://rizanne-f.github.io/blog-preview-card)

## My process

### Built with

- Semantic HTML5 markup
- CSS custom properties
- Flexbox
- Mobile-first workflow

### What I learned

We can take advantage of Flexbox to set the gap between elements instead of using margin-bottom multiple times in different selectors.
```html
<article class="blog-preview">
    <img src="..." alt="..." class="preview-image">
    <div class="card-content">...</div>
    <footer class="card-footer">...</footer>
</article>
```
```css
.blog-preview {
    display: flex;
    flex-direction: column;
    gap: 24px;
}
```

I also keep forgetting that we can change specific ancestor property when the parent container is selected via the descendant selector.
```css
.blog-preview:hover .blog-title {
    color: var(--Yellow);
}
```

### Continued development

Instead of using fixed units, I will consider if relative units will be more appropriate for the use case going forward.
```css
.blog-tag, .date-published, .blog-author { font-size: 0.75rem; }
.blog-title { font-size: 1.25rem; }
```

### Useful resources

- [The Surprising Truth About Pixels and Accessibility](https://www.joshwcomeau.com/css/surprising-truth-about-pixels-and-accessibility/) - This helped me understand the difference between using pixels vs rem and em which is important for accessibility.

## Author

- LinkedIn - [Rizanne Fernandez](https://ph.linkedin.com/in/rizanne-fernandez)
- Frontend Mentor - [@rizanne-f](https://www.frontendmentor.io/profile/rizanne-f)
