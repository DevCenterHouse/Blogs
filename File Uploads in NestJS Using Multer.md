
<div class="wp-block-group has-global-padding is-layout-constrained wp-block-group-is-layout-constrained" style="margin-bottom:var(--wp--preset--spacing--40);padding-top:var(--wp--preset--spacing--50)">
<figure class="wp-block-post-featured-image" style="margin-bottom:var(--wp--preset--spacing--40);"><img alt="" class="attachment-post-thumbnail size-post-thumbnail wp-post-image" decoding="async" fetchpriority="high" height="1080" sizes="(max-width: 1920px) 100vw, 1920px" src="https://www.devcentrehouse.eu/blogs/wp-content/uploads/2025/05/nestjs-fileupload.jpg" srcset="https://www.devcentrehouse.eu/blogs/wp-content/uploads/2025/05/nestjs-fileupload.jpg 1920w, https://www.devcentrehouse.eu/blogs/wp-content/uploads/2025/05/nestjs-fileupload-300x169.jpg 300w, https://www.devcentrehouse.eu/blogs/wp-content/uploads/2025/05/nestjs-fileupload-1024x576.jpg 1024w, https://www.devcentrehouse.eu/blogs/wp-content/uploads/2025/05/nestjs-fileupload-768x432.jpg 768w, https://www.devcentrehouse.eu/blogs/wp-content/uploads/2025/05/nestjs-fileupload-1536x864.jpg 1536w" style="object-fit:cover;" width="1920"/></figure>
<div class="wp-block-group is-vertical is-content-justification-stretch is-layout-flex wp-container-core-group-is-layout-6215b345 wp-block-group-is-layout-flex" style="padding-top:0;padding-bottom:0">
<h1 class="wp-block-post-title has-x-large-font-size">File Uploads in NestJS Using Multer</h1>
<div class="wp-block-template-part">
<div class="wp-block-group has-global-padding is-layout-constrained wp-block-group-is-layout-constrained">
<div class="wp-block-group is-content-justification-left is-layout-flex wp-container-core-group-is-layout-dfe8e91f wp-block-group-is-layout-flex">
<div class="wp-block-post-date"><time datetime="2025-05-16T14:47:23+00:00"><a href="https://www.devcentrehouse.eu/blogs/file-uploads-in-nestjs-with-multer/">May 16, 2025</a></time></div>
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
<p>Handling file uploads is a critical part of many web applications—from uploading profile pictures to processing documents. Fortunately, <strong>NestJS</strong> offers a clean and structured way to handle this using <strong>Multer</strong>, a powerful middleware for handling <code>multipart/form-data</code>.</p>
<p>In this guide, you’ll learn how to implement <strong>file uploads in NestJS using Multer</strong>, including single and multiple file uploads, file validation, and storage configuration.</p>
<h2 class="wp-block-heading">Why Use Multer with NestJS?</h2>
<p>Multer integrates seamlessly with NestJS via the <code>@nestjs/platform-express</code> package. It allows you to control storage location, rename files, validate file types and sizes, and limit uploads per route—all while keeping your code modular and clean.</p>
<h2 class="wp-block-heading">Setting Up Your NestJS Project</h2>
<p>If you’re starting from scratch:</p>
<figure class="wp-block-image size-large"><img alt="" class="wp-image-1770" decoding="async" height="77" sizes="(max-width: 1024px) 100vw, 1024px" src="https://www.devcentrehouse.eu/blogs/wp-content/uploads/2025/05/Screenshot-2025-05-16-at-15.43.15-1024x77.png" srcset="https://www.devcentrehouse.eu/blogs/wp-content/uploads/2025/05/Screenshot-2025-05-16-at-15.43.15-1024x77.png 1024w, https://www.devcentrehouse.eu/blogs/wp-content/uploads/2025/05/Screenshot-2025-05-16-at-15.43.15-300x23.png 300w, https://www.devcentrehouse.eu/blogs/wp-content/uploads/2025/05/Screenshot-2025-05-16-at-15.43.15-768x58.png 768w, https://www.devcentrehouse.eu/blogs/wp-content/uploads/2025/05/Screenshot-2025-05-16-at-15.43.15.png 1382w" width="1024"/></figure>
<p>Install required packages:</p>
<figure class="wp-block-image size-large"><img alt="" class="wp-image-1769" decoding="async" height="56" sizes="(max-width: 1024px) 100vw, 1024px" src="https://www.devcentrehouse.eu/blogs/wp-content/uploads/2025/05/Screenshot-2025-05-16-at-15.43.11-1024x56.png" srcset="https://www.devcentrehouse.eu/blogs/wp-content/uploads/2025/05/Screenshot-2025-05-16-at-15.43.11-1024x56.png 1024w, https://www.devcentrehouse.eu/blogs/wp-content/uploads/2025/05/Screenshot-2025-05-16-at-15.43.11-300x16.png 300w, https://www.devcentrehouse.eu/blogs/wp-content/uploads/2025/05/Screenshot-2025-05-16-at-15.43.11-768x42.png 768w, https://www.devcentrehouse.eu/blogs/wp-content/uploads/2025/05/Screenshot-2025-05-16-at-15.43.11.png 1382w" width="1024"/></figure>
<h2 class="wp-block-heading">Creating the Upload Module</h2>
<p>First, create a module, controller, and service:</p>
<figure class="wp-block-image size-large"><img alt="" class="wp-image-1768" decoding="async" height="95" loading="lazy" sizes="auto, (max-width: 1024px) 100vw, 1024px" src="https://www.devcentrehouse.eu/blogs/wp-content/uploads/2025/05/Screenshot-2025-05-16-at-15.43.06-1024x95.png" srcset="https://www.devcentrehouse.eu/blogs/wp-content/uploads/2025/05/Screenshot-2025-05-16-at-15.43.06-1024x95.png 1024w, https://www.devcentrehouse.eu/blogs/wp-content/uploads/2025/05/Screenshot-2025-05-16-at-15.43.06-300x28.png 300w, https://www.devcentrehouse.eu/blogs/wp-content/uploads/2025/05/Screenshot-2025-05-16-at-15.43.06-768x71.png 768w, https://www.devcentrehouse.eu/blogs/wp-content/uploads/2025/05/Screenshot-2025-05-16-at-15.43.06.png 1400w" width="1024"/></figure>
<p>Now let’s dive into building the file upload feature.</p>
<h2 class="wp-block-heading">Single File Upload</h2>
<p>In your <code>upload.controller.ts</code>:</p>
<figure class="wp-block-image size-large"><img alt="" class="wp-image-1767" decoding="async" height="732" loading="lazy" sizes="auto, (max-width: 1024px) 100vw, 1024px" src="https://www.devcentrehouse.eu/blogs/wp-content/uploads/2025/05/Screenshot-2025-05-16-at-15.42.56-1024x732.png" srcset="https://www.devcentrehouse.eu/blogs/wp-content/uploads/2025/05/Screenshot-2025-05-16-at-15.42.56-1024x732.png 1024w, https://www.devcentrehouse.eu/blogs/wp-content/uploads/2025/05/Screenshot-2025-05-16-at-15.42.56-300x214.png 300w, https://www.devcentrehouse.eu/blogs/wp-content/uploads/2025/05/Screenshot-2025-05-16-at-15.42.56-768x549.png 768w, https://www.devcentrehouse.eu/blogs/wp-content/uploads/2025/05/Screenshot-2025-05-16-at-15.42.56.png 1394w" width="1024"/></figure>
<p>Make sure the <code>uploads</code> directory exists or handle its creation.</p>
<h2 class="wp-block-heading">Multiple File Uploads</h2>
<p>To upload more than one file:</p>
<figure class="wp-block-image size-large"><img alt="" class="wp-image-1766" decoding="async" height="548" loading="lazy" sizes="auto, (max-width: 1024px) 100vw, 1024px" src="https://www.devcentrehouse.eu/blogs/wp-content/uploads/2025/05/Screenshot-2025-05-16-at-15.42.48-1024x548.png" srcset="https://www.devcentrehouse.eu/blogs/wp-content/uploads/2025/05/Screenshot-2025-05-16-at-15.42.48-1024x548.png 1024w, https://www.devcentrehouse.eu/blogs/wp-content/uploads/2025/05/Screenshot-2025-05-16-at-15.42.48-300x161.png 300w, https://www.devcentrehouse.eu/blogs/wp-content/uploads/2025/05/Screenshot-2025-05-16-at-15.42.48-768x411.png 768w, https://www.devcentrehouse.eu/blogs/wp-content/uploads/2025/05/Screenshot-2025-05-16-at-15.42.48.png 1398w" width="1024"/></figure>
<p>This limits the number of uploaded files to 5. You can change that number as needed.</p>
<h2 class="wp-block-heading">Validating File Types and Size</h2>
<p>Use the <code>ParseFilePipeBuilder</code> to add validation:</p>
<figure class="wp-block-image size-large"><img alt="" class="wp-image-1765" decoding="async" height="530" loading="lazy" sizes="auto, (max-width: 1024px) 100vw, 1024px" src="https://www.devcentrehouse.eu/blogs/wp-content/uploads/2025/05/Screenshot-2025-05-16-at-15.42.43-1024x530.png" srcset="https://www.devcentrehouse.eu/blogs/wp-content/uploads/2025/05/Screenshot-2025-05-16-at-15.42.43-1024x530.png 1024w, https://www.devcentrehouse.eu/blogs/wp-content/uploads/2025/05/Screenshot-2025-05-16-at-15.42.43-300x155.png 300w, https://www.devcentrehouse.eu/blogs/wp-content/uploads/2025/05/Screenshot-2025-05-16-at-15.42.43-768x397.png 768w, https://www.devcentrehouse.eu/blogs/wp-content/uploads/2025/05/Screenshot-2025-05-16-at-15.42.43.png 1392w" width="1024"/></figure>
<p>This ensures only <code>.jpeg</code> files under 1MB are accepted.</p>
<h2 class="wp-block-heading">Serving Uploaded Files</h2>
<p>To serve uploaded files, update <code>main.ts</code>:</p>
<figure class="wp-block-image size-large"><img alt="" class="wp-image-1764" decoding="async" height="287" loading="lazy" sizes="auto, (max-width: 1024px) 100vw, 1024px" src="https://www.devcentrehouse.eu/blogs/wp-content/uploads/2025/05/Screenshot-2025-05-16-at-15.42.37-1024x287.png" srcset="https://www.devcentrehouse.eu/blogs/wp-content/uploads/2025/05/Screenshot-2025-05-16-at-15.42.37-1024x287.png 1024w, https://www.devcentrehouse.eu/blogs/wp-content/uploads/2025/05/Screenshot-2025-05-16-at-15.42.37-300x84.png 300w, https://www.devcentrehouse.eu/blogs/wp-content/uploads/2025/05/Screenshot-2025-05-16-at-15.42.37-768x215.png 768w, https://www.devcentrehouse.eu/blogs/wp-content/uploads/2025/05/Screenshot-2025-05-16-at-15.42.37.png 1358w" width="1024"/></figure>
<p>Now you can access uploaded files via <code>http://localhost:3000/filename</code>.</p>
<h2 class="wp-block-heading">Best Practices</h2>
<ul class="wp-block-list">
<li>Store sensitive files in a protected folder, not public.</li>
<li>Use UUIDs or hash-based names to avoid collisions.</li>
<li>Move files to cloud storage like AWS S3 or Cloudinary for production.</li>
<li>Clean up old or unused files periodically.</li>
</ul>
<h2 class="wp-block-heading">Final Thoughts</h2>
<figure class="wp-block-image size-large"><img alt="" class="wp-image-1754" decoding="async" height="576" loading="lazy" sizes="auto, (max-width: 1024px) 100vw, 1024px" src="https://www.devcentrehouse.eu/blogs/wp-content/uploads/2025/05/node-dch-latest-2-1024x576.jpg" srcset="https://www.devcentrehouse.eu/blogs/wp-content/uploads/2025/05/node-dch-latest-2-1024x576.jpg 1024w, https://www.devcentrehouse.eu/blogs/wp-content/uploads/2025/05/node-dch-latest-2-300x169.jpg 300w, https://www.devcentrehouse.eu/blogs/wp-content/uploads/2025/05/node-dch-latest-2-768x432.jpg 768w, https://www.devcentrehouse.eu/blogs/wp-content/uploads/2025/05/node-dch-latest-2-1536x864.jpg 1536w, https://www.devcentrehouse.eu/blogs/wp-content/uploads/2025/05/node-dch-latest-2.jpg 1920w" width="1024"/></figure>
<p><strong>Uploading files in NestJS using Multer</strong> is straightforward and flexible. You get full control over how files are stored, validated, and accessed—making it perfect for applications that need to handle user uploads reliably.</p>
<p>For more scalable backend solutions with <strong>NestJS and Node.js</strong>, check out <a href="https://www.devcentrehouse.eu/en/technologies/back-end/nodejs">this backend tech stack guide from Dev Centre House Ireland</a>.</p>
<!--— Calendly inline widget begin ---->


