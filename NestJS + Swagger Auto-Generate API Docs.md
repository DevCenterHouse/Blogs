
<div class="wp-block-group has-global-padding is-layout-constrained wp-block-group-is-layout-constrained" style="margin-bottom:var(--wp--preset--spacing--40);padding-top:var(--wp--preset--spacing--50)">
<figure class="wp-block-post-featured-image" style="margin-bottom:var(--wp--preset--spacing--40);"><img alt="Swagger" class="attachment-post-thumbnail size-post-thumbnail wp-post-image" decoding="async" fetchpriority="high" height="1080" sizes="(max-width: 1920px) 100vw, 1920px" src="https://www.devcentrehouse.eu/blogs/wp-content/uploads/2025/05/nest-swagger.jpg" srcset="https://www.devcentrehouse.eu/blogs/wp-content/uploads/2025/05/nest-swagger.jpg 1920w, https://www.devcentrehouse.eu/blogs/wp-content/uploads/2025/05/nest-swagger-300x169.jpg 300w, https://www.devcentrehouse.eu/blogs/wp-content/uploads/2025/05/nest-swagger-1024x576.jpg 1024w, https://www.devcentrehouse.eu/blogs/wp-content/uploads/2025/05/nest-swagger-768x432.jpg 768w, https://www.devcentrehouse.eu/blogs/wp-content/uploads/2025/05/nest-swagger-1536x864.jpg 1536w" style="object-fit:cover;" width="1920"/></figure>
<div class="wp-block-group is-vertical is-content-justification-stretch is-layout-flex wp-container-core-group-is-layout-6215b345 wp-block-group-is-layout-flex" style="padding-top:0;padding-bottom:0">
<h1 class="wp-block-post-title has-x-large-font-size">NestJS + Swagger: Auto-Generate API Docs</h1>
<div class="wp-block-template-part">
<div class="wp-block-group has-global-padding is-layout-constrained wp-block-group-is-layout-constrained">
<div class="wp-block-group is-content-justification-left is-layout-flex wp-container-core-group-is-layout-dfe8e91f wp-block-group-is-layout-flex">
<div class="wp-block-post-date"><time datetime="2025-05-12T13:37:19+00:00"><a href="https://www.devcentrehouse.eu/blogs/nestjs-swagger-auto-generate-api-docs/">May 12, 2025</a></time></div>
<p class="has-contrast-2-color has-text-color">—</p>
<p class="has-small-font-size has-contrast-2-color has-text-color">by</p>
<div class="wp-block-post-author-name"><a class="wp-block-post-author-name__link" href="https://www.devcentrehouse.eu/blogs/author/adstar/" target="_self">Anthony Mc Cann</a></div>
<div class="taxonomy-category wp-block-post-terms"><span class="wp-block-post-terms__prefix">in </span><a href="https://www.devcentrehouse.eu/blogs/category/technology/" rel="tag">Technology</a></div>
</div>
</div>
</div>
</div>
</div>
<div class="entry-content alignfull wp-block-post-content has-global-padding is-layout-constrained wp-block-post-content-is-layout-constrained">
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
</div>
<div class="wp-block-group has-global-padding is-layout-constrained wp-block-group-is-layout-constrained" style="margin-top:var(--wp--preset--spacing--40);padding-bottom:var(--wp--preset--spacing--50)">
<div class="taxonomy-post_tag is-style-pill wp-block-post-terms"><a href="https://www.devcentrehouse.eu/blogs/tag/api/" rel="tag">api</a><span class="wp-block-post-terms__separator"> </span><a href="https://www.devcentrehouse.eu/blogs/tag/api-documentation/" rel="tag">API Documentation</a><span class="wp-block-post-terms__separator"> </span><a href="https://www.devcentrehouse.eu/blogs/tag/backend-development/" rel="tag">backend development</a><span class="wp-block-post-terms__separator"> </span><a href="https://www.devcentrehouse.eu/blogs/tag/dev-centre-house-ireland/" rel="tag">Dev Centre House Ireland</a><span class="wp-block-post-terms__separator"> </span><a href="https://www.devcentrehouse.eu/blogs/tag/development/" rel="tag">Development</a><span class="wp-block-post-terms__separator"> </span><a href="https://www.devcentrehouse.eu/blogs/tag/nestjs/" rel="tag">nESTjs</a><span class="wp-block-post-terms__separator"> </span><a href="https://www.devcentrehouse.eu/blogs/tag/swagger/" rel="tag">Swagger</a></div>
<div class="wp-block-group has-global-padding is-layout-constrained wp-block-group-is-layout-constrained">
<div aria-hidden="true" class="wp-block-spacer" style="height:var(--wp--preset--spacing--40)">
</div>
<hr class="wp-block-separator has-text-color has-contrast-3-color has-alpha-channel-opacity has-contrast-3-background-color has-background is-style-wide" style="margin-bottom:var(--wp--preset--spacing--40)"/>
<div class="wp-block-comments wp-block-comments-query-loop">
<h2 class="wp-block-heading">Comments</h2>
<div class="comment-respond wp-block-post-comments-form" id="respond" style="padding-top:var(--wp--preset--spacing--20);padding-bottom:var(--wp--preset--spacing--20);">
<h3 class="comment-reply-title" id="reply-title">Leave a Reply <small><a href="/blogs/nestjs-swagger-auto-generate-api-docs/#respond" id="cancel-comment-reply-link" rel="nofollow" style="display:none;">Cancel reply</a></small></h3><form action="https://www.devcentrehouse.eu/blogs/wp-comments-post.php" class="comment-form" id="commentform" method="post" novalidate=""><p class="comment-notes"><span id="email-notes">Your email address will not be published.</span> <span class="required-field-message">Required fields are marked <span class="required">*</span></span></p><p class="comment-form-comment"><label for="comment">Comment <span class="required">*</span></label> <textarea cols="45" id="comment" maxlength="65525" name="comment" required="" rows="8"></textarea></p><p class="comment-form-author"><label for="author">Name <span class="required">*</span></label> <input autocomplete="name" id="author" maxlength="245" name="author" required="" size="30" type="text" value=""/></p>
<p class="comment-form-email"><label for="email">Email <span class="required">*</span></label> <input aria-describedby="email-notes" autocomplete="email" id="email" maxlength="100" name="email" required="" size="30" type="email" value=""/></p>
<p class="comment-form-url"><label for="url">Website</label> <input autocomplete="url" id="url" maxlength="200" name="url" size="30" type="url" value=""/></p>
<p class="comment-form-cookies-consent"><input id="wp-comment-cookies-consent" name="wp-comment-cookies-consent" type="checkbox" value="yes"/> <label for="wp-comment-cookies-consent">Save my name, email, and website in this browser for the next time I comment.</label></p>
<input class="agr-recaptcha-response" name="g-recaptcha-response" type="hidden" value=""/><script>
                function wpcaptcha_captcha(){
                    grecaptcha.execute("6LcqUfIqAAAAAGsZpRiaxTHv4zNpIeTivYdNQsZI", {action: "submit"}).then(function(token) {
                        var captchas = document.querySelectorAll(".agr-recaptcha-response");
                        captchas.forEach(function(captcha) {
                            captcha.value = token;
                        });
                    });
                }
                </script><script id="wpcaptcha-recaptcha-js" src="https://www.google.com/recaptcha/api.js?onload=wpcaptcha_captcha&amp;render=6LcqUfIqAAAAAGsZpRiaxTHv4zNpIeTivYdNQsZI&amp;ver=1.29"></script><p class="form-submit wp-block-button"><input class="wp-block-button__link wp-element-button" id="submit" name="submit" type="submit" value="Post Comment"/> <input id="comment_post_ID" name="comment_post_ID" type="hidden" value="1686"/>
