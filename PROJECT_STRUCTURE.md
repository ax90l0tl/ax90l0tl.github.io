# Project Structure Guide

This document explains the structure of the portfolio website and how the template system works.

## Directory Structure

```
ax90l0tl.github.io/
├── index.html              # Homepage with all sections
├── base-template.html      # Base template for creating new pages
├── styles.css              # Global styles for all pages
├── script.js               # JavaScript for interactions
├── _config.yml             # Jekyll configuration (for GitHub Pages)
├── projects/               # Directory for individual project pages
│   ├── project1.html       # Example: Full-stack web app project
│   ├── project2.html       # Example: Machine learning project
│   └── project3.html       # Example: E-commerce project
├── CUSTOMIZATION_GUIDE.md  # Guide for customizing the portfolio
├── PROJECT_STRUCTURE.md    # This file
└── README.md               # Repository description
```

## How It Works

### Base Template System

The `base-template.html` file serves as a reusable template for creating new pages:

1. **Header with Navigation**: Consistent navigation across all pages
2. **Content Placeholder**: Area where page-specific content goes
3. **Footer**: Consistent footer across all pages
4. **Relative Paths**: All paths use `../` to work from subdirectories

### Creating New Pages

To create a new page using the base template:

1. Copy `base-template.html` to your desired location
2. Replace these placeholders:
   - `TITLE_PLACEHOLDER` - Page title
   - `DESCRIPTION_PLACEHOLDER` - Meta description
   - `CONTENT_PLACEHOLDER` - Main page content

**Or** copy an existing project page from the `projects/` folder and modify it.

### Linking Pages

- **From homepage to project page**: `href="projects/project1.html"`
- **From project page to homepage**: `href="../index.html"`
- **From project page to homepage section**: `href="../index.html#section"`

### Styling

All pages use the same `styles.css` file:
- Homepage uses its own sections and styles
- Project pages use `.page-content` and `.project-detail` classes
- Consistent color scheme defined in CSS variables

## Jekyll Compatibility

This site works with both:
- **Static hosting**: Direct HTML files served as-is
- **Jekyll (GitHub Pages)**: The `_config.yml` ensures Jekyll doesn't interfere with HTML files

The configuration excludes the base template from processing and serves all HTML files directly.

## Adding New Projects

### Step 1: Create Project Card on Homepage

In `index.html`, add a new project card in the projects section:

```html
<div class="project-card">
    <h3>New Project Name</h3>
    <p class="project-description">Brief description...</p>
    <div class="project-tags">
        <span class="tag">Technology 1</span>
        <span class="tag">Technology 2</span>
    </div>
    <a href="projects/new-project.html" class="project-link">View Project →</a>
</div>
```

### Step 2: Create Dedicated Project Page

Copy an existing project page or use the base template:

```bash
cp projects/project1.html projects/new-project.html
```

Then edit the content to match your new project.

### Step 3: Update Links and Metadata

- Update the `<title>` tag
- Update the meta description
- Update all content sections
- Update GitHub and demo links

## Testing Locally

Test your changes before deploying:

```bash
# Start a local web server
python3 -m http.server 8080

# Or use any other local server
# Then visit http://localhost:8080
```

Test navigation:
1. Homepage loads correctly
2. Project cards link to project pages
3. Project pages link back to homepage
4. All styles load correctly
5. Navigation works across pages

## Deployment

Push changes to the main branch, and GitHub Pages will automatically deploy:

```bash
git add .
git commit -m "Add new project page"
git push origin main
```

Your site will be available at: `https://ax90l0tl.github.io`

## Best Practices

1. **File Naming**: Use lowercase with hyphens (e.g., `my-project.html`)
2. **Consistency**: Keep the same structure across all project pages
3. **Images**: Store images in an `images/` or `assets/` folder
4. **Links**: Always test links work from both homepage and project pages
5. **Mobile**: Test on different screen sizes (site is responsive)

## Troubleshooting

### Styles not loading on project pages
- Check that `href="../styles.css"` path is correct
- Verify the file is in the root directory

### Links not working
- Use relative paths: `../` to go up one directory
- Test both from root and subdirectories

### Jekyll issues
- Ensure `_config.yml` is present
- The configuration prevents Jekyll from processing HTML files

### Navigation broken
- All project pages should use `../index.html` to link to homepage
- Homepage should use `projects/project-name.html` to link to projects

## Support

For more help, see:
- [CUSTOMIZATION_GUIDE.md](CUSTOMIZATION_GUIDE.md) - Customization instructions
- [GitHub Pages Documentation](https://docs.github.com/en/pages)
