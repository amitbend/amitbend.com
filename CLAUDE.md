# CLAUDE.md - AI Assistant Documentation

## Overview

This is a personal website and blog for Amit Bendor, an AI & Engineering Executive. The site is built with Jekyll (static site generator), uses a Gulp-based build pipeline, and is deployed on GitHub Pages with a custom domain (amitbend.com).

**Repository:** amitbend.com
**Tech Stack:** Jekyll 3.8.6, Ruby, Node.js, SCSS, Gulp
**Deployment:** GitHub Pages
**Domain:** https://amitbend.com

---

## Tech Stack

### Core Framework
- **Jekyll 3.8.6** - Static site generator (Ruby-based)
- **Ruby** - Backend language for Jekyll
- **Node.js/npm** - Frontend build tools and automation

### Ruby Gems (Backend Dependencies)
```ruby
- jekyll-seo-tag (2.5.0)         # SEO optimization & meta tags
- jekyll-assets (3.0.11)         # Asset pipeline & preprocessing
- amp-jekyll (1.0.2)             # AMP (Accelerated Mobile Pages) support
- jekyll-feed (0.10.0)           # RSS/Atom feed generation
- image_optim (0.26.1)           # Image optimization
- image_optim_bin (0.0.7)        # Image optimization binaries
```

### Node.js Dependencies (Build Tools)
```json
- gulp (^3.9.1)                  # Task runner/build automation
- gulp-sass (^3.1.0)             # SCSS compilation
- gulp-uglify (^2.0.0)           # JavaScript minification
- gulp-csso (^2.0.0)             # CSS optimization
- gulp-imagemin (^3.1.1)         # Image optimization
- browser-sync (^2.26.7)         # Live reload dev server
- netlify-cms (^2.9.6)           # Headless CMS
```

### Frontend Libraries
- **Skeleton CSS 2.0.4** - Lightweight responsive CSS framework
- **Font Awesome 5.9.0** - Icon library
- **DevIcon** - Development tool icons
- **Particles.js 2.0.0** - Particle animation for hero section
- **SweetScroll** - Smooth scrolling library
- **Montserrat** - Google Font (primary typeface)

### Content Management
- **Forestry CMS** - Visual content editor for Jekyll (configured in `.forestry/`)
- **Netlify CMS** - Alternative Git-based CMS (configured in `admin/config.yml`)

---

## Project Structure

```
amitbend.com/
├── _config.yml                    # Jekyll configuration (CRITICAL)
├── Gemfile / Gemfile.lock         # Ruby dependencies
├── package.json / package-lock.json # Node.js dependencies
├── gulpfile.js                    # Gulp build tasks
├── CNAME                          # Custom domain configuration
├── robots.txt / sitemap.xml       # SEO files
├── feed.xml / feed.html           # RSS feeds
├── manifest.json                  # PWA configuration
├── pwabuilder-sw.js              # Service worker for offline support
├── .gitignore                     # Git ignore rules
│
├── Content & Templates (Jekyll)
│   ├── _posts/                    # Blog posts (markdown files, YYYY-MM-DD-slug.md)
│   ├── _drafts/                   # Draft posts (not published)
│   ├── _layouts/                  # Page templates (base.html, default.html, post.html, amp.html)
│   ├── _includes/                 # Reusable components (header, footer, about, skills, etc.)
│   ├── _data/                     # Data files (projects.yml)
│   ├── index.html                 # Homepage
│   ├── blog.html                  # Blog listing page
│   ├── 404.html                   # Error page
│   ├── promo-bot.html            # Promo page
│   └── llm.html                   # LLM resources page
│
├── Source Files (Pre-compilation)
│   └── src/
│       ├── styles/
│       │   └── main.scss          # SCSS source → compiles to assets/css/main.css
│       ├── js/
│       │   └── app.js             # JavaScript source → minifies to assets/js/main.js
│       └── img/                   # Source images → optimizes to assets/img/
│
├── Compiled Assets (Build Output)
│   └── assets/
│       ├── css/                   # Compiled CSS files
│       │   ├── main.css          # Primary stylesheet (from src/styles/main.scss)
│       │   ├── posts.css         # Blog post styles
│       │   ├── calendar.css      # Calendly widget styles
│       │   └── posts/            # Post-related CSS (reset, markdown, syntax)
│       ├── js/                    # JavaScript files
│       │   ├── main.js           # Minified app.js
│       │   ├── sweet-scroll.min.js
│       │   ├── analytics.js
│       │   └── promo/particles.js
│       └── img/                   # Optimized images
│
├── CMS Configuration
│   ├── .forestry/                 # Forestry CMS config
│   │   ├── settings.yml
│   │   └── front_matter/templates/
│   ├── .pages.yml                 # Pages CMS config
│   └── admin/
│       ├── config.yml             # Netlify CMS config
│       └── index.html             # CMS admin interface
│
├── Build Output (Git-ignored)
│   ├── _site/                     # Jekyll build output (DO NOT EDIT)
│   ├── .sass-cache/              # SCSS compilation cache
│   ├── .jekyll-cache/            # Jekyll build cache
│   └── node_modules/             # Node.js dependencies
│
└── uploads/                       # CMS-uploaded files
```

