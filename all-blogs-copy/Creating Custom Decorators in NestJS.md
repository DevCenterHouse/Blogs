
<div class="inside-article">
<header aria-label="Content" class="entry-header">
<h1 class="entry-title" itemprop="headline">Creating Custom Decorators in NestJS</h1> 
</header>
<div class="featured-image cv-col-12 post-image">
<img alt="" class="size-full cv-col-12 wp-post-image" decoding="async" fetchpriority="high" height="1080" itemprop="image" sizes="(max-width: 1920px) 100vw, 1920px" src="https://www.devcentrehouse.eu/blogs/wp-content/uploads/2025/05/nestjs-decorators.jpg" srcset="https://www.devcentrehouse.eu/blogs/wp-content/uploads/2025/05/nestjs-decorators.jpg 1920w, https://www.devcentrehouse.eu/blogs/wp-content/uploads/2025/05/nestjs-decorators-300x169.jpg 300w, https://www.devcentrehouse.eu/blogs/wp-content/uploads/2025/05/nestjs-decorators-1024x576.jpg 1024w, https://www.devcentrehouse.eu/blogs/wp-content/uploads/2025/05/nestjs-decorators-768x432.jpg 768w, https://www.devcentrehouse.eu/blogs/wp-content/uploads/2025/05/nestjs-decorators-1536x864.jpg 1536w" style="aspect-ratio:0;" width="1920"/> </div>
<div class="entry-content" itemprop="text">
<p><br/>NestJS, with its modular and expressive syntax, is built around decorators. While Nest provides a wide variety of built-in decorators—like @Controller(), @Injectable(), and @Get()—you’re not limited to just those. In fact, one of the most powerful features of NestJS is the ability to create your own custom decorator to encapsulate logic, improve readability, and promote code reuse.<br/>In this guide, we’ll explore how to build and use <strong>custom decorators in NestJS</strong>, explain when to use them, and show practical examples.</p>
<h2 class="wp-block-heading">What Are Decorators in NestJS?</h2>
<p>Decorators are special functions prefixed with <code>@</code> that attach metadata to classes, methods, properties, or parameters. NestJS uses decorators heavily for things like routing, dependency injection, and more.<br/>Custom decorators let you extend this concept by defining your own annotations for frequently-used logic or patterns.</p>
<h2 class="wp-block-heading">Why Create Custom Decorators?</h2>
<p>Here’s why custom decorators can improve your codebase:</p>
<ul class="wp-block-list">
<li><strong>Code Reusability</strong>: Extract repeating logic into reusable decorators.</li>
<li><strong>Cleaner Controllers</strong>: Keep controllers lean and readable by offloading responsibilities.</li>
<li><strong>Separation of Concerns</strong>: Abstract away logic like authentication, permissions, or metadata extraction.</li>
</ul>
<h2 class="wp-block-heading">Creating a Simple Parameter Decorator</h2>
<p>Let’s start with a basic example: a decorator that retrieves the current user from the request object.</p>
<h3 class="wp-block-heading"><code>@CurrentUser()</code> Decorator</h3>
<figure class="wp-block-image size-large"><img alt="" class="wp-image-1744" decoding="async" height="220" sizes="(max-width: 1024px) 100vw, 1024px" src="https://www.devcentrehouse.eu/blogs/wp-content/uploads/2025/05/Screenshot-2025-05-15-at-10.04.07-1024x220.png" srcset="https://www.devcentrehouse.eu/blogs/wp-content/uploads/2025/05/Screenshot-2025-05-15-at-10.04.07-1024x220.png 1024w, https://www.devcentrehouse.eu/blogs/wp-content/uploads/2025/05/Screenshot-2025-05-15-at-10.04.07-300x64.png 300w, https://www.devcentrehouse.eu/blogs/wp-content/uploads/2025/05/Screenshot-2025-05-15-at-10.04.07-768x165.png 768w, https://www.devcentrehouse.eu/blogs/wp-content/uploads/2025/05/Screenshot-2025-05-15-at-10.04.07-1536x330.png 1536w, https://www.devcentrehouse.eu/blogs/wp-content/uploads/2025/05/Screenshot-2025-05-15-at-10.04.07.png 1546w" width="1024"/></figure>
<p>Usage in a controller:</p>
<figure class="wp-block-image size-large"><img alt="" class="wp-image-1745" decoding="async" height="128" sizes="(max-width: 1024px) 100vw, 1024px" src="https://www.devcentrehouse.eu/blogs/wp-content/uploads/2025/05/Screenshot-2025-05-15-at-10.05.28-1024x128.png" srcset="https://www.devcentrehouse.eu/blogs/wp-content/uploads/2025/05/Screenshot-2025-05-15-at-10.05.28-1024x128.png 1024w, https://www.devcentrehouse.eu/blogs/wp-content/uploads/2025/05/Screenshot-2025-05-15-at-10.05.28-300x38.png 300w, https://www.devcentrehouse.eu/blogs/wp-content/uploads/2025/05/Screenshot-2025-05-15-at-10.05.28-768x96.png 768w, https://www.devcentrehouse.eu/blogs/wp-content/uploads/2025/05/Screenshot-2025-05-15-at-10.05.28-1536x192.png 1536w, https://www.devcentrehouse.eu/blogs/wp-content/uploads/2025/05/Screenshot-2025-05-15-at-10.05.28.png 1548w" width="1024"/></figure>
<p>This avoids repeating <code>request.user</code> logic inside every controller.</p>
<h2 class="wp-block-heading">Creating a Custom Method Decorator</h2>
<p>Method decorators are ideal for cross-cutting concerns like logging or authorization. Let’s create a custom role-checking decorator.</p>
<h3 class="wp-block-heading"><code>@Roles()</code> Decorator</h3>
<figure class="wp-block-image size-large"><img alt="" class="wp-image-1746" decoding="async" height="122" loading="lazy" sizes="auto, (max-width: 1024px) 100vw, 1024px" src="https://www.devcentrehouse.eu/blogs/wp-content/uploads/2025/05/Screenshot-2025-05-15-at-10.05.49-1024x122.png" srcset="https://www.devcentrehouse.eu/blogs/wp-content/uploads/2025/05/Screenshot-2025-05-15-at-10.05.49-1024x122.png 1024w, https://www.devcentrehouse.eu/blogs/wp-content/uploads/2025/05/Screenshot-2025-05-15-at-10.05.49-300x36.png 300w, https://www.devcentrehouse.eu/blogs/wp-content/uploads/2025/05/Screenshot-2025-05-15-at-10.05.49-768x91.png 768w, https://www.devcentrehouse.eu/blogs/wp-content/uploads/2025/05/Screenshot-2025-05-15-at-10.05.49-1536x182.png 1536w, https://www.devcentrehouse.eu/blogs/wp-content/uploads/2025/05/Screenshot-2025-05-15-at-10.05.49.png 1550w" width="1024"/></figure>
<p>This decorator doesn’t contain logic itself—it simply sets metadata. You’d use it alongside a guard:</p>
<figure class="wp-block-image size-large"><img alt="" class="wp-image-1747" decoding="async" height="146" loading="lazy" sizes="auto, (max-width: 1024px) 100vw, 1024px" src="https://www.devcentrehouse.eu/blogs/wp-content/uploads/2025/05/Screenshot-2025-05-15-at-10.06.05-1024x146.png" srcset="https://www.devcentrehouse.eu/blogs/wp-content/uploads/2025/05/Screenshot-2025-05-15-at-10.06.05-1024x146.png 1024w, https://www.devcentrehouse.eu/blogs/wp-content/uploads/2025/05/Screenshot-2025-05-15-at-10.06.05-300x43.png 300w, https://www.devcentrehouse.eu/blogs/wp-content/uploads/2025/05/Screenshot-2025-05-15-at-10.06.05-768x110.png 768w, https://www.devcentrehouse.eu/blogs/wp-content/uploads/2025/05/Screenshot-2025-05-15-at-10.06.05-1536x219.png 1536w, https://www.devcentrehouse.eu/blogs/wp-content/uploads/2025/05/Screenshot-2025-05-15-at-10.06.05.png 1554w" width="1024"/></figure>
<p>Then a <code>RolesGuard</code> would read the metadata and decide access.</p>
<h2 class="wp-block-heading">Custom Class Decorator Example</h2>
<p>You can even apply decorators to classes—for example, to automatically apply global middleware or metadata:</p>
<figure class="wp-block-image size-large"><img alt="" class="wp-image-1748" decoding="async" height="194" loading="lazy" sizes="auto, (max-width: 1024px) 100vw, 1024px" src="https://www.devcentrehouse.eu/blogs/wp-content/uploads/2025/05/Screenshot-2025-05-15-at-10.06.22-1024x194.png" srcset="https://www.devcentrehouse.eu/blogs/wp-content/uploads/2025/05/Screenshot-2025-05-15-at-10.06.22-1024x194.png 1024w, https://www.devcentrehouse.eu/blogs/wp-content/uploads/2025/05/Screenshot-2025-05-15-at-10.06.22-300x57.png 300w, https://www.devcentrehouse.eu/blogs/wp-content/uploads/2025/05/Screenshot-2025-05-15-at-10.06.22-768x145.png 768w, https://www.devcentrehouse.eu/blogs/wp-content/uploads/2025/05/Screenshot-2025-05-15-at-10.06.22-1536x291.png 1536w, https://www.devcentrehouse.eu/blogs/wp-content/uploads/2025/05/Screenshot-2025-05-15-at-10.06.22.png 1552w" width="1024"/></figure>
<p>This isn’t as common as method or parameter decorators, but it’s useful in advanced use cases.</p>
<h2 class="wp-block-heading">NestJS Decorators + Reflect Metadata</h2>
<p>Most custom decorators work using <a href="https://rbuckton.github.io/reflect-metadata/" rel="noopener" target="_blank">Reflect Metadata</a>. It allows you to attach and retrieve metadata at runtime:</p>
<figure class="wp-block-image size-large"><img alt="" class="wp-image-1749" decoding="async" height="82" loading="lazy" sizes="auto, (max-width: 1024px) 100vw, 1024px" src="https://www.devcentrehouse.eu/blogs/wp-content/uploads/2025/05/Screenshot-2025-05-15-at-10.07.04-1024x82.png" srcset="https://www.devcentrehouse.eu/blogs/wp-content/uploads/2025/05/Screenshot-2025-05-15-at-10.07.04-1024x82.png 1024w, https://www.devcentrehouse.eu/blogs/wp-content/uploads/2025/05/Screenshot-2025-05-15-at-10.07.04-300x24.png 300w, https://www.devcentrehouse.eu/blogs/wp-content/uploads/2025/05/Screenshot-2025-05-15-at-10.07.04-768x61.png 768w, https://www.devcentrehouse.eu/blogs/wp-content/uploads/2025/05/Screenshot-2025-05-15-at-10.07.04.png 1532w" width="1024"/></figure>
<p>This is how NestJS passes data between decorators and guards, interceptors, or middleware.</p>
<h2 class="wp-block-heading">Best Practices for Custom Decorators</h2>
<ul class="wp-block-list">
<li>Keep them <strong>single-responsibility</strong>: One decorator should do one thing.</li>
<li>Avoid excessive logic inside the decorator itself.</li>
<li>Pair with guards/interceptors when decorators need enforcement logic.</li>
<li>Use <strong>naming conventions</strong> (<code>@CurrentUser</code>, <code>@Public</code>, <code>@Roles</code>, etc.) for clarity.</li>
</ul>
<h2 class="wp-block-heading">Real-World Use Cases</h2>
<ul class="wp-block-list">
<li><strong>Authentication</strong>: <code>@Public()</code> for routes that bypass auth.</li>
<li><strong>Authorization</strong>: <code>@Roles('admin')</code> for RBAC.</li>
<li><strong>Validation</strong>: Custom decorators for DTO transformation.</li>
<li><strong>Logging/Tracking</strong>: Tag routes or services for monitoring tools.</li>
<li><strong>Feature Flags</strong>: Enable/disable features conditionally.</li>
</ul>
<h2 class="wp-block-heading">Final Thoughts</h2>
<figure class="wp-block-image size-large"><img alt="" class="wp-image-1750" decoding="async" height="576" loading="lazy" sizes="auto, (max-width: 1024px) 100vw, 1024px" src="https://www.devcentrehouse.eu/blogs/wp-content/uploads/2025/05/node-dch-2-1024x576.jpg" srcset="https://www.devcentrehouse.eu/blogs/wp-content/uploads/2025/05/node-dch-2-1024x576.jpg 1024w, https://www.devcentrehouse.eu/blogs/wp-content/uploads/2025/05/node-dch-2-300x169.jpg 300w, https://www.devcentrehouse.eu/blogs/wp-content/uploads/2025/05/node-dch-2-768x432.jpg 768w, https://www.devcentrehouse.eu/blogs/wp-content/uploads/2025/05/node-dch-2-1536x864.jpg 1536w, https://www.devcentrehouse.eu/blogs/wp-content/uploads/2025/05/node-dch-2.jpg 1920w" width="1024"/></figure>
<p><br/>Creating custom decorators in NestJS empowers you to write more expressive, clean, and reusable code. Whether you’re extracting metadata, wrapping logic, or extending existing patterns, decorators help keep your project organised and modular.</p>
<p><br/>By mastering <strong>custom decorators in NestJS</strong>, you’re adding a powerful tool to your backend development toolkit.<br/>Explore how seasoned backend teams apply advanced NestJS patterns at <a href="https://www.devcentrehouse.eu/en/technologies/back-end/nodejs">Dev Centre House Ireland</a>.<a href="https://dev-centre-house.slack.com/files/U07HV6HPEKD/F08MJPQGT38/nestjs-decorators.jpg" rel="noopener" target="_blank">nestjs-decorators.jpg</a></p>
<p></p>
<!--— Calendly inline widget begin ---->


<!--— Calendly inline widget end ---->
<h2 class="wp-block-heading"></h2>
<p></p>
</div> <footer aria-label="Entry meta" class="entry-meta">
</footer>
</div>
