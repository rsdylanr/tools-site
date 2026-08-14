# GitHub Tools Suite

A modular-but-monolithic single-page tools suite deployed automatically using GitHub Pages.

## Features

- Modular tool system
- Dynamic sidebar
- Password generator tool
- Easy to extend with new tools

## Deployment

This repository uses GitHub Actions to deploy automatically to GitHub Pages.

Push to the `main` branch and the site will update within seconds.

## Adding New Tools

Inside `index.html`, create a new module:

```js
const MyTool = {
    render() {
        const div = document.createElement("div");
        div.className = "tool-container";
        div.innerHTML = "<h2>My Tool</h2>";
        return div;
    }
};

ToolRegistry.register("My Tool", MyTool);