---

## Key Configuration Files

### _config.yml (Jekyll Configuration)
**Location:** `/home/user/amitbend.com/_config.yml`

```yaml
# Site metadata
title: Amit Bendor | AI & Engineering Executive
url: https://amitbend.com
username: Amit BenDor
user_title: AI & Engineering Executive

# Plugins
plugins:
  - jekyll-seo-tag         # SEO meta tags
  - jekyll-assets          # Asset pipeline
  - amp-jekyll             # AMP support
  - jekyll-feed            # RSS feeds

# Build settings
sass:
  sass_dir: _sass
  style: compressed

# Exclusions from build
exclude:
  - package.json
  - src/
  - node_modules/
  - vendor/bundle/
  - Gemfile
  - Gemfile.lock
  - gulpfile.js
```

**IMPORTANT:** Always review `_config.yml` before making structural changes. Changes to this file require a Jekyll rebuild.

### package.json (Node.js Dependencies)
**Location:** `/home/user/amitbend.com/package.json`

Defines npm scripts and Gulp build dependencies. Run `npm install` after cloning or when dependencies change.

### gulpfile.js (Build Automation)
**Location:** `/home/user/amitbend.com/gulpfile.js`

Gulp task definitions for:
- SCSS compilation (`sass` task)
- JavaScript minification (`js` task)
- Image optimization (`imagemin` task)
- Jekyll builds (`jekyll-build` task)
- Development server (`browser-sync` task)
- File watching (`watch` task)

### .gitignore
**Location:** `/home/user/amitbend.com/.gitignore`

```
.vs/               # Visual Studio files
_site/             # Jekyll build output (NEVER commit)
.sass-cache/       # SCSS compilation cache
node_modules/      # Node.js dependencies
.DS_STORE          # macOS system files
```

**CRITICAL:** Never commit `_site/` or `node_modules/` directories.

---

## Development Workflow

### Initial Setup
```bash
# Install Ruby dependencies
bundle install --path vendor/bundle

# Install Node.js dependencies
npm install

# Run Gulp to compile assets
gulp
```

### Development Server (Hot Reload)
```bash
# Option 1: Using Gulp (recommended)
gulp  # Starts browser-sync on localhost:3000

# Option 2: Using Jekyll directly
bundle exec jekyll serve --drafts --port 4000
```

**Gulp default task runs:**
1. Compiles SCSS → CSS
2. Minifies JS
3. Builds Jekyll site
4. Starts browser-sync server
5. Watches files for changes (auto-reload)

### Build Pipeline Flow

```
Source Files                Build Process              Output
─────────────────────────────────────────────────────────────────
src/styles/main.scss    →   gulp sass              →  assets/css/main.css
src/js/app.js           →   gulp js (uglify)       →  assets/js/main.js
src/img/*.{jpg,png}     →   gulp imagemin          →  assets/img/
_posts/*.md             →   jekyll build           →  _site/
_layouts/*.html         →   jekyll build           →  _site/
_includes/*.html        →   jekyll build           →  _site/
```

### Gulp Tasks Reference

```bash
gulp                          # Default: compile all + watch + browser-sync
gulp sass                     # Compile SCSS to CSS
gulp js                       # Minify JavaScript
gulp imagemin                 # Optimize images
gulp jekyll-build             # Build Jekyll site
gulp jekyll-rebuild           # Rebuild Jekyll + reload browser
gulp watch                    # Watch for file changes
gulp fetch-newest-analytics   # Download latest Google Analytics script
```

### Making Changes

#### 1. Editing Styles
```bash
# Edit source file
vim src/styles/main.scss

# Gulp automatically compiles to assets/css/main.css (if watching)
# Or manually run:
gulp sass
```

