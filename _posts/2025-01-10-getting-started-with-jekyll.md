---
title: "Getting Started with Jekyll and GitHub Pages"
date: 2025-01-10
---

Jekyll is a fantastic static site generator that powers GitHub Pages. In this post, I'll walk you through how I set up this simple blog.

## Why Jekyll?

Jekyll is perfect for blogging because:

- **Free hosting** with GitHub Pages
- **Markdown support** - Write posts in markdown
- **Automatic deployment** - Push to GitHub and it's live
- **Version control** - All content is tracked with Git
- **Themes and plugins** - Extensive ecosystem

## Setting Up Jekyll

The setup process is straightforward:

### 1. Create the Repository

Create a new repository on GitHub. For a user site, name it `username.github.io`.

### 2. Add Jekyll Files

Create these essential files:
- `_config.yml` - Jekyll configuration
- `_layouts/` - HTML templates
- `_posts/` - Your blog posts
- `index.html` - Homepage

### 3. Configure GitHub Pages

In your repository settings:
1. Go to the "Pages" section
2. Select your source branch
3. GitHub will automatically build your Jekyll site

## Writing Posts

Jekyll posts use a specific naming convention: `YYYY-MM-DD-title.md`

Each post starts with YAML frontmatter:

```yaml
---
title: "Your Post Title"
date: 2025-01-10
---
```

Then write your content in markdown below the frontmatter.

## The Power of Liquid Templates

Jekyll uses Liquid templating to make your site dynamic:

{% raw %}
```liquid
{% for post in site.posts %}
  <h2>{{ post.title }}</h2>
  <p>{{ post.date | date: "%B %d, %Y" }}</p>
{% endfor %}
```
{% endraw %}

This loops through all posts and displays them with formatted dates.

## What's Next?

With Jekyll, adding new posts is as simple as:

1. Creating a new markdown file in `_posts/`
2. Adding the proper frontmatter
3. Writing your content
4. Pushing to GitHub

Jekyll will automatically build and deploy your updated site!