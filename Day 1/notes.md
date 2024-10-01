<h4>1. What is Astro?</h4>
Astro is a modern static site generator designed for building fast, optimized websites. It focuses on delivering HTML-first pages and uses JavaScript only when necessary, making it ideal for building highly performant sites.

<hr/>

<h4>Key Features of Astro:</h4>
<ul>
<li>"Islands Architecture": Astro ships no JavaScript by default but allows you to add interactivity (like buttons, modals, etc.) in specific components when needed.</li>

<li>No JavaScript Runtime by Default: Astro builds static HTML for most of your pages, only using JavaScript where it’s necessary.</li>

<li>Component-Based: You can create reusable components, and Astro natively supports HTML, Markdown, and Vanilla JS.</li>

<li>Data-Fetching: You can fetch data from APIs or Markdown files and render them into your static site.</li>
</ul>

<hr/>

<h4>2. Why Use Vanilla JS with Astro?</h4>
While Astro supports various frontend frameworks like React, Vue, and Svelte, using Vanilla JS keeps things lightweight and simple, especially when you don't need complex state management or component libraries.

<hr/>

<h4>Using Vanilla JS in Astro allows you to:</h4>

Keep full control over how JavaScript interacts with the DOM.
Build faster and smaller websites by only including the JavaScript you need.

<hr/>

<h4>3. Astro's Island Architecture</h4>
Astro uses an "Island Architecture" where your page is mostly static HTML, and you can add small "islands" of interactivity using Vanilla JS only where needed.

<b>For example:</b>
A blog page can be static (no JavaScript needed).
A contact form or interactive button can be an "island" with Vanilla JS to handle user interaction.

<hr/>

<h4>Explore the Project Structure</h4>

<b>With the sample files included, your project will have some prebuilt directories and files. Here’s a breakdown of the important ones:</b>

<ul>
<li>src/pages/: This is where your site’s individual pages are stored.</li>
    <ul>
        <li>index.astro: The homepage of your site.</li>
    </ul>
<li>src/layouts/: This folder might have a layout file that wraps around your pages.</li>

<li>public/: This is where you put static assets like images, fonts, etc.</li>

</ul>

<hr/>

<h4>Step 1: Create Your First Page</h4>

Now, let’s add a new page to see how Astro works. Follow these steps:

In the src/pages/ folder, create a new file called about.astro.

<pre><code>
---// This is the frontmatter section <br/>
for Astro components---

&lt;h1&gt;About Page&lt;/h1&gt;
&lt;p&gt;Welcome to the about page, built with <br/>
 Astro and Vanilla JS!&lt;/p&gt;</code>
</pre>

<hr/>


<h4>Frontmatter Section</h4>
<h6>In Astro, the frontmatter section is a block of code written between triple dashes (---). </h6>

<h6>It is used at the top of .astro files (and also Markdown files) to define data, import components, or write JavaScript logic that is necessary for the page or component.</h6>

<blockquote>Think of the frontmatter as a way to define variables or logic that runs before rendering the HTML of the page.</blockquote>

<h5>Here’s what the frontmatter section can be used for:</h5>

<ul>
<li>Declaring Variables: You can define variables or data that will be used in the HTML part of your page.</li>

<li>Importing Components: You can import and use other components in your page, like layout files or other reusable components.</li>

<li>Running JavaScript Logic: You can write basic JavaScript logic or even fetch data from an API.</li>

</ul>

<h5>Example Breakdown:</h5>

<pre>
<code>---
    const title = 'About Page';
    // This is the frontmatter section where you can declare 
    <br/>variables, import components, or run JavaScript logic.
---

&lt;h1&gt;{title}&lt;/h1&gt;
&lt;p&gt;Welcome to the about page, built with Astro <br/>
and Vanilla JS!&lt;/p&gt;
</code>
</pre>

<hr/>

<h4>When Do You Use the Frontmatter?</h4>

<ul>
    <li>Whenever you need to use data (variables, functions) or import components in a page or component.</li>
    <li>If your page is completely static (like plain HTML), you might not need frontmatter at all.</li>
</ul>

<h5>Empty Frontmatter</h5>

<em>If you don’t need any variables or logic, you can leave the frontmatter empty:</em>

<pre>
    <code>
    ---
    ---
    </code>
</pre>

<blockquote>In the above case, it’s just a placeholder, and you can focus on the HTML below.</blockquote>

<hr/>