**IMPORTANT:** NEVER edit `assets/css/main.css` directly. Always edit `src/styles/main.scss`.

#### 2. Editing JavaScript
```bash
# Edit source file
vim src/js/app.js

# Gulp automatically minifies to assets/js/main.js (if watching)
# Or manually run:
gulp js
```

**IMPORTANT:** NEVER edit `assets/js/main.js` directly. Always edit `src/js/app.js`.

#### 3. Adding Blog Posts
```bash
# Create new post file (YYYY-MM-DD-slug.md format)
touch _posts/2026-01-13-my-new-post.md

# Add front matter and content
cat > _posts/2026-01-13-my-new-post.md << 'EOF'
---
layout: post
title: "My New Post Title"
date: 2026-01-13
categories: [AI, Engineering]
description: "SEO-friendly description"
---

Post content goes here...
EOF

# Jekyll automatically rebuilds (if watching)
```

**Post Filename Convention:** `YYYY-MM-DD-title-slug.md`
**Required Front Matter:**
- `layout: post` (uses `_layouts/post.html`)
- `title:` Post title
- `date:` Publication date
- `categories:` Array of categories
- `description:` SEO meta description (optional)

#### 4. Editing Page Content
```bash
# Edit reusable components
vim _includes/about.html        # About Me section
vim _includes/skills.html       # Skills section
vim _includes/projects.html     # Projects section
vim _includes/header.html       # Hero/header section

# Edit page layouts
vim _layouts/default.html       # Homepage layout
vim _layouts/post.html          # Blog post layout

# Edit data files
vim _data/projects.yml          # Project metadata
```

#### 5. Optimizing Images
```bash
# Place source images in src/img/
cp ~/Downloads/new-image.jpg src/img/

# Run image optimization
gulp imagemin

# Output: assets/img/new-image.jpg (optimized)
```

---

## Content Management

### Blog Posts

**Location:** `_posts/`
**Format:** Markdown with YAML front matter
**Filename:** `YYYY-MM-DD-title-slug.md`

**Example Post:**
```markdown
---
layout: post
title: "Understanding LLMs in 2026"
date: 2026-01-13
categories: [AI, LLM, Machine Learning]
description: "A comprehensive guide to Large Language Models in 2026"
image: /assets/img/llm-thumbnail.jpg
rating: 5
---

## Introduction

Post content goes here...

### Key Points

- Point 1
- Point 2

## Conclusion

Wrap-up content...
```

**Current Posts (9 published):**
1. 2018-06-06: Test Your Bot
2. 2018-07-23: Amazon Alexa vs Google Assistant
3. 2018-08-20: Content List
4. 2018-12-26: Chatbot Voice Resources
5. 2019-05-13: Five Free Ways to Host Your Node App (2019)
6. 2019-08-19: AutoML Open Source Tools
7. 2019-09-25: SaaS Starters
8. 2020-04-28: 6 Free Options to Host Your Node.js App
9. 2024-11-24: Available LLMs List GenAI

### Data-Driven Content

**Projects (_data/projects.yml):**
```yaml
- title: Cloud AI
  url: https://cloudai.network
  description: AI/ML API directory
  category: Directories
  img: /assets/img/google-cloud.jpg

- title: Madrasa
  url: https://madrasa.org
  description: Free online Arabic learning school
  category: Education
  img: /assets/img/madrasa.jpg
```

**Project Fields:**
- `title:` Project name
- `url:` External link
- `description:` Short description
- `category:` Type (Directories, Education, Community)
- `img:` Image path (relative to site root)

### Using CMS (Optional)

#### Forestry CMS
1. Visit Forestry.io dashboard
2. Import from GitHub
3. Edit content visually
4. Changes push to git automatically

#### Netlify CMS
1. Visit `/admin` on deployed site
2. Authenticate via Git Gateway
3. Create/edit blog posts
4. Media uploads go to `assets/img/`

**Note:** CMS-created files may require formatting cleanup for consistency.

---

## Build & Deployment

### GitHub Pages Deployment

**Hosting:** GitHub Pages
**Branch:** `main` (or `gh-pages` depending on configuration)
**Custom Domain:** amitbend.com (via CNAME file)

**Deployment Process:**
1. Push changes to GitHub
2. GitHub Pages automatically builds Jekyll site
3. Site deploys to https://amitbend.com

