
<div class="wp-block-group has-global-padding is-layout-constrained wp-block-group-is-layout-constrained" style="margin-bottom:var(--wp--preset--spacing--40);padding-top:var(--wp--preset--spacing--50)">
<figure class="wp-block-post-featured-image" style="margin-bottom:var(--wp--preset--spacing--40);"><img alt="" class="attachment-post-thumbnail size-post-thumbnail wp-post-image" decoding="async" fetchpriority="high" height="1080" sizes="(max-width: 1920px) 100vw, 1920px" src="https://www.devcentrehouse.eu/blogs/wp-content/uploads/2025/05/nest-env.jpg" srcset="https://www.devcentrehouse.eu/blogs/wp-content/uploads/2025/05/nest-env.jpg 1920w, https://www.devcentrehouse.eu/blogs/wp-content/uploads/2025/05/nest-env-300x169.jpg 300w, https://www.devcentrehouse.eu/blogs/wp-content/uploads/2025/05/nest-env-1024x576.jpg 1024w, https://www.devcentrehouse.eu/blogs/wp-content/uploads/2025/05/nest-env-768x432.jpg 768w, https://www.devcentrehouse.eu/blogs/wp-content/uploads/2025/05/nest-env-1536x864.jpg 1536w" style="object-fit:cover;" width="1920"/></figure>
<div class="wp-block-group is-vertical is-content-justification-stretch is-layout-flex wp-container-core-group-is-layout-6215b345 wp-block-group-is-layout-flex" style="padding-top:0;padding-bottom:0">
<h1 class="wp-block-post-title has-x-large-font-size">Using Environment Variables in NestJS Projects</h1>
<div class="wp-block-template-part">
<div class="wp-block-group has-global-padding is-layout-constrained wp-block-group-is-layout-constrained">
<div class="wp-block-group is-content-justification-left is-layout-flex wp-container-core-group-is-layout-dfe8e91f wp-block-group-is-layout-flex">
<div class="wp-block-post-date"><time datetime="2025-05-15T11:44:56+00:00"><a href="https://www.devcentrehouse.eu/blogs/using-environment-variables-in-nestjs-projects/">May 15, 2025</a></time></div>
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
</div>
<div class="wp-block-group has-global-padding is-layout-constrained wp-block-group-is-layout-constrained" style="margin-top:var(--wp--preset--spacing--40);padding-bottom:var(--wp--preset--spacing--50)">
<div class="taxonomy-post_tag is-style-pill wp-block-post-terms"><a href="https://www.devcentrehouse.eu/blogs/tag/dev-centre-house/" rel="tag">Dev Centre House</a><span class="wp-block-post-terms__separator"> </span><a href="https://www.devcentrehouse.eu/blogs/tag/dev-centre-house-ireland/" rel="tag">Dev Centre House Ireland</a><span class="wp-block-post-terms__separator"> </span><a href="https://www.devcentrehouse.eu/blogs/tag/development/" rel="tag">Development</a><span class="wp-block-post-terms__separator"> </span><a href="https://www.devcentrehouse.eu/blogs/tag/nestjs/" rel="tag">nESTjs</a><span class="wp-block-post-terms__separator"> </span><a href="https://www.devcentrehouse.eu/blogs/tag/software-development/" rel="tag">software development</a></div>
<div class="wp-block-group has-global-padding is-layout-constrained wp-block-group-is-layout-constrained">
<div aria-hidden="true" class="wp-block-spacer" style="height:var(--wp--preset--spacing--40)">
</div>
<hr class="wp-block-separator has-text-color has-contrast-3-color has-alpha-channel-opacity has-contrast-3-background-color has-background is-style-wide" style="margin-bottom:var(--wp--preset--spacing--40)"/>
<div class="wp-block-comments wp-block-comments-query-loop">
<h2 class="wp-block-heading">Comments</h2>
<div class="comment-respond wp-block-post-comments-form" id="respond" style="padding-top:var(--wp--preset--spacing--20);padding-bottom:var(--wp--preset--spacing--20);">
<h3 class="comment-reply-title" id="reply-title">Leave a Reply <small><a href="/blogs/using-environment-variables-in-nestjs-projects/#respond" id="cancel-comment-reply-link" rel="nofollow" style="display:none;">Cancel reply</a></small></h3><form action="https://www.devcentrehouse.eu/blogs/wp-comments-post.php" class="comment-form" id="commentform" method="post" novalidate=""><p class="comment-notes"><span id="email-notes">Your email address will not be published.</span> <span class="required-field-message">Required fields are marked <span class="required">*</span></span></p><p class="comment-form-comment"><label for="comment">Comment <span class="required">*</span></label> <textarea cols="45" id="comment" maxlength="65525" name="comment" required="" rows="8"></textarea></p><p class="comment-form-author"><label for="author">Name <span class="required">*</span></label> <input autocomplete="name" id="author" maxlength="245" name="author" required="" size="30" type="text" value=""/></p>
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
                </script><script id="wpcaptcha-recaptcha-js" src="https://www.google.com/recaptcha/api.js?onload=wpcaptcha_captcha&amp;render=6LcqUfIqAAAAAGsZpRiaxTHv4zNpIeTivYdNQsZI&amp;ver=1.29"></script><p class="form-submit wp-block-button"><input class="wp-block-button__link wp-element-button" id="submit" name="submit" type="submit" value="Post Comment"/> <input id="comment_post_ID" name="comment_post_ID" type="hidden" value="1752"/>
<input id="comment_parent" name="comment_parent" type="hidden" value="0"/>
</p></form> </div><!-- #respond -->
</div>
<nav aria-label="Posts" class="wp-block-group is-content-justification-space-between is-nowrap is-layout-flex wp-container-core-group-is-layout-c08a3ef2 wp-block-group-is-layout-flex" style="padding-top:var(--wp--preset--spacing--40);padding-bottom:var(--wp--preset--spacing--40)">
<div class="post-navigation-link-previous wp-block-post-navigation-link"><span aria-hidden="true" class="wp-block-post-navigation-link__arrow-previous is-arrow-arrow">←</span><a href="https://www.devcentrehouse.eu/blogs/creating-custom-decorators-in-nestjs/" rel="prev"><span class="post-navigation-link__label">Previous: </span> <span class="post-navigation-link__title">Creating Custom Decorators in NestJS</span></a></div>
<div class="post-navigation-link-next wp-block-post-navigation-link"><a href="https://www.devcentrehouse.eu/blogs/file-uploads-in-nestjs-with-multer/" rel="next"><span class="post-navigation-link__label">Next: </span> <span class="post-navigation-link__title">File Uploads in NestJS Using Multer</span></a><span aria-hidden="true" class="wp-block-post-navigation-link__arrow-next is-arrow-arrow">→</span></div>
</nav>
</div>
</div>
