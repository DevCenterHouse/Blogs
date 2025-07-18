
<div class="inside-article">
<header aria-label="Content" class="entry-header">
<h1 class="entry-title" itemprop="headline">Using Environment Variables in NestJS Projects</h1> 
</header>
<div class="featured-image cv-col-12 post-image">
<img alt="" class="size-full cv-col-12 wp-post-image" decoding="async" fetchpriority="high" height="1080" itemprop="image" sizes="(max-width: 1920px) 100vw, 1920px" src="https://www.devcentrehouse.eu/blogs/wp-content/uploads/2025/05/nest-env.jpg" srcset="https://www.devcentrehouse.eu/blogs/wp-content/uploads/2025/05/nest-env.jpg 1920w, https://www.devcentrehouse.eu/blogs/wp-content/uploads/2025/05/nest-env-300x169.jpg 300w, https://www.devcentrehouse.eu/blogs/wp-content/uploads/2025/05/nest-env-1024x576.jpg 1024w, https://www.devcentrehouse.eu/blogs/wp-content/uploads/2025/05/nest-env-768x432.jpg 768w, https://www.devcentrehouse.eu/blogs/wp-content/uploads/2025/05/nest-env-1536x864.jpg 1536w" style="aspect-ratio:0;" width="1920"/> </div>
<div class="entry-content" itemprop="text">
<p>When building modern applications, configuration flexibility is essential. Hardcoding sensitive data such as API keys, database URLs, or secrets directly into your codebase is a recipe for trouble. That’s where <strong>environment variables in NestJS</strong> shine.<br/>NestJS supports environment variables out of the box via its built-in <code>@nestjs/config</code> package, helping developers write clean, secure, and easily configurable applications.<br/>In this article, you’ll learn how to set up, use, and manage environment variables in your NestJS project the right way.</p>
<h2 class="wp-block-heading">Why Use Environment Variables?</h2>
<p>Environment variables offer a secure and flexible way to manage configuration values. By storing credentials, tokens, and configuration settings outside your source code, you can:</p>
<ul class="wp-block-list">
<li>Keep secrets out of version control</li>
<li>Easily switch configurations between development, staging, and production</li>
<li>Avoid code repetition and simplify deployments</li>
</ul>
<h2 class="wp-block-heading">Setting Up Environment Variables in NestJS</h2>
<p>To begin using environment variables in your NestJS app, install the official <code>@nestjs/config</code> package:</p>
<pre class="wp-block-preformatted">npm install @nestjs/config</pre>
<p>Then import <code>ConfigModule</code> into your <code>AppModule</code>:</p>
<figure class="wp-block-image size-large"><img alt="" class="wp-image-1756" decoding="async" height="286" sizes="(max-width: 1024px) 100vw, 1024px" src="https://www.devcentrehouse.eu/blogs/wp-content/uploads/2025/05/Screenshot-2025-05-15-at-12.35.38-1024x286.png" srcset="https://www.devcentrehouse.eu/blogs/wp-content/uploads/2025/05/Screenshot-2025-05-15-at-12.35.38-1024x286.png 1024w, https://www.devcentrehouse.eu/blogs/wp-content/uploads/2025/05/Screenshot-2025-05-15-at-12.35.38-300x84.png 300w, https://www.devcentrehouse.eu/blogs/wp-content/uploads/2025/05/Screenshot-2025-05-15-at-12.35.38-768x214.png 768w, https://www.devcentrehouse.eu/blogs/wp-content/uploads/2025/05/Screenshot-2025-05-15-at-12.35.38-1536x428.png 1536w, https://www.devcentrehouse.eu/blogs/wp-content/uploads/2025/05/Screenshot-2025-05-15-at-12.35.38.png 1556w" width="1024"/></figure>
<p>Create a <code>.env</code> file in your root directory:</p>
<figure class="wp-block-image size-large"><img alt="" class="wp-image-1757" decoding="async" height="103" sizes="(max-width: 1024px) 100vw, 1024px" src="https://www.devcentrehouse.eu/blogs/wp-content/uploads/2025/05/Screenshot-2025-05-15-at-12.36.18-1024x103.png" srcset="https://www.devcentrehouse.eu/blogs/wp-content/uploads/2025/05/Screenshot-2025-05-15-at-12.36.18-1024x103.png 1024w, https://www.devcentrehouse.eu/blogs/wp-content/uploads/2025/05/Screenshot-2025-05-15-at-12.36.18-300x30.png 300w, https://www.devcentrehouse.eu/blogs/wp-content/uploads/2025/05/Screenshot-2025-05-15-at-12.36.18-768x77.png 768w, https://www.devcentrehouse.eu/blogs/wp-content/uploads/2025/05/Screenshot-2025-05-15-at-12.36.18-1536x154.png 1536w, https://www.devcentrehouse.eu/blogs/wp-content/uploads/2025/05/Screenshot-2025-05-15-at-12.36.18.png 1552w" width="1024"/></figure>
<p>Now these variables are accessible throughout your app using <code>ConfigService</code>.</p>
<h2 class="wp-block-heading">Accessing Environment Variables</h2>
<p>To access environment variables inside services, controllers, or providers, inject <code>ConfigService</code>:</p>
<figure class="wp-block-image size-large"><img alt="" class="wp-image-1758" decoding="async" height="238" loading="lazy" sizes="auto, (max-width: 1024px) 100vw, 1024px" src="https://www.devcentrehouse.eu/blogs/wp-content/uploads/2025/05/Screenshot-2025-05-15-at-12.36.59-1024x238.png" srcset="https://www.devcentrehouse.eu/blogs/wp-content/uploads/2025/05/Screenshot-2025-05-15-at-12.36.59-1024x238.png 1024w, https://www.devcentrehouse.eu/blogs/wp-content/uploads/2025/05/Screenshot-2025-05-15-at-12.36.59-300x70.png 300w, https://www.devcentrehouse.eu/blogs/wp-content/uploads/2025/05/Screenshot-2025-05-15-at-12.36.59-768x179.png 768w, https://www.devcentrehouse.eu/blogs/wp-content/uploads/2025/05/Screenshot-2025-05-15-at-12.36.59-1536x358.png 1536w, https://www.devcentrehouse.eu/blogs/wp-content/uploads/2025/05/Screenshot-2025-05-15-at-12.36.59.png 1546w" width="1024"/></figure>
<p>The second argument to <code>.get()</code> is a default value in case the environment variable isn’t set.</p>
<h2 class="wp-block-heading">Validating Environment Variables</h2>
<p>A best practice is to validate your <code>.env</code> variables to avoid runtime errors. Use the <code>Joi</code> library for schema validation:</p>
<pre class="wp-block-preformatted">npm install joi</pre>
<p>Update <code>ConfigModule</code> setup:</p>
<figure class="wp-block-image size-large"><img alt="" class="wp-image-1759" decoding="async" height="246" loading="lazy" sizes="auto, (max-width: 1024px) 100vw, 1024px" src="https://www.devcentrehouse.eu/blogs/wp-content/uploads/2025/05/Screenshot-2025-05-15-at-12.37.21-1024x246.png" srcset="https://www.devcentrehouse.eu/blogs/wp-content/uploads/2025/05/Screenshot-2025-05-15-at-12.37.21-1024x246.png 1024w, https://www.devcentrehouse.eu/blogs/wp-content/uploads/2025/05/Screenshot-2025-05-15-at-12.37.21-300x72.png 300w, https://www.devcentrehouse.eu/blogs/wp-content/uploads/2025/05/Screenshot-2025-05-15-at-12.37.21-768x184.png 768w, https://www.devcentrehouse.eu/blogs/wp-content/uploads/2025/05/Screenshot-2025-05-15-at-12.37.21-1536x369.png 1536w, https://www.devcentrehouse.eu/blogs/wp-content/uploads/2025/05/Screenshot-2025-05-15-at-12.37.21.png 1550w" width="1024"/></figure>
<p>This ensures that your app won’t start if essential environment variables are missing or incorrectly typed.</p>
<h2 class="wp-block-heading">Using Multiple .env Files</h2>
<p>For better organisation across environments, you can specify different <code>.env</code> files like:</p>
<ul class="wp-block-list">
<li><code>.env</code> for default values</li>
<li><code>.env.development</code></li>
<li><code>.env.production</code><br/>Set <code>envFilePath</code> dynamically based on the <code>NODE_ENV</code>:</li>
</ul>
<figure class="wp-block-image size-large"><img alt="" class="wp-image-1760" decoding="async" height="124" loading="lazy" sizes="auto, (max-width: 1024px) 100vw, 1024px" src="https://www.devcentrehouse.eu/blogs/wp-content/uploads/2025/05/Screenshot-2025-05-15-at-12.37.40-1024x124.png" srcset="https://www.devcentrehouse.eu/blogs/wp-content/uploads/2025/05/Screenshot-2025-05-15-at-12.37.40-1024x124.png 1024w, https://www.devcentrehouse.eu/blogs/wp-content/uploads/2025/05/Screenshot-2025-05-15-at-12.37.40-300x36.png 300w, https://www.devcentrehouse.eu/blogs/wp-content/uploads/2025/05/Screenshot-2025-05-15-at-12.37.40-768x93.png 768w, https://www.devcentrehouse.eu/blogs/wp-content/uploads/2025/05/Screenshot-2025-05-15-at-12.37.40-1536x186.png 1536w, https://www.devcentrehouse.eu/blogs/wp-content/uploads/2025/05/Screenshot-2025-05-15-at-12.37.40.png 1552w" width="1024"/></figure>
<p>Set the <code>NODE_ENV</code> in your scripts:</p>
<figure class="wp-block-image size-large"><img alt="" class="wp-image-1761" decoding="async" height="125" loading="lazy" sizes="auto, (max-width: 1024px) 100vw, 1024px" src="https://www.devcentrehouse.eu/blogs/wp-content/uploads/2025/05/Screenshot-2025-05-15-at-12.38.12-1024x125.png" srcset="https://www.devcentrehouse.eu/blogs/wp-content/uploads/2025/05/Screenshot-2025-05-15-at-12.38.12-1024x125.png 1024w, https://www.devcentrehouse.eu/blogs/wp-content/uploads/2025/05/Screenshot-2025-05-15-at-12.38.12-300x37.png 300w, https://www.devcentrehouse.eu/blogs/wp-content/uploads/2025/05/Screenshot-2025-05-15-at-12.38.12-768x94.png 768w, https://www.devcentrehouse.eu/blogs/wp-content/uploads/2025/05/Screenshot-2025-05-15-at-12.38.12-1536x188.png 1536w, https://www.devcentrehouse.eu/blogs/wp-content/uploads/2025/05/Screenshot-2025-05-15-at-12.38.12.png 1556w" width="1024"/></figure>
<h2 class="wp-block-heading">Security Considerations</h2>
<ul class="wp-block-list">
<li>Never commit your <code>.env</code> files to version control — use <code>.gitignore</code></li>
<li>Store production secrets securely using CI/CD secrets or managed services (e.g., AWS Secrets Manager)</li>
<li>Always validate and sanitize values coming from the environment</li>
</ul>
<h2 class="wp-block-heading">Real-World Use Cases</h2>
<p>You can use environment variables to configure:</p>
<ul class="wp-block-list">
<li>Database connection strings</li>
<li>API base URLs</li>
<li>3rd-party keys (Stripe, Twilio, Firebase)</li>
<li>Feature flags</li>
<li>Logging levels</li>
<li>Environment-specific configurations</li>
</ul>
<h2 class="wp-block-heading">Final Thoughts</h2>
<figure class="wp-block-image size-large"><img alt="" class="wp-image-1754" decoding="async" height="576" loading="lazy" sizes="auto, (max-width: 1024px) 100vw, 1024px" src="https://www.devcentrehouse.eu/blogs/wp-content/uploads/2025/05/node-dch-latest-2-1024x576.jpg" srcset="https://www.devcentrehouse.eu/blogs/wp-content/uploads/2025/05/node-dch-latest-2-1024x576.jpg 1024w, https://www.devcentrehouse.eu/blogs/wp-content/uploads/2025/05/node-dch-latest-2-300x169.jpg 300w, https://www.devcentrehouse.eu/blogs/wp-content/uploads/2025/05/node-dch-latest-2-768x432.jpg 768w, https://www.devcentrehouse.eu/blogs/wp-content/uploads/2025/05/node-dch-latest-2-1536x864.jpg 1536w, https://www.devcentrehouse.eu/blogs/wp-content/uploads/2025/05/node-dch-latest-2.jpg 1920w" width="1024"/></figure>
<p><br/>Using <strong>environment variables in NestJS</strong> projects ensures that your app remains secure, flexible, and easy to manage across different environments. By leveraging the power of <code>@nestjs/config</code>, you get seamless integration with validation and support for multiple configurations out of the box.<br/>Ready to take your Node.js backend to the next level? Discover how professional teams manage configurations and build scalable architectures with <a href="https://www.devcentrehouse.eu/en/technologies/back-end/nodejs">NestJS and Node.js at Dev Centre House Ireland</a>.</p>
<!--— Calendly inline widget begin ---->


<!--— Calendly inline widget end ---->
</div> <footer aria-label="Entry meta" class="entry-meta">
</footer>
</div>
