
<div class="wp-block-group has-global-padding is-layout-constrained wp-block-group-is-layout-constrained" style="margin-bottom:var(--wp--preset--spacing--40);padding-top:var(--wp--preset--spacing--50)">
<figure class="wp-block-post-featured-image" style="margin-bottom:var(--wp--preset--spacing--40);"><img alt="Git" class="attachment-post-thumbnail size-post-thumbnail wp-post-image" decoding="async" fetchpriority="high" height="520" sizes="(max-width: 1000px) 100vw, 1000px" src="https://www.devcentrehouse.eu/blogs/wp-content/uploads/2025/04/git_commands.png" srcset="https://www.devcentrehouse.eu/blogs/wp-content/uploads/2025/04/git_commands.png 1000w, https://www.devcentrehouse.eu/blogs/wp-content/uploads/2025/04/git_commands-300x156.png 300w, https://www.devcentrehouse.eu/blogs/wp-content/uploads/2025/04/git_commands-768x399.png 768w" style="object-fit:cover;" width="1000"/></figure>
<div class="wp-block-group is-vertical is-content-justification-stretch is-layout-flex wp-container-core-group-is-layout-6215b345 wp-block-group-is-layout-flex" style="padding-top:0;padding-bottom:0">
<h1 class="wp-block-post-title has-x-large-font-size">Git Guide: 20 Must-Know Commands with Real-World Examples</h1>
<div class="wp-block-template-part">
<div class="wp-block-group has-global-padding is-layout-constrained wp-block-group-is-layout-constrained">
<div class="wp-block-group is-content-justification-left is-layout-flex wp-container-core-group-is-layout-dfe8e91f wp-block-group-is-layout-flex">
<div class="wp-block-post-date"><time datetime="2025-04-28T14:09:04+00:00"><a href="https://www.devcentrehouse.eu/blogs/git-guide-commands-real-world-examples/">Apr 28, 2025</a></time></div>
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
<p><a href="https://en.wikipedia.org/wiki/Git" rel="noreferrer noopener" target="_blank">Git</a> is an essential tool for developers, allowing them to track code changes, collaborate with teams, and maintain project history. Whether you’re a beginner or an experienced developer, understanding the most powerful Git commands can make your workflow much more efficient.<br/><br/>In this guide, we’ll cover <strong>20 powerful Git commands</strong> every developer must know, with real-world examples to demonstrate their use.</p>
<h2 class="wp-block-heading">1. <code>git init</code></h2>
<p>The first command you will use when starting a new Git project is <code>git init</code>. This command initializes a new Git repository in your project directory, allowing Git to track your code.<br/><br/><strong>Example</strong>:</p>
<ul class="wp-block-list">
<li>git init</li>
</ul>
<p>This will create a <code>.git</code> directory where Git stores all its version control information.</p>
<h2 class="wp-block-heading">2. <code>git clone</code></h2>
<p>If you need to create a local copy of a remote repository, use <code>git clone</code>. This command downloads the entire repository, including its history, from a remote location.<br/><br/><strong>Example</strong>:</p>
<ul class="wp-block-list">
<li>git clone https://github.com/user/repository.git</li>
</ul>
<p>This will create a local copy of the repository on your machine.</p>
<h2 class="wp-block-heading">3. <code>git status</code></h2>
<p><code>git status</code> shows the current state of your working directory. It displays files that have been modified, added, or deleted but not yet committed.<br/><br/><strong>Example</strong>:</p>
<ul class="wp-block-list">
<li>git status</li>
</ul>
<p>This will show the status of all files in your repository.</p>
<h2 class="wp-block-heading">4. <code>git add</code></h2>
<p>Before committing changes, you must stage them using <code>git add</code>. This command adds file changes to the staging area.<br/><br/><strong>Example</strong>:</p>
<ul class="wp-block-list">
<li>git add file.txt</li>
</ul>
<p>This will stage <code>file.txt</code> for the next commit.<br/><br/>To add all modified files:</p>
<ul class="wp-block-list">
<li>git add .</li>
</ul>
<h2 class="wp-block-heading">5. <code>git commit</code></h2>
<p>Once you’ve added files to the staging area, use <code>git commit</code> to save those changes to the repository.<br/><br/><strong>Example</strong>:</p>
<ul class="wp-block-list">
<li>git commit -m “Initial commit”</li>
</ul>
<p>This command commits the changes with a message describing the update.</p>
<h2 class="wp-block-heading">6. <code>git log</code></h2>
<p><code>git log</code> is one of the most powerful commands for viewing the history of commits. It shows a detailed log of commits made in the current branch.<br/><br/><strong>Example</strong>:</p>
<ul class="wp-block-list">
<li>git log</li>
</ul>
<p>This will show a list of all commits, along with the commit hash, author, date, and commit message.</p>
<h2 class="wp-block-heading">7. <code>git diff</code></h2>
<p>To see the differences between changes in your working directory and the last commit, use <code>git diff</code>. It shows the exact line-by-line changes made to files.<br/><br/><strong>Example</strong>:</p>
<ul class="wp-block-list">
<li>git diff</li>
</ul>
<p>This will show uncommitted changes in your working directory.</p>
<h2 class="wp-block-heading">8. <code>git branch</code></h2>
<p><code>git branch</code> shows all the branches in your repository and highlights the currently active branch. You can also use it to create new branches.<br/><br/><strong>Example</strong>:</p>
<ul class="wp-block-list">
<li>git branch</li>
</ul>
<p>To create a new branch:</p>
<ul class="wp-block-list">
<li>git branch new-branch</li>
</ul>
<h2 class="wp-block-heading">9. <code>git checkout</code></h2>
<p><code>git checkout</code> is used to switch between branches or to restore files from a previous commit.<br/><br/><strong>Example</strong>:</p>
<ul class="wp-block-list">
<li>git checkout new-branch</li>
</ul>
<p>This switches to the <code>new-branch</code>.<br/><br/>To restore a deleted file:</p>
<ul class="wp-block-list">
<li>git checkout HEAD file.txt</li>
</ul>
<h2 class="wp-block-heading">10. <code>git merge</code></h2>
<p>To merge changes from one branch into another, use <code>git merge</code>. This command combines the changes made in different branches.<br/><br/><strong>Example</strong>:</p>
<ul class="wp-block-list">
<li>git checkout main</li>
<li>git merge new-branch</li>
</ul>
<p>This merges the changes from <code>new-branch</code> into the <code>main</code> branch.</p>
<h2 class="wp-block-heading">11. <code>git pull</code></h2>
<p><code>git pull</code> is used to fetch and merge changes from a remote repository into your current branch. It’s the equivalent of running <code>git fetch</code> followed by <code>git merge</code>.<br/><br/><strong>Example</strong>:</p>
<ul class="wp-block-list">
<li>git pull origin main</li>
</ul>
<p>This pulls the latest changes from the <code>main</code> branch of the remote repository and merges them into your current branch.</p>
<h2 class="wp-block-heading">12. <code>git push</code></h2>
<p>Once you’ve made and committed changes locally, you can use <code>git push</code> to send those changes to a remote repository.<br/><br/><strong>Example</strong>:</p>
<ul class="wp-block-list">
<li>git push origin main</li>
</ul>
<p>This pushes the local <code>main</code> branch to the remote repository.</p>
<h2 class="wp-block-heading">13. <code>git reset</code></h2>
<p>To undo changes in your working directory, <code>git reset</code> is your go-to command. It can be used to unstage changes or even reset your entire repository to a previous state.<br/><br/><strong>Example</strong>:<br/>To unstage a file:</p>
<ul class="wp-block-list">
<li>git reset file.txt</li>
</ul>
<p>To reset the repository to the last commit:</p>
<ul class="wp-block-list">
<li>git reset –hard</li>
</ul>
<h2 class="wp-block-heading">14. <code>git stash</code></h2>
<p>If you’re in the middle of a task but need to switch branches without committing your changes, use <code>git stash</code>. It temporarily stores your uncommitted changes and allows you to come back to them later.<br/><br/><strong>Example</strong>:</p>
<ul class="wp-block-list">
<li>git stash</li>
</ul>
<p>This will stash your changes. To apply them later:</p>
<ul class="wp-block-list">
<li>git stash apply</li>
</ul>
<h2 class="wp-block-heading">15. <code>git fetch</code></h2>
<p><code>git fetch</code> downloads changes from a remote repository but doesn’t merge them into your working directory. It’s useful if you want to see what changes are available before merging.<br/><br/><strong>Example</strong>:</p>
<ul class="wp-block-list">
<li>git fetch origin</li>
</ul>
<p>This fetches all branches from the remote but doesn’t merge them into your local repository.</p>
<h2 class="wp-block-heading">16. <code>git remote</code></h2>
<p><code>git remote</code> shows the URLs of remote repositories linked to your project. You can also use this command to add, remove, or rename remotes.<br/><br/><strong>Example</strong>:</p>
<ul class="wp-block-list">
<li>git remote -v</li>
</ul>
<p>This lists all remotes associated with your project.<br/><br/>To add a new remote:</p>
<ul class="wp-block-list">
<li>git remote add origin https://github.com/user/repository.git</li>
</ul>
<h2 class="wp-block-heading">17. <code>git tag</code></h2>
<p><code>git tag</code> allows you to mark specific points in your repository’s history, usually to indicate releases or versions.<br/><br/><strong>Example</strong>:</p>
<ul class="wp-block-list">
<li>git tag v1.0.0</li>
</ul>
<p>This tags the current commit with <code>v1.0.0</code>.</p>
<h2 class="wp-block-heading">18. <code>git cherry-pick</code></h2>
<p><code>git cherry-pick</code> is used to apply a commit from one branch onto another. This is helpful when you want to bring specific changes from one branch without merging the entire branch.<br/><br/><strong>Example</strong>:</p>
<ul class="wp-block-list">
<li>git cherry-pick &lt;commit-hash&gt;</li>
</ul>
<p>This applies the commit with the specified hash to your current branch.</p>
<h2 class="wp-block-heading">19. <code>git rebase</code></h2>
<p><code>git rebase</code> is a powerful way to rewrite the history of your commits. It is often used to clean up commit history before merging into the main branch.<br/><br/><strong>Example</strong>:</p>
<ul class="wp-block-list">
<li>git rebase main</li>
</ul>
<p>This rebases your current branch on top of the latest <code>main</code> branch.</p>
<h2 class="wp-block-heading">20. <code>git config</code></h2>
<p><code>git config</code> is used to configure Git settings for your repository or globally across your system. You can configure things like your name, email, and editor.<br/><br/><strong>Example</strong>:<br/><br/>To set your name and email:</p>
<ul class="wp-block-list">
<li>git config –global user.name “Your Name”</li>
<li>git config –global user.email “<a class="__cf_email__" data-cfemail="166f796364737b777f7a56736e777b667a733875797b" href="/cdn-cgi/l/email-protection">[email protected]</a>”</li>
</ul>
<h2 class="wp-block-heading">Conclusion</h2>
<figure class="wp-block-image size-large"><img alt="Git" class="wp-image-1521" decoding="async" height="729" sizes="(max-width: 1024px) 100vw, 1024px" src="https://www.devcentrehouse.eu/blogs/wp-content/uploads/2025/04/dch-devops-1024x729.png" srcset="https://www.devcentrehouse.eu/blogs/wp-content/uploads/2025/04/dch-devops-1024x729.png 1024w, https://www.devcentrehouse.eu/blogs/wp-content/uploads/2025/04/dch-devops-300x214.png 300w, https://www.devcentrehouse.eu/blogs/wp-content/uploads/2025/04/dch-devops-768x547.png 768w, https://www.devcentrehouse.eu/blogs/wp-content/uploads/2025/04/dch-devops.png 1147w" width="1024"/></figure>
<p>Mastering Git commands is essential for any developer. With these <strong>20 powerful Git commands</strong>, you’ll be able to work more efficiently, track changes in your projects, and collaborate seamlessly with your team.<br/><br/>Whether you’re just getting started with Git or looking to enhance your skills, these commands will help you build a solid foundation in version control. Start using these commands today and make your Git workflow faster and more efficient!<br/><br/>For further reading on backend development with Git CI/CD, visit <a href="https://www.devcentrehouse.eu/en/services/devops">Dev Centre House Ireland – Devops Services </a>.</p>
<!--— Calendly inline widget begin ---->

