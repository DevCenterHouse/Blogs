
<div class="wp-block-columns alignwide is-layout-flex wp-container-core-columns-is-layout-8ba3830c wp-block-columns-is-layout-flex" style="margin-top:0;margin-bottom:0;padding-right:0;padding-left:0">
<div class="wp-block-column is-layout-flow wp-block-column-is-layout-flow" style="flex-basis:70%">
<div class="wp-block-group has-global-padding is-layout-constrained wp-block-group-is-layout-constrained"><figure class="alignwide wp-block-post-featured-image" style="padding-bottom:2vh;"><img alt="Node.js" class="attachment-post-thumbnail size-post-thumbnail wp-post-image" decoding="async" fetchpriority="high" height="720" sizes="(max-width: 1280px) 100vw, 1280px" src="https://www.devcentrehouse.eu/blogs/wp-content/uploads/2025/05/microservices.png" srcset="https://www.devcentrehouse.eu/blogs/wp-content/uploads/2025/05/microservices.png 1280w, https://www.devcentrehouse.eu/blogs/wp-content/uploads/2025/05/microservices-300x169.png 300w, https://www.devcentrehouse.eu/blogs/wp-content/uploads/2025/05/microservices-1024x576.png 1024w, https://www.devcentrehouse.eu/blogs/wp-content/uploads/2025/05/microservices-768x432.png 768w" style="object-fit:cover;" width="1280"/></figure>
<h1 class="alignwide wp-block-post-title has-x-large-font-size">Node.js Best Practices: 8 Critical Tips for Building Scalable Microservices</h1>
<div aria-hidden="true" class="wp-block-spacer" style="height:var(--wp--preset--spacing--10)"></div>
</div>
<div class="wp-block-group has-global-padding is-layout-constrained wp-block-group-is-layout-constrained"><div class="entry-content alignwide wp-block-post-content has-global-padding is-layout-constrained wp-container-core-post-content-is-layout-a5dd074b wp-block-post-content-is-layout-constrained">
<p><strong><a href="https://en.wikipedia.org/wiki/Microservices" rel="noreferrer noopener nofollow" target="_blank">Microservices architecture</a></strong> has become a go-to approach for building <strong>scalable and maintainable</strong> applications, and <strong><a href="https://www.devcentrehouse.eu/en/technologies/back-end/nodejs">Node.js</a></strong> is one of the most popular frameworks for developing them. With its <strong>event-driven, non-blocking I/O model</strong>, Node.js enables high-performance microservices that can efficiently handle concurrent requests.<br/>However, building <strong>scalable microservices</strong> in Node.js requires <strong>best practices</strong> to ensure <strong>performance, reliability, and maintainability</strong>. </p>
<p>In this guide, we’ll cover <strong>eight critical tips</strong> to help you design <strong>efficient, robust, and future-proof</strong> microservices in Node.js.</p>
<h2 class="wp-block-heading"><strong>1. Use a Monorepo for Better Code Management</strong></h2>
<p>Managing multiple microservices can become a challenge as your system grows. Instead of handling separate repositories for each service, consider using a <strong>monorepo</strong> structure.</p>
<h3 class="wp-block-heading"><strong>Why?</strong></h3>
<ul class="wp-block-list">
<li style="padding-top:var(--wp--preset--spacing--xx-small);padding-bottom:var(--wp--preset--spacing--xx-small)"><strong>Easier dependency management</strong> – Share packages across services.</li>
<li style="padding-top:var(--wp--preset--spacing--xx-small);padding-bottom:var(--wp--preset--spacing--xx-small)"><strong>Consistent versioning</strong> – Avoid compatibility issues between services.</li>
<li style="padding-top:var(--wp--preset--spacing--xx-small);padding-bottom:var(--wp--preset--spacing--xx-small)"><strong>Simplified CI/CD pipelines</strong> – Deploy all microservices efficiently.</li>
</ul>
<p><strong>Tool Suggestion:</strong> Use <strong>Nx</strong> or <strong>Lerna</strong> for managing monorepos in a scalable way.</p>
<h2 class="wp-block-heading"><strong>2. Implement API Gateway for Centralized Routing</strong></h2>
<p>Microservices often expose multiple APIs, making it complex for clients to interact with them. A <strong>centralized API gateway</strong> helps streamline communication and manage <strong>authentication, caching, rate limiting, and logging</strong> in one place.</p>
<h3 class="wp-block-heading"><strong>Why?</strong></h3>
<ul class="wp-block-list">
<li style="padding-top:var(--wp--preset--spacing--xx-small);padding-bottom:var(--wp--preset--spacing--xx-small)"><strong>Reduces complexity</strong> – Clients interact with a single API.</li>
<li style="padding-top:var(--wp--preset--spacing--xx-small);padding-bottom:var(--wp--preset--spacing--xx-small)"><strong>Improves security</strong> – Apply authentication and authorization at one entry point.</li>
<li style="padding-top:var(--wp--preset--spacing--xx-small);padding-bottom:var(--wp--preset--spacing--xx-small)"><strong>Optimizes performance</strong> – Use caching and load balancing.</li>
</ul>
<p><strong>Tool Suggestion:</strong> Use <strong>Kong, NGINX, or Express Gateway</strong> for API management.</p>
<h2 class="wp-block-heading"><strong>3. Use Asynchronous Communication with Message Queues</strong></h2>
<p>While REST APIs are useful, microservices scale better with <strong>asynchronous communication</strong> using <strong>message queues</strong>. This prevents bottlenecks and ensures <strong>high availability</strong>.</p>
<h3 class="wp-block-heading"><strong>Why?</strong></h3>
<ul class="wp-block-list">
<li style="padding-top:var(--wp--preset--spacing--xx-small);padding-bottom:var(--wp--preset--spacing--xx-small)"><strong>Decouples microservices</strong> – Services don’t wait for responses.</li>
<li style="padding-top:var(--wp--preset--spacing--xx-small);padding-bottom:var(--wp--preset--spacing--xx-small)"><strong>Handles high loads</strong> – Queues prevent request overload.</li>
<li style="padding-top:var(--wp--preset--spacing--xx-small);padding-bottom:var(--wp--preset--spacing--xx-small)"><strong>Improves fault tolerance</strong> – Failed messages can be retried.</li>
</ul>
<p><strong>Tool Suggestion:</strong> Use <strong>RabbitMQ, Apache Kafka, or NATS</strong> for event-driven communication.</p>
<h2 class="wp-block-heading"><strong>4. Containerize Microservices with Docker</strong></h2>
<p>Deploying microservices individually can be painful. Using <strong>Docker containers</strong> simplifies the process by ensuring that each microservice runs with the <strong>same environment</strong> across different machines.</p>
<h3 class="wp-block-heading"><strong>Why?</strong></h3>
<ul class="wp-block-list">
<li style="padding-top:var(--wp--preset--spacing--xx-small);padding-bottom:var(--wp--preset--spacing--xx-small)"><strong>Portable and lightweight</strong> – Run anywhere without compatibility issues.</li>
<li style="padding-top:var(--wp--preset--spacing--xx-small);padding-bottom:var(--wp--preset--spacing--xx-small)"><strong>Easier scaling</strong> – Deploy multiple instances quickly.</li>
<li style="padding-top:var(--wp--preset--spacing--xx-small);padding-bottom:var(--wp--preset--spacing--xx-small)"><strong>Better dependency management</strong> – No more “it works on my machine” issues.</li>
</ul>
<p><strong>Tool Suggestion:</strong> Use <strong>Docker Compose</strong> for local development and <strong>Kubernetes</strong> for production orchestration.</p>
<h2 class="wp-block-heading"><strong>5. Implement Proper Logging and Monitoring</strong></h2>
<p>Microservices generate large volumes of logs. Without <strong>structured logging and monitoring</strong>, debugging becomes difficult.</p>
<h3 class="wp-block-heading"><strong>Best Practices:</strong></h3>
<ul class="wp-block-list">
<li style="padding-top:var(--wp--preset--spacing--xx-small);padding-bottom:var(--wp--preset--spacing--xx-small)">Use a <strong>centralized logging system</strong> (e.g., ELK Stack, Loki, or Fluentd).</li>
<li style="padding-top:var(--wp--preset--spacing--xx-small);padding-bottom:var(--wp--preset--spacing--xx-small)">Include <strong>correlation IDs</strong> to track requests across services.</li>
<li style="padding-top:var(--wp--preset--spacing--xx-small);padding-bottom:var(--wp--preset--spacing--xx-small)">Set up <strong>real-time monitoring</strong> using <strong>Prometheus and Grafana</strong>.</li>
</ul>
<p><strong>Tool Suggestion:</strong> Use <strong>Winston</strong> or <strong>Pino</strong> for logging in Node.js.</p>
<h2 class="wp-block-heading"><strong>6. Secure Microservices with Authentication and Authorization</strong></h2>
<p>Security is critical in microservices. Implement robust authentication and authorization mechanisms to <strong>prevent unauthorized access</strong>.</p>
<h3 class="wp-block-heading"><strong>Best Practices:</strong></h3>
<ul class="wp-block-list">
<li style="padding-top:var(--wp--preset--spacing--xx-small);padding-bottom:var(--wp--preset--spacing--xx-small)">Use <strong>OAuth 2.0 and OpenID Connect</strong> for secure authentication.</li>
<li style="padding-top:var(--wp--preset--spacing--xx-small);padding-bottom:var(--wp--preset--spacing--xx-small)">Implement <strong>JWT (JSON Web Tokens)</strong> for stateless authentication.</li>
<li style="padding-top:var(--wp--preset--spacing--xx-small);padding-bottom:var(--wp--preset--spacing--xx-small)">Restrict access using <strong>Role-Based Access Control (RBAC)</strong> or <strong>Attribute-Based Access Control (ABAC)</strong>.</li>
</ul>
<p><strong>Tool Suggestion:</strong> Use <strong>Keycloak, Auth0, or Passport.js</strong> for authentication.</p>
<h2 class="wp-block-heading"><strong>7. Optimize Database Access with Connection Pooling</strong></h2>
<p>Database bottlenecks can significantly impact the scalability of microservices. Each service should <strong>efficiently manage</strong> database connections.</p>
<h3 class="wp-block-heading"><strong>Best Practices:</strong></h3>
<ul class="wp-block-list">
<li style="padding-top:var(--wp--preset--spacing--xx-small);padding-bottom:var(--wp--preset--spacing--xx-small)">Use <strong>connection pooling</strong> to reuse database connections.</li>
<li style="padding-top:var(--wp--preset--spacing--xx-small);padding-bottom:var(--wp--preset--spacing--xx-small)">Avoid <strong>long-running transactions</strong> that lock resources.</li>
<li style="padding-top:var(--wp--preset--spacing--xx-small);padding-bottom:var(--wp--preset--spacing--xx-small)">Implement <strong>database replication and sharding</strong> for better performance.</li>
</ul>
<p><strong>Tool Suggestion:</strong> Use <strong>pg-pool</strong> for PostgreSQL or <strong>Sequelize with pooling options</strong> in Node.js.</p>
<h2 class="wp-block-heading"><strong>8. Automate Deployment with CI/CD Pipelines</strong></h2>
<p>Manual deployments can introduce <strong>errors and delays</strong>. <strong>Automated CI/CD pipelines</strong> ensure that code changes are tested and deployed seamlessly.</p>
<h3 class="wp-block-heading"><strong>Best Practices:</strong></h3>
<ul class="wp-block-list">
<li style="padding-top:var(--wp--preset--spacing--xx-small);padding-bottom:var(--wp--preset--spacing--xx-small)">Use <strong>GitHub Actions, GitLab CI/CD, or Jenkins</strong> for automation.</li>
<li style="padding-top:var(--wp--preset--spacing--xx-small);padding-bottom:var(--wp--preset--spacing--xx-small)">Implement <strong>blue-green deployments</strong> to minimize downtime.</li>
<li style="padding-top:var(--wp--preset--spacing--xx-small);padding-bottom:var(--wp--preset--spacing--xx-small)">Use <strong>feature flags</strong> for controlled rollouts.</li>
</ul>
<p><strong>Tool Suggestion:</strong> Use <strong>ArgoCD or Spinnaker</strong> for Kubernetes-based deployments.</p>
<h2 class="wp-block-heading"><strong>Final Thoughts: Build Scalable Node.js Microservices the Right Way</strong></h2>
<p>Scalability and maintainability are the <strong>core principles</strong> of microservices architecture. By implementing these <strong>best practices</strong>, you ensure that your Node.js microservices remain <strong>highly performant, secure, and resilient</strong>.</p>
<h3 class="wp-block-heading"><strong>Quick Recap of Best Practices:</strong></h3>
<figure class="wp-block-table"><table class="has-fixed-layout"><thead><tr><th><strong>Best Practice</strong></th><th><strong>Benefit</strong></th></tr></thead><tbody><tr><td><strong>Monorepo</strong></td><td>Centralized code management</td></tr><tr><td><strong>API Gateway</strong></td><td>Simplifies routing &amp; security</td></tr><tr><td><strong>Message Queues</strong></td><td>Asynchronous, scalable communication</td></tr><tr><td><strong>Docker &amp; Kubernetes</strong></td><td>Portable, containerized deployment</td></tr><tr><td><strong>Logging &amp; Monitoring</strong></td><td>Easy debugging &amp; observability</td></tr><tr><td><strong>Authentication &amp; Security</strong></td><td>Protects microservices from threats</td></tr><tr><td><strong>Database Connection Pooling</strong></td><td>Improves performance</td></tr><tr><td><strong>CI/CD Automation</strong></td><td>Faster, error-free deployments</td></tr><tr><td>By applying these <strong>critical tips</strong>, you’ll be able to develop <strong>robust, future-proof microservices</strong> in <strong>Node.js</strong> that can handle <strong>large-scale applications</strong> efficiently.</td><td></td></tr></tbody></table></figure>
<h2 class="wp-block-heading">Concluding Insights: Node.js, via Dev Centre House Ireland</h2>
<figure class="wp-block-image size-large"><img alt="Node.js" class="wp-image-1570" decoding="async" height="730" sizes="(max-width: 1024px) 100vw, 1024px" src="https://www.devcentrehouse.eu/blogs/wp-content/uploads/2025/05/node-dch-1-1024x730.png" srcset="https://www.devcentrehouse.eu/blogs/wp-content/uploads/2025/05/node-dch-1-1024x730.png 1024w, https://www.devcentrehouse.eu/blogs/wp-content/uploads/2025/05/node-dch-1-300x214.png 300w, https://www.devcentrehouse.eu/blogs/wp-content/uploads/2025/05/node-dch-1-768x548.png 768w, https://www.devcentrehouse.eu/blogs/wp-content/uploads/2025/05/node-dch-1.png 1150w" width="1024"/></figure>
<p>In conclusion, Node.js stands out as a powerful and versatile runtime environment for building scalable and high-performance backend applications. Its event-driven, non-blocking architecture, coupled with the vast npm ecosystem, enables developers to create efficient and responsive solutions. Whether you’re building real-time applications, APIs, or microservices, Node.js offers a robust foundation for modern web development, making it a valuable asset in any developer’s toolkit. </p>
<p>For further exploration and learning, refer to the detailed information provided in the resource: <a href="https://www.devcentrehouse.eu/en/technologies/back-end/nodejs">https://www.devcentrehouse.eu/en/technologies/back-end/nodejs</a>.</p>
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
<li class="wp-social-link wp-social-link-mail wp-block-social-link"><a class="wp-block-social-link-anchor" href="/cdn-cgi/l/email-protection#cbede8fafbfff0ede8fafbfaf0a7a7a4ede8fbfdfff0ede8fafbfbf0aeede8fafaf3f0ede8fbf2f2f0ede8fafbfaf0ede8fafafbf0bfede8fafafff0ede8fafbfaf0ede8fafbfff0ede8fafafaf0beede8fafafef0aee5aeede8fafafcf0"><svg aria-hidden="true" focusable="false" height="24" version="1.1" viewbox="0 0 24 24" width="24" xmlns="http://www.w3.org/2000/svg"><path d="M19,5H5c-1.1,0-2,.9-2,2v10c0,1.1.9,2,2,2h14c1.1,0,2-.9,2-2V7c0-1.1-.9-2-2-2zm.5,12c0,.3-.2.5-.5.5H5c-.3,0-.5-.2-.5-.5V9.8l7.5,5.6,7.5-5.6V17zm0-9.1L12,13.6,4.5,7.9V7c0-.3.2-.5.5-.5h14c.3,0,.5.2.5.5v.9z"></path></svg><span class="wp-block-social-link-label screen-reader-text">Mail</span></a></li>
<li class="wp-social-link wp-social-link-instagram wp-block-social-link"><a class="wp-block-social-link-anchor" href="https://www.instagram.com/devcentrehouse/"><svg aria-hidden="true" focusable="false" height="24" version="1.1" viewbox="0 0 24 24" width="24" xmlns="http://www.w3.org/2000/svg"><path d="M12,4.622c2.403,0,2.688,0.009,3.637,0.052c0.877,0.04,1.354,0.187,1.671,0.31c0.42,0.163,0.72,0.358,1.035,0.673 c0.315,0.315,0.51,0.615,0.673,1.035c0.123,0.317,0.27,0.794,0.31,1.671c0.043,0.949,0.052,1.234,0.052,3.637 s-0.009,2.688-0.052,3.637c-0.04,0.877-0.187,1.354-0.31,1.671c-0.163,0.42-0.358,0.72-0.673,1.035 c-0.315,0.315-0.615,0.51-1.035,0.673c-0.317,0.123-0.794,0.27-1.671,0.31c-0.949,0.043-1.233,0.052-3.637,0.052 s-2.688-0.009-3.637-0.052c-0.877-0.04-1.354-0.187-1.671-0.31c-0.42-0.163-0.72-0.358-1.035-0.673 c-0.315-0.315-0.51-0.615-0.673-1.035c-0.123-0.317-0.27-0.794-0.31-1.671C4.631,14.688,4.622,14.403,4.622,12 s0.009-2.688,0.052-3.637c0.04-0.877,0.187-1.354,0.31-1.671c0.163-0.42,0.358-0.72,0.673-1.035 c0.315-0.315,0.615-0.51,1.035-0.673c0.317-0.123,0.794-0.27,1.671-0.31C9.312,4.631,9.597,4.622,12,4.622 M12,3 C9.556,3,9.249,3.01,8.289,3.054C7.331,3.098,6.677,3.25,6.105,3.472C5.513,3.702,5.011,4.01,4.511,4.511 c-0.5,0.5-0.808,1.002-1.038,1.594C3.25,6.677,3.098,7.331,3.054,8.289C3.01,9.249,3,9.556,3,12c0,2.444,0.01,2.751,0.054,3.711 c0.044,0.958,0.196,1.612,0.418,2.185c0.23,0.592,0.538,1.094,1.038,1.594c0.5,0.5,1.002,0.808,1.594,1.038 c0.572,0.222,1.227,0.375,2.185,0.418C9.249,20.99,9.556,21,12,21s2.751-0.01,3.711-0.054c0.958-0.044,1.612-0.196,2.185-0.418 c0.592-0.23,1.094-0.538,1.594-1.038c0.5-0.5,0.808-1.002,1.038-1.594c0.222-0.572,0.375-1.227,0.418-2.185 C20.99,14.751,21,14.444,21,12s-0.01-2.751-0.054-3.711c-0.044-0.958-0.196-1.612-0.418-2.185c-0.23-0.592-0.538-1.094-1.038-1.594 c-0.5-0.5-1.002-0.808-1.594-1.038c-0.572-0.222-1.227-0.375-2.185-0.418C14.751,3.01,14.444,3,12,3L12,3z M12,7.378 c-2.552,0-4.622,2.069-4.622,4.622S9.448,16.622,12,16.622s4.622-2.069,4.622-4.622S14.552,7.378,12,7.378z M12,15 c-1.657,0-3-1.343-3-3s1.343-3,3-3s3,1.343,3,3S13.657,15,12,15z M16.804,6.116c-0.596,0-1.08,0.484-1.08,1.08 s0.484,1.08,1.08,1.08c0.596,0,1.08-0.484,1.08-1.08S17.401,6.116,16.804,6.116z"></path></svg><span class="wp-block-social-link-label screen-reader-text">Instagram</span></a></li></ul>
<hr class="wp-block-separator has-text-color has-contrast-color has-alpha-channel-opacity has-contrast-background-color has-background is-style-wide"/>
<div class="wp-block-group is-vertical is-content-justification-stretch is-layout-flex wp-container-core-group-is-layout-38a18bb4 wp-block-group-is-layout-flex">
<h2 class="wp-block-heading" style="font-size:clamp(1.039rem, 1.039rem + ((1vw - 0.2rem) * 0.935), 1.6rem);">Search</h2>
<form action="https://www.devcentrehouse.eu/blogs/" class="wp-block-search__button-outside wp-block-search__text-button wp-block-search" method="get" role="search"><label class="wp-block-search__label screen-reader-text" for="wp-block-search__input-2">Search</label><div class="wp-block-search__inside-wrapper" style="width: 100%"><input class="wp-block-search__input" id="wp-block-search__input-2" name="s" placeholder="Search..." required="" type="search" value=""/><button aria-label="Search" class="wp-block-search__button wp-element-button" type="submit">Search</button></div></form></div>
<div aria-hidden="true" class="wp-block-spacer" style="height:var(--wp--preset--spacing--10)"></div>
</div>
</aside></div>
</div>
