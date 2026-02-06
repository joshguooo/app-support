# App Support Documentation

GitHub Pages site hosting terms of conditions and privacy policies for multiple apps.

## Structure

```
/app-support/
├── index.html              # Main table of contents
└── [app-name]/
    ├── toc/
    │   └── index.html      # Terms of Conditions
    └── privacy/
        └── index.html      # Privacy Policy
```

## Adding a New App

1. Create the app directory structure:
   ```bash
   mkdir -p [app-name]/toc [app-name]/privacy
   ```

2. Copy the template files from `example-app/` to your new app directory

3. Update the content in the TOC and privacy policy files

4. Add your app to the main `index.html` by adding a new app section:
   ```html
   <div class="app-section">
       <h2>Your App Name</h2>
       <p>Description of your app</p>
       <div class="links">
           <a href="/app-support/[app-name]/toc">Terms of Conditions</a>
           <a href="/app-support/[app-name]/privacy">Privacy Policy</a>
       </div>
   </div>
   ```

## GitHub Pages Setup

1. Push this repo to GitHub
2. Go to repository Settings → Pages
3. Set Source to "Deploy from a branch"
4. Select branch (usually `main`) and root directory
5. Save and wait for deployment

Your site will be available at: `https://[username].github.io/app-support/`