<script data-cfasync="false" src="/cdn-cgi/scripts/5c5dd728/cloudflare-static/email-decode.min.js"></script>
<!--— Calendly inline widget end ---->
</div>
<div class="wp-block-group has-global-padding is-layout-constrained wp-block-group-is-layout-constrained" style="margin-top:var(--wp--preset--spacing--40);padding-bottom:var(--wp--preset--spacing--50)">
<div class="taxonomy-post_tag is-style-pill wp-block-post-terms"><a href="https://www.devcentrehouse.eu/blogs/tag/commands/" rel="tag">Commands</a><span class="wp-block-post-terms__separator"> </span><a href="https://www.devcentrehouse.eu/blogs/tag/dev-centre-house-ireland/" rel="tag">Dev Centre House Ireland</a><span class="wp-block-post-terms__separator"> </span><a href="https://www.devcentrehouse.eu/blogs/tag/git/" rel="tag">GIT</a><span class="wp-block-post-terms__separator"> </span><a href="https://www.devcentrehouse.eu/blogs/tag/github/" rel="tag">GitHub</a><span class="wp-block-post-terms__separator"> </span><a href="https://www.devcentrehouse.eu/blogs/tag/guide/" rel="tag">guide</a><span class="wp-block-post-terms__separator"> </span><a href="https://www.devcentrehouse.eu/blogs/tag/real-world-examples/" rel="tag">Real world Examples</a></div>
<div class="wp-block-group has-global-padding is-layout-constrained wp-block-group-is-layout-constrained">
<div aria-hidden="true" class="wp-block-spacer" style="height:var(--wp--preset--spacing--40)">
</div>
<hr class="wp-block-separator has-text-color has-contrast-3-color has-alpha-channel-opacity has-contrast-3-background-color has-background is-style-wide" style="margin-bottom:var(--wp--preset--spacing--40)"/>
<div class="wp-block-comments wp-block-comments-query-loop">
<h2 class="wp-block-heading">Comments</h2>
<div class="comment-respond wp-block-post-comments-form" id="respond" style="padding-top:var(--wp--preset--spacing--20);padding-bottom:var(--wp--preset--spacing--20);">
<h3 class="comment-reply-title" id="reply-title">Leave a Reply <small><a href="/blogs/git-guide-commands-real-world-examples/#respond" id="cancel-comment-reply-link" rel="nofollow" style="display:none;">Cancel reply</a></small></h3><form action="https://www.devcentrehouse.eu/blogs/wp-comments-post.php" class="comment-form" id="commentform" method="post" novalidate=""><p class="comment-notes"><span id="email-notes">Your email address will not be published.</span> <span class="required-field-message">Required fields are marked <span class="required">*</span></span></p><p class="comment-form-comment"><label for="comment">Comment <span class="required">*</span></label> <textarea cols="45" id="comment" maxlength="65525" name="comment" required="" rows="8"></textarea></p><p class="comment-form-author"><label for="author">Name <span class="required">*</span></label> <input autocomplete="name" id="author" maxlength="245" name="author" required="" size="30" type="text" value=""/></p>
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
                </script><script id="wpcaptcha-recaptcha-js" src="https://www.google.com/recaptcha/api.js?onload=wpcaptcha_captcha&amp;render=6LcqUfIqAAAAAGsZpRiaxTHv4zNpIeTivYdNQsZI&amp;ver=1.29"></script><p class="form-submit wp-block-button"><input class="wp-block-button__link wp-element-button" id="submit" name="submit" type="submit" value="Post Comment"/> <input id="comment_post_ID" name="comment_post_ID" type="hidden" value="1520"/>