**IMPORTANT:** GitHub Pages uses Jekyll 3.9.x by default. Ensure `_config.yml` and `Gemfile` are compatible.

### Manual Deployment

```bash
# Build site locally
bundle exec jekyll build

# Output: _site/ directory contains static HTML

# Optional: Test locally before deploying
bundle exec jekyll serve
```

### Git Workflow

**Current Branch:** `claude/add-claude-documentation-xHri7`

**Branch Naming Convention:**
- Feature branches: `claude/<feature-name>-<session-id>`
- All changes should be developed on feature branches
- Push with: `git push -u origin <branch-name>`

**Commit Message Guidelines:**
- Use present tense ("Add feature" not "Added feature")
- Be descriptive but concise
- Reference issues/PRs when applicable

**Example Git Flow:**
```bash
# Check current branch
git status

# Stage changes
git add .

# Commit with descriptive message
git commit -m "Add CLAUDE.md documentation for AI assistants"

# Push to feature branch
git push -u origin claude/add-claude-documentation-xHri7

# Create pull request (using gh CLI)
gh pr create --title "Add comprehensive CLAUDE.md documentation" \
  --body "Adds detailed documentation for AI assistants including codebase structure, workflows, and conventions."
```

**Git Push Retry Logic:**
- If push fails due to network errors, retry up to 4 times
- Use exponential backoff: 2s, 4s, 8s, 16s
- Only retry for network errors, NOT for authentication or conflict errors

---

## Key Conventions & Best Practices

### 1. File Editing Rules

**DO:**
- Edit source files in `src/` (SCSS, JS, images)
- Edit content in `_posts/`, `_includes/`, `_layouts/`, `_data/`
- Run Gulp to compile changes
- Test locally before pushing

**DO NOT:**
- Edit compiled files in `assets/` directly (main.css, main.js)
- Edit `_site/` directory (auto-generated, git-ignored)
- Commit `node_modules/` or `.sass-cache/`
- Push broken builds to main branch

### 2. Style Guidelines

**CSS/SCSS:**
- Write styles in `src/styles/main.scss`
- Use SCSS variables for colors:
  ```scss
  $background-color: #0D2333;  // Dark blue
  $primary-color: #1B9C82;     // Teal
  $accent-color: #CEAB67;      // Gold
  ```
- Mobile-first approach with 768px breakpoint
- Compressed output for production

**JavaScript:**
- Write code in `src/js/app.js`
- Use ES5 syntax (compatible with older browsers)
- Minified output for production
- External libraries in `assets/js/` (sweet-scroll, particles.js)

**Images:**
- Place originals in `src/img/`
- Run `gulp imagemin` to optimize
- Use descriptive filenames (e.g., `profile-photo.jpg`, not `IMG_1234.jpg`)
- Prefer JPG for photos, PNG for graphics/logos

### 3. SEO Best Practices

**Meta Tags (via jekyll-seo-tag):**
- Automatic generation of:
  - `<title>` tags
  - `<meta name="description">`
  - Open Graph tags
  - Twitter Card tags
  - Canonical URLs

**Manual SEO:**
- Add `description:` to post front matter
- Use descriptive URLs (post slugs)
- Optimize images with alt text
- Keep page load times fast (<3s)

**Structured Data:**
- Schema.org/Person for author info
- Schema.org/BlogPosting for blog posts
- Open Graph for social sharing

### 4. Responsive Design

**Breakpoints:**
```scss
// Mobile first (default: 0-767px)
@media (max-width: 767px) { ... }

// Desktop (768px+)
@media (min-width: 768px) { ... }
```

**Testing:**
- Test on mobile (375px, 414px widths)
- Test on tablet (768px, 1024px widths)
- Test on desktop (1280px, 1920px widths)

### 5. Performance Optimization

**Asset Optimization:**
- CSS minification via `gulp-csso`
- JS minification via `gulp-uglify`
- Image optimization via `gulp-imagemin`
- SCSS compilation with `style: compressed`

**Caching:**
- Browser caching via Jekyll headers
- Service worker for offline support (pwabuilder-sw.js)
- Asset versioning via jekyll-assets

**Lazy Loading:**
- Consider adding lazy loading for images (not currently implemented)
- Defer non-critical JS

### 6. Accessibility

**Current Implementations:**
- Semantic HTML5 elements
- Alt text on images
- ARIA labels where needed
- Keyboard navigation support

