<div style="font-family: Arial, sans-serif; line-height: 1.6; color: #333; margin: 0; padding: 0;">
    <h1 style="color: #007bff;">NPM Package Template Instructions</h1>
    <p>Follow these instructions to set up and publish your npm package using the provided template.</p>

    <div style="margin-bottom: 2em;">
        <h2 style="color: #007bff;">Step 1: Update Project Information</h2>
        <p>Modify the following files to include your package's metadata:</p>

        <h3 style="color: #007bff;">1. Update <code style="background-color: #f8f9fa; border-radius: 4px; padding: 0.2em 0.4em; font-size: 0.9em; color: #e83e8c;">package.json</code></h3>
        <ul style="margin: 0; padding: 0 0 0 2em;">
            <li><strong><code style="background-color: #f8f9fa; border-radius: 4px; padding: 0.2em 0.4em; font-size: 0.9em; color: #e83e8c;">"name"</code></strong>: Replace <code style="background-color: #f8f9fa; border-radius: 4px; padding: 0.2em 0.4em; font-size: 0.9em; color: #e83e8c;">"your-package-name-here"</code> with your actual package name.</li>
            <li><strong><code style="background-color: #f8f9fa; border-radius: 4px; padding: 0.2em 0.4em; font-size: 0.9em; color: #e83e8c;">"version"</code></strong>: Set the initial version of your package.</li>
            <li><strong><code style="background-color: #f8f9fa; border-radius: 4px; padding: 0.2em 0.4em; font-size: 0.9em; color: #e83e8c;">"description"</code></strong>: Provide a concise description of your package.</li>
            <li><strong><code style="background-color: #f8f9fa; border-radius: 4px; padding: 0.2em 0.4em; font-size: 0.9em; color: #e83e8c;">"author"</code></strong>: Add your name or the organization’s name.</li>
            <li><strong><code style="background-color: #f8f9fa; border-radius: 4px; padding: 0.2em 0.4em; font-size: 0.9em; color: #e83e8c;">"license"</code></strong>: Specify the license (e.g., MIT).</li>
            <li><strong><code style="background-color: #f8f9fa; border-radius: 4px; padding: 0.2em 0.4em; font-size: 0.9em; color: #e83e8c;">"repository"</code></strong>: Add the GitHub URL of the project.</li>
            <li><strong><code style="background-color: #f8f9fa; border-radius: 4px; padding: 0.2em 0.4em; font-size: 0.9em; color: #e83e8c;">"keywords"</code></strong>: List relevant keywords for better discoverability.</li>
            <li><strong><code style="background-color: #f8f9fa; border-radius: 4px; padding: 0.2em 0.4em; font-size: 0.9em; color: #e83e8c;">"homepage"</code></strong>: Add a link to the project’s website or documentation.</li>
            <li><strong><code style="background-color: #f8f9fa; border-radius: 4px; padding: 0.2em 0.4em; font-size: 0.9em; color: #e83e8c;">"bugs"</code></strong>: Provide a link to your issue tracker.</li>
        </ul>

        <pre style="background-color: #f8f9fa; border-radius: 4px; padding: 1em; overflow-x: auto;">
<code>{
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

        <h3 style="color: #007bff;">2. Update <code style="background-color: #f8f9fa; border-radius: 4px; padding: 0.2em 0.4em; font-size: 0.9em; color: #e83e8c;">rollup.config.js</code></h3>
        <p>Replace <code style="background-color: #f8f9fa; border-radius: 4px; padding: 0.2em 0.4em; font-size: 0.9em; color: #e83e8c;">"your-package-name-here"</code> with your actual package name in the Rollup configuration.</p>
    </div>

    <div style="margin-bottom: 2em;">
        <h2 style="color: #007bff;">Step 2: Organize Your Project Structure</h2>
        <p>Set up and structure the <code style="background-color: #f8f9fa; border-radius: 4px; padding: 0.2em 0.4em; font-size: 0.9em; color: #e83e8c;">/src</code> directory as needed. A common structure includes:</p>

        <pre style="background-color: #f8f9fa; border-radius: 4px; padding: 1em; overflow-x: auto;">
<code>/src
  /components  -> React components
  /hooks       -> Custom hooks
  /styles      -> Stylesheets or CSS files
  /utils       -> Utility functions</code></pre>

        <p>Ensure you import and export your components and utilities in <code style="background-color: #f8f9fa; border-radius: 4px; padding: 0.2em 0.4em; font-size: 0.9em; color: #e83e8c;">src/index.js</code>:</p>

        <pre style="background-color: #f8f9fa; border-radius: 4px; padding: 1em; overflow-x: auto;">
<code>export { default as MyComponent } from './components/MyComponent';
export { useMyCustomHook } from './hooks/useMyCustomHook';
export { myUtilityFunction } from './utils/myUtilityFunction';</code></pre>
    </div>

    <div style="margin-bottom: 2em;">
        <h2 style="color: #007bff;">Step 3: Build the Package</h2>
        <p>Run the build command from your terminal:</p>

        <pre style="background-color: #f8f9fa; border-radius: 4px; padding: 1em; overflow-x: auto;">
<code>npm run build</code></pre>

        <p>Ensure that the build completes successfully and resolve any errors that arise.</p>
    </div>

    <div style="margin-bottom: 2em;">
        <h2 style="color: #007bff;">Step 4: Publish the Package</h2>
        <h3 style="color: #007bff;">1. Login to npm</h3>
        <p>If you're not logged in, run:</p>

        <pre style="background-color: #f8f9fa; border-radius: 4px; padding: 1em; overflow-x: auto;">
<code>npm login</code></pre>

        <p>Enter your npm username, password, and email.</p>

        <h3 style="color: #007bff;">2. Publish the Package</h3>
        <p>To publish your package, run:</p>

        <pre style="background-color: #f8f9fa; border-radius: 4px; padding: 1em; overflow-x: auto;">
<code>npm publish</code></pre>

        <p>For pre-release or beta versions, use:</p>

        <pre style="background-color: #f8f9fa; border-radius: 4px; padding: 1em; overflow-x: auto;">
<code>npm publish --tag beta</code></pre>
    </div>

      <h2 style="color: #007bff;">Recap of Steps</h2>
    <ul style="margin: 0; padding: 0 0 0 2em;">
        <li>Update all fields in <code style="background-color: #f8f9fa; border-radius: 4px; padding: 0.2em 0.4em; font-size: 0.9em; color: #e83e8c;">package.json</code> and <code style="background-color: #f8f9fa; border-radius: 4px; padding: 0.2em 0.4em; font-size: 0.9em; color: #e83e8c;">rollup.config.js</code>.</li>
        <li>Structure your <code style="background-color: #f8f9fa; border-radius: 4px; padding: 0.2em 0.4em; font-size: 0.9em; color: #e83e8c;">/src</code> folder and export everything via <code style="background-color: #f8f9fa; border-radius: 4px; padding: 0.2em 0.4em; font-size: 0.9em; color: #e83e8c;">src/index.js</code>.</li>
        <li>Build the package with <code style="background-color: #f8f9fa; border-radius: 4px; padding: 0.2em 0.4em; font-size: 0.9em; color: #e83e8c;">npm run build</code>.</li>
        <li>Login to npm and publish with <code style="background-color: #f8f9fa; border-radius: 4px; padding: 0.2em 0.4em; font-size: 0.9em; color: #e83e8c;">npm publish</code>.</li>
    </ul>

    <p>Now your package is live on npm and ready for use!</p>
</div>

