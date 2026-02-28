# SEO Setup Guide

This guide explains how to complete the SEO setup for your Jekyll blog.

## Current SEO Features Implemented

### ✅ Meta Tags & Social Media
- **Open Graph tags** for Facebook, LinkedIn sharing
- **Twitter Card tags** for Twitter sharing
- **Canonical URLs** to prevent duplicate content
- **Author and description meta tags**
- **Structured data (JSON-LD)** for rich snippets

### ✅ Search Engine Optimization
- **Sitemap.xml** automatically generated from all posts and pages
- **Robots.txt** with proper crawling guidelines
- **SEO-friendly URLs** via Jekyll permalinks
- **Mobile-responsive design** for mobile-first indexing

## Next Steps to Complete SEO Setup

### 1. Google Analytics Setup
1. Create a Google Analytics 4 property at [analytics.google.com](https://analytics.google.com)
2. Get your Measurement ID (format: `G-XXXXXXXXXX`)
3. Add to `_config.yml`:
   ```yaml
   google_analytics: G-XXXXXXXXXX
   ```

### 2. Google Search Console Setup
1. Go to [search.google.com/search-console](https://search.google.com/search-console)
2. Add your property: `https://manask322.github.io/blogs/`
3. Verify ownership using the HTML tag method
4. Add verification code to `_config.yml`:
   ```yaml
   google_site_verification: your_verification_code_here
   ```
5. Submit your sitemap: `https://manask322.github.io/blogs/sitemap.xml`

### 3. Bing Webmaster Tools (Optional)
1. Go to [www.bing.com/webmasters](https://www.bing.com/webmasters)
2. Add your site and verify ownership
3. Add verification code to `_config.yml`:
   ```yaml
   bing_site_verification: your_bing_verification_code
   ```

### 4. Social Media Optimization
- Add a custom favicon (`favicon.ico`) to your root directory
- Consider adding a blog banner image for social media sharing
- Test social media previews using:
  - [Facebook Sharing Debugger](https://developers.facebook.com/tools/debug/)
  - [Twitter Card Validator](https://cards-dev.twitter.com/validator)

### 5. Content SEO Best Practices

#### Blog Post Front Matter Template:
```yaml
---
title: "Your SEO-Optimized Title (under 60 characters)"
date: 2026-02-28
tags: [relevant, keywords, here]
excerpt: "Compelling description that appears in search results and social media (under 160 characters)"
---
```

#### SEO Writing Tips:
- Use descriptive, keyword-rich titles
- Write compelling meta descriptions (excerpts)
- Use proper heading hierarchy (H1, H2, H3)
- Include internal links between posts
- Optimize images with alt text
- Use relevant tags for categorization

## Monitoring and Analytics

### Key Metrics to Track:
- **Organic search traffic** (Google Analytics)
- **Search rankings** (Google Search Console)
- **Click-through rates** from search results
- **Social media engagement** on shared posts
- **Page load speed** (Google PageSpeed Insights)

### Regular SEO Maintenance:
1. **Update content regularly** to maintain freshness
2. **Monitor for 404 errors** in Search Console
3. **Review top-performing content** and optimize similar posts
4. **Build internal linking** between related posts
5. **Monitor Core Web Vitals** for page experience

## Technical SEO Features Already Implemented

```yaml
# Already configured in _config.yml
plugins:
  - jekyll-feed        # Creates RSS feed for subscribers
  - jekyll-sitemap     # Generates sitemap.xml automatically
```

Your blog is now SEO-ready! Complete the setup steps above to start tracking performance and improving search visibility.