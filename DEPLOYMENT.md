# Deployment Guide — GitHub Pages

This portfolio is automatically deployed to GitHub Pages using GitHub Actions.

## ✅ Current Setup

- **Base Path:** `/Professional-Portfolio/`
- **Build Tool:** Vite
- **Deployment:** GitHub Actions (auto-build on push)
- **Branch:** `main`

## 🚀 Live URL

Once GitHub Pages is enabled, your portfolio will be live at:

```
https://tekigowtham2204.github.io/Professional-Portfolio/
```

## ⚙️ Enable GitHub Pages

1. Go to your repository: [Professional-Portfolio Settings](https://github.com/tekigowtham2204/Professional-Portfolio/settings)
2. Scroll to **Pages** section (left sidebar)
3. Under "Source", select:
   - **Deploy from a branch**
   - Branch: **main**
   - Folder: **/ (root)**
4. Click **Save**

Alternatively, GitHub Pages may auto-detect the GitHub Actions workflow and use `gh-pages` branch.

## 🔄 How It Works

The GitHub Actions workflow (`.github/workflows/deploy.yml`) automatically:

1. **On Push to Main:**
   - Installs dependencies (`npm install`)
   - Builds the project (`npm run build`)
   - Uploads the `dist/` folder as a GitHub Pages artifact
   - Deploys to GitHub Pages

2. **Result:** Your portfolio is live at the GitHub Pages URL above

## 📝 Build Output

When you build locally:

```bash
npm run build
```

This generates a production-optimized `dist/` folder with:
- Minified HTML, CSS, JavaScript
- Optimized assets and images
- Proper base path routing for GitHub Pages

## 🔗 Update Links

All internal links in your portfolio are automatically prefixed with `/Professional-Portfolio/` due to the Vite base path configuration.

## 📊 Deployment Status

Check deployment status:
- Go to **Actions** tab in your repository
- View the latest workflow run
- Click **deploy** job to see logs

## 🆘 Troubleshooting

**Portfolio not loading?**
- Wait 1-2 minutes after enabling GitHub Pages
- Check Actions tab for build errors
- Verify base path in `vite.config.ts`

**Assets not loading?**
- Ensure `vite.config.ts` has `base: '/Professional-Portfolio/'`
- Check browser console for path errors

**Blank page?**
- Check if `npm run build` runs successfully locally
- Verify `dist/index.html` exists after build

## 🎯 Custom Domain

To use a custom domain instead of `github.io`:

1. Update DNS records pointing to GitHub Pages IPs
2. In repo settings > Pages, enter custom domain under "Custom domain"
3. GitHub will create a `CNAME` file automatically

## 📚 Resources

- [GitHub Pages Documentation](https://docs.github.com/en/pages)
- [GitHub Actions Documentation](https://docs.github.com/en/actions)
- [Vite Deployment Guide](https://vitejs.dev/guide/static-deploy.html#github-pages)

---

**Next Steps:**
1. Enable GitHub Pages in repository settings
2. Wait for first deployment to complete
3. Visit `https://tekigowtham2204.github.io/Professional-Portfolio/`