<!--— Calendly inline widget end ---->
</div>
<div class="wp-block-group has-global-padding is-layout-constrained wp-block-group-is-layout-constrained" style="margin-top:var(--wp--preset--spacing--40);padding-bottom:var(--wp--preset--spacing--50)">
<div class="taxonomy-post_tag is-style-pill wp-block-post-terms"><a href="https://www.devcentrehouse.eu/blogs/tag/backend/" rel="tag">backend</a><span class="wp-block-post-terms__separator"> </span><a href="https://www.devcentrehouse.eu/blogs/tag/backend-development/" rel="tag">backend development</a><span class="wp-block-post-terms__separator"> </span><a href="https://www.devcentrehouse.eu/blogs/tag/dev-centre-house-ireland/" rel="tag">Dev Centre House Ireland</a><span class="wp-block-post-terms__separator"> </span><a href="https://www.devcentrehouse.eu/blogs/tag/development/" rel="tag">Development</a><span class="wp-block-post-terms__separator"> </span><a href="https://www.devcentrehouse.eu/blogs/tag/multer/" rel="tag">Multer</a><span class="wp-block-post-terms__separator"> </span><a href="https://www.devcentrehouse.eu/blogs/tag/nestjs/" rel="tag">nESTjs</a><span class="wp-block-post-terms__separator"> </span><a href="https://www.devcentrehouse.eu/blogs/tag/software-development/" rel="tag">software development</a></div>
<div class="wp-block-group has-global-padding is-layout-constrained wp-block-group-is-layout-constrained">
<div aria-hidden="true" class="wp-block-spacer" style="height:var(--wp--preset--spacing--40)">
</div>
<hr class="wp-block-separator has-text-color has-contrast-3-color has-alpha-channel-opacity has-contrast-3-background-color has-background is-style-wide" style="margin-bottom:var(--wp--preset--spacing--40)"/>
<div class="wp-block-comments wp-block-comments-query-loop">
<h2 class="wp-block-heading">Comments</h2>
<div class="comment-respond wp-block-post-comments-form" id="respond" style="padding-top:var(--wp--preset--spacing--20);padding-bottom:var(--wp--preset--spacing--20);">
<h3 class="comment-reply-title" id="reply-title">Leave a Reply <small><a href="/blogs/file-uploads-in-nestjs-with-multer/#respond" id="cancel-comment-reply-link" rel="nofollow" style="display:none;">Cancel reply</a></small></h3><form action="https://www.devcentrehouse.eu/blogs/wp-comments-post.php" class="comment-form" id="commentform" method="post" novalidate=""><p class="comment-notes"><span id="email-notes">Your email address will not be published.</span> <span class="required-field-message">Required fields are marked <span class="required">*</span></span></p><p class="comment-form-comment"><label for="comment">Comment <span class="required">*</span></label> <textarea cols="45" id="comment" maxlength="65525" name="comment" required="" rows="8"></textarea></p><p class="comment-form-author"><label for="author">Name <span class="required">*</span></label> <input autocomplete="name" id="author" maxlength="245" name="author" required="" size="30" type="text" value=""/></p>
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
                </script><script id="wpcaptcha-recaptcha-js" src="https://www.google.com/recaptcha/api.js?onload=wpcaptcha_captcha&amp;render=6LcqUfIqAAAAAGsZpRiaxTHv4zNpIeTivYdNQsZI&amp;ver=1.29"></script><p class="form-submit wp-block-button"><input class="wp-block-button__link wp-element-button" id="submit" name="submit" type="submit" value="Post Comment"/> <input id="comment_post_ID" name="comment_post_ID" type="hidden" value="1763"/>
