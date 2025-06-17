# HTML Email Templates

This project contains responsive email templates built with MJML.

## Project Structure

```
.
├── src/            # MJML source files
│   └── welcome.mjml
├── dist/           # Generated HTML files
│   └── welcome.html
├── package.json    # Project configuration
└── README.md      # This file
```

## Setup

1. Install dependencies:
```bash
npm install
```

2. Build the templates:
```bash
# Build all templates
npm run build:all

# Build specific template
npm run build:welcome

# Watch for changes and auto-build
npm run watch
```

## Available Scripts

- `npm run build`: Builds the welcome template (alias for build:welcome)
- `npm run build:welcome`: Builds only the welcome template
- `npm run build:all`: Builds all MJML templates in the src directory
- `npm run watch`: Watches for changes in src/*.mjml and rebuilds automatically

## Adding New Templates

1. Create a new MJML file in the `src` directory (e.g., `src/newsletter.mjml`)
2. Add a new build script in `package.json` if needed:
   ```json
   "build:newsletter": "mjml src/newsletter.mjml -o dist/newsletter.html"
   ```
3. Run `npm run build:all` to build all templates or your specific build script

## Customization

To customize any template:

1. Edit the MJML file in the `src` directory
2. Replace placeholder images with your own
3. Update colors, text, and links
4. Run the appropriate build command to generate the new HTML

## Testing

Test the generated HTML emails (from the `dist` directory) in various email clients to ensure compatibility. 