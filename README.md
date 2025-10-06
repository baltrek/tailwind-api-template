# Example API Documentation

A modern, responsive REST API documentation template built with Tailwind CSS and Alpine.js. This template provides a clean, professional interface for documenting your API endpoints with support for dark mode and multiple viewing modes.

## 🌐 Live Demo

Check out the live demo: [https://baltrek.github.io/tailwind-api-template/](https://baltrek.github.io/tailwind-api-template/)

## Features

- **🎨 Modern Design**: Clean and professional UI built with Tailwind CSS
- **🌓 Dark Mode**: Full dark mode support with seamless transitions
- **📱 Fully Responsive**: Works perfectly on desktop, tablet, and mobile devices
- **🔄 Dual View Modes**: 
  - SPA Mode: Content switching without page reload
  - Scroll Mode: Single-page scrolling with anchor navigation
- **💾 Persistent Preferences**: Dark mode and view mode settings saved to localStorage
- **🎯 Interactive Navigation**: Sticky sidebar navigation for easy browsing
- **📋 Copy to Clipboard**: One-click code copying for all examples
- **⚡ Lightweight**: No heavy frameworks, just Alpine.js for interactivity

## Technologies Used

- **HTML5**: Semantic markup
- **Tailwind CSS**: Utility-first CSS framework for styling
- **Alpine.js**: Lightweight JavaScript framework for interactivity
- **Highlight.js**: Syntax highlighting for code examples

## Getting Started

### Prerequisites

This is a static HTML template, so you only need:
- A modern web browser
- A web server (for local development, you can use Python's built-in server, VS Code Live Server, etc.)

### Installation

1. Clone or download this repository
2. Open the `index.html` file in your web browser, or

## Usage

### Customization

#### Changing Colors

The template uses Tailwind CSS classes for styling. To change the color scheme:

1. Find and replace color classes throughout the HTML:
   - Primary colors: `blue-*`, `slate-*`
   - Dark mode colors: `zinc-*`
   - Accent colors for highlights

#### Adding New Endpoints

To add a new API endpoint:

1. Add a new navigation item in the sidebar:
```html
<li>
    <a @click="scrollToSection('your-endpoint')"
       :class="activeSection === 'your-endpoint' ? 'text-blue-600 dark:text-blue-400 font-semibold' : 'text-slate-700 dark:text-zinc-400 hover:text-slate-400 dark:hover:text-zinc-300'"
       class="block py-1 cursor-pointer sidebar-link">
        Your Endpoint
    </a>
</li>
```

2. Add the endpoint content section:
```html
<div id="your-endpoint" x-show="scrollMode || activeSection === 'your-endpoint'" :class="scrollMode ? 'mb-16' : ''">
    <!-- Your endpoint documentation here -->
</div>
```

#### Customizing the Logo

Replace the SVG logo in the header section with your own:
```html
<a href="#" class="flex items-center space-x-3">
    <!-- Your logo SVG or image here -->
    <span class="font-bold text-xl text-slate-900 dark:text-white">Your API</span>
</a>
```

### View Modes

The template supports two viewing modes:

1. **SPA Mode** (Default): Content sections are shown/hidden dynamically as you navigate
2. **Scroll Mode**: All content loads at once, menu items work as anchor links

Toggle between modes using the button in the navigation bar.

## Structure

```
documentation/
├── index.html          # Main documentation page
├── soob-logo.svg      # Logo file
└── README.md          # This file
```

## Customization Tips

1. **Update API Base URL**: Change all instances of `https://api.example.com/v1` to your actual API URL
2. **Modify Endpoints**: Update the endpoint sections with your actual API endpoints
3. **Add Authentication Details**: Update the authentication section with your specific auth method
4. **Customize Examples**: Replace example requests/responses with real data from your API
5. **Update Error Codes**: Modify the error codes table to match your API's error handling

## License

This template is free to use for personal and commercial projects.

## Credits

- Built with [Tailwind CSS](https://tailwindcss.com/)
- Powered by [Alpine.js](https://alpinejs.dev/)
- Syntax highlighting by [Highlight.js](https://highlightjs.org/)
- Logo by [Soobstudio](https://soobstudio.pl/)

## Support

For issues, questions, or suggestions, please open an issue in the repository.

---

**Note**: This is a template for API documentation. Make sure to replace all example content with your actual API details before deploying to production.
