
<div class="wp-block-group has-global-padding is-layout-constrained wp-block-group-is-layout-constrained" style="margin-bottom:var(--wp--preset--spacing--40);padding-top:var(--wp--preset--spacing--50)">
<figure class="wp-block-post-featured-image" style="margin-bottom:var(--wp--preset--spacing--40);"><img alt="" class="attachment-post-thumbnail size-post-thumbnail wp-post-image" decoding="async" fetchpriority="high" height="1080" sizes="(max-width: 1920px) 100vw, 1920px" src="https://www.devcentrehouse.eu/blogs/wp-content/uploads/2025/05/nestjs-decorators.jpg" srcset="https://www.devcentrehouse.eu/blogs/wp-content/uploads/2025/05/nestjs-decorators.jpg 1920w, https://www.devcentrehouse.eu/blogs/wp-content/uploads/2025/05/nestjs-decorators-300x169.jpg 300w, https://www.devcentrehouse.eu/blogs/wp-content/uploads/2025/05/nestjs-decorators-1024x576.jpg 1024w, https://www.devcentrehouse.eu/blogs/wp-content/uploads/2025/05/nestjs-decorators-768x432.jpg 768w, https://www.devcentrehouse.eu/blogs/wp-content/uploads/2025/05/nestjs-decorators-1536x864.jpg 1536w" style="object-fit:cover;" width="1920"/></figure>
<div class="wp-block-group is-vertical is-content-justification-stretch is-layout-flex wp-container-core-group-is-layout-6215b345 wp-block-group-is-layout-flex" style="padding-top:0;padding-bottom:0">
<h1 class="wp-block-post-title has-x-large-font-size">Creating Custom Decorators in NestJS</h1>
<div class="wp-block-template-part">
<div class="wp-block-group has-global-padding is-layout-constrained wp-block-group-is-layout-constrained">
<div class="wp-block-group is-content-justification-left is-layout-flex wp-container-core-group-is-layout-dfe8e91f wp-block-group-is-layout-flex">
<div class="wp-block-post-date"><time datetime="2025-05-15T09:31:59+00:00"><a href="https://www.devcentrehouse.eu/blogs/creating-custom-decorators-in-nestjs/">May 15, 2025</a></time></div>
<p class="has-contrast-2-color has-text-color">—</p>
<p class="has-small-font-size has-contrast-2-color has-text-color">by</p>
<div class="wp-block-post-author-name"><a class="wp-block-post-author-name__link" href="https://www.devcentrehouse.eu/blogs/author/adstar/" target="_self">Anthony Mc Cann</a></div>
<div class="taxonomy-category wp-block-post-terms"><span class="wp-block-post-terms__prefix">in </span><a href="https://www.devcentrehouse.eu/blogs/category/uncategorized/" rel="tag">Uncategorized</a><span class="wp-block-post-terms__separator">, </span><a href="https://www.devcentrehouse.eu/blogs/category/technology/" rel="tag">Technology</a></div>
</div>
</div>
</div>
</div>
</div>
<div class="entry-content alignfull wp-block-post-content has-global-padding is-layout-constrained wp-block-post-content-is-layout-constrained">
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
</div>
<div class="wp-block-group has-global-padding is-layout-constrained wp-block-group-is-layout-constrained" style="margin-top:var(--wp--preset--spacing--40);padding-bottom:var(--wp--preset--spacing--50)">
<div class="taxonomy-post_tag is-style-pill wp-block-post-terms"><a href="https://www.devcentrehouse.eu/blogs/tag/dev-centre-house-ireland/" rel="tag">Dev Centre House Ireland</a><span class="wp-block-post-terms__separator"> </span><a href="https://www.devcentrehouse.eu/blogs/tag/development/" rel="tag">Development</a><span class="wp-block-post-terms__separator"> </span><a href="https://www.devcentrehouse.eu/blogs/tag/nestjs/" rel="tag">nESTjs</a><span class="wp-block-post-terms__separator"> </span><a href="https://www.devcentrehouse.eu/blogs/tag/software-development/" rel="tag">software development</a></div>
<div class="wp-block-group has-global-padding is-layout-constrained wp-block-group-is-layout-constrained">
<div aria-hidden="true" class="wp-block-spacer" style="height:var(--wp--preset--spacing--40)">
</div>
<hr class="wp-block-separator has-text-color has-contrast-3-color has-alpha-channel-opacity has-contrast-3-background-color has-background is-style-wide" style="margin-bottom:var(--wp--preset--spacing--40)"/>
<div class="wp-block-comments wp-block-comments-query-loop">
<h2 class="wp-block-heading">Comments</h2>
<div class="comment-respond wp-block-post-comments-form" id="respond" style="padding-top:var(--wp--preset--spacing--20);padding-bottom:var(--wp--preset--spacing--20);">
<h3 class="comment-reply-title" id="reply-title">Leave a Reply <small><a href="/blogs/creating-custom-decorators-in-nestjs/#respond" id="cancel-comment-reply-link" rel="nofollow" style="display:none;">Cancel reply</a></small></h3><form action="https://www.devcentrehouse.eu/blogs/wp-comments-post.php" class="comment-form" id="commentform" method="post" novalidate=""><p class="comment-notes"><span id="email-notes">Your email address will not be published.</span> <span class="required-field-message">Required fields are marked <span class="required">*</span></span></p><p class="comment-form-comment"><label for="comment">Comment <span class="required">*</span></label> <textarea cols="45" id="comment" maxlength="65525" name="comment" required="" rows="8"></textarea></p><p class="comment-form-author"><label for="author">Name <span class="required">*</span></label> <input autocomplete="name" id="author" maxlength="245" name="author" required="" size="30" type="text" value=""/></p>
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
                </script><script id="wpcaptcha-recaptcha-js" src="https://www.google.com/recaptcha/api.js?onload=wpcaptcha_captcha&amp;render=6LcqUfIqAAAAAGsZpRiaxTHv4zNpIeTivYdNQsZI&amp;ver=1.29"></script><p class="form-submit wp-block-button"><input class="wp-block-button__link wp-element-button" id="submit" name="submit" type="submit" value="Post Comment"/> <input id="comment_post_ID" name="comment_post_ID" type="hidden" value="1742"/>
<input id="comment_parent" name="comment_parent" type="hidden" value="0"/>
</p></form> </div><!-- #respond -->
</div>
<nav aria-label="Posts" class="wp-block-group is-content-justification-space-between is-nowrap is-layout-flex wp-container-core-group-is-layout-c08a3ef2 wp-block-group-is-layout-flex" style="padding-top:var(--wp--preset--spacing--40);padding-bottom:var(--wp--preset--spacing--40)">
<div class="post-navigation-link-previous wp-block-post-navigation-link"><span aria-hidden="true" class="wp-block-post-navigation-link__arrow-previous is-arrow-arrow">←</span><a href="https://www.devcentrehouse.eu/blogs/nestjs-dtos-pipes-scalable-backend-apps/" rel="prev"><span class="post-navigation-link__label">Previous: </span> <span class="post-navigation-link__title">Using DTOs and Validation Pipes in NestJS</span></a></div>
<div class="post-navigation-link-next wp-block-post-navigation-link"><a href="https://www.devcentrehouse.eu/blogs/using-environment-variables-in-nestjs-projects/" rel="next"><span class="post-navigation-link__label">Next: </span> <span class="post-navigation-link__title">Using Environment Variables in NestJS Projects</span></a><span aria-hidden="true" class="wp-block-post-navigation-link__arrow-next is-arrow-arrow">→</span></div>
</nav>
</div>
</div>
