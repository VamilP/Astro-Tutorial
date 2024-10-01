<h3>Day 2: Astro Project Setup & Layouts</h3>

<h4>1. Creating a Layout</h4>

<em>Let’s create a simple layout that we can reuse across multiple pages.</em>

<b>Step 1: Create a Layout File</b>
<p>Inside your src/layouts/ folder, create a new file called MainLayout.astro.</p>

<h6>Add the following content to MainLayout.astro:</h6>

<pre>
    <code>
    ---
// The frontmatter is empty here, but it's<br/>
required to separate logic from the HTML
    ---
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>My Astro Site</title>
  </head>
  <body>
    <header>
      <h1>My Astro Website</h1>
      <nav>
        <ul>
          <li><a href="/">Home</a></li>
          <li><a href="/about">About</a></li>
        </ul>
      </nav>
    </header>

    <main>
      <!-- This is where the page content will go -->
      <slot />
    </main>

    <footer>
      <p>&copy; 2024 My Astro Website</p>
    </footer>
  </body>
</html>
</code>
</pre>


`<slot />` is a placeholder where the content of individual pages will be injected into the layout.

<blockquote>This layout includes a header with a title and navigation links, a footer, and a slot for page-specific content.</blockquote>

<hr/>

<h4>2. Using the Layout in Pages</h4>
<em>Now that we’ve created the layout, let’s use it in the Home and About pages.</em>

<h5>Step 2: Update the index.astro File</h5>

Open the src/pages/index.astro file (this is your homepage).
<h6>Modify it to use the new layout like this:</h6>

<pre>
  <code>
  ---
  import MainLayout from '../layouts/MainLayout.astro';
  ---
&lt;MainLayout&gt;
  &lt;h2&gt;Welcome to the Home Page&lt;/h2&gt; 
  &lt;p&gt;This is the home page of my </br>
  Astro site using a reusable layout!&lt;/p&gt;
&lt;/MainLayout&gt;
</code>
</pre>

1. We import the layout using `import MainLayout from '../layouts/MainLayout.astro';.`

2. The layout wraps the page content using `<MainLayout>...</MainLayout>.`

<hr/>

<h4>Step 3: Update the about.astro File</h4>

<em>Open the src/pages/about.astro file and modify it to also use the layout:</em>

<pre>
  <code>
  ---
  import MainLayout from '../layouts/MainLayout.astro';
  ---
&lt;MainLayout&gt;
  &lt;h2&gt;About Us&lt;/h2&gt;
  &lt;p&gt;This is the about page,<br/>
  now with a reusable layout.&lt;/p&gt;
&lt;/MainLayout&gt;
</code>
</pre>

<hr/>