**Improvements to Consider:**
- Skip to main content link
- Focus indicators
- Screen reader testing
- Color contrast validation (WCAG AA)

### 7. Security

**Current Measures:**
- No server-side code (static site = minimal attack surface)
- HTTPS via GitHub Pages
- No user authentication/input (no XSS/CSRF risk)

**Best Practices:**
- Don't commit secrets (API keys, tokens) to git
- Use environment variables for sensitive config
- Keep dependencies updated (`npm audit`, `bundle audit`)

---

## Common Tasks for AI Assistants

### Task 1: Add a New Blog Post

```bash
# 1. Create post file
touch _posts/2026-01-13-new-post-title.md

# 2. Add content with front matter
cat > _posts/2026-01-13-new-post-title.md << 'EOF'
---
layout: post
title: "New Post Title"
date: 2026-01-13
categories: [Category1, Category2]
description: "SEO description here"
---

# Introduction

Post content...
EOF

# 3. Build and preview
bundle exec jekyll serve

# 4. Commit and push
git add _posts/2026-01-13-new-post-title.md
git commit -m "Add blog post: New Post Title"
git push -u origin <branch-name>
```

### Task 2: Update Site Styles

```bash
# 1. Edit SCSS source
vim src/styles/main.scss

# 2. Compile SCSS
gulp sass

# 3. Preview changes
gulp  # Starts browser-sync

# 4. Commit compiled CSS
git add src/styles/main.scss assets/css/main.css
git commit -m "Update site styles: [describe changes]"
git push
```

### Task 3: Add a New Project

```bash
# 1. Edit projects data file
vim _data/projects.yml

# 2. Add new project entry
cat >> _data/projects.yml << 'EOF'
- title: New Project
  url: https://example.com
  description: Project description
  category: Category
  img: /assets/img/project-image.jpg
EOF

# 3. Add project image (if needed)
cp ~/path/to/image.jpg src/img/project-image.jpg
gulp imagemin

# 4. Rebuild site
bundle exec jekyll build

# 5. Commit changes
git add _data/projects.yml assets/img/project-image.jpg
git commit -m "Add new project: New Project"
git push
```

### Task 4: Update Header/About Section

```bash
# 1. Edit include file
vim _includes/header.html      # For hero section
# OR
vim _includes/about.html       # For about section

# 2. Preview changes
bundle exec jekyll serve

# 3. Commit changes
git add _includes/header.html
git commit -m "Update header section"
git push
```

### Task 5: Optimize Images

```bash
# 1. Add new images to source directory
cp ~/Downloads/*.jpg src/img/

# 2. Run optimization
gulp imagemin

# 3. Verify optimized output
ls -lh assets/img/

# 4. Commit optimized images
git add src/img/ assets/img/
git commit -m "Add and optimize new images"
git push
```

### Task 6: Update Dependencies

```bash
# Update Ruby gems
bundle update

# Update Node.js packages
npm update

# Check for security vulnerabilities
npm audit
bundle audit

# Commit lockfile changes
git add Gemfile.lock package-lock.json
git commit -m "Update dependencies"
git push
```

### Task 7: Create a Pull Request

```bash
# 1. Ensure all changes are committed
git status

# 2. Push branch to remote
git push -u origin <branch-name>

# 3. Create PR using gh CLI
gh pr create \
  --title "Brief description" \
  --body "## Summary
- Change 1
- Change 2

## Test Plan
- [x] Tested locally
- [x] Verified build passes
"

# 4. View PR in browser
gh pr view --web
```

---

## Important Files Reference

### Configuration Files
| File | Purpose | Edit Frequency |
|------|---------|----------------|
| `_config.yml` | Jekyll configuration | Rare |
| `Gemfile` | Ruby dependencies | Rare |
| `package.json` | Node.js dependencies | Rare |
| `gulpfile.js` | Build tasks | Rare |
| `.gitignore` | Git exclusions | Rare |
| `CNAME` | Custom domain | Never |

### Content Files
| File | Purpose | Edit Frequency |
|------|---------|----------------|
| `_posts/*.md` | Blog posts | Frequent |
| `_data/projects.yml` | Project data | Occasional |
| `_includes/*.html` | Reusable sections | Occasional |
| `_layouts/*.html` | Page templates | Rare |
| `index.html` | Homepage | Occasional |

