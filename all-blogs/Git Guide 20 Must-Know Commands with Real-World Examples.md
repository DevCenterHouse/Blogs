
<div class="wp-block-columns alignwide is-layout-flex wp-container-core-columns-is-layout-8ba3830c wp-block-columns-is-layout-flex" style="margin-top:0;margin-bottom:0;padding-right:0;padding-left:0">
<div class="wp-block-column is-layout-flow wp-block-column-is-layout-flow" style="flex-basis:70%">
<div class="wp-block-group has-global-padding is-layout-constrained wp-block-group-is-layout-constrained"><figure class="alignwide wp-block-post-featured-image" style="padding-bottom:2vh;"><img alt="Git" class="attachment-post-thumbnail size-post-thumbnail wp-post-image" decoding="async" fetchpriority="high" height="520" sizes="(max-width: 1000px) 100vw, 1000px" src="https://www.devcentrehouse.eu/blogs/wp-content/uploads/2025/04/git_commands.png" srcset="https://www.devcentrehouse.eu/blogs/wp-content/uploads/2025/04/git_commands.png 1000w, https://www.devcentrehouse.eu/blogs/wp-content/uploads/2025/04/git_commands-300x156.png 300w, https://www.devcentrehouse.eu/blogs/wp-content/uploads/2025/04/git_commands-768x399.png 768w" style="border-radius:0px;object-fit:cover;" width="1000"/></figure>
<h1 class="alignwide wp-block-post-title has-x-large-font-size">Git Guide: 20 Must-Know Commands with Real-World Examples</h1>
<div aria-hidden="true" class="wp-block-spacer" style="height:var(--wp--preset--spacing--10)"></div>
</div>
<div class="wp-block-group has-global-padding is-layout-constrained wp-block-group-is-layout-constrained"><div class="entry-content alignwide wp-block-post-content has-global-padding is-layout-constrained wp-container-core-post-content-is-layout-a5dd074b wp-block-post-content-is-layout-constrained">
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
<li>git config –global user.email “<a class="__cf_email__" data-cfemail="51283e2423343c30383d113429303c213d347f323e3c" href="/cdn-cgi/l/email-protection">[email protected]</a>”</li>
</ul>
<h2 class="wp-block-heading">Conclusion</h2>
<figure class="wp-block-image size-large"><img alt="Git" class="wp-image-1521" decoding="async" height="729" sizes="(max-width: 1024px) 100vw, 1024px" src="https://www.devcentrehouse.eu/blogs/wp-content/uploads/2025/04/dch-devops-1024x729.png" srcset="https://www.devcentrehouse.eu/blogs/wp-content/uploads/2025/04/dch-devops-1024x729.png 1024w, https://www.devcentrehouse.eu/blogs/wp-content/uploads/2025/04/dch-devops-300x214.png 300w, https://www.devcentrehouse.eu/blogs/wp-content/uploads/2025/04/dch-devops-768x547.png 768w, https://www.devcentrehouse.eu/blogs/wp-content/uploads/2025/04/dch-devops.png 1147w" width="1024"/></figure>
<p>Mastering Git commands is essential for any developer. With these <strong>20 powerful Git commands</strong>, you’ll be able to work more efficiently, track changes in your projects, and collaborate seamlessly with your team.<br/><br/>Whether you’re just getting started with Git or looking to enhance your skills, these commands will help you build a solid foundation in version control. Start using these commands today and make your Git workflow faster and more efficient!<br/><br/>For further reading on backend development with Git CI/CD, visit <a href="https://www.devcentrehouse.eu/en/services/devops">Dev Centre House Ireland – Devops Services </a>.</p>
<!--— Calendly inline widget begin ---->

