# NPM Package Template Instructions

Follow these steps to set up and publish your npm package using the provided template.

## Step 1: Update Project Information

Modify the following files to include your package's metadata:

### 1. Update `package.json`

- **`"name"`**: Replace `"your-package-name-here"` with your actual package name.
- **`"version"`**: Set the initial version of your package.
- **`"description"`**: Provide a concise description of your package.
- **`"author"`**: Add your name or the organization’s name.
- **`"license"`**: Specify the license (e.g., MIT).
- **`"repository"`**: Add the GitHub URL of the project.
- **`"keywords"`**: List relevant keywords for better discoverability.
- **`"homepage"`**: Add a link to the project’s website or documentation.
- **`"bugs"`**: Provide a link to your issue tracker.

Example `package.json`:

```json
{
  "name": "your-awesome-package",
  "version": "1.0.0",
  "description": "A concise description of your package",
  "author": "Your Name",
  "license": "MIT",
  "repository": {
    "type": "git",
    "url": "https://github.com/yourname/your-awesome-package"
  },
  "keywords": ["keyword1", "keyword2", "react", "npm-package"]
}
```
### 2. Update rollup.config.js
Replace "your-package-name-here" with your actual package name in the Rollup configuration.

## Step 2. Organize Your Project Structure
Set up the /src directory as needed. A common structure includes:

```bash
/src
  /components  -> React components
  /hooks       -> Custom hooks
  /styles      -> Stylesheets or CSS files
  /utils       -> Utility functions
  /index.js
```

Ensure you import and export your components and utilities in `src/index.js`:

```js
// Import styles
import './styles.css';

// Import components and hooks
import MyComponent from './components/MyComponent';
import { useMyCustomHook } from './hooks/useMyCustomHook';
import { myUtilityFunction } from './utils/myUtilityFunction';

// Export components and hooks
export { default as MyComponent } from './components/MyComponent';
export { useMyCustomHook } from './hooks/useMyCustomHook';
export { myUtilityFunction } from './utils/myUtilityFunction';
```

## Step 3: Build the Package
Run the build command from your terminal:

```bash
npm run build
```

## Step 4: Publish the Package

### 1. Login to npm
If you're not logged in, run:

```bash
npm login
```

### 2. Publish the Package
To publish the package, run:

```bash
npm publish
```

For pre-release or beta versions, use:

```bash
npm publish --tag beta
```

## Recap of Steps:

- Update all fields in `package.json` and `rollup.config.js`.
- Structure your `/src folder` and export everything via `src/index.js`.
- Build the package with `npm run build`.
- Login to npm and publish with `npm publish`.

Your package is now live on npm and ready for use!
