
<div class="inside-article">
<header aria-label="Content" class="entry-header">
<h1 class="entry-title" itemprop="headline">NestJS + Swagger: Auto-Generate API Docs</h1> 
</header>
<div class="featured-image cv-col-12 post-image">
<img alt="Swagger" class="size-full cv-col-12 wp-post-image" decoding="async" fetchpriority="high" height="1080" itemprop="image" sizes="(max-width: 1920px) 100vw, 1920px" src="https://www.devcentrehouse.eu/blogs/wp-content/uploads/2025/05/nest-swagger.jpg" srcset="https://www.devcentrehouse.eu/blogs/wp-content/uploads/2025/05/nest-swagger.jpg 1920w, https://www.devcentrehouse.eu/blogs/wp-content/uploads/2025/05/nest-swagger-300x169.jpg 300w, https://www.devcentrehouse.eu/blogs/wp-content/uploads/2025/05/nest-swagger-1024x576.jpg 1024w, https://www.devcentrehouse.eu/blogs/wp-content/uploads/2025/05/nest-swagger-768x432.jpg 768w, https://www.devcentrehouse.eu/blogs/wp-content/uploads/2025/05/nest-swagger-1536x864.jpg 1536w" style="aspect-ratio:0;" width="1920"/> </div>
<div class="entry-content" itemprop="text">
<p>In modern web development, ensuring your APIs are well-documented is just as important as creating them. API documentation makes it easier for developers to understand how to interact with your service, and having up-to-date docs can save time during development and troubleshooting. </p>
<p>Fortunately, with <strong><a href="https://www.devcentrehouse.eu/en/technologies/back-end/nodejs">NestJS</a></strong> and <strong><a href="https://en.wikipedia.org/wiki/Swagger_(software)" rel="noreferrer noopener" target="_blank">Swagger</a></strong>, you can automate this process to ensure that your <a href="https://en.wikipedia.org/wiki/API" rel="noreferrer noopener" target="_blank">API</a> documentation is always in sync with your codebase.</p>
<p>In this post, we’ll walk through how to <strong>auto-generate API documentation</strong> using <strong>NestJS</strong> and <strong>Swagger</strong>. By the end, you’ll be able to create clean, interactive API documentation that’s automatically updated as your code evolves.</p>
<h2 class="wp-block-heading">What is Swagger?</h2>
<p>Swagger is a framework for API documentation that provides a powerful set of tools to describe, consume, and visualize RESTful APIs. It is widely adopted in the industry due to its ability to automatically generate API docs, create interactive user interfaces, and help with API testing. Swagger’s user-friendly UI allows developers to easily interact with an API and see the request/response structure without needing to inspect the backend code directly.</p>
<h2 class="wp-block-heading">Benefits of Using Swagger with NestJS</h2>
<p>Integrating Swagger with NestJS brings a range of benefits to developers and teams, including:</p>
<ul class="wp-block-list">
<li style="padding-top:var(--wp--preset--spacing--xx-small);padding-bottom:var(--wp--preset--spacing--xx-small)"><strong>Auto-Generated Docs</strong>: Swagger auto-generates API documentation from your NestJS controllers and DTOs (Data Transfer Objects), keeping it up to date as you modify your code.</li>
<li style="padding-top:var(--wp--preset--spacing--xx-small);padding-bottom:var(--wp--preset--spacing--xx-small)"><strong>Interactive UI</strong>: Swagger provides an interactive interface where developers can make real API requests directly from the docs.</li>
<li style="padding-top:var(--wp--preset--spacing--xx-small);padding-bottom:var(--wp--preset--spacing--xx-small)"><strong>Validation</strong>: It helps with request validation, so you can ensure that the requests being made to your API are correctly formatted.</li>
<li style="padding-top:var(--wp--preset--spacing--xx-small);padding-bottom:var(--wp--preset--spacing--xx-small)"><strong>Easy Collaboration</strong>: Teams can collaboratively work on an API, thanks to the auto-generated and easily understandable documentation.</li>
</ul>
<h2 class="wp-block-heading">Setting Up Swagger in a NestJS Project</h2>
<p>Integrating Swagger into your NestJS application is simple. You’ll need to install the necessary dependencies and set up the configuration.</p>
<h3 class="wp-block-heading">Step 1: Install Dependencies</h3>
<p>Start by installing the <code>@nestjs/swagger</code> package and <code>swagger-ui-express</code> for the Swagger UI.</p>
<figure class="wp-block-image size-large"><img alt="" class="wp-image-1688" decoding="async" height="62" sizes="(max-width: 1024px) 100vw, 1024px" src="https://www.devcentrehouse.eu/blogs/wp-content/uploads/2025/05/Screenshot-2025-05-12-at-14.33.04-1024x62.png" srcset="https://www.devcentrehouse.eu/blogs/wp-content/uploads/2025/05/Screenshot-2025-05-12-at-14.33.04-1024x62.png 1024w, https://www.devcentrehouse.eu/blogs/wp-content/uploads/2025/05/Screenshot-2025-05-12-at-14.33.04-300x18.png 300w, https://www.devcentrehouse.eu/blogs/wp-content/uploads/2025/05/Screenshot-2025-05-12-at-14.33.04-768x47.png 768w, https://www.devcentrehouse.eu/blogs/wp-content/uploads/2025/05/Screenshot-2025-05-12-at-14.33.04.png 1352w" width="1024"/></figure>
<h3 class="wp-block-heading">Step 2: Configure Swagger</h3>
<p>Next, configure Swagger in the <code>main.ts</code> file of your NestJS application. Add the following code after initializing the NestJS app:</p>
<figure class="wp-block-image size-large"><img alt="" class="wp-image-1689" decoding="async" height="479" sizes="(max-width: 1024px) 100vw, 1024px" src="https://www.devcentrehouse.eu/blogs/wp-content/uploads/2025/05/Screenshot-2025-05-12-at-14.33.09-1024x479.png" srcset="https://www.devcentrehouse.eu/blogs/wp-content/uploads/2025/05/Screenshot-2025-05-12-at-14.33.09-1024x479.png 1024w, https://www.devcentrehouse.eu/blogs/wp-content/uploads/2025/05/Screenshot-2025-05-12-at-14.33.09-300x140.png 300w, https://www.devcentrehouse.eu/blogs/wp-content/uploads/2025/05/Screenshot-2025-05-12-at-14.33.09-768x360.png 768w, https://www.devcentrehouse.eu/blogs/wp-content/uploads/2025/05/Screenshot-2025-05-12-at-14.33.09.png 1354w" width="1024"/></figure>
<p>This will configure Swagger and make the documentation available at the <code>/api</code> endpoint of your application.</p>
<h3 class="wp-block-heading">Step 3: Add Swagger Annotations to Your Controllers and DTOs</h3>
<p>To make your API documentation more informative, you can use <strong>Swagger decorators</strong> to describe the endpoints, parameters, request bodies, and responses.</p>
<h4 class="wp-block-heading">Example: A Simple Controller</h4>
<p>Let’s say we have a simple <code>CatsController</code> that handles CRUD operations for “cats”:</p>
<figure class="wp-block-image size-large"><img alt="" class="wp-image-1690" decoding="async" height="715" loading="lazy" sizes="auto, (max-width: 1024px) 100vw, 1024px" src="https://www.devcentrehouse.eu/blogs/wp-content/uploads/2025/05/Screenshot-2025-05-12-at-14.33.15-1024x715.png" srcset="https://www.devcentrehouse.eu/blogs/wp-content/uploads/2025/05/Screenshot-2025-05-12-at-14.33.15-1024x715.png 1024w, https://www.devcentrehouse.eu/blogs/wp-content/uploads/2025/05/Screenshot-2025-05-12-at-14.33.15-300x209.png 300w, https://www.devcentrehouse.eu/blogs/wp-content/uploads/2025/05/Screenshot-2025-05-12-at-14.33.15-768x536.png 768w, https://www.devcentrehouse.eu/blogs/wp-content/uploads/2025/05/Screenshot-2025-05-12-at-14.33.15.png 1384w" width="1024"/></figure>
<h4 class="wp-block-heading">Example: DTO (Data Transfer Object)</h4>
<p>For request bodies, you can use <strong>DTOs</strong> to define the structure of your input data. In this case, we’re creating a <code>CreateCatDto</code> class to define the data structure for creating a new cat:</p>
<figure class="wp-block-image size-large"><img alt="" class="wp-image-1691" decoding="async" height="251" loading="lazy" sizes="auto, (max-width: 1024px) 100vw, 1024px" src="https://www.devcentrehouse.eu/blogs/wp-content/uploads/2025/05/Screenshot-2025-05-12-at-14.33.21-1024x251.png" srcset="https://www.devcentrehouse.eu/blogs/wp-content/uploads/2025/05/Screenshot-2025-05-12-at-14.33.21-1024x251.png 1024w, https://www.devcentrehouse.eu/blogs/wp-content/uploads/2025/05/Screenshot-2025-05-12-at-14.33.21-300x74.png 300w, https://www.devcentrehouse.eu/blogs/wp-content/uploads/2025/05/Screenshot-2025-05-12-at-14.33.21-768x188.png 768w, https://www.devcentrehouse.eu/blogs/wp-content/uploads/2025/05/Screenshot-2025-05-12-at-14.33.21.png 1354w" width="1024"/></figure>
<p>Here, the <code>@ApiProperty()</code> decorator is used to describe the properties of the <code>CreateCatDto</code>. These annotations will be reflected in the auto-generated Swagger docs.</p>
<h3 class="wp-block-heading">Step 4: Running the Application</h3>
<p>Now, when you run your NestJS app using:</p>
<pre class="wp-block-preformatted">npm run start</pre>
<p>You can navigate to <code>http://localhost:3000/api</code> to see the interactive Swagger documentation for your API. You’ll be able to view all your routes, parameters, and response models in a neatly organised, easy-to-navigate UI.</p>
<h2 class="wp-block-heading">Customizing Your Swagger Documentation</h2>
<p>You can further customise the appearance and behaviour of your Swagger documentation. For example:</p>
<ul class="wp-block-list">
<li style="padding-top:var(--wp--preset--spacing--xx-small);padding-bottom:var(--wp--preset--spacing--xx-small)"><strong>Customizing Models</strong>: Use the <code>@ApiResponse()</code> decorator to describe the structure of the responses.</li>
<li style="padding-top:var(--wp--preset--spacing--xx-small);padding-bottom:var(--wp--preset--spacing--xx-small)"><strong>Grouping Endpoints</strong>: You can group endpoints by tags using <code>@ApiTags()</code>, which is particularly useful for large APIs.</li>
<li style="padding-top:var(--wp--preset--spacing--xx-small);padding-bottom:var(--wp--preset--spacing--xx-small)"><strong>Authentication</strong>: Swagger can also be configured to document API authentication methods like OAuth2 or JWT tokens.</li>
</ul>
<h3 class="wp-block-heading">Example of Grouping Endpoints with Tags</h3>
<figure class="wp-block-image size-large"><img alt="" class="wp-image-1692" decoding="async" height="263" loading="lazy" sizes="auto, (max-width: 1024px) 100vw, 1024px" src="https://www.devcentrehouse.eu/blogs/wp-content/uploads/2025/05/Screenshot-2025-05-12-at-14.33.26-1024x263.png" srcset="https://www.devcentrehouse.eu/blogs/wp-content/uploads/2025/05/Screenshot-2025-05-12-at-14.33.26-1024x263.png 1024w, https://www.devcentrehouse.eu/blogs/wp-content/uploads/2025/05/Screenshot-2025-05-12-at-14.33.26-300x77.png 300w, https://www.devcentrehouse.eu/blogs/wp-content/uploads/2025/05/Screenshot-2025-05-12-at-14.33.26-768x197.png 768w, https://www.devcentrehouse.eu/blogs/wp-content/uploads/2025/05/Screenshot-2025-05-12-at-14.33.26.png 1340w" width="1024"/></figure>
<h2 class="wp-block-heading">Conclusion</h2>
<figure class="wp-block-image size-large"><img alt="" class="wp-image-1687" decoding="async" height="576" loading="lazy" sizes="auto, (max-width: 1024px) 100vw, 1024px" src="https://www.devcentrehouse.eu/blogs/wp-content/uploads/2025/05/node-dch-3-1024x576.jpg" srcset="https://www.devcentrehouse.eu/blogs/wp-content/uploads/2025/05/node-dch-3-1024x576.jpg 1024w, https://www.devcentrehouse.eu/blogs/wp-content/uploads/2025/05/node-dch-3-300x169.jpg 300w, https://www.devcentrehouse.eu/blogs/wp-content/uploads/2025/05/node-dch-3-768x432.jpg 768w, https://www.devcentrehouse.eu/blogs/wp-content/uploads/2025/05/node-dch-3-1536x864.jpg 1536w, https://www.devcentrehouse.eu/blogs/wp-content/uploads/2025/05/node-dch-3.jpg 1920w" width="1024"/></figure>
<p>Integrating <strong>Swagger</strong> with <strong>NestJS</strong> is a straightforward process that provides significant benefits to any API project. With auto-generated, interactive API documentation, your team can be more productive and confident about how to use the API.</p>
<p>Swagger doesn’t just improve documentation; it enhances testing, validation, and collaboration. And by leveraging <strong>NestJS</strong>’s powerful decorators and Swagger integration, you can automate the documentation process and ensure it stays up to date with minimal effort.</p>
<p>Start adding Swagger to your <strong>NestJS projects</strong> today to improve your API development workflow and enhance collaboration with your team.</p>
<p>For more insights into powerful backend technologies like NestJS, visit <a href="https://www.devcentrehouse.eu/en/technologies/back-end/nodejs">Dev Centre HouseI reland’s Node.js expertise page</a>.</p>
<!--— Calendly inline widget begin ---->


<!--— Calendly inline widget end ---->
</div> <footer aria-label="Entry meta" class="entry-meta">
</footer>
</div>
