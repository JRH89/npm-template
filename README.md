<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Package Setup Instructions</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            line-height: 1.6;
            color: #333;
            margin: 0;
            padding: 0;
        }
        h1, h2, h3 {
            color: #007bff;
        }
        code {
            background-color: #f8f9fa;
            border-radius: 4px;
            padding: 0.2em 0.4em;
            font-size: 0.9em;
            color: #e83e8c;
        }
        pre {
            background-color: #f8f9fa;
            border-radius: 4px;
            padding: 1em;
            overflow-x: auto;
        }
        .step {
            margin-bottom: 2em;
        }
        .step h2 {
            margin-bottom: 0.5em;
        }
        ul {
            margin: 0;
            padding: 0 0 0 2em;
        }
    </style>
</head>
<body>
    <h1>NPM Package Template Instructions</h1>
    <p>Follow these instructions to set up and publish your npm package using the provided template.</p>

    <div class="step">
        <h2>Step 1: Update Project Information</h2>
        <p>Modify the following files to include your package's metadata:</p>

        <h3>1. Update <code>package.json</code></h3>
        <ul>
            <li><strong><code>"name"</code></strong>: Replace <code>"your-package-name-here"</code> with your actual package name.</li>
            <li><strong><code>"version"</code></strong>: Set the initial version of your package.</li>
            <li><strong><code>"description"</code></strong>: Provide a concise description of your package.</li>
            <li><strong><code>"author"</code></strong>: Add your name or the organization’s name.</li>
            <li><strong><code>"license"</code></strong>: Specify the license (e.g., MIT).</li>
            <li><strong><code>"repository"</code></strong>: Add the GitHub URL of the project.</li>
            <li><strong><code>"keywords"</code></strong>: List relevant keywords for better discoverability.</li>
            <li><strong><code>"homepage"</code></strong>: Add a link to the project’s website or documentation.</li>
            <li><strong><code>"bugs"</code></strong>: Provide a link to your issue tracker.</li>
        </ul>

        <pre><code>{
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
}</code></pre>

        <h3>2. Update <code>rollup.config.js</code></h3>
        <p>Replace <code>"your-package-name-here"</code> with your actual package name in the Rollup configuration.</p>
    </div>

    <div class="step">
        <h2>Step 2: Organize Your Project Structure</h2>
        <p>Set up and structure the <code>/src</code> directory as needed. Common structure includes:</p>

        <pre><code>/src
  /components  -> React components
  /hooks       -> Custom hooks
  /styles      -> Stylesheets or CSS files
  /utils       -> Utility functions</code></pre>

        <p>Ensure you import and export your components and utilities in <code>src/index.js</code>:</p>

        <pre><code>export { default as MyComponent } from './components/MyComponent';
export { useMyCustomHook } from './hooks/useMyCustomHook';
export { myUtilityFunction } from './utils/myUtilityFunction';</code></pre>
    </div>

    <div class="step">
        <h2>Step 3: Build the Package</h2>
        <p>Run the build command from your terminal:</p>

        <pre><code>npm run build</code></pre>

        <p>Ensure that the build completes successfully and resolve any errors that arise.</p>
    </div>

    <div class="step">
        <h2>Step 4: Publish the Package</h2>
        <h3>1. Login to npm</h3>
        <p>If you're not logged in, run:</p>

        <pre><code>npm login</code></pre>

        <p>Enter your npm username, password, and email.</p>

        <h3>2. Publish the Package</h3>
        <p>To publish your package, run:</p>

        <pre><code>npm publish</code></pre>

        <p>For pre-release or beta versions, use:</p>

        <pre><code>npm publish --tag beta</code></pre>
    </div>

    <h2>Recap of Steps</h2>
    <ul>
        <li>Update all fields in <code>package.json</code> and <code>rollup.config.js</code>.</li>
        <li>Structure your <code>/src</code> folder and export everything via <code>src/index.js</code>.</li>
        <li>Build the package with <code>npm run build</code>.</li>
        <li>Login to npm and publish with <code>npm publish</code>.</li>
    </ul>

    <p>Now your package is live on npm and ready for use!</p>
</body>
</html>
