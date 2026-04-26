# AGENT.md

## Project Overview

- **Type**: Static HTML documentation website for FPGA tutorials (Thai language)
- **Live URL**: https://wichayen.github.io/fpgathailand/
- **Host**: GitHub Pages (Jekyll disabled)
- **Styling**: Bootstrap 5.3.2 + custom styles.css

## File Structure

```
fpgathailand/
├── *.html              # Tutorial pages (root level)
├── *_files/            # Source code/examples for each tutorial
├── index.html          # Main page
├── sitemap.xml         # Manually maintained (not auto-generated)
├── styles.css         # Custom styles
├── _config.yml        # Jekyll config (disabled)
└── AGENT.md           # This file
```

## Development

### Preview Locally

Open HTML files directly in browser, or use simple HTTP server:

```powershell
python -m http.server 8000
# Then visit http://localhost:8000
```

### Build/Deploy

Push to main branch. GitHub Pages will automatically deploy.

## Update Sitemap

Since Jekyll sitemap plugin is disabled, manually update `sitemap.xml`:

1. Add new `<url>` entry:
   ```xml
   <url>
   <loc>https://wichayen.github.io/fpgathailand/[filename].html</loc>
   <lastmod>YYYY-MM-DD</lastmod>
   </url>
   ```
2. Keep sorted or append at end

## Common Tasks

- **Edit tutorial**: Find corresponding `*.html` file
- **Add source code**: Add to `*_files/` folder
- **Update navigation**: Edit `<nav>` section in HTML files
- **Test locally**: Open HTML in browser or use `python -m http.server`