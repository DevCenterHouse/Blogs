
<div class="wp-block-columns alignwide is-layout-flex wp-container-core-columns-is-layout-8ba3830c wp-block-columns-is-layout-flex" style="margin-top:0;margin-bottom:0;padding-right:0;padding-left:0">
<div class="wp-block-column is-layout-flow wp-block-column-is-layout-flow" style="flex-basis:70%">
<div class="wp-block-group has-global-padding is-layout-constrained wp-block-group-is-layout-constrained"><figure class="alignwide wp-block-post-featured-image" style="padding-bottom:2vh;"><img alt="Node.js" class="attachment-post-thumbnail size-post-thumbnail wp-post-image" decoding="async" fetchpriority="high" height="1080" sizes="(max-width: 1920px) 100vw, 1920px" src="https://www.devcentrehouse.eu/blogs/wp-content/uploads/2025/05/Nest-js-vs-Express-js.jpg" srcset="https://www.devcentrehouse.eu/blogs/wp-content/uploads/2025/05/Nest-js-vs-Express-js.jpg 1920w, https://www.devcentrehouse.eu/blogs/wp-content/uploads/2025/05/Nest-js-vs-Express-js-300x169.jpg 300w, https://www.devcentrehouse.eu/blogs/wp-content/uploads/2025/05/Nest-js-vs-Express-js-1024x576.jpg 1024w, https://www.devcentrehouse.eu/blogs/wp-content/uploads/2025/05/Nest-js-vs-Express-js-768x432.jpg 768w, https://www.devcentrehouse.eu/blogs/wp-content/uploads/2025/05/Nest-js-vs-Express-js-1536x864.jpg 1536w" style="object-fit:cover;" width="1920"/></figure>
<h1 class="alignwide wp-block-post-title has-x-large-font-size">Battle of the Node.js Frameworks: NestJS vs Express.js</h1>
<div aria-hidden="true" class="wp-block-spacer" style="height:var(--wp--preset--spacing--10)"></div>
</div>
<div class="wp-block-group has-global-padding is-layout-constrained wp-block-group-is-layout-constrained"><div class="entry-content alignwide wp-block-post-content has-global-padding is-layout-constrained wp-container-core-post-content-is-layout-a5dd074b wp-block-post-content-is-layout-constrained">
<p>Choosing the right backend framework is crucial when building scalable and maintainable web applications. Among the many options available, two stand out: <strong><a href="https://nestjs.com/" rel="noreferrer noopener" target="_blank">NestJS</a></strong> and <strong><a href="https://expressjs.com/" rel="noreferrer noopener" target="_blank">Express.js</a></strong>. Both are powerful in their own right, but each serves different needs and developer preferences.</p>
<p><br/>In this comparison, we’ll explore the architecture, performance, scalability, learning curve, and use cases for both <strong>NestJS</strong> and <strong>Express.js</strong>, helping you decide which is best for your next project.</p>
<h2 class="wp-block-heading">Understanding Express.js</h2>
<p><strong>Express.js</strong> is a minimalist and flexible <a href="https://www.devcentrehouse.eu/en/technologies/back-end/nodejs">Node.js</a> web application framework that provides a robust set of features for building web and mobile applications. It has been the go-to framework for Node.js since its inception due to its simplicity and performance.</p>
<h3 class="wp-block-heading">Why Developers Love Express.js</h3>
<ul class="wp-block-list">
<li>Lightweight and unopinionated</li>
<li>Quick to set up and get started</li>
<li>Massive ecosystem and community</li>
<li>Ideal for building APIs and microservices<br/><br/>However, Express’s unstructured approach can lead to messy codebases as the application scales. This is where frameworks like NestJS come into play.</li>
</ul>
<h2 class="wp-block-heading">Introducing NestJS</h2>
<p><strong>NestJS</strong> is a progressive Node.js framework built with TypeScript and heavily inspired by Angular’s architecture. It brings a structured and modular approach to building server-side applications, making it a favourite for large-scale enterprise projects.</p>
<h3 class="wp-block-heading">Key Features of NestJS</h3>
<ul class="wp-block-list">
<li>Out-of-the-box support for TypeScript</li>
<li>Modular architecture and dependency injection</li>
<li>Built-in support for testing, validation, and security</li>
<li>Integrates seamlessly with tools like TypeORM, Prisma, and Swagger</li>
</ul>
<p>NestJS is ideal for developers who prefer opinionated frameworks and scalable code organisation.</p>
<h2 class="wp-block-heading">Architecture: Structured vs Unstructured</h2>
<p>One of the most significant differences between <strong>NestJS</strong> and <strong>Express.js</strong> lies in their architecture.</p>
<h3 class="wp-block-heading">Express.js Architecture</h3>
<p>Express does not enforce a particular project structure. This gives developers flexibility but can also lead to inconsistent and hard-to-maintain code in large projects.</p>
<p><br/>Example:</p>
<figure class="wp-block-image size-large"><img alt="" class="wp-image-1730" decoding="async" height="101" sizes="(max-width: 1024px) 100vw, 1024px" src="https://www.devcentrehouse.eu/blogs/wp-content/uploads/2025/05/Screenshot-2025-05-14-at-14.30.14-1024x101.png" srcset="https://www.devcentrehouse.eu/blogs/wp-content/uploads/2025/05/Screenshot-2025-05-14-at-14.30.14-1024x101.png 1024w, https://www.devcentrehouse.eu/blogs/wp-content/uploads/2025/05/Screenshot-2025-05-14-at-14.30.14-300x30.png 300w, https://www.devcentrehouse.eu/blogs/wp-content/uploads/2025/05/Screenshot-2025-05-14-at-14.30.14-768x76.png 768w, https://www.devcentrehouse.eu/blogs/wp-content/uploads/2025/05/Screenshot-2025-05-14-at-14.30.14.png 1380w" width="1024"/></figure>
<p>While this is simple and fast for small apps, managing routes, middleware, and services manually can become tedious over time.</p>
<h3 class="wp-block-heading">NestJS Architecture</h3>
<p>NestJS promotes a <strong>modular architecture</strong>, encouraging developers to divide their code into modules, controllers, and services. This leads to cleaner code and better separation of concerns.</p>
<p><br/>Example:</p>
<figure class="wp-block-image size-large"><img alt="" class="wp-image-1731" decoding="async" height="212" sizes="(max-width: 1024px) 100vw, 1024px" src="https://www.devcentrehouse.eu/blogs/wp-content/uploads/2025/05/Screenshot-2025-05-14-at-14.30.18-1024x212.png" srcset="https://www.devcentrehouse.eu/blogs/wp-content/uploads/2025/05/Screenshot-2025-05-14-at-14.30.18-1024x212.png 1024w, https://www.devcentrehouse.eu/blogs/wp-content/uploads/2025/05/Screenshot-2025-05-14-at-14.30.18-300x62.png 300w, https://www.devcentrehouse.eu/blogs/wp-content/uploads/2025/05/Screenshot-2025-05-14-at-14.30.18-768x159.png 768w, https://www.devcentrehouse.eu/blogs/wp-content/uploads/2025/05/Screenshot-2025-05-14-at-14.30.18.png 1354w" width="1024"/></figure>
<p>The use of decorators and DI (dependency injection) helps keep code organised and testable.</p>
<h2 class="wp-block-heading">TypeScript Support</h2>
<p>While both frameworks support TypeScript, NestJS is built entirely around it. Express can use TypeScript, but setup and type safety are not as seamless.</p>
<ul class="wp-block-list">
<li><strong>Express.js</strong>: Optional TypeScript with more manual configuration</li>
<li><strong>NestJS</strong>: First-class TypeScript support and built-in decorators</li>
</ul>
<p>If your project values type safety, NestJS is the stronger choice.</p>
<h2 class="wp-block-heading">Performance Comparison</h2>
<p>Performance is often a top concern for backend developers.</p>
<ul class="wp-block-list">
<li><strong>Express.js</strong> is known for its lightweight and fast performance. It has less overhead and is ideal for building fast APIs.</li>
<li><strong>NestJS</strong>, while slightly heavier due to its abstractions, is still highly performant and optimised for production use.</li>
</ul>
<p>The performance gap between the two is minimal in most real-world applications, especially when NestJS is used efficiently.</p>
<h2 class="wp-block-heading">Ecosystem and Community</h2>
<ul class="wp-block-list">
<li><strong>Express.js</strong> has been around longer and has a vast ecosystem of middleware and community resources.</li>
<li><strong>NestJS</strong> is newer but has grown rapidly in popularity, especially in the enterprise development space.</li>
</ul>
<p>NestJS builds on the strengths of Express (it uses Express under the hood by default), but offers more structure and features out-of-the-box.</p>
<h2 class="wp-block-heading">Use Cases: When to Use Which?</h2>
<h3 class="wp-block-heading">Choose Express.js If:</h3>
<ul class="wp-block-list">
<li>You need a lightweight framework for small apps or microservices.</li>
<li>You prefer full control over architecture and tooling.</li>
<li>You want to build fast prototypes or MVPs.</li>
</ul>
<h3 class="wp-block-heading">Choose NestJS If:</h3>
<ul class="wp-block-list">
<li>You’re building a large-scale application that needs clear structure.</li>
<li>Your team values maintainability and TypeScript.</li>
<li>You require features like DI, modularity, and robust testing support.</li>
</ul>
<h2 class="wp-block-heading">Learning Curve</h2>
<ul class="wp-block-list">
<li><strong>Express.js</strong> has a gentle learning curve and is ideal for beginners.</li>
<li><strong>NestJS</strong> has a steeper learning curve due to its concepts like decorators, modules, and services—but this investment pays off in larger applications.</li>
</ul>
<p>If you’re familiar with Angular or enterprise-level development, NestJS feels familiar and powerful.</p>
<h2 class="wp-block-heading">Final Verdict</h2>
<figure class="wp-block-image size-large"><img alt="" class="wp-image-1720" decoding="async" height="576" loading="lazy" sizes="auto, (max-width: 1024px) 100vw, 1024px" src="https://www.devcentrehouse.eu/blogs/wp-content/uploads/2025/05/node-dch-latest-1-1-1024x576.jpg" srcset="https://www.devcentrehouse.eu/blogs/wp-content/uploads/2025/05/node-dch-latest-1-1-1024x576.jpg 1024w, https://www.devcentrehouse.eu/blogs/wp-content/uploads/2025/05/node-dch-latest-1-1-300x169.jpg 300w, https://www.devcentrehouse.eu/blogs/wp-content/uploads/2025/05/node-dch-latest-1-1-768x432.jpg 768w, https://www.devcentrehouse.eu/blogs/wp-content/uploads/2025/05/node-dch-latest-1-1-1536x864.jpg 1536w, https://www.devcentrehouse.eu/blogs/wp-content/uploads/2025/05/node-dch-latest-1-1.jpg 1920w" width="1024"/></figure>
<p>Both <strong>NestJS</strong> and <strong>Express.js</strong> are excellent frameworks. Your choice depends on the specific needs of your project.</p>
<ul class="wp-block-list">
<li>For <strong>flexibility and speed</strong>, go with <strong>Express.js</strong>.</li>
<li>For <strong>structure, scalability, and enterprise-readiness</strong>, <strong>NestJS</strong> is the better pick.</li>
</ul>
<p>Ultimately, you can even use both—NestJS allows switching to <strong>Fastify</strong> or even using custom <strong>Express</strong> handlers when needed, offering the best of both worlds.</p>
<h2 class="wp-block-heading">FAQ</h2>
<p><strong>Question: </strong>What problems do DTOs solve in NestJS applications?<br/><strong>Answer:</strong> DTOs (Data Transfer Objects) help enforce structured, validated input and output formats in NestJS apps. They prevent invalid data from entering services and simplify transformation logic. Dev Centre House Ireland uses DTOs to maintain clean architectures and ensure data consistency in scalable backend systems.</p>
<hr class="wp-block-separator has-alpha-channel-opacity"/>
<p><strong>Question: </strong>How do pipes enhance request validation in NestJS?<br/><strong>Answer:</strong> Pipes in NestJS perform transformation and validation before a request reaches the controller. Using built-in pipes like <code>ValidationPipe</code>, or custom ones, helps prevent invalid input early. At Dev Centre House Ireland, we integrate pipes into DTO logic to secure endpoints and reduce runtime errors.</p>
<hr class="wp-block-separator has-alpha-channel-opacity"/>
<p><strong>Question: </strong>Why is modular architecture important in NestJS?<br/><strong>Answer:</strong> NestJS organises code into modules, controllers, and services, making it easier to scale, test, and maintain backend systems. Dev Centre House Ireland leverages Nest’s modular structure to build backend platforms that grow seamlessly with business requirements.</p>
<hr class="wp-block-separator has-alpha-channel-opacity"/>
<p><strong>Question: </strong>When should I choose NestJS over Express for a backend project?<br/><strong>Answer:</strong> Choose NestJS if you need architecture, TypeScript-first design, dependency injection, and enterprise-grade structure. Express may suit simpler or faster prototypes, but for long-term maintainability, Dev Centre House Ireland recommends NestJS in larger projects.</p>
<hr class="wp-block-separator has-alpha-channel-opacity"/>
<p><strong>Question: </strong>What are the trade-offs between performance and structure in NestJS vs Express?<br/><strong>Answer:</strong> Express is more lightweight and may offer slightly better performance. However, NestJS provides rich structure, built-in features, and strong TypeScript support. Dev Centre House Ireland designs systems that balance both factors, using NestJS with Fastify where performance is critical. </p>
<hr class="wp-block-separator has-alpha-channel-opacity"/>
<p><strong>Question: </strong>How does dependency injection in NestJS support maintainability?<br/><strong>Answer:</strong> Dependency injection decouples services and promotes reusable, testable code. NestJS includes DI out of the box, which simplifies wiring modules and improves test coverage. Dev Centre House Ireland uses DI to architect robust backend systems that evolve easily.</p>
<hr class="wp-block-separator has-alpha-channel-opacity"/>
<p><strong>Question:</strong> Is NestJS suitable for microservices and serverless architectures?<br/><strong>Answer:</strong> Yes. NestJS has built-in support for microservice patterns, WebSockets, GraphQL, and serverless deployments. Dev Centre House Ireland uses NestJS to build scalable, event-driven systems and cloud-native backends.</p>
<hr class="wp-block-separator has-alpha-channel-opacity"/>
<p><strong>Question: </strong>What is the learning curve like for NestJS compared to Express?<br/><strong>Answer:</strong> NestJS has a steeper learning curve due to decorators, TypeScript conventions, and enforced architecture. Express is simpler to start with. Dev Centre House Ireland partners with teams to onboard and train developers quickly in NestJS best practices.</p>
<hr class="wp-block-separator has-alpha-channel-opacity"/>
<p><strong>Question: </strong>How does NestJS help with testing backend code effectively?<br/><strong>Answer:</strong> NestJS provides built-in integration with testing tools (e.g. Jest) and generates spec templates with controllers and services. Its modular architecture makes unit and e2e testing straightforward. At Dev Centre House Ireland, we build backend systems that are testable and maintain high quality.</p>
<hr class="wp-block-separator has-alpha-channel-opacity"/>
<p><strong>Question: </strong>Why is NestJS a better choice for large teams and enterprise applications?<br/><strong>Answer:</strong> NestJS enforces consistency, modularity, security, and maintainability, critical for large-scale applications. With clear patterns across modules, teams stay aligned. Dev Centre House Ireland specialises in building enterprise-grade systems using NestJS architecture to support long-term team collaboration and growth.</p>
<hr class="wp-block-separator has-alpha-channel-opacity"/>
<p><strong>Question: </strong>Where can I learn more about NestJS backend development with Dev Centre House Ireland?<br/><strong>Answer:</strong> Visit <a class="" href="https://www.devcentrehouse.eu/en">https://www.devcentrehouse.eu/en</a> to explore how we build scalable NestJS backend systems tailored for enterprise and startup needs.</p>
<hr class="wp-block-separator has-alpha-channel-opacity"/>
<p>Looking to scale your Node.js development with structured architecture? Visit <a href="https://www.devcentrehouse.eu/en/technologies/back-end/nodejs">DevCentreHouseIreland – Node.js Development</a> for expert insights and backend solutions tailored for modern applications.</p>
<!--— Calendly inline widget begin ---->


