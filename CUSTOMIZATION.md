# Customization Guide

This guide will help you customize your portfolio website to make it your own.

## Quick Customization Checklist

### 1. Personal Information (index.html)

Replace the following placeholders:

- **Line 7**: Change the page title
  ```html
  <title>Portfolio - Your Name</title>
  <!-- Change to -->
  <title>Portfolio - John Doe</title>
  ```

- **Line 27**: Update your name in the hero section
  ```html
  <h1 class="hero-title">Hi, I'm <span class="highlight">Your Name</span></h1>
  <!-- Change to -->
  <h1 class="hero-title">Hi, I'm <span class="highlight">John Doe</span></h1>
  ```

- **Line 28**: Update your title/role
  ```html
  <p class="hero-subtitle">Full Stack Developer | Designer | Creator</p>
  ```

- **Lines 30-32**: Customize your introduction
  ```html
  <p class="hero-description">
      I build beautiful and functional web applications that solve real-world problems.
  </p>
  ```

### 2. About Section (index.html, lines 50-71)

Replace the placeholder text with your actual story, background, and interests.

### 3. Projects (index.html, lines 76-158)

For each project card, update:
- **Project emoji/icon** (line 79, 94, 109)
- **Project title** (line 82, 97, 112)
- **Description** (line 83-86, 98-101, 113-116)
- **Technology tags** (line 88-90, 103-105, 118-120)
- **Links** (line 93-94, 108-109, 123-124)

Example:
```html
<h3 class="project-title">My Awesome App</h3>
<p class="project-description">
    A real description of your actual project.
</p>
<div class="project-tags">
    <span class="tag">React</span>
    <span class="tag">Node.js</span>
</div>
<div class="project-links">
    <a href="https://myapp.com" class="project-link">Live Demo →</a>
    <a href="https://github.com/yourusername/myapp" class="project-link">GitHub →</a>
</div>
```

### 4. Skills (index.html, lines 165-213)

Update the skills lists to match your actual skillset. You can:
- Add or remove skills from any list
- Add new skill categories by duplicating the `.skill-category` div
- Reorder skills based on proficiency

### 5. Contact Information (index.html, lines 223-243)

Update all contact links:
```html
<a href="mailto:your.email@example.com" class="contact-method">
<!-- Change to your actual email -->
<a href="mailto:john.doe@gmail.com" class="contact-method">
```

Update social media links:
```html
<a href="https://github.com/yourusername" target="_blank" class="contact-method">
<!-- Change to -->
<a href="https://github.com/johndoe" target="_blank" class="contact-method">
```

### 6. Footer (index.html, line 252)

Update the footer text:
```html
<p>&copy; 2025 Your Name. Built with ❤️ and deployed on Vercel.</p>
<!-- Change to -->
<p>&copy; 2025 John Doe. Built with ❤️ and deployed on Vercel.</p>
```

## Color Customization (styles.css)

### Changing the Color Scheme

Edit the CSS variables at the top of `styles.css` (lines 7-18):

```css
:root {
    --primary-color: #6366f1;      /* Main brand color */
    --secondary-color: #8b5cf6;    /* Secondary brand color */
    --accent-color: #fbbf24;       /* Accent/highlight color */
    --text-primary: #1f2937;       /* Main text color */
    --text-secondary: #6b7280;     /* Secondary text color */
    --bg-primary: #ffffff;         /* Main background */
    --bg-secondary: #f9fafb;       /* Alternate background */
    --bg-dark: #111827;            /* Dark background (footer) */
}
```

### Popular Color Schemes

**Blue Professional:**
```css
--primary-color: #2563eb;
--secondary-color: #3b82f6;
--accent-color: #60a5fa;
```

**Green Fresh:**
```css
--primary-color: #059669;
--secondary-color: #10b981;
--accent-color: #34d399;
```

**Orange Energetic:**
```css
--primary-color: #ea580c;
--secondary-color: #f97316;
--accent-color: #fb923c;
```

**Purple Creative:**
```css
--primary-color: #7c3aed;
--secondary-color: #8b5cf6;
--accent-color: #a78bfa;
```

## Adding Your Own Images

### Project Images

Replace the emoji placeholders with actual images:

1. Add your project images to the repository (create an `images/` folder)
2. Update the HTML:

```html
<!-- Replace this: -->
<div class="project-image">
    <div class="project-placeholder">🚀</div>
</div>

<!-- With this: -->
<div class="project-image">
    <img src="images/project1.jpg" alt="Project One">
</div>
```

3. Add this CSS to `styles.css`:

```css
.project-image img {
    width: 100%;
    height: 100%;
    object-fit: cover;
}
```

### Profile Photo

To add a profile photo to the About section:

1. Add your photo to an `images/` folder
2. In `index.html`, add the photo in the About section:

```html
<div class="about-content">
    <img src="images/profile.jpg" alt="Your Name" class="profile-photo">
    <div class="about-text">
        <!-- existing content -->
    </div>
</div>
```

3. Add styling in `styles.css`:

```css
.profile-photo {
    width: 200px;
    height: 200px;
    border-radius: 50%;
    margin: 0 auto 2rem;
    display: block;
    object-fit: cover;
    box-shadow: var(--shadow-lg);
}
```

## Font Customization

To use a different font, add a Google Fonts link in the `<head>` of `index.html`:

```html
<link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;600;700;800&display=swap" rel="stylesheet">
```

Then update `styles.css`:

```css
body {
    font-family: 'Poppins', -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, sans-serif;
    /* ... */
}
```

## Adding More Sections

To add a new section (e.g., "Blog" or "Testimonials"):

1. Add navigation link in `index.html`:
```html
<li><a href="#blog" class="nav-link">Blog</a></li>
```

2. Add the section:
```html
<section id="blog" class="blog">
    <div class="container">
        <h2 class="section-title">Blog</h2>
        <!-- Your content here -->
    </div>
</section>
```

3. Add styling in `styles.css` if needed.

## Tips

- Use the browser's developer tools (F12) to experiment with styles in real-time
- Test your changes on different screen sizes
- Keep the design consistent with the existing style
- Make sure all links work before deploying
- Optimize images (use WebP format and compress them)

## Need Help?

- Check the browser console (F12) for JavaScript errors
- Validate your HTML at https://validator.w3.org/
- Test responsive design using browser dev tools
- Review the existing code for examples

Happy customizing! 🎨