<script data-cfasync="false" src="/cdn-cgi/scripts/5c5dd728/cloudflare-static/email-decode.min.js"></script>
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
<li class="wp-social-link wp-social-link-mail wp-block-social-link"><a class="wp-block-social-link-anchor" href="/cdn-cgi/l/email-protection#e68ec0c5d7d6d7ddc0c5d7d6dedd8ac0c5d7d7d7ddc0c5d6d0d2ddc0c5d7d6d6dd8390c0c5d6dfdfddc0c5d7d6d7ddc0c5d7d7d6ddc0c5d7d7d0dd94c0c5d7d6d7dd8e89c0c5d7d7d1dd9583c0c5d6d2d0ddc0c5d7d6d7ddc0c5d7d7d1dd"><svg aria-hidden="true" focusable="false" height="24" version="1.1" viewbox="0 0 24 24" width="24" xmlns="http://www.w3.org/2000/svg"><path d="M19,5H5c-1.1,0-2,.9-2,2v10c0,1.1.9,2,2,2h14c1.1,0,2-.9,2-2V7c0-1.1-.9-2-2-2zm.5,12c0,.3-.2.5-.5.5H5c-.3,0-.5-.2-.5-.5V9.8l7.5,5.6,7.5-5.6V17zm0-9.1L12,13.6,4.5,7.9V7c0-.3.2-.5.5-.5h14c.3,0,.5.2.5.5v.9z"></path></svg><span class="wp-block-social-link-label screen-reader-text">Mail</span></a></li>
<li class="wp-social-link wp-social-link-instagram wp-block-social-link"><a class="wp-block-social-link-anchor" href="https://www.instagram.com/devcentrehouse/"><svg aria-hidden="true" focusable="false" height="24" version="1.1" viewbox="0 0 24 24" width="24" xmlns="http://www.w3.org/2000/svg"><path d="M12,4.622c2.403,0,2.688,0.009,3.637,0.052c0.877,0.04,1.354,0.187,1.671,0.31c0.42,0.163,0.72,0.358,1.035,0.673 c0.315,0.315,0.51,0.615,0.673,1.035c0.123,0.317,0.27,0.794,0.31,1.671c0.043,0.949,0.052,1.234,0.052,3.637 s-0.009,2.688-0.052,3.637c-0.04,0.877-0.187,1.354-0.31,1.671c-0.163,0.42-0.358,0.72-0.673,1.035 c-0.315,0.315-0.615,0.51-1.035,0.673c-0.317,0.123-0.794,0.27-1.671,0.31c-0.949,0.043-1.233,0.052-3.637,0.052 s-2.688-0.009-3.637-0.052c-0.877-0.04-1.354-0.187-1.671-0.31c-0.42-0.163-0.72-0.358-1.035-0.673 c-0.315-0.315-0.51-0.615-0.673-1.035c-0.123-0.317-0.27-0.794-0.31-1.671C4.631,14.688,4.622,14.403,4.622,12 s0.009-2.688,0.052-3.637c0.04-0.877,0.187-1.354,0.31-1.671c0.163-0.42,0.358-0.72,0.673-1.035 c0.315-0.315,0.615-0.51,1.035-0.673c0.317-0.123,0.794-0.27,1.671-0.31C9.312,4.631,9.597,4.622,12,4.622 M12,3 C9.556,3,9.249,3.01,8.289,3.054C7.331,3.098,6.677,3.25,6.105,3.472C5.513,3.702,5.011,4.01,4.511,4.511 c-0.5,0.5-0.808,1.002-1.038,1.594C3.25,6.677,3.098,7.331,3.054,8.289C3.01,9.249,3,9.556,3,12c0,2.444,0.01,2.751,0.054,3.711 c0.044,0.958,0.196,1.612,0.418,2.185c0.23,0.592,0.538,1.094,1.038,1.594c0.5,0.5,1.002,0.808,1.594,1.038 c0.572,0.222,1.227,0.375,2.185,0.418C9.249,20.99,9.556,21,12,21s2.751-0.01,3.711-0.054c0.958-0.044,1.612-0.196,2.185-0.418 c0.592-0.23,1.094-0.538,1.594-1.038c0.5-0.5,0.808-1.002,1.038-1.594c0.222-0.572,0.375-1.227,0.418-2.185 C20.99,14.751,21,14.444,21,12s-0.01-2.751-0.054-3.711c-0.044-0.958-0.196-1.612-0.418-2.185c-0.23-0.592-0.538-1.094-1.038-1.594 c-0.5-0.5-1.002-0.808-1.594-1.038c-0.572-0.222-1.227-0.375-2.185-0.418C14.751,3.01,14.444,3,12,3L12,3z M12,7.378 c-2.552,0-4.622,2.069-4.622,4.622S9.448,16.622,12,16.622s4.622-2.069,4.622-4.622S14.552,7.378,12,7.378z M12,15 c-1.657,0-3-1.343-3-3s1.343-3,3-3s3,1.343,3,3S13.657,15,12,15z M16.804,6.116c-0.596,0-1.08,0.484-1.08,1.08 s0.484,1.08,1.08,1.08c0.596,0,1.08-0.484,1.08-1.08S17.401,6.116,16.804,6.116z"></path></svg><span class="wp-block-social-link-label screen-reader-text">Instagram</span></a></li></ul>
<hr class="wp-block-separator has-text-color has-contrast-color has-alpha-channel-opacity has-contrast-background-color has-background is-style-wide"/>
<div class="wp-block-group is-vertical is-content-justification-stretch is-layout-flex wp-container-core-group-is-layout-38a18bb4 wp-block-group-is-layout-flex">
<h2 class="wp-block-heading" style="font-size:clamp(1.039rem, 1.039rem + ((1vw - 0.2rem) * 0.935), 1.6rem);">Search</h2>
<form action="https://www.devcentrehouse.eu/blogs/" class="wp-block-search__button-outside wp-block-search__text-button wp-block-search" method="get" role="search"><label class="wp-block-search__label screen-reader-text" for="wp-block-search__input-2">Search</label><div class="wp-block-search__inside-wrapper" style="width: 100%"><input class="wp-block-search__input" id="wp-block-search__input-2" name="s" placeholder="Search..." required="" type="search" value=""/><button aria-label="Search" class="wp-block-search__button wp-element-button" type="submit">Search</button></div></form></div>
<div aria-hidden="true" class="wp-block-spacer" style="height:var(--wp--preset--spacing--10)"></div>
</div>
</aside></div>
</div>