<!--— Calendly inline widget end ---->
</div></div>
</div>
<div class="wp-block-column is-layout-flow wp-block-column-is-layout-flow" style="flex-basis:30%"><aside class="wp-block-template-part">
<div class="wp-block-group is-layout-flow wp-container-core-group-is-layout-0ba1ad86 wp-block-group-is-layout-flow" style="padding-right:0;padding-left:0">
<hr class="wp-block-separator has-text-color has-contrast-color has-alpha-channel-opacity has-contrast-background-color has-background is-style-wide"/>
<h4 class="wp-block-heading has-large-font-size"><strong>Latest Post</strong></h4>
<ul class="wp-block-latest-posts__list has-dates wp-block-latest-posts" style="margin-top:0;margin-bottom:0;margin-left:0;margin-right:0;"><li><a class="wp-block-latest-posts__post-title" href="https://www.devcentrehouse.eu/blogs/uk-founders-tech-runway-strategies-2025/">How UK Founders Stretch Their Tech Runway in 2025</a><time class="wp-block-latest-posts__post-date" datetime="2025-07-21T12:16:21+00:00">July 21, 2025</time></li>
<li><a class="wp-block-latest-posts__post-title" href="https://www.devcentrehouse.eu/blogs/how-to-choose-the-right-mobile-app-development-company-in-ireland-2025-guide/">How to Choose the Right Mobile App Development Company in Ireland (2025 Guide)</a><time class="wp-block-latest-posts__post-date" datetime="2025-07-21T12:04:38+00:00">July 21, 2025</time></li>
<li><a class="wp-block-latest-posts__post-title" href="https://www.devcentrehouse.eu/blogs/norwegian-startups-developer-hiring-challenges/">Norwegian Startups Struggle with Dev Hires, How To Solve</a><time class="wp-block-latest-posts__post-date" datetime="2025-07-21T12:02:22+00:00">July 21, 2025</time></li>
<li><a class="wp-block-latest-posts__post-title" href="https://www.devcentrehouse.eu/blogs/irelands-lean-dev-teams-outperform-big-budget-builds/">Ireland’s Lean Dev Teams Outperform Big Budget Builds</a><time class="wp-block-latest-posts__post-date" datetime="2025-07-18T13:10:01+00:00">July 18, 2025</time></li>
<li><a class="wp-block-latest-posts__post-title" href="https://www.devcentrehouse.eu/blogs/what-startup-founders-must-know-from-an-ex-ibmer-cto/">What Startup Founders Must Know from an ex-IBMer CTO</a><time class="wp-block-latest-posts__post-date" datetime="2025-07-17T14:38:33+00:00">July 17, 2025</time></li>
</ul>
<hr class="wp-block-separator has-text-color has-contrast-color has-alpha-channel-opacity has-contrast-background-color has-background is-style-wide"/>
<ul class="wp-block-social-links is-layout-flex wp-block-social-links-is-layout-flex"><li class="wp-social-link wp-social-link-linkedin wp-block-social-link"><a class="wp-block-social-link-anchor" href="https://www.linkedin.com/company/devcentrehouse/"><svg aria-hidden="true" focusable="false" height="24" version="1.1" viewbox="0 0 24 24" width="24" xmlns="http://www.w3.org/2000/svg"><path d="M19.7,3H4.3C3.582,3,3,3.582,3,4.3v15.4C3,20.418,3.582,21,4.3,21h15.4c0.718,0,1.3-0.582,1.3-1.3V4.3 C21,3.582,20.418,3,19.7,3z M8.339,18.338H5.667v-8.59h2.672V18.338z M7.004,8.574c-0.857,0-1.549-0.694-1.549-1.548 c0-0.855,0.691-1.548,1.549-1.548c0.854,0,1.547,0.694,1.547,1.548C8.551,7.881,7.858,8.574,7.004,8.574z M18.339,18.338h-2.669 v-4.177c0-0.996-0.017-2.278-1.387-2.278c-1.389,0-1.601,1.086-1.601,2.206v4.249h-2.667v-8.59h2.559v1.174h0.037 c0.356-0.675,1.227-1.387,2.526-1.387c2.703,0,3.203,1.779,3.203,4.092V18.338z"></path></svg><span class="wp-block-social-link-label screen-reader-text">LinkedIn</span></a></li>
<li class="wp-social-link wp-social-link-facebook wp-block-social-link"><a class="wp-block-social-link-anchor" href="https://www.facebook.com/devcentrehouse"><svg aria-hidden="true" focusable="false" height="24" version="1.1" viewbox="0 0 24 24" width="24" xmlns="http://www.w3.org/2000/svg"><path d="M12 2C6.5 2 2 6.5 2 12c0 5 3.7 9.1 8.4 9.9v-7H7.9V12h2.5V9.8c0-2.5 1.5-3.9 3.8-3.9 1.1 0 2.2.2 2.2.2v2.5h-1.3c-1.2 0-1.6.8-1.6 1.6V12h2.8l-.4 2.9h-2.3v7C18.3 21.1 22 17 22 12c0-5.5-4.5-10-10-10z"></path></svg><span class="wp-block-social-link-label screen-reader-text">Facebook</span></a></li>
<li class="wp-social-link wp-social-link-mail wp-block-social-link"><a class="wp-block-social-link-anchor" href="/cdn-cgi/l/email-protection#6b4d485a5b5f504d485a5b5a504d485a5b5350074d485a5a5a504d485b5d5f504d485a5b5b504d485a5b5a501d4d485b5252504d485a5b5a50054d485a5a5d50190e4d485a5b5f504d485a5a5a504d485a5a5c50180e450e1e"><svg aria-hidden="true" focusable="false" height="24" version="1.1" viewbox="0 0 24 24" width="24" xmlns="http://www.w3.org/2000/svg"><path d="M19,5H5c-1.1,0-2,.9-2,2v10c0,1.1.9,2,2,2h14c1.1,0,2-.9,2-2V7c0-1.1-.9-2-2-2zm.5,12c0,.3-.2.5-.5.5H5c-.3,0-.5-.2-.5-.5V9.8l7.5,5.6,7.5-5.6V17zm0-9.1L12,13.6,4.5,7.9V7c0-.3.2-.5.5-.5h14c.3,0,.5.2.5.5v.9z"></path></svg><span class="wp-block-social-link-label screen-reader-text">Mail</span></a></li>
<li class="wp-social-link wp-social-link-instagram wp-block-social-link"><a class="wp-block-social-link-anchor" href="https://www.instagram.com/devcentrehouse/"><svg aria-hidden="true" focusable="false" height="24" version="1.1" viewbox="0 0 24 24" width="24" xmlns="http://www.w3.org/2000/svg"><path d="M12,4.622c2.403,0,2.688,0.009,3.637,0.052c0.877,0.04,1.354,0.187,1.671,0.31c0.42,0.163,0.72,0.358,1.035,0.673 c0.315,0.315,0.51,0.615,0.673,1.035c0.123,0.317,0.27,0.794,0.31,1.671c0.043,0.949,0.052,1.234,0.052,3.637 s-0.009,2.688-0.052,3.637c-0.04,0.877-0.187,1.354-0.31,1.671c-0.163,0.42-0.358,0.72-0.673,1.035 c-0.315,0.315-0.615,0.51-1.035,0.673c-0.317,0.123-0.794,0.27-1.671,0.31c-0.949,0.043-1.233,0.052-3.637,0.052 s-2.688-0.009-3.637-0.052c-0.877-0.04-1.354-0.187-1.671-0.31c-0.42-0.163-0.72-0.358-1.035-0.673 c-0.315-0.315-0.51-0.615-0.673-1.035c-0.123-0.317-0.27-0.794-0.31-1.671C4.631,14.688,4.622,14.403,4.622,12 s0.009-2.688,0.052-3.637c0.04-0.877,0.187-1.354,0.31-1.671c0.163-0.42,0.358-0.72,0.673-1.035 c0.315-0.315,0.615-0.51,1.035-0.673c0.317-0.123,0.794-0.27,1.671-0.31C9.312,4.631,9.597,4.622,12,4.622 M12,3 C9.556,3,9.249,3.01,8.289,3.054C7.331,3.098,6.677,3.25,6.105,3.472C5.513,3.702,5.011,4.01,4.511,4.511 c-0.5,0.5-0.808,1.002-1.038,1.594C3.25,6.677,3.098,7.331,3.054,8.289C3.01,9.249,3,9.556,3,12c0,2.444,0.01,2.751,0.054,3.711 c0.044,0.958,0.196,1.612,0.418,2.185c0.23,0.592,0.538,1.094,1.038,1.594c0.5,0.5,1.002,0.808,1.594,1.038 c0.572,0.222,1.227,0.375,2.185,0.418C9.249,20.99,9.556,21,12,21s2.751-0.01,3.711-0.054c0.958-0.044,1.612-0.196,2.185-0.418 c0.592-0.23,1.094-0.538,1.594-1.038c0.5-0.5,0.808-1.002,1.038-1.594c0.222-0.572,0.375-1.227,0.418-2.185 C20.99,14.751,21,14.444,21,12s-0.01-2.751-0.054-3.711c-0.044-0.958-0.196-1.612-0.418-2.185c-0.23-0.592-0.538-1.094-1.038-1.594 c-0.5-0.5-1.002-0.808-1.594-1.038c-0.572-0.222-1.227-0.375-2.185-0.418C14.751,3.01,14.444,3,12,3L12,3z M12,7.378 c-2.552,0-4.622,2.069-4.622,4.622S9.448,16.622,12,16.622s4.622-2.069,4.622-4.622S14.552,7.378,12,7.378z M12,15 c-1.657,0-3-1.343-3-3s1.343-3,3-3s3,1.343,3,3S13.657,15,12,15z M16.804,6.116c-0.596,0-1.08,0.484-1.08,1.08 s0.484,1.08,1.08,1.08c0.596,0,1.08-0.484,1.08-1.08S17.401,6.116,16.804,6.116z"></path></svg><span class="wp-block-social-link-label screen-reader-text">Instagram</span></a></li></ul>
<hr class="wp-block-separator has-text-color has-contrast-color has-alpha-channel-opacity has-contrast-background-color has-background is-style-wide"/>
<div class="wp-block-group is-vertical is-content-justification-stretch is-layout-flex wp-container-core-group-is-layout-38a18bb4 wp-block-group-is-layout-flex">
<h2 class="wp-block-heading" style="font-size:clamp(1.039rem, 1.039rem + ((1vw - 0.2rem) * 0.935), 1.6rem);">Search</h2>
<form action="https://www.devcentrehouse.eu/blogs/" class="wp-block-search__button-outside wp-block-search__text-button wp-block-search" method="get" role="search"><label class="wp-block-search__label screen-reader-text" for="wp-block-search__input-2">Search</label><div class="wp-block-search__inside-wrapper" style="width: 100%"><input class="wp-block-search__input" id="wp-block-search__input-2" name="s" placeholder="Search..." required="" type="search" value=""/><button aria-label="Search" class="wp-block-search__button wp-element-button" type="submit">Search</button></div></form></div>
<div aria-hidden="true" class="wp-block-spacer" style="height:var(--wp--preset--spacing--10)"></div>
</div>
</aside></div>
</div>
