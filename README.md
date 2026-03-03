# InferShield Blog

Official blog for InferShield - secure OAuth authentication for AI workflows.

**Live Site:** https://blog.infershield.io  
**GitHub Pages:** https://infershield.github.io/infershield-blog/

---

## About

This repository hosts the InferShield blog, a static HTML site deployed via GitHub Pages. The blog features product announcements, technical deep-dives, and updates about InferShield's development.

### Current Posts
- [**Announcing InferShield v1.0**](launch-v1.0.html) - Production-ready OAuth integration for AI workflows (March 6, 2026)

---

## Site Structure

- **`index.html`** - Blog homepage with post previews
- **`launch-v1.0.html`** - M1 v1.0 launch announcement
- **`style.css`** - Responsive CSS stylesheet
- **`CNAME`** - Custom domain configuration
- **`DEPLOYMENT.md`** - Deployment guide and DNS configuration

---

## Adding New Posts

### 1. Create Post HTML
Create a new file `{post-slug}.html`:

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Post Title | InferShield Blog</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <header>
        <h1><a href="index.html">InferShield Blog</a></h1>
        <nav>
            <a href="https://infershield.io">Home</a>
            <a href="https://docs.infershield.dev">Docs</a>
            <a href="https://github.com/InferShield/infershield">GitHub</a>
        </nav>
    </header>
    
    <main>
        <article class="blog-post">
            <!-- Post content here -->
        </article>
    </main>
    
    <footer>
        <p>&copy; 2026 InferShield. All rights reserved.</p>
    </footer>
</body>
</html>
```

### 2. Update index.html
Add a post preview:

```html
<article class="post-preview">
    <h2><a href="new-post.html">Post Title</a></h2>
    <p class="meta">Date • Category</p>
    <p>Post excerpt...</p>
    <a href="new-post.html" class="read-more">Read more →</a>
</article>
```

### 3. Commit and Push
```bash
git add .
git commit -m "feat: Add new blog post"
git push origin main
```

GitHub Pages will automatically deploy (30-60 seconds).

---

## Local Development

To preview the blog locally:

```bash
# Clone the repository
git clone https://github.com/InferShield/infershield-blog.git
cd infershield-blog

# Serve locally (using Python)
python3 -m http.server 8000

# Or using Node.js
npx http-server

# Open in browser
open http://localhost:8000
```

---

## Deployment

The blog is automatically deployed via GitHub Pages when changes are pushed to the `main` branch.

**Deployment Status:** Check [Actions](https://github.com/InferShield/infershield-blog/actions) tab

For detailed deployment instructions and DNS configuration, see [DEPLOYMENT.md](DEPLOYMENT.md).

---

## DNS Configuration

The blog uses the custom domain `blog.infershield.io`. DNS configuration is required:

**Required DNS Record:**
| Type  | Name | Value                | TTL  |
|-------|------|----------------------|------|
| CNAME | blog | infershield.github.io | 3600 |

See [DEPLOYMENT.md](DEPLOYMENT.md) for complete DNS setup instructions.

---

## Contributing

Blog posts are authored by the InferShield team. For corrections or feedback:
- Open an issue: https://github.com/InferShield/infershield-blog/issues
- Submit a pull request with suggested changes

---

## License

Content: © 2026 InferShield. All rights reserved.  
Code (HTML/CSS): MIT License

---

## Links

- **InferShield Main Repo:** https://github.com/InferShield/infershield
- **Documentation:** https://docs.infershield.dev
- **Website:** https://infershield.io
- **Discord:** https://discord.gg/infershield

---

**Maintained by:** InferShield Engineering Team  
**Questions?** Open an issue or join us on Discord.
