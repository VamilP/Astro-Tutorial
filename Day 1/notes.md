<h4>1. What is Astro?</h4>
Astro is a modern static site generator designed for building fast, optimized websites. It focuses on delivering HTML-first pages and uses JavaScript only when necessary, making it ideal for building highly performant sites.

<hr/>

<h4>Key Features of Astro:</h4>
<ul>
<li>"Islands Architecture": Astro ships no JavaScript by default but allows you to add interactivity (like buttons, modals, etc.) in specific components when needed.</li>

<li>No JavaScript Runtime by Default: Astro builds static HTML for most of your pages, only using JavaScript where it’s necessary.</li>

<li>Component-Based: You can create reusable components, and Astro natively supports HTML, Markdown, and Vanilla JS.</li>

<>Data-Fetching: You can fetch data from APIs or Markdown files and render them into your static site.</>
</ul>

<hr/>

<h4>2. Why Use Vanilla JS with Astro?</h4>
While Astro supports various frontend frameworks like React, Vue, and Svelte, using Vanilla JS keeps things lightweight and simple, especially when you don't need complex state management or component libraries.

<hr/>

Using Vanilla JS in Astro allows you to:

Keep full control over how JavaScript interacts with the DOM.
Build faster and smaller websites by only including the JavaScript you need.

<hr/>

<h4>3. Astro's Island Architecture</h4>
Astro uses an "Island Architecture" where your page is mostly static HTML, and you can add small "islands" of interactivity using Vanilla JS only where needed.

For example:
A blog page can be static (no JavaScript needed).
A contact form or interactive button can be an "island" with Vanilla JS to handle user interaction.