---
layout: default
title: Vector Databases Explained 7 Essential Concepts for AI-Powered Search
permalink: /vectordatabasesexplained7essentialconceptsforai-poweredsearch/
---


<div class="wp-block-columns alignwide is-layout-flex wp-container-core-columns-is-layout-8ba3830c wp-block-columns-is-layout-flex" style="margin-top:0;margin-bottom:0;padding-right:0;padding-left:0">
<div class="wp-block-column is-layout-flow wp-block-column-is-layout-flow" style="flex-basis:70%">
<div class="wp-block-group has-global-padding is-layout-constrained wp-block-group-is-layout-constrained"><figure class="alignwide wp-block-post-featured-image" style="padding-bottom:2vh;"><img alt="Vector Database" class="attachment-post-thumbnail size-post-thumbnail wp-post-image" decoding="async" fetchpriority="high" height="1080" sizes="(max-width: 1920px) 100vw, 1920px" src="https://www.devcentrehouse.eu/blogs/wp-content/uploads/2025/04/vector_database.jpg" srcset="https://www.devcentrehouse.eu/blogs/wp-content/uploads/2025/04/vector_database.jpg 1920w, https://www.devcentrehouse.eu/blogs/wp-content/uploads/2025/04/vector_database-300x169.jpg 300w, https://www.devcentrehouse.eu/blogs/wp-content/uploads/2025/04/vector_database-1024x576.jpg 1024w, https://www.devcentrehouse.eu/blogs/wp-content/uploads/2025/04/vector_database-768x432.jpg 768w, https://www.devcentrehouse.eu/blogs/wp-content/uploads/2025/04/vector_database-1536x864.jpg 1536w" style="border-radius:0px;object-fit:cover;" width="1920"/></figure>
<h1 class="alignwide wp-block-post-title has-x-large-font-size">Vector Databases Explained: 7 Essential Concepts for AI-Powered Search</h1>
<div aria-hidden="true" class="wp-block-spacer" style="height:var(--wp--preset--spacing--10)"></div>
</div>
<div class="wp-block-group has-global-padding is-layout-constrained wp-block-group-is-layout-constrained"><div class="entry-content alignwide wp-block-post-content has-global-padding is-layout-constrained wp-container-core-post-content-is-layout-a5dd074b wp-block-post-content-is-layout-constrained">
<p>As <a href="https://www.devcentrehouse.eu/en/services/artificial-intelligence">artificial intelligence</a> (AI) continues to evolve, search technologies must keep pace. Traditional keyword-based search engines struggle to handle complex queries, leading to the rise of <strong><a href="https://en.wikipedia.org/wiki/Vector_database" rel="noopener" target="_blank">vector databases</a></strong>. These databases power AI-driven search systems by leveraging numerical representations of data, known as <strong>embeddings</strong>, to enable more accurate and context-aware search results.</p>
<p><br/>In this guide, we’ll explore seven essential concepts behind vector databases and how they revolutionise AI-powered search.</p>
<h3 class="wp-block-heading"><strong>1. What Are Vector Databases?</strong></h3>
<p>A <strong>vector database</strong> stores data as high-dimensional numerical representations (vectors) rather than text or structured records. These vectors encode semantic meanings, allowing AI to compare and retrieve relevant information based on similarity rather than exact keyword matches.</p>
<h4 class="wp-block-heading"><strong>Why It Matters</strong></h4>
<p>Unlike traditional databases, vector databases enable more intuitive and human-like search experiences by understanding <strong>context, intent, and relationships</strong> between data points.</p>
<h3 class="wp-block-heading"><strong>2. Embeddings: The Foundation of Vector Search</strong></h3>
<p>Embeddings are numerical representations of data, generated using AI models such as <strong>transformers</strong> or <strong>word2vec</strong>. These vectors encapsulate relationships and similarities between different pieces of information.</p>
<h4 class="wp-block-heading"><strong>How It Works</strong></h4>
<ul class="wp-block-list">
<li style="padding-top:var(--wp--preset--spacing--xx-small);padding-bottom:var(--wp--preset--spacing--xx-small)">Text, images, or audio data are transformed into multi-dimensional vectors.</li>
<li style="padding-top:var(--wp--preset--spacing--xx-small);padding-bottom:var(--wp--preset--spacing--xx-small)">Similar items will have vectors positioned closely in the vector space.</li>
<li style="padding-top:var(--wp--preset--spacing--xx-small);padding-bottom:var(--wp--preset--spacing--xx-small)">AI-powered search engines rank results based on their <strong>distance</strong> in this space.</li>
</ul>
<h3 class="wp-block-heading"><strong>3. Similarity Metrics: Measuring Relevance</strong></h3>
<p>Vector databases use <strong>similarity metrics</strong> to compare vectors and determine search results.</p>
<h4 class="wp-block-heading"><strong>Common Metrics</strong></h4>
<ul class="wp-block-list">
<li style="padding-top:var(--wp--preset--spacing--xx-small);padding-bottom:var(--wp--preset--spacing--xx-small)"><strong>Cosine Similarity</strong>: Measures the angle between vectors.</li>
<li style="padding-top:var(--wp--preset--spacing--xx-small);padding-bottom:var(--wp--preset--spacing--xx-small)"><strong>Euclidean Distance</strong>: Calculates the straight-line distance.</li>
<li style="padding-top:var(--wp--preset--spacing--xx-small);padding-bottom:var(--wp--preset--spacing--xx-small)"><strong>Dot Product</strong>: Evaluates vector magnitude and direction.<br/>Choosing the right metric depends on the application. Cosine similarity, for example, is widely used in <strong>natural language processing (NLP)</strong> tasks.</li>
</ul>
<h3 class="wp-block-heading"><strong>4. Indexing Techniques for Fast Retrieval</strong></h3>
<p>Searching through millions of vectors requires efficient <strong>indexing</strong>. Vector databases employ special indexing techniques to speed up searches.</p>
<h4 class="wp-block-heading"><strong>Popular Indexing Methods</strong></h4>
<ul class="wp-block-list">
<li style="padding-top:var(--wp--preset--spacing--xx-small);padding-bottom:var(--wp--preset--spacing--xx-small)"><strong>Hierarchical Navigable Small World (HNSW)</strong>: A graph-based approach that balances speed and accuracy.</li>
<li style="padding-top:var(--wp--preset--spacing--xx-small);padding-bottom:var(--wp--preset--spacing--xx-small)"><strong>Product Quantization (PQ)</strong>: Reduces the size of vectors to optimise memory usage.</li>
<li style="padding-top:var(--wp--preset--spacing--xx-small);padding-bottom:var(--wp--preset--spacing--xx-small)"><strong>Approximate Nearest Neighbors (ANN)</strong>: Finds results efficiently by approximating distances.</li>
</ul>
<h3 class="wp-block-heading"><strong>5. Real-World Applications of Vector Databases</strong></h3>
<p>Vector databases power various AI-driven applications across industries:</p>
<ul class="wp-block-list">
<li style="padding-top:var(--wp--preset--spacing--xx-small);padding-bottom:var(--wp--preset--spacing--xx-small)"><strong>Semantic Search</strong>: Improves search accuracy by understanding user intent rather than just matching keywords.</li>
<li style="padding-top:var(--wp--preset--spacing--xx-small);padding-bottom:var(--wp--preset--spacing--xx-small)"><strong>Recommendation Systems</strong>: Suggests personalised content based on user preferences and behaviour.</li>
<li style="padding-top:var(--wp--preset--spacing--xx-small);padding-bottom:var(--wp--preset--spacing--xx-small)"><strong>Fraud Detection</strong>: Identifies anomalies in financial transactions by comparing vector patterns.</li>
<li style="padding-top:var(--wp--preset--spacing--xx-small);padding-bottom:var(--wp--preset--spacing--xx-small)"><strong>Image &amp; Video Search</strong>: Enables reverse image lookup and facial recognition.</li>
</ul>
<h3 class="wp-block-heading"><strong>6. Popular Vector Databases</strong></h3>
<p>Several databases specialise in handling vector data efficiently:</p>
<ul class="wp-block-list">
<li style="padding-top:var(--wp--preset--spacing--xx-small);padding-bottom:var(--wp--preset--spacing--xx-small)"><strong>FAISS (Facebook AI Similarity Search)</strong>: Open-source library optimised for fast vector retrieval.</li>
<li style="padding-top:var(--wp--preset--spacing--xx-small);padding-bottom:var(--wp--preset--spacing--xx-small)"><strong>Milvus</strong>: Scalable vector database built for high-performance applications.</li>
<li style="padding-top:var(--wp--preset--spacing--xx-small);padding-bottom:var(--wp--preset--spacing--xx-small)"><strong>Pinecone</strong>: Cloud-native solution that provides real-time vector search.</li>
<li style="padding-top:var(--wp--preset--spacing--xx-small);padding-bottom:var(--wp--preset--spacing--xx-small)"><strong>Weaviate</strong>: Combines vector search with knowledge graphs for enhanced AI reasoning.</li>
</ul>
<h3 class="wp-block-heading"><strong>7. Challenges and Future Trends</strong></h3>
<p>While vector databases offer impressive capabilities, they also present challenges:</p>
<ul class="wp-block-list">
<li style="padding-top:var(--wp--preset--spacing--xx-small);padding-bottom:var(--wp--preset--spacing--xx-small)"><strong>Scalability</strong>: Handling billions of vectors requires significant computational power.</li>
<li style="padding-top:var(--wp--preset--spacing--xx-small);padding-bottom:var(--wp--preset--spacing--xx-small)"><strong>Accuracy vs. Speed</strong>: Balancing precision with real-time performance is crucial.</li>
<li style="padding-top:var(--wp--preset--spacing--xx-small);padding-bottom:var(--wp--preset--spacing--xx-small)"><strong>Data Privacy</strong>: Securing vector-based data against potential misuse.</li>
</ul>
<h4 class="wp-block-heading"><strong>Future Trends</strong></h4>
<ul class="wp-block-list">
<li style="padding-top:var(--wp--preset--spacing--xx-small);padding-bottom:var(--wp--preset--spacing--xx-small)">Integration with <strong>multimodal AI</strong> for text, images, and video searches.</li>
<li style="padding-top:var(--wp--preset--spacing--xx-small);padding-bottom:var(--wp--preset--spacing--xx-small)">Enhanced support for <strong>self-hosted and hybrid cloud solutions</strong>.</li>
<li style="padding-top:var(--wp--preset--spacing--xx-small);padding-bottom:var(--wp--preset--spacing--xx-small)">Improvements in <strong>efficient indexing techniques</strong> to handle growing datasets.</li>
</ul>
<h3 class="wp-block-heading"><strong>Conclusion</strong></h3>
<p>Vector databases are transforming AI-powered search by enabling more intelligent, context-aware, and scalable search experiences. As AI continues to advance, these databases will play an increasingly vital role in applications ranging from search engines to recommendation systems. By understanding these seven essential concepts, developers and businesses can leverage vector databases to build smarter and more efficient search solutions.</p>
<h3 class="wp-block-heading"><strong>FAQ</strong></h3>
<p><strong>Question:</strong> What is a vector database?<br/><strong>Answer:</strong> A vector database stores and indexes high-dimensional vector embeddings, numeric representations of data used by AI models for semantic search and similarity matching.</p>
<hr class="wp-block-separator has-alpha-channel-opacity"/>
<p><strong>Question:</strong> Why are vector databases important for AI search?<br/><strong>Answer:</strong> They enable fast, scalable similarity searches by efficiently retrieving nearest neighbors of a query vector essential for AI-powered search, recommendations, and retrieval-augmented generation (RAG).</p>
<hr class="wp-block-separator has-alpha-channel-opacity"/>
<p><strong>Question:</strong> How do vector embeddings work in search pipelines?<br/><strong>Answer:</strong> Embeddings convert text, images, or other data into vectors. These are stored in the vector database and compared to query embeddings using distance metrics like cosine similarity.</p>
<hr class="wp-block-separator has-alpha-channel-opacity"/>
<p><strong>Question:</strong> What types of data can be stored in vector databases?<br/><strong>Answer:</strong> Any data that can be embedded, text, images, audio, or code, making vector databases versatile for multimodal AI applications.</p>
<hr class="wp-block-separator has-alpha-channel-opacity"/>
<p><strong>Question:</strong> How does approximate nearest neighbor (ANN) indexing improve performance?<br/><strong>Answer:</strong> ANN algorithms like HNSW and IVF reduce search latency and memory usage by approximating nearest neighbors, enabling scalable and fast querying.</p>
<hr class="wp-block-separator has-alpha-channel-opacity"/>
<p><strong>Question:</strong> What are common distance metrics used in vector search?<br/><strong>Answer:</strong> Cosine similarity, Euclidean distance, and dot product are frequently used to measure vector closeness and return relevant results.</p>
<hr class="wp-block-separator has-alpha-channel-opacity"/>
<p><strong>Question:</strong> Can vector databases integrate with existing AI models?<br/><strong>Answer:</strong> Absolutely. They work with popular frameworks like OpenAI, Hugging Face, and TensorFlow, allowing pipelines that embed data, index vectors, and perform semantic matching.</p>
<hr class="wp-block-separator has-alpha-channel-opacity"/>
<p><strong>Question:</strong> What challenges come with using vector databases?<br/><strong>Answer:</strong> Key challenges include deciding on embedding strategy, maintaining index updates with dynamic data, and ensuring retrieval accuracy with evolving models.</p>
<hr class="wp-block-separator has-alpha-channel-opacity"/>
<p><strong>Question:</strong> How are vector databases different from traditional databases?<br/><strong>Answer:</strong> Traditional databases rely on exact matching and relational queries, while vector databases focus on semantic similarity, enabling AI-driven search and AI-native applications.</p>
<hr class="wp-block-separator has-alpha-channel-opacity"/>
<p><strong>Question:</strong> How do enterprises benefit from vector search in AI applications?<br/><strong>Answer:</strong> Vector search enables better information retrieval, personalized recommendations, and improved RAG capabilities measurably boosting AI products’ effectiveness.</p>
<hr class="wp-block-separator has-alpha-channel-opacity"/>
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
<li class="wp-social-link wp-social-link-mail wp-block-social-link"><a class="wp-block-social-link-anchor" href="/cdn-cgi/l/email-protection#076f62212436373f3c212436373f3c21243636363c21243731333c6362212436363f3c2124373e3e3c62697321243636333c21243637363c21243637333c6821243636303c21243636323c62296272"><svg aria-hidden="true" focusable="false" height="24" version="1.1" viewbox="0 0 24 24" width="24" xmlns="http://www.w3.org/2000/svg"><path d="M19,5H5c-1.1,0-2,.9-2,2v10c0,1.1.9,2,2,2h14c1.1,0,2-.9,2-2V7c0-1.1-.9-2-2-2zm.5,12c0,.3-.2.5-.5.5H5c-.3,0-.5-.2-.5-.5V9.8l7.5,5.6,7.5-5.6V17zm0-9.1L12,13.6,4.5,7.9V7c0-.3.2-.5.5-.5h14c.3,0,.5.2.5.5v.9z"></path></svg><span class="wp-block-social-link-label screen-reader-text">Mail</span></a></li>
<li class="wp-social-link wp-social-link-instagram wp-block-social-link"><a class="wp-block-social-link-anchor" href="https://www.instagram.com/devcentrehouse/"><svg aria-hidden="true" focusable="false" height="24" version="1.1" viewbox="0 0 24 24" width="24" xmlns="http://www.w3.org/2000/svg"><path d="M12,4.622c2.403,0,2.688,0.009,3.637,0.052c0.877,0.04,1.354,0.187,1.671,0.31c0.42,0.163,0.72,0.358,1.035,0.673 c0.315,0.315,0.51,0.615,0.673,1.035c0.123,0.317,0.27,0.794,0.31,1.671c0.043,0.949,0.052,1.234,0.052,3.637 s-0.009,2.688-0.052,3.637c-0.04,0.877-0.187,1.354-0.31,1.671c-0.163,0.42-0.358,0.72-0.673,1.035 c-0.315,0.315-0.615,0.51-1.035,0.673c-0.317,0.123-0.794,0.27-1.671,0.31c-0.949,0.043-1.233,0.052-3.637,0.052 s-2.688-0.009-3.637-0.052c-0.877-0.04-1.354-0.187-1.671-0.31c-0.42-0.163-0.72-0.358-1.035-0.673 c-0.315-0.315-0.51-0.615-0.673-1.035c-0.123-0.317-0.27-0.794-0.31-1.671C4.631,14.688,4.622,14.403,4.622,12 s0.009-2.688,0.052-3.637c0.04-0.877,0.187-1.354,0.31-1.671c0.163-0.42,0.358-0.72,0.673-1.035 c0.315-0.315,0.615-0.51,1.035-0.673c0.317-0.123,0.794-0.27,1.671-0.31C9.312,4.631,9.597,4.622,12,4.622 M12,3 C9.556,3,9.249,3.01,8.289,3.054C7.331,3.098,6.677,3.25,6.105,3.472C5.513,3.702,5.011,4.01,4.511,4.511 c-0.5,0.5-0.808,1.002-1.038,1.594C3.25,6.677,3.098,7.331,3.054,8.289C3.01,9.249,3,9.556,3,12c0,2.444,0.01,2.751,0.054,3.711 c0.044,0.958,0.196,1.612,0.418,2.185c0.23,0.592,0.538,1.094,1.038,1.594c0.5,0.5,1.002,0.808,1.594,1.038 c0.572,0.222,1.227,0.375,2.185,0.418C9.249,20.99,9.556,21,12,21s2.751-0.01,3.711-0.054c0.958-0.044,1.612-0.196,2.185-0.418 c0.592-0.23,1.094-0.538,1.594-1.038c0.5-0.5,0.808-1.002,1.038-1.594c0.222-0.572,0.375-1.227,0.418-2.185 C20.99,14.751,21,14.444,21,12s-0.01-2.751-0.054-3.711c-0.044-0.958-0.196-1.612-0.418-2.185c-0.23-0.592-0.538-1.094-1.038-1.594 c-0.5-0.5-1.002-0.808-1.594-1.038c-0.572-0.222-1.227-0.375-2.185-0.418C14.751,3.01,14.444,3,12,3L12,3z M12,7.378 c-2.552,0-4.622,2.069-4.622,4.622S9.448,16.622,12,16.622s4.622-2.069,4.622-4.622S14.552,7.378,12,7.378z M12,15 c-1.657,0-3-1.343-3-3s1.343-3,3-3s3,1.343,3,3S13.657,15,12,15z M16.804,6.116c-0.596,0-1.08,0.484-1.08,1.08 s0.484,1.08,1.08,1.08c0.596,0,1.08-0.484,1.08-1.08S17.401,6.116,16.804,6.116z"></path></svg><span class="wp-block-social-link-label screen-reader-text">Instagram</span></a></li></ul>
<hr class="wp-block-separator has-text-color has-contrast-color has-alpha-channel-opacity has-contrast-background-color has-background is-style-wide"/>
<div class="wp-block-group is-vertical is-content-justification-stretch is-layout-flex wp-container-core-group-is-layout-38a18bb4 wp-block-group-is-layout-flex">
<h2 class="wp-block-heading" style="font-size:clamp(1.039rem, 1.039rem + ((1vw - 0.2rem) * 0.935), 1.6rem);">Search</h2>
<form action="https://www.devcentrehouse.eu/blogs/" class="wp-block-search__button-outside wp-block-search__text-button wp-block-search" method="get" role="search"><label class="wp-block-search__label screen-reader-text" for="wp-block-search__input-2">Search</label><div class="wp-block-search__inside-wrapper" style="width: 100%"><input class="wp-block-search__input" id="wp-block-search__input-2" name="s" placeholder="Search..." required="" type="search" value=""/><button aria-label="Search" class="wp-block-search__button wp-element-button" type="submit">Search</button></div></form></div>
<div aria-hidden="true" class="wp-block-spacer" style="height:var(--wp--preset--spacing--10)"></div>
</div>
</aside></div>
</div>
