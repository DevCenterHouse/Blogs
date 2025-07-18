
<div class="inside-article">
<header aria-label="Content" class="entry-header">
<h1 class="entry-title" itemprop="headline">File Uploads in NestJS Using Multer</h1> 
</header>
<div class="featured-image cv-col-12 post-image">
<img alt="" class="size-full cv-col-12 wp-post-image" decoding="async" fetchpriority="high" height="1080" itemprop="image" sizes="(max-width: 1920px) 100vw, 1920px" src="https://www.devcentrehouse.eu/blogs/wp-content/uploads/2025/05/nestjs-fileupload.jpg" srcset="https://www.devcentrehouse.eu/blogs/wp-content/uploads/2025/05/nestjs-fileupload.jpg 1920w, https://www.devcentrehouse.eu/blogs/wp-content/uploads/2025/05/nestjs-fileupload-300x169.jpg 300w, https://www.devcentrehouse.eu/blogs/wp-content/uploads/2025/05/nestjs-fileupload-1024x576.jpg 1024w, https://www.devcentrehouse.eu/blogs/wp-content/uploads/2025/05/nestjs-fileupload-768x432.jpg 768w, https://www.devcentrehouse.eu/blogs/wp-content/uploads/2025/05/nestjs-fileupload-1536x864.jpg 1536w" style="aspect-ratio:0;" width="1920"/> </div>
<div class="entry-content" itemprop="text">
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
</div> <footer aria-label="Entry meta" class="entry-meta">
</footer>
</div>