<input id="comment_parent" name="comment_parent" type="hidden" value="0"/>
</p></form> </div><!-- #respond -->
</div>
<nav aria-label="Posts" class="wp-block-group is-content-justification-space-between is-nowrap is-layout-flex wp-container-core-group-is-layout-c08a3ef2 wp-block-group-is-layout-flex" style="padding-top:var(--wp--preset--spacing--40);padding-bottom:var(--wp--preset--spacing--40)">
<div class="post-navigation-link-previous wp-block-post-navigation-link"><span aria-hidden="true" class="wp-block-post-navigation-link__arrow-previous is-arrow-arrow">←</span><a href="https://www.devcentrehouse.eu/blogs/opensearch-vs-elasticsearch-difference/" rel="prev"><span class="post-navigation-link__label">Previous: </span> <span class="post-navigation-link__title">OpenSearch vs. Elasticsearch: 7 Key Differences You Can’t Ignore</span></a></div>
<div class="post-navigation-link-next wp-block-post-navigation-link"><a href="https://www.devcentrehouse.eu/blogs/ai-inference-backend-solutions/" rel="next"><span class="post-navigation-link__label">Next: </span> <span class="post-navigation-link__title">Real-Time AI Inference: 5 Backend Solutions for Blazing-Fast Predictions</span></a><span aria-hidden="true" class="wp-block-post-navigation-link__arrow-next is-arrow-arrow">→</span></div>
</nav>
</div>
</div>
