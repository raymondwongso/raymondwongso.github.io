# Deployment Guide

This guide will help you deploy your resume website to GitHub Pages.

## 🚀 Quick Deployment Steps

### 1. Push to GitHub

First, commit and push all your changes to your GitHub repository:

```bash
git add .
git commit -m "Add resume website template"
git push origin main
```

### 2. Enable GitHub Pages

1. Go to your repository on GitHub: `https://github.com/raymondwongso/raymondwongso.github.io`
2. Click on **Settings** tab
3. Scroll down to **Pages** section in the left sidebar
4. Under **Source**, select **GitHub Actions**
5. The workflow will automatically run and deploy your site

### 3. Access Your Website

After the deployment is complete (usually takes 2-3 minutes), your website will be available at:
`https://raymondwongso.github.io`

## 📝 Before Deploying

Make sure to update all the sample data with your actual information:

### ✅ Update Checklist

- [ ] **Header.svelte**: Personal information, contact details
- [ ] **About.svelte**: About text and highlights
- [ ] **Experience.svelte**: Work experience and achievements
- [ ] **Projects.svelte**: Your actual projects with links
- [ ] **Skills.svelte**: Your technical skills and proficiency levels
- [ ] **Education.svelte**: Education history and certifications
- [ ] **Contact.svelte**: Contact information and social links
- [ ] **app.html**: Page title and meta description
- [ ] **package.json**: Author name and description

### 🎨 Customization Tips

1. **Colors**: Update the primary color (`#2563eb`) in the CSS to match your brand
2. **Fonts**: Change the Google Fonts import in `app.html` if desired
3. **Layout**: Modify component order in `+page.svelte`
4. **Content**: Add or remove sections as needed

## 🔄 Making Updates

After your initial deployment, any changes you push to the `main` branch will automatically trigger a new deployment.

```bash
# Make your changes
git add .
git commit -m "Update experience section"
git push origin main
```

## 🐛 Troubleshooting

### Build Fails

If the build fails in GitHub Actions:

1. Check the Actions tab in your repository
2. Look at the error logs
3. Common issues:
   - TypeScript errors (run `npm run check` locally)
   - Missing dependencies (run `npm install`)
   - Build errors (run `npm run build` locally)

### Site Not Loading

If your site doesn't load:

1. Wait 5-10 minutes after deployment
2. Check that GitHub Pages is enabled in repository settings
3. Verify the workflow completed successfully
4. Try accessing `https://yourusername.github.io` (not `http://`)

### 404 Errors

If you get 404 errors:

1. Ensure your repository is named `yourusername.github.io`
2. Check that the `build/` directory contains an `index.html` file
3. Verify the static adapter is configured correctly

## 📈 Performance Tips

1. **Images**: Optimize any images you add (use WebP format if possible)
2. **Content**: Keep content concise and focused
3. **Links**: Ensure all external links work correctly
4. **Mobile**: Test on various screen sizes

## 🔒 Security

- Never commit sensitive information (API keys, passwords)
- Use environment variables for any secrets (not needed for a static resume site)
- Keep dependencies updated regularly

## 📊 Analytics (Optional)

To track visitors, you can add Google Analytics:

1. Get a Google Analytics tracking ID
2. Add the tracking script to `src/app.html`
3. Respect privacy laws (GDPR, CCPA) if applicable

## 🎯 SEO Optimization

The template includes basic SEO:

- Semantic HTML structure
- Meta tags
- Proper heading hierarchy
- Descriptive link text

For better SEO:

1. Add more specific meta descriptions
2. Include structured data (JSON-LD)
3. Optimize for relevant keywords
4. Submit to Google Search Console

---

Need help? Check the GitHub repository issues or create a new one for support!
