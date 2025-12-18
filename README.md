# Portfolio Website

A simple, modern, and responsive portfolio website that can be easily deployed on Vercel.

## Features

- 🎨 Clean and modern design
- 📱 Fully responsive (mobile, tablet, desktop)
- ⚡ Fast and lightweight
- 🚀 Easy deployment on Vercel
- 🎯 SEO friendly
- ♿ Accessible

## Sections

- **Home**: Hero section with introduction
- **About**: Personal information and background
- **Projects**: Showcase of your work
- **Skills**: Technical skills and expertise
- **Contact**: Ways to get in touch

## Local Development

To run this website locally:

1. Clone the repository
2. Open `index.html` in your browser, or
3. Use a local server:
   ```bash
   npm run dev
   ```
   Or with Python:
   ```bash
   python3 -m http.server 8000
   ```
   Then visit `http://localhost:8000`

## Deployment on Vercel

### Option 1: Deploy via Vercel CLI

```bash
npm install -g vercel
vercel
```

### Option 2: Deploy via GitHub

1. Push this repository to GitHub
2. Go to [Vercel](https://vercel.com)
3. Click "New Project"
4. Import your GitHub repository
5. Click "Deploy"

Your site will be live in seconds!

## Customization

Edit the following files to customize your portfolio:

- `index.html`: Update your name, bio, projects, and contact information
- `styles.css`: Modify colors, fonts, and styling
- `script.js`: Add or modify interactive features

### Color Scheme

The default color scheme uses:
- Primary: `#6366f1` (Indigo)
- Secondary: `#8b5cf6` (Purple)

To change colors, update the CSS variables in `styles.css`:

```css
:root {
    --primary-color: #6366f1;
    --secondary-color: #8b5cf6;
    /* ... */
}
```

## Browser Support

- Chrome (latest)
- Firefox (latest)
- Safari (latest)
- Edge (latest)

## License

MIT License - feel free to use this template for your own portfolio!

## Credits

Built with HTML, CSS, and JavaScript. Optimized for Vercel deployment.
