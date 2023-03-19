# vue_app

How Deploy vue 3 (Vite) to github pages

1. Set base to vite.config.js

```javascript
export default defineConfig({
  base:
    process.env.NODE_ENV === "production"
      ? "/YOUR_PROJECT_NAME/" // production
      : "/", // development
});
```

2. Remove dist from .gitignore
3. build project

```
npm run build
```

4. Make sure to commit & push origin master/main

5. Use subtree

```
 git subtree push --prefix dist origin gh-pages

```

6. Go to your project repo & open settings > pages > on Build and deployment
   branch change to gh-pages & save.
7. Done. Visite site