### Source Files (Pre-compilation)
| File | Purpose | Compiles To |
|------|---------|-------------|
| `src/styles/main.scss` | Main stylesheet | `assets/css/main.css` |
| `src/js/app.js` | Main JavaScript | `assets/js/main.js` |
| `src/img/*` | Source images | `assets/img/*` |

### Output Files (DO NOT EDIT)
| File | Source | Notes |
|------|--------|-------|
| `assets/css/main.css` | `src/styles/main.scss` | Auto-generated by Gulp |
| `assets/js/main.js` | `src/js/app.js` | Auto-generated by Gulp |
| `_site/*` | Jekyll build | Git-ignored, never commit |

---

## Design System

### Color Palette
```scss
$background-color: #0D2333;    // Dark blue (page background)
$primary-color: #1B9C82;       // Teal (links, accents)
$accent-color: #CEAB67;        // Gold (highlights, particle connections)
$text-color: #FFFFFF;          // White (primary text)
$text-secondary: #CCCCCC;      // Light gray (secondary text)
```

### Typography
```scss
$font-family: 'Montserrat', sans-serif;
$font-size-base: 16px;
$font-size-h1: 3rem;
$font-size-h2: 2.5rem;
$font-size-h3: 2rem;
```

### Spacing
```scss
$spacing-unit: 1rem;           // 16px
$spacing-small: 0.5rem;        // 8px
$spacing-large: 2rem;          // 32px
$spacing-xlarge: 4rem;         // 64px
```

### Breakpoints
```scss
$mobile-max: 767px;            // Max width for mobile
$tablet-min: 768px;            // Min width for tablet/desktop
$desktop-min: 1024px;          // Min width for desktop
```

---

## Troubleshooting

### Issue: Jekyll Build Fails

**Symptoms:** `bundle exec jekyll build` throws errors

**Solutions:**
```bash
# 1. Update dependencies
bundle install

# 2. Clear cache
rm -rf _site .sass-cache .jekyll-cache

# 3. Rebuild
bundle exec jekyll build

# 4. Check for syntax errors in:
#    - _config.yml (YAML syntax)
#    - _posts/*.md (front matter syntax)
#    - _data/*.yml (YAML syntax)
```

### Issue: Gulp Tasks Fail

**Symptoms:** `gulp` command throws errors

**Solutions:**
```bash
# 1. Reinstall Node.js dependencies
rm -rf node_modules package-lock.json
npm install

# 2. Check Node.js version (should be 12+)
node --version

# 3. Try running individual tasks
gulp sass
gulp js
gulp imagemin
```

### Issue: Styles Not Updating

**Symptoms:** CSS changes don't appear on site

**Solutions:**
```bash
# 1. Clear browser cache (Cmd+Shift+R or Ctrl+Shift+R)

# 2. Ensure you're editing source file (not output)
vim src/styles/main.scss  # Edit this
# NOT: vim assets/css/main.css

# 3. Manually recompile SCSS
gulp sass

# 4. Check for SCSS syntax errors
sass-lint src/styles/main.scss
```

### Issue: JavaScript Not Working

**Symptoms:** Particle animations or smooth scroll broken

**Solutions:**
```bash
# 1. Check browser console for errors

# 2. Verify libraries are loaded
# Check _includes/head.html for:
# - particles.js
# - sweet-scroll.min.js

# 3. Rebuild JavaScript
gulp js

# 4. Test in incognito mode (disable extensions)
```

### Issue: Images Not Displaying

**Symptoms:** Broken image icons on site

**Solutions:**
```bash
# 1. Verify image paths are correct
# Use absolute paths from site root: /assets/img/image.jpg
# NOT relative paths: ../img/image.jpg

# 2. Check file permissions
chmod 644 assets/img/*.jpg

# 3. Optimize images if too large
gulp imagemin

# 4. Verify image exists in both src and assets
ls src/img/image.jpg
ls assets/img/image.jpg
```

### Issue: Git Push Fails (403 Error)

**Symptoms:** `git push` returns 403 Forbidden

**Solutions:**
```bash
# 1. Ensure branch name follows convention
# Must start with 'claude/' and end with session ID
git branch  # Check current branch name

# 2. Retry with exponential backoff (network errors)
sleep 2 && git push -u origin <branch-name>
sleep 4 && git push -u origin <branch-name>

# 3. Check authentication
git config --list | grep user

# 4. Use correct remote URL
git remote -v
```

---

## Performance Benchmarks

