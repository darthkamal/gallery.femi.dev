# Edge

A visually aesthetic [Ghost](https://github.com/TryGhost/Ghost) theme designed for creative professionals with a clean, paper-like aesthetic. Showcase your works with minimal style, elegant presentation, and a subtle dot pattern background.

**Version:** 1.0.0  
**Ghost Compatibility:** 5.0+

## ✨ Features

- **Paper-like Background**: Subtle dot pattern background (#e8e5e1) creating a sophisticated paper texture
- **Masonry Grid Layout**: Beautifully organized photo gallery with responsive columns
- **Clean Footer**: Minimalist footer design without branding
- **Responsive Design**: Fully responsive across all devices
- **Font Options**: Choose between modern sans-serif (Inter) or elegant serif (Lora) fonts
- **Navigation Layouts**: Three layout options - Logo on left, center, or stacked
- **Related Posts**: Optional related posts section on article pages
- **Built-in Search**: Ghost search integration
- **Members Support**: Full Ghost membership and subscription support
- **Optimized Performance**: Minimal, compiled CSS and JavaScript

## 📦 Installation

### Quick Install

1. Download the latest release: `dist/edge.zip`
2. Log into your Ghost admin panel
3. Navigate to **Settings** → **Design**
4. Click **Change theme** → **Upload theme**
5. Select the `edge.zip` file
6. Click **Activate** to make it live

### Development Install

If you want to customize the theme:

```bash
# Clone or download this repository
git clone <repository-url>
cd Edge

# Install dependencies
npm install

# Build theme assets
npm run zip

# Upload dist/edge.zip to your Ghost site
```

## 🎨 Customization

### Theme Settings

Access these in Ghost Admin → **Settings** → **Design** → **Site-wide**:

#### Navigation Layout
- **Logo on the left**: Traditional left-aligned header
- **Logo in the middle**: Centered logo with navigation
- **Stacked**: Vertically stacked layout

#### Typography
- **Title Font**: Modern sans-serif (Inter) or Elegant serif (Lora)
- **Body Font**: Modern sans-serif (Inter) or Elegant serif (Lora)

#### Related Posts
- **Show Related Posts**: Toggle related posts on article pages
- **Related Posts Title**: Customize the section heading (default: "You might also like...")

### Background Pattern

The theme features a subtle dot pattern background. To customize:

Edit `assets/css/general/background.css`:

```css
body {
    background-color: #ffffff;
    background-image: radial-gradient(circle, #e8e5e1 1px, transparent 1px);
    background-size: 20px 20px;
}
```

**Customization options:**
- Change `#e8e5e1` to adjust dot color (lighter = more subtle)
- Adjust `1px` to change dot size
- Modify `20px 20px` to change dot spacing

### Custom Fonts

The theme uses Inter (sans-serif) and Lora (serif). To add custom fonts:

1. Edit `default.hbs` to add Google Fonts or other font links
2. Update font variables in `assets/css/general/vars.css`

## 🛠 Development

### Requirements

- [Node.js](https://nodejs.org/) (v14+)
- [npm](https://www.npmjs.com/) or [Yarn](https://yarnpkg.com/)
- [Gulp](https://gulpjs.com) (installed automatically as dev dependency)

### Development Workflow

```bash
# Install dependencies
npm install

# Run build & watch for changes (with live reload)
npm run dev

# Build production assets
npm run zip

# Validate theme with gscan
npm test
```

### Project Structure

```
Edge/
├── assets/
│   ├── css/              # Source CSS files
│   │   ├── general/      # Global styles (vars, fonts, background)
│   │   ├── site/         # Site layout, header, footer
│   │   ├── blog/         # Blog-specific styles
│   │   └── misc/         # PhotoSwipe gallery styles
│   ├── js/               # JavaScript files
│   ├── built/            # Compiled assets (auto-generated)
│   └── fonts/            # Web fonts (Inter, Lora)
├── partials/             # Handlebars partials
├── default.hbs           # Base template
├── index.hbs             # Home page template
├── post.hbs              # Post template
├── page.hbs              # Page template
└── package.json          # Theme configuration
```

### Building for Production

The `zip` command creates `dist/edge.zip` ready for upload:

```bash
npm run zip
```

This packages all necessary theme files including:
- Compiled CSS (`assets/built/screen.css`)
- Minified JavaScript (`assets/built/main.min.js`)
- Templates and partials
- Fonts and images

## 🧪 Testing & Validation

Run Ghost's official theme validation tool:

```bash
npm test
```

This runs `gscan` to check for:
- Template compatibility
- Ghost version compatibility
- Best practices compliance
- Required files and structure

## 📝 Changelog

### Version 1.0.0
- Initial customized release
- Added paper-like dot pattern background
- Optimized dot transparency (#e8e5e1)
- Removed default branding from footer
- Unified background pattern across header and body
- Maintained full Ghost 5.0+ compatibility

## 🤝 Support

- **Ghost Documentation**: https://ghost.org/docs/themes/
- **Theme Development**: https://ghost.org/docs/themes/structure/
- **Ghost Forum**: https://forum.ghost.org/

## 📄 License

Copyright (c) 2013-2025 Ghost Foundation - Released under the [MIT license](LICENSE).

---

**Enjoy your beautifully minimal Ghost theme! 📸**
