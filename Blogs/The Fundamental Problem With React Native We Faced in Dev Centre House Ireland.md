
<div class="inside-article">
<header aria-label="Content" class="entry-header">
<h1 class="entry-title" itemprop="headline">The Fundamental Problem With React Native We Faced in Dev Centre House Ireland</h1> 
</header>
<div class="featured-image cv-col-12 post-image">
<img alt="" class="size-full cv-col-12 wp-post-image" decoding="async" fetchpriority="high" height="540" itemprop="image" sizes="(max-width: 960px) 100vw, 960px" src="https://www.devcentrehouse.eu/blogs/wp-content/uploads/2024/07/article-2.png" srcset="https://www.devcentrehouse.eu/blogs/wp-content/uploads/2024/07/article-2.png 960w, https://www.devcentrehouse.eu/blogs/wp-content/uploads/2024/07/article-2-300x169.png 300w, https://www.devcentrehouse.eu/blogs/wp-content/uploads/2024/07/article-2-768x432.png 768w" style="aspect-ratio:0;" width="960"/> </div>
<div class="entry-content" itemprop="text">
<p></p>
<p>React Native is an excellent framework for building cross-platform native mobile apps. However, there is one major issue at its core that is often either not talked about or simply misunderstood.</p>
<div aria-hidden="true" class="wp-block-spacer" style="height:20px"></div>
<h2 class="wp-block-heading">What is the problem?</h2>
<p>Imagine an example where in order to finish a project, we need a specific resource that we can only get from someone who happens to be Japanese.</p>
<p>There is no Google Translate for us to use so. Therefore, the only way we can communicate with this person is to either learn Japanese or bring in someone who can do the communication for us. What you just read above perfectly illustrates an inherent flaw in React Native and the given name for this scenario is the creation of a <em>“Bridge”</em>, also known as <em>“Bridging”</em>.</p>
<p>Any time we need to access a platform API such as, for example, the microphone, camera, Bluetooth, or something as specific as Apple Music on an iPhone app, a bridge has to create.</p>
<p>If the process of creating bridges wasn’t bad enough to hear already, the bigger problem is that these bridges must be written in the platform’s language. Therefore, we’d likely still need to keep some developers nearby in case we have to build a bridge for some specific feature in iOS or Android, which will then finally be used by the React developer.</p>
<div aria-hidden="true" class="wp-block-spacer" style="height:20px"></div>
<h2 class="wp-block-heading">How can this be true, and why are developers not angry?</h2>
<p>The answer to this question is <a href="https://expo.io" rel="noreferrer noopener" target="_blank">expo.io</a>, a tool built by the community to overcome the problems we’ve discussed with React Native.</p>
<p>In a nutshell, Expo comes with a bunch of bridges that developers can use along with other useful features as well, which are excellent.</p>
<div aria-hidden="true" class="wp-block-spacer" style="height:20px"></div>
<h2 class="wp-block-heading">Problem solved then, right?</h2>
<p>Not exactly, Expo remedies the problem by not needing us to spend countless hours building bridges, but in return, it locks us into the Expo environment.</p>
<p>One of the many features we lose by using Expo is the ability to actually create a bridge ourselves if the need arises. This means that even if Expo helps us build 80% of our project if the remaining 20% can’t also be remedied with Expo, then we are screwed with two options:</p>
<ol class="wp-block-list">
<li>Sacrifice 20% of the project.</li>
<li>Sacrifice using Expo, which then means building all the <strong>bridges manually ourselves, requiring iOS and Android developers</strong> on top of the React Native developers.</li>
</ol>
<p>In summary, you’re either in or you’re out, there’s no in-between.</p>
<div aria-hidden="true" class="wp-block-spacer" style="height:20px"></div>
<h2 class="wp-block-heading">That’s pretty bad, is there anything else?</h2>
<p>There’s one more aspect very important to this project, and that is the desktop app for Mac and Windows.</p>
<p>Expo does not support React Native desktop apps, so even if we could use Expo in our iOS and Android app, we’d have to build an entirely separate React Native project to handle the desktop app.</p>
<p>Even more troubling news, since we are using the base React Native solution without Expo, we’ll likely need C# and Swift developers to create the bridges for Windows and Mac.</p>
<div aria-hidden="true" class="wp-block-spacer" style="height:20px"></div>
<h2 class="wp-block-heading">Real-world enterprise problems</h2>
<p>In <a href="https://devcentrehouse.eu/">Dev Centre House</a>, we are developing native IOS &amp; Android apps, in addition to using Nativescript, and also used to React Native. So as a software development company, we use and understand the different routes on hand for building IOS and Android apps. However, it often depends on the problem on hand, which we often get back to Native IOS &amp; Android development.</p>
<p>Enterprises are often requesting to build apps using one unified platform like React Native or Nativescript to save cost, time, and development maintenance going forward. However, it is not always possible for all cases, and in some cases, we are still much better off going the fully native route to our experience working on all three.</p>
<div aria-hidden="true" class="wp-block-spacer" style="height:20px"></div>
<h2 class="wp-block-heading">Conclusion</h2>
<p>We’re fully aware that this document puts the spotlight on React Native in a negative manner. However, it is vital to understand these flaws before resources are invested. Furthermore, everything can be crosschecked and verified using the references provided below, all of which are from official sources only. Above are some of the few issues you might face when needing to use React Native.</p>
<p><strong>For this matter, what are the issues or challenges you are facing in your organization using React Native?</strong></p>
</div> <footer aria-label="Entry meta" class="entry-meta">
</footer>
</div>