### Target Metrics
- **Page Load Time:** <3 seconds
- **First Contentful Paint:** <1.5 seconds
- **Time to Interactive:** <3.5 seconds
- **Lighthouse Score:** >90/100

### Optimization Checklist
- [x] CSS minification (gulp-csso)
- [x] JS minification (gulp-uglify)
- [x] Image optimization (gulp-imagemin)
- [x] SCSS compilation (compressed output)
- [x] Service worker (offline support)
- [ ] Lazy loading images
- [ ] Critical CSS inlining
- [ ] Deferred JavaScript loading
- [ ] WebP image format
- [ ] CDN for static assets

---

## Resources

### Documentation
- **Jekyll Docs:** https://jekyllrb.com/docs/
- **Gulp Docs:** https://gulpjs.com/docs/en/getting-started/quick-start
- **SCSS Docs:** https://sass-lang.com/documentation
- **Skeleton CSS:** http://getskeleton.com/

### Tools
- **Jekyll:** Static site generator
- **Gulp:** Build automation
- **Browser-sync:** Live reload server
- **Image optimization:** image_optim, gulp-imagemin
- **CSS optimization:** gulp-csso
- **JS minification:** gulp-uglify

### External Services
- **GitHub Pages:** Hosting
- **Google Analytics:** UA-121328300-1
- **Calendly:** Scheduling widget
- **Font Awesome:** Icon library
- **Google Fonts:** Montserrat typeface

---

## Summary for AI Assistants

### Quick Reference
1. **This is a Jekyll static site** - not a dynamic web app
2. **Source files in `src/`** - SCSS, JS, images (edit these)
3. **Compiled files in `assets/`** - CSS, JS, optimized images (don't edit)
4. **Content in `_posts/`, `_includes/`, `_layouts/`** - markdown and HTML
5. **Build with Gulp** - `gulp` command compiles everything
6. **Deploy via Git** - push to GitHub, Pages auto-deploys
7. **Branch naming** - `claude/<feature>-<session-id>`

### Most Common Operations
```bash
# Start development
npm install && bundle install && gulp

# Add blog post
touch _posts/YYYY-MM-DD-title.md
# (add front matter + content)

# Update styles
vim src/styles/main.scss
gulp sass

# Update JavaScript
vim src/js/app.js
gulp js

# Optimize images
cp new-image.jpg src/img/
gulp imagemin

# Commit changes
git add .
git commit -m "Description"
git push -u origin <branch-name>

# Create PR
gh pr create --title "Title" --body "Description"
```

### Critical Rules
1. **NEVER** edit `assets/css/main.css` or `assets/js/main.js` directly
2. **NEVER** commit `_site/`, `node_modules/`, `.sass-cache/`
3. **ALWAYS** edit source files in `src/` directory
4. **ALWAYS** test locally before pushing (`gulp` or `jekyll serve`)
5. **ALWAYS** use feature branches, never push directly to main
6. **ALWAYS** follow post naming convention: `YYYY-MM-DD-slug.md`
7. **ALWAYS** include front matter in posts (layout, title, date)

### File Editing Priority
**High Priority (Edit Often):**
- `_posts/*.md` - Blog content
- `src/styles/main.scss` - Styles
- `src/js/app.js` - JavaScript
- `_includes/*.html` - Page sections
- `_data/projects.yml` - Project data

**Medium Priority (Edit Occasionally):**
- `_layouts/*.html` - Page templates
- `index.html` - Homepage
- `blog.html` - Blog listing

**Low Priority (Rarely Edit):**
- `_config.yml` - Jekyll config
- `package.json` - Dependencies
- `Gemfile` - Ruby gems
- `gulpfile.js` - Build tasks

**Never Edit:**
- `_site/*` - Build output
- `assets/css/main.css` - Compiled CSS
- `assets/js/main.js` - Compiled JS
- `node_modules/*` - Dependencies
- `.sass-cache/*` - Cache

---

## Version History

| Date | Version | Changes |
|------|---------|---------|
| 2026-01-13 | 1.0.0 | Initial CLAUDE.md documentation created |

---

## Contact & Support

**Website:** https://amitbend.com
**GitHub:** https://github.com/amitbend/amitbend.com
**Calendar:** Schedule via Calendly widget on homepage

For issues or questions about this documentation, please create an issue in the GitHub repository.

---

**Last Updated:** 2026-01-13
**Maintained By:** Claude AI Assistant
**Purpose:** Guide AI assistants in understanding and working with this codebase
