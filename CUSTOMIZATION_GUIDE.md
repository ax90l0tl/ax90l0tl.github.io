# Portfolio Customization Guide

This guide will help you personalize your engineering portfolio.

## Quick Start

Your portfolio is now live! To view it, visit: `https://ax90l0tl.github.io`

## Customization Steps

### 1. Update Personal Information

**In `index.html`:**

- **Line 163**: Update LinkedIn URL
  ```html
  <!-- Change from: -->
  <a href="https://linkedin.com/in/yourprofile">
  <!-- To your actual profile: -->
  <a href="https://linkedin.com/in/your-actual-username">
  ```

- **Line 169**: Update email address
  ```html
  <!-- Change from: -->
  <a href="mailto:your.email@example.com">
  <!-- To your actual email: -->
  <a href="mailto:your.actual.email@example.com">
  ```

### 2. Customize Content

**Hero Section (Lines 31-40):**
- Update the title and subtitle to match your role and tagline

**About Me (Lines 44-52):**
- Write your personal introduction
- Highlight your unique approach and philosophy

**Technical Skills (Lines 57-93):**
- Add or remove programming languages
- Update frameworks and tools you use
- List your areas of expertise

**Projects (Lines 98-130):**
- Replace placeholder projects with your actual work
- Update project names, descriptions, and technologies
- Change `href="#"` to link to:
  - GitHub repositories
  - Live demos
  - Case studies

**Education (Lines 137-153):**
- Update your degree information
- Add your university name
- Update graduation dates
- Add or remove certifications

### 3. Add More Projects

#### Adding a Project Card on Homepage

To add a new project card on the homepage, copy this template in the projects section of `index.html`:

```html
<div class="project-card">
    <h3>Your Project Name</h3>
    <p class="project-description">Brief description of what this project does and its impact.</p>
    <div class="project-tags">
        <span class="tag">Technology 1</span>
        <span class="tag">Technology 2</span>
        <span class="tag">Technology 3</span>
    </div>
    <a href="projects/your-project.html" class="project-link">View Project →</a>
</div>
```

#### Creating a Dedicated Project Page

Each project can have its own detailed page. To create one:

1. **Use the base template** (`base-template.html`) as a starting point
2. **Or copy an existing project page** from the `projects/` folder (e.g., `project1.html`)
3. **Update the content**:
   - Change the page title and meta description
   - Update the project name, overview, technologies, features, and challenges
   - Update the links to your GitHub repo and live demo
4. **Save it** in the `projects/` folder with a descriptive filename (e.g., `projects/my-awesome-app.html`)
5. **Link to it** from the homepage by updating the project card's link

**Example structure for a project page:**

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="Your project description">
    <title>Your Project Name | ax90l0tl</title>
    <link rel="stylesheet" href="../styles.css">
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700&display=swap" rel="stylesheet">
</head>
<body>
    <header>
        <nav>
            <div class="nav-container">
                <h1 class="logo"><a href="../index.html" style="text-decoration: none; color: inherit;">ax90l0tl</a></h1>
                <ul class="nav-links">
                    <li><a href="../index.html">Home</a></li>
                    <li><a href="../index.html#about">About</a></li>
                    <li><a href="../index.html#skills">Skills</a></li>
                    <li><a href="../index.html#projects">Projects</a></li>
                    <li><a href="../index.html#contact">Contact</a></li>
                </ul>
            </div>
        </nav>
    </header>

    <main>
        <div class="page-content">
            <section class="section">
                <div class="container">
                    <h1 class="section-title">Your Project Name</h1>
                    
                    <div class="project-detail">
                        <div class="project-overview">
                            <h2>Overview</h2>
                            <p>Detailed description of your project...</p>
                        </div>

                        <div class="project-technologies">
                            <h2>Technologies Used</h2>
                            <div class="project-tags">
                                <span class="tag">Tech 1</span>
                                <span class="tag">Tech 2</span>
                            </div>
                        </div>

                        <div class="project-features">
                            <h2>Key Features</h2>
                            <ul class="feature-list">
                                <li>Feature 1</li>
                                <li>Feature 2</li>
                            </ul>
                        </div>

                        <div class="project-links">
                            <h2>Links</h2>
                            <div class="project-buttons">
                                <a href="YOUR_GITHUB_URL" class="btn btn-primary" target="_blank">View on GitHub</a>
                                <a href="YOUR_DEMO_URL" class="btn btn-secondary">Live Demo</a>
                            </div>
                        </div>
                    </div>
                </div>
            </section>
        </div>
    </main>

    <footer>
        <div class="container">
            <p>&copy; 2024 ax90l0tl. Built with passion for engineering excellence.</p>
        </div>
    </footer>

    <script src="../script.js"></script>
</body>
</html>
```

### 4. Customize Colors

**In `styles.css` (Lines 11-18):**

```css
:root {
    --primary-color: #2563eb;        /* Main brand color */
    --secondary-color: #1e40af;      /* Hover states */
    --text-primary: #1f2937;         /* Body text */
    --text-secondary: #6b7280;       /* Secondary text */
    --bg-white: #ffffff;             /* Background */
    --bg-gray: #f9fafb;              /* Alternate sections */
    --accent-color: #10b981;         /* Accents */
}
```

Change these hex color codes to match your preferred color scheme.

### 5. Change Hero Gradient

**In `styles.css` (Line 73):**

```css
background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
```

Use a gradient generator like [cssgradient.io](https://cssgradient.io/) to create your own.

### 6. Add Your Photo (Optional)

1. Add an image file (e.g., `profile.jpg`) to the repository
2. In `index.html`, add this code in the About section:

```html
<img src="profile.jpg" alt="Your Name" class="profile-photo">
```

3. In `styles.css`, add styling:

```css
.profile-photo {
    width: 200px;
    height: 200px;
    border-radius: 50%;
    margin: 0 auto 2rem;
    display: block;
    box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
}
```

## Testing Locally

To test changes locally:

```bash
python3 -m http.server 8080
```

Then open `http://localhost:8080` in your browser.

## Deployment

Changes pushed to the main branch will automatically deploy to GitHub Pages.

## Need Help?

- CSS: [MDN Web Docs](https://developer.mozilla.org/en-US/docs/Web/CSS)
- HTML: [MDN Web Docs](https://developer.mozilla.org/en-US/docs/Web/HTML)
- JavaScript: [MDN Web Docs](https://developer.mozilla.org/en-US/docs/Web/JavaScript)

## Tips

1. Keep descriptions concise and impactful
2. Use action words (built, developed, designed, implemented)
3. Include metrics when possible (e.g., "improved performance by 50%")
4. Keep the design clean and professional
5. Test on different screen sizes
6. Ensure all links work before sharing

Enjoy your new portfolio! 🚀