<input id="comment_parent" name="comment_parent" type="hidden" value="0"/>
</p></form> </div><!-- #respond -->
</div>
<nav aria-label="Posts" class="wp-block-group is-content-justification-space-between is-nowrap is-layout-flex wp-container-core-group-is-layout-c08a3ef2 wp-block-group-is-layout-flex" style="padding-top:var(--wp--preset--spacing--40);padding-bottom:var(--wp--preset--spacing--40)">
<div class="post-navigation-link-previous wp-block-post-navigation-link"><span aria-hidden="true" class="wp-block-post-navigation-link__arrow-previous is-arrow-arrow">←</span><a href="https://www.devcentrehouse.eu/blogs/using-environment-variables-in-nestjs-projects/" rel="prev"><span class="post-navigation-link__label">Previous: </span> <span class="post-navigation-link__title">Using Environment Variables in NestJS Projects</span></a></div>
<div class="post-navigation-link-next wp-block-post-navigation-link"><a href="https://www.devcentrehouse.eu/blogs/pagination-nestjs-api-practices/" rel="next"><span class="post-navigation-link__label">Next: </span> <span class="post-navigation-link__title">Pagination and Filtering in NestJS APIs</span></a><span aria-hidden="true" class="wp-block-post-navigation-link__arrow-next is-arrow-arrow">→</span></div>
</nav>
</div>
</div>