<input id="comment_parent" name="comment_parent" type="hidden" value="0"/>
</p></form> </div><!-- #respond -->
</div>
<nav aria-label="Posts" class="wp-block-group is-content-justification-space-between is-nowrap is-layout-flex wp-container-core-group-is-layout-c08a3ef2 wp-block-group-is-layout-flex" style="padding-top:var(--wp--preset--spacing--40);padding-bottom:var(--wp--preset--spacing--40)">
<div class="post-navigation-link-previous wp-block-post-navigation-link"><span aria-hidden="true" class="wp-block-post-navigation-link__arrow-previous is-arrow-arrow">←</span><a href="https://www.devcentrehouse.eu/blogs/angular-beginners-guide-key-features/" rel="prev"><span class="post-navigation-link__label">Previous: </span> <span class="post-navigation-link__title">A Beginner’s Guide to Angular: Key Features and How to Get Started</span></a></div>
<div class="post-navigation-link-next wp-block-post-navigation-link"><a href="https://www.devcentrehouse.eu/blogs/launch-nestjs-fast-deploy-once-scale/" rel="next"><span class="post-navigation-link__label">Next: </span> <span class="post-navigation-link__title">Launch NestJS Fast: Deploy Once, Scale Anywhere</span></a><span aria-hidden="true" class="wp-block-post-navigation-link__arrow-next is-arrow-arrow">→</span></div>
</nav>
</div>
</div>
