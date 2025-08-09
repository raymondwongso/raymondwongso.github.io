# Raymond Wongso - Resume Website

A modern, elegant resume website built with SvelteKit and TypeScript. This project showcases professional experience, projects, skills, and education in a clean, responsive design.

## 🚀 Features

- **Responsive Design**: Looks great on desktop, tablet, and mobile devices
- **Modern UI**: Clean and professional design with smooth transitions
- **TypeScript**: Full type safety throughout the application
- **Component-Based**: Modular components for easy customization
- **Performance**: Fast loading and optimized for web performance
- **SEO Friendly**: Proper meta tags and semantic HTML

## 🛠️ Tech Stack

- **Framework**: SvelteKit
- **Language**: TypeScript
- **Styling**: CSS with custom properties
- **Fonts**: Inter (Google Fonts)
- **Build Tool**: Vite
- **Hosting**: GitHub Pages (recommended)

## 📁 Project Structure

```
src/
├── routes/
│   └── +page.svelte          # Main page
├── lib/
│   └── components/
│       ├── Header.svelte      # Personal info and contact details
│       ├── About.svelte       # About section
│       ├── Experience.svelte  # Work experience
│       ├── Projects.svelte    # Featured projects
│       ├── Skills.svelte      # Technical skills
│       ├── Education.svelte   # Education and certifications
│       └── Contact.svelte     # Contact information
└── app.html                   # HTML template
```

## 🎨 Customization

### 1. Personal Information

Update the personal information in each component:

**Header.svelte**: Update the `personalInfo` object with your details
**About.svelte**: Replace the `aboutText` and `highlights` with your information
**Experience.svelte**: Replace the `experiences` array with your work history
**Projects.svelte**: Update the `projects` array with your projects
**Skills.svelte**: Modify the `skillCategories` array with your technical skills
**Education.svelte**: Update the `education` and `certifications` arrays
**Contact.svelte**: Update the `contactInfo` object with your contact details

### 2. Styling

The website uses a consistent color scheme and typography. Key design tokens:

- **Primary Color**: `#2563eb` (blue)
- **Text Colors**: `#1a1a1a` (dark), `#4b5563` (medium), `#6b7280` (light)
- **Background**: `#fafafa` (light gray)
- **Font**: Inter (Google Fonts)

### 3. Adding New Sections

To add new sections:

1. Create a new component in `src/lib/components/`
2. Import and use it in `src/routes/+page.svelte`
3. Follow the existing styling patterns

## 🚀 Development

### Prerequisites

- Node.js (v18 or higher)
- npm

### Getting Started

1. **Install dependencies**:
   ```bash
   npm install
   ```

2. **Start development server**:
   ```bash
   npm run dev
   ```

3. **Open your browser**:
   Navigate to `http://localhost:5173`

### Available Scripts

- `npm run dev` - Start development server
- `npm run build` - Build for production
- `npm run preview` - Preview production build
- `npm run check` - Run TypeScript checks
- `npm run lint` - Run linter (if configured)

## 📦 Building for Production

1. **Build the project**:
   ```bash
   npm run build
   ```

2. **Preview the build**:
   ```bash
   npm run preview
   ```

The build output will be in the `build/` directory.

## 🌐 Deployment

### GitHub Pages

1. Build the project for static hosting:
   ```bash
   npm run build
   ```

2. Configure SvelteKit for static deployment by adding to `svelte.config.js`:
   ```js
   import adapter from '@sveltejs/adapter-static';
   
   export default {
     kit: {
       adapter: adapter({
         pages: 'build',
         assets: 'build',
         fallback: null,
         precompress: false,
         strict: true
       })
     }
   };
   ```

3. Add a `.nojekyll` file to the `static/` directory

4. Deploy the `build/` directory to GitHub Pages

### Other Platforms

- **Vercel**: Connect your GitHub repository and deploy automatically
- **Netlify**: Drag and drop the `build/` folder or connect via Git
- **Firebase Hosting**: Use Firebase CLI to deploy

## 📝 Content Guidelines

### Writing Tips

- **Be Concise**: Keep descriptions clear and to the point
- **Use Action Verbs**: Start bullet points with strong action verbs
- **Quantify Results**: Include numbers and metrics where possible
- **Show Impact**: Focus on achievements and outcomes

### Project Descriptions

For each project, include:
- Brief description of what it does
- Technologies used
- Key features or achievements
- Links to live demo and/or code repository

### Skills Organization

Skills are organized by category:
- Programming Languages
- Frontend Technologies
- Backend Technologies
- Databases
- Cloud & DevOps
- Tools & Others

Rate your skills honestly:
- **Expert**: 5+ years, can teach others
- **Advanced**: 3-5 years, very comfortable
- **Intermediate**: 1-3 years, can work independently
- **Beginner**: < 1 year, still learning

## 🎯 Best Practices

1. **Keep it Updated**: Regularly update your experience and projects
2. **Mobile-First**: Test on mobile devices frequently
3. **Performance**: Optimize images and minimize bundle size
4. **Accessibility**: Ensure proper contrast and semantic HTML
5. **SEO**: Use descriptive titles and meta descriptions

## 📄 License

This project is open source and available under the [MIT License](LICENSE).

## 🤝 Contributing

Feel free to submit issues and pull requests to improve this template!

---

**Note**: This is a template with sample data. Make sure to replace all placeholder content with your actual information before deploying.
