# Quarto Blog Profile

A personal profile and blog website built with [Quarto](https://quarto.org/).

## Project Structure

- **`_quarto.yml`**: The main configuration file. Controls the navigation bar, site title, theme, and standard CSS.
- **`index.qmd`**: The home page. It is configured to list the blog posts found in the `posts/` directory.
- **`about.qmd`**: The "About" or "Profile" page containing your bio, skills, and contact info.
- **`styles.css`**: Custom CSS styles to maintain your specific profile page aesthetics.
- **`posts/`**: This directory contains all your blog posts.
  - **`posts/welcome/`**: An example post.

## How to Add a New Blog Post

1.  **Create a Folder**: Inside the `posts/` directory, create a new folder for your post (e.g., `posts/my-new-post`).
2.  **Create File**: Inside that new folder, create a file named `index.qmd`.
3.  **Add Metadata**: At the top of `index.qmd`, add the YAML metadata:
    ```yaml
    ---
    title: "My New Post"
    author: "Ramón"
    date: "2024-12-12"
    categories: [code, design]
    image: "image.jpg"
    ---
    ```
4.  **Write Content**: Write your post content below the metadata using Markdown.
5.  **Preview**: Run `quarto preview` in your terminal to see the changes.

## Development

- **Preview**: `quarto preview` to run a local server that auto-updates.
- **Render**: `quarto render` to build the static site into the `_site/` directory.

## Deployment

### Option 1: Quarto Publish (Recommended)

Publish directly to GitHub Pages (gh-pages branch):

```bash
quarto publish gh-pages
```

### Option 2: Render to Docs (Classic)

1.  Change `output-dir: docs` in `_quarto.yml`.
2.  Run `quarto render`.
3.  Push the `docs/` folder to GitHub.
4.  Configure GitHub Pages to serve from the `/docs` folder on your main branch.
