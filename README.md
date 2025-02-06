# docs

## MDX Setup

To support JSX in MDX, we use the `rehype-raw` plugin. This allows us to parse and render raw HTML within MDX files.

## GitHub Pages Deployment

We use GitHub Actions to deploy our site to GitHub Pages. The deployment workflow is defined in the `.github/workflows/deploy.yml` file.

## MDX and GitHub Pages

To set up MDX with JSX support and deploy to GitHub Pages, follow these steps:

1. Add `rehype-raw` to the `rehypePlugins` array in `next.config.js`.
2. Ensure `pageExtensions` includes `mdx` in `next.config.js`.
3. Add `@mdx-js/loader` to `dependencies` in `package.json`.
4. Add `gh-pages` to `devDependencies` in `package.json`.
5. Add a `deploy` script to `scripts` in `package.json`.
6. Create a simple React component with a heading in `pages/index.js`.
7. Ensure the `publish_dir` is set to `./out` in `.github/workflows/deploy.yml`.
