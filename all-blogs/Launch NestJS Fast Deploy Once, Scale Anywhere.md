
<div class="wp-block-columns alignwide is-layout-flex wp-container-core-columns-is-layout-8ba3830c wp-block-columns-is-layout-flex" style="margin-top:0;margin-bottom:0;padding-right:0;padding-left:0">
<div class="wp-block-column is-layout-flow wp-block-column-is-layout-flow" style="flex-basis:70%">
<div class="wp-block-group has-global-padding is-layout-constrained wp-block-group-is-layout-constrained"><figure class="alignwide wp-block-post-featured-image" style="padding-bottom:2vh;"><img alt="NestJS" class="attachment-post-thumbnail size-post-thumbnail wp-post-image" decoding="async" fetchpriority="high" height="1080" sizes="(max-width: 1920px) 100vw, 1920px" src="https://www.devcentrehouse.eu/blogs/wp-content/uploads/2025/05/deploy-a-nest-app.jpg" srcset="https://www.devcentrehouse.eu/blogs/wp-content/uploads/2025/05/deploy-a-nest-app.jpg 1920w, https://www.devcentrehouse.eu/blogs/wp-content/uploads/2025/05/deploy-a-nest-app-300x169.jpg 300w, https://www.devcentrehouse.eu/blogs/wp-content/uploads/2025/05/deploy-a-nest-app-1024x576.jpg 1024w, https://www.devcentrehouse.eu/blogs/wp-content/uploads/2025/05/deploy-a-nest-app-768x432.jpg 768w, https://www.devcentrehouse.eu/blogs/wp-content/uploads/2025/05/deploy-a-nest-app-1536x864.jpg 1536w" style="border-radius:0px;object-fit:cover;" width="1920"/></figure>
<h1 class="alignwide wp-block-post-title has-x-large-font-size">Launch NestJS Fast: Deploy Once, Scale Anywhere</h1>
<div aria-hidden="true" class="wp-block-spacer" style="height:var(--wp--preset--spacing--10)"></div>
</div>
<div class="wp-block-group has-global-padding is-layout-constrained wp-block-group-is-layout-constrained"><div class="entry-content alignwide wp-block-post-content has-global-padding is-layout-constrained wp-container-core-post-content-is-layout-a5dd074b wp-block-post-content-is-layout-constrained">
<p>NestJS is one of the most powerful and flexible Node.js frameworks for building scalable server-side applications. Once your app is production-ready, the next step is deployment. In this guide, you’ll learn how to deploy a <strong><a href="https://www.devcentrehouse.eu/en/technologies/back-end/nodejs">NestJS</a> application</strong> to <strong><a href="https://render.com/" rel="noreferrer noopener" target="_blank">Render</a></strong>, <strong><a href="https://railway.com/" rel="noreferrer noopener" target="_blank">Railway</a></strong>, and <strong><a href="https://vercel.com/" rel="noreferrer noopener" target="_blank">Vercel</a></strong>, three modern platforms that simplify cloud hosting.</p>
<h2 class="wp-block-heading">Why Deploy NestJS on Modern Platforms?</h2>
<p>Before jumping into the specifics, it’s important to understand why platforms like <strong>Render</strong>, <strong>Railway</strong>, and <strong>Vercel</strong> are increasingly popular:</p>
<ul class="wp-block-list">
<li style="padding-top:var(--wp--preset--spacing--xx-small);padding-bottom:var(--wp--preset--spacing--xx-small)"><strong>Zero-config deployments</strong></li>
<li style="padding-top:var(--wp--preset--spacing--xx-small);padding-bottom:var(--wp--preset--spacing--xx-small)"><strong>CI/CD out of the box</strong></li>
<li style="padding-top:var(--wp--preset--spacing--xx-small);padding-bottom:var(--wp--preset--spacing--xx-small)"><strong>Integrated monitoring and logs</strong></li>
<li style="padding-top:var(--wp--preset--spacing--xx-small);padding-bottom:var(--wp--preset--spacing--xx-small)"><strong>Scalable infrastructure</strong></li>
<li style="padding-top:var(--wp--preset--spacing--xx-small);padding-bottom:var(--wp--preset--spacing--xx-small)"><strong>Free tier available for small projects</strong></li>
</ul>
<p>Now let’s walk through how to get your NestJS app live on each platform.</p>
<h2 class="wp-block-heading">Deploying NestJS on Render</h2>
<p>Render offers a simple setup for deploying backend applications. Here’s how to deploy a NestJS app:</p>
<h3 class="wp-block-heading">1. Prepare Your App</h3>
<p>Make sure your app has a <code>start</code> script in <code>package.json</code>:</p>
<figure class="wp-block-image size-large"><img alt="" class="wp-image-1698" decoding="async" height="97" sizes="(max-width: 1024px) 100vw, 1024px" src="https://www.devcentrehouse.eu/blogs/wp-content/uploads/2025/05/Screenshot-2025-05-12-at-15.08.05-1024x97.png" srcset="https://www.devcentrehouse.eu/blogs/wp-content/uploads/2025/05/Screenshot-2025-05-12-at-15.08.05-1024x97.png 1024w, https://www.devcentrehouse.eu/blogs/wp-content/uploads/2025/05/Screenshot-2025-05-12-at-15.08.05-300x28.png 300w, https://www.devcentrehouse.eu/blogs/wp-content/uploads/2025/05/Screenshot-2025-05-12-at-15.08.05-768x73.png 768w, https://www.devcentrehouse.eu/blogs/wp-content/uploads/2025/05/Screenshot-2025-05-12-at-15.08.05.png 1370w" width="1024"/></figure>
<p>Also, ensure the app is built using:</p>
<pre class="wp-block-preformatted">npm run build</pre>
<h3 class="wp-block-heading">2. Push Your Code to GitHub</h3>
<p>Render pulls code from GitHub, so push your NestJS project there if you haven’t already.</p>
<h3 class="wp-block-heading">3. Create a New Web Service</h3>
<ul class="wp-block-list">
<li>Go to <a href="https://dashboard.render.com/" rel="noopener" target="_blank">Render Dashboard</a></li>
<li>Click <strong>“New Web Service”</strong></li>
<li>Connect your GitHub repo</li>
<li>Set the build command: <code>npm install &amp;&amp; npm run build</code></li>
<li>Set the start command: <code>npm run start</code></li>
</ul>
<h3 class="wp-block-heading">4. Choose the Branch and Deploy</h3>
<p>Once you link the branch, Render will deploy your app. Subsequent pushes will trigger automatic redeployments.</p>
<h2 class="wp-block-heading">Deploying NestJS on Railway</h2>
<p><strong>Railway</strong> is a developer-friendly platform with a beautiful interface and flexible project structure.</p>
<h3 class="wp-block-heading">1. Import Your GitHub Project</h3>
<ul class="wp-block-list">
<li>Go to <a href="https://railway.app/" rel="noopener" target="_blank">Railway</a></li>
<li>Click <strong>“Start a New Project”</strong></li>
<li>Select “Deploy from GitHub repo”</li>
<li>Choose your NestJS app repo</li>
</ul>
<h3 class="wp-block-heading">2. Set Environment Variables</h3>
<p>If your app uses any environment variables (like a <code>.env</code> file), add them under the <strong>Variables</strong> tab in the Railway dashboard.</p>
<h3 class="wp-block-heading">3. Define Build and Start Commands</h3>
<ul class="wp-block-list">
<li>Build command: <code>npm install &amp;&amp; npm run build</code></li>
<li>Start command: <code>npm run start</code></li>
</ul>
<h3 class="wp-block-heading">4. Done!</h3>
<p>Railway provides a URL where your API is now live. You can scale it vertically or horizontally from the dashboard.</p>
<h2 class="wp-block-heading">Deploying NestJS on Vercel (Workaround)</h2>
<p>While Vercel is primarily optimised for frontend (like Next.js), you can still deploy a NestJS app as a <strong>Serverless Function</strong> or run it via a custom server using an API handler.</p>
<blockquote class="wp-block-quote is-layout-flow wp-block-quote-is-layout-flow">
<p>Note: Vercel is not the ideal choice for full backend applications like NestJS, but can work for small-scale APIs or SSR hybrid setups.</p>
</blockquote>
<h3 class="wp-block-heading">1. Set Up a Vercel Project</h3>
<ul class="wp-block-list">
<li>Install the Vercel CLI: <code>npm i -g vercel</code></li>
<li>Run <code>vercel</code> and follow the prompts</li>
</ul>
<h3 class="wp-block-heading">2. Configure <code>vercel.json</code></h3>
<p>Create a <code>vercel.json</code> file to specify the output:</p>
<figure class="wp-block-image size-large"><img alt="" class="wp-image-1697" decoding="async" height="206" sizes="(max-width: 1024px) 100vw, 1024px" src="https://www.devcentrehouse.eu/blogs/wp-content/uploads/2025/05/Screenshot-2025-05-12-at-15.07.33-1024x206.png" srcset="https://www.devcentrehouse.eu/blogs/wp-content/uploads/2025/05/Screenshot-2025-05-12-at-15.07.33-1024x206.png 1024w, https://www.devcentrehouse.eu/blogs/wp-content/uploads/2025/05/Screenshot-2025-05-12-at-15.07.33-300x60.png 300w, https://www.devcentrehouse.eu/blogs/wp-content/uploads/2025/05/Screenshot-2025-05-12-at-15.07.33-768x154.png 768w, https://www.devcentrehouse.eu/blogs/wp-content/uploads/2025/05/Screenshot-2025-05-12-at-15.07.33.png 1374w" width="1024"/></figure>
<h3 class="wp-block-heading">3. Push and Deploy</h3>
<p>Run <code>vercel --prod</code> to deploy. You may need to tweak NestJS to be more compatible with serverless.</p>
<h2 class="wp-block-heading">Choosing the Right Platform</h2>
<figure class="wp-block-table"><table class="has-fixed-layout"><thead><tr><th>Feature</th><th>Render</th><th>Railway</th><th>Vercel</th></tr></thead><tbody><tr><td>Best For</td><td>Full-stack apps</td><td>Quick deploy &amp; prototyping</td><td>Frontend + APIs</td></tr><tr><td>Serverless</td><td>No</td><td>Yes (optional)</td><td>Yes</td></tr><tr><td>Free Tier</td><td>Yes</td><td>Yes</td><td>Yes</td></tr><tr><td>CI/CD</td><td>Built-in</td><td>Built-in</td><td>Built-in</td></tr><tr><td>Environment Setup</td><td>Easy</td><td>Very Easy</td><td>Basic</td></tr><tr><td>Each platform has its perks. For full NestJS apps, <strong>Render</strong> or <strong>Railway</strong> are generally more backend-friendly.</td><td></td><td></td><td></td></tr></tbody></table></figure>
<h2 class="wp-block-heading">Final Thoughts</h2>
<figure class="wp-block-image size-large"><img alt="" class="wp-image-1687" decoding="async" height="576" loading="lazy" sizes="auto, (max-width: 1024px) 100vw, 1024px" src="https://www.devcentrehouse.eu/blogs/wp-content/uploads/2025/05/node-dch-3-1024x576.jpg" srcset="https://www.devcentrehouse.eu/blogs/wp-content/uploads/2025/05/node-dch-3-1024x576.jpg 1024w, https://www.devcentrehouse.eu/blogs/wp-content/uploads/2025/05/node-dch-3-300x169.jpg 300w, https://www.devcentrehouse.eu/blogs/wp-content/uploads/2025/05/node-dch-3-768x432.jpg 768w, https://www.devcentrehouse.eu/blogs/wp-content/uploads/2025/05/node-dch-3-1536x864.jpg 1536w, https://www.devcentrehouse.eu/blogs/wp-content/uploads/2025/05/node-dch-3.jpg 1920w" width="1024"/></figure>
<p>Deploying a <strong>NestJS application</strong> doesn’t have to be complicated. Whether you prefer the simplicity of Render, the flexibility of Railway, or want to experiment with Vercel, you now have a clear path forward.</p>
<p><br/>Each platform offers excellent documentation, and most of the heavy lifting is abstracted away. Choose the one that fits your workflow, and ship your NestJS backend with confidence.</p>
<h2 class="wp-block-heading">FAQ</h2>
<p><strong>Question:</strong> What makes NestJS suitable for scalable backend development?<br/><strong>Answer:</strong> NestJS is built with scalability in mind, offering a modular architecture, dependency injection, and support for microservices, all of which make it ideal for scaling applications as business needs grow. Dev Centre House Ireland leverages NestJS for clients needing both rapid deployment and long-term scalability.</p>
<hr class="wp-block-separator has-alpha-channel-opacity"/>
<p><strong>Question:</strong> How does NestJS support fast deployment?<br/><strong>Answer:</strong> With a strong CLI, out-of-the-box structure, and integration-ready features, NestJS allows teams to move quickly from development to production. Dev Centre House Ireland uses these tools to launch MVPs and full-scale products with speed and precision.</p>
<hr class="wp-block-separator has-alpha-channel-opacity"/>
<p><strong>Question:</strong> What are the core features of NestJS that help in scaling applications?<br/><strong>Answer:</strong> Key features include modular design, lazy loading, microservices support, and GraphQL integration. These allow apps to grow without rewrites, a strategy often employed by Dev Centre House Ireland for long-term success.</p>
<hr class="wp-block-separator has-alpha-channel-opacity"/>
<p><strong>Question:</strong> How does modular architecture aid in scalability?<br/><strong>Answer:</strong> Modular architecture allows developers to build features as independent units that can be added or scaled individually. This approach is especially useful for enterprise-grade solutions where different teams manage different parts of the application.</p>
<hr class="wp-block-separator has-alpha-channel-opacity"/>
<p><strong>Question:</strong> Why is TypeScript an advantage in NestJS development?<br/><strong>Answer:</strong> TypeScript offers type safety and better tooling, making code more maintainable and less error-prone. Dev Centre House Ireland uses TypeScript with NestJS to deliver high-quality and reliable backend services.</p>
<hr class="wp-block-separator has-alpha-channel-opacity"/>
<p><strong>Question:</strong> What role does Docker play in fast deployment with NestJS?<br/><strong>Answer:</strong> Docker helps containerise the NestJS application, ensuring consistent environments across development, staging, and production. It simplifies deployment pipelines and is a standard at Dev Centre House Ireland.</p>
<hr class="wp-block-separator has-alpha-channel-opacity"/>
<p><strong>Question:</strong> How does Dev Centre House Ireland approach rapid launch and future scaling with NestJS?<br/><strong>Answer:</strong> The team focuses on clean architecture, CI/CD pipelines, and modular design to deploy fast and scale when required. Clients benefit from quicker time-to-market and cost-effective expansion.</p>
<hr class="wp-block-separator has-alpha-channel-opacity"/>
<p><br/>Want to explore how experts use Node.js in production environments? <a href="https://www.devcentrehouse.eu/en/technologies/back-end/nodejs">Check out DevCentreHouseIreland’s Node.js technology stack</a> to learn more.</p>
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
<li class="wp-social-link wp-social-link-mail wp-block-social-link"><a class="wp-block-social-link-anchor" href="/cdn-cgi/l/email-protection#97b1b4a6a7a3acb1b4a6a7a6acb1b4a6a7afacfbf8b1b4a7a1a3acb1b4a6a7a7acf2b1b4a6a6afacf4b1b4a6a7a6acb1b4a6a6a7acb1b4a6a6a1acb1b4a6a6a3acb1b4a6a7a6acb1b4a6a7a3acb1b4a6a6a6acb1b4a6a6a0acb1b4a6a6a2acf2b1b4a7a3a1acb1b4a6a7a6acb1b4a6a6a0ac"><svg aria-hidden="true" focusable="false" height="24" version="1.1" viewbox="0 0 24 24" width="24" xmlns="http://www.w3.org/2000/svg"><path d="M19,5H5c-1.1,0-2,.9-2,2v10c0,1.1.9,2,2,2h14c1.1,0,2-.9,2-2V7c0-1.1-.9-2-2-2zm.5,12c0,.3-.2.5-.5.5H5c-.3,0-.5-.2-.5-.5V9.8l7.5,5.6,7.5-5.6V17zm0-9.1L12,13.6,4.5,7.9V7c0-.3.2-.5.5-.5h14c.3,0,.5.2.5.5v.9z"></path></svg><span class="wp-block-social-link-label screen-reader-text">Mail</span></a></li>
<li class="wp-social-link wp-social-link-instagram wp-block-social-link"><a class="wp-block-social-link-anchor" href="https://www.instagram.com/devcentrehouse/"><svg aria-hidden="true" focusable="false" height="24" version="1.1" viewbox="0 0 24 24" width="24" xmlns="http://www.w3.org/2000/svg"><path d="M12,4.622c2.403,0,2.688,0.009,3.637,0.052c0.877,0.04,1.354,0.187,1.671,0.31c0.42,0.163,0.72,0.358,1.035,0.673 c0.315,0.315,0.51,0.615,0.673,1.035c0.123,0.317,0.27,0.794,0.31,1.671c0.043,0.949,0.052,1.234,0.052,3.637 s-0.009,2.688-0.052,3.637c-0.04,0.877-0.187,1.354-0.31,1.671c-0.163,0.42-0.358,0.72-0.673,1.035 c-0.315,0.315-0.615,0.51-1.035,0.673c-0.317,0.123-0.794,0.27-1.671,0.31c-0.949,0.043-1.233,0.052-3.637,0.052 s-2.688-0.009-3.637-0.052c-0.877-0.04-1.354-0.187-1.671-0.31c-0.42-0.163-0.72-0.358-1.035-0.673 c-0.315-0.315-0.51-0.615-0.673-1.035c-0.123-0.317-0.27-0.794-0.31-1.671C4.631,14.688,4.622,14.403,4.622,12 s0.009-2.688,0.052-3.637c0.04-0.877,0.187-1.354,0.31-1.671c0.163-0.42,0.358-0.72,0.673-1.035 c0.315-0.315,0.615-0.51,1.035-0.673c0.317-0.123,0.794-0.27,1.671-0.31C9.312,4.631,9.597,4.622,12,4.622 M12,3 C9.556,3,9.249,3.01,8.289,3.054C7.331,3.098,6.677,3.25,6.105,3.472C5.513,3.702,5.011,4.01,4.511,4.511 c-0.5,0.5-0.808,1.002-1.038,1.594C3.25,6.677,3.098,7.331,3.054,8.289C3.01,9.249,3,9.556,3,12c0,2.444,0.01,2.751,0.054,3.711 c0.044,0.958,0.196,1.612,0.418,2.185c0.23,0.592,0.538,1.094,1.038,1.594c0.5,0.5,1.002,0.808,1.594,1.038 c0.572,0.222,1.227,0.375,2.185,0.418C9.249,20.99,9.556,21,12,21s2.751-0.01,3.711-0.054c0.958-0.044,1.612-0.196,2.185-0.418 c0.592-0.23,1.094-0.538,1.594-1.038c0.5-0.5,0.808-1.002,1.038-1.594c0.222-0.572,0.375-1.227,0.418-2.185 C20.99,14.751,21,14.444,21,12s-0.01-2.751-0.054-3.711c-0.044-0.958-0.196-1.612-0.418-2.185c-0.23-0.592-0.538-1.094-1.038-1.594 c-0.5-0.5-1.002-0.808-1.594-1.038c-0.572-0.222-1.227-0.375-2.185-0.418C14.751,3.01,14.444,3,12,3L12,3z M12,7.378 c-2.552,0-4.622,2.069-4.622,4.622S9.448,16.622,12,16.622s4.622-2.069,4.622-4.622S14.552,7.378,12,7.378z M12,15 c-1.657,0-3-1.343-3-3s1.343-3,3-3s3,1.343,3,3S13.657,15,12,15z M16.804,6.116c-0.596,0-1.08,0.484-1.08,1.08 s0.484,1.08,1.08,1.08c0.596,0,1.08-0.484,1.08-1.08S17.401,6.116,16.804,6.116z"></path></svg><span class="wp-block-social-link-label screen-reader-text">Instagram</span></a></li></ul>
<hr class="wp-block-separator has-text-color has-contrast-color has-alpha-channel-opacity has-contrast-background-color has-background is-style-wide"/>
<div class="wp-block-group is-vertical is-content-justification-stretch is-layout-flex wp-container-core-group-is-layout-38a18bb4 wp-block-group-is-layout-flex">
<h2 class="wp-block-heading" style="font-size:clamp(1.039rem, 1.039rem + ((1vw - 0.2rem) * 0.935), 1.6rem);">Search</h2>
<form action="https://www.devcentrehouse.eu/blogs/" class="wp-block-search__button-outside wp-block-search__text-button wp-block-search" method="get" role="search"><label class="wp-block-search__label screen-reader-text" for="wp-block-search__input-2">Search</label><div class="wp-block-search__inside-wrapper" style="width: 100%"><input class="wp-block-search__input" id="wp-block-search__input-2" name="s" placeholder="Search..." required="" type="search" value=""/><button aria-label="Search" class="wp-block-search__button wp-element-button" type="submit">Search</button></div></form></div>
<div aria-hidden="true" class="wp-block-spacer" style="height:var(--wp--preset--spacing--10)"></div>
</div>
</aside></div>
</div>
