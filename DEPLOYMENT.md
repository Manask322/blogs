# GitHub Pages Deployment Guide

This document explains how to deploy this Jekyll blog to GitHub Pages.

## Repository Setup

- **Repository**: `Manask322/blogs`
- **Target URL**: `https://manask322.github.io/blogs/`
- **Deployment Type**: Project Pages (not User Pages)

## GitHub Pages Configuration

### Step 1: Enable GitHub Pages
1. Go to your repository on GitHub: `https://github.com/Manask322/blogs`
2. Navigate to **Settings** → **Pages**
3. Under **Build and deployment**:
   - **Source**: Select "Deploy from a branch"
   - **Branch**: Select `main`
   - **Folder**: Select `/ (root)`

### Step 2: Verify Configuration
- GitHub Pages will automatically detect Jekyll and build your site
- The site will be available at: `https://manask322.github.io/blogs/`
- Build status can be monitored in the **Actions** tab

## Important Configuration Notes

### Base URL Configuration
The `_config.yml` is configured with:
```yaml
url: "https://manask322.github.io"
baseurl: "/blogs"
```

This ensures all internal links work correctly when hosted under the `/blogs/` path.

### File Structure
```
/
├── _config.yml          # Jekyll configuration
├── index.html           # Homepage with blog listing
├── _posts/              # Blog posts directory
│   ├── 2026-02-28-confidence-to-code.md
│   ├── 2026-02-28-upi-as-a-service.md
│   └── 2026-02-28-starting-day-and-career.md
└── assets/
    └── css/
        └── style.css    # Site styling
```

## Deployment Process

1. **Push to main branch**: Any push to the `main` branch triggers a build
2. **GitHub Actions**: GitHub automatically runs Jekyll build
3. **Deployment**: Built site is deployed to GitHub Pages
4. **Access**: Site becomes available at the configured URL

## Verification Steps

After deployment:
1. Visit `https://manask322.github.io/blogs/`
2. Verify the homepage loads with blog post listings
3. Check that individual blog post links work
4. Test responsive design on mobile devices
5. Verify dark mode styling works

## Linking from Main Website

To link from your main website (`manask322.github.io`):
- Update the "Blogs" link to point to: `https://manask322.github.io/blogs/`
- This allows visitors to navigate from your main site to your blog hub

## Adding New Blog Posts

To add new posts:
1. Create new `.md` files in the `_posts/` directory
2. Use the naming convention: `YYYY-MM-DD-title-slug.md`
3. Include proper YAML front matter with `title`, `date`, `tags`, and `excerpt`
4. Push to the `main` branch to trigger deployment

## Troubleshooting

- **Build fails**: Check the Actions tab for detailed error messages
- **Links broken**: Verify `baseurl` configuration in `_config.yml`
- **Styling issues**: Ensure CSS path uses `{{ '/assets/css/style.css' | relative_url }}`
- **Posts not appearing**: Check file naming convention and YAML front matter