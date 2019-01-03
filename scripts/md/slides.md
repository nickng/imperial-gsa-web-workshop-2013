title: Agenda
cass: big

Things we'll cover:

- How to read and write HTML
- Using CSS to style up HTML pages
- Tools and tips that can help you
- Other stuff you are interested in (tell me!)
- Unfortunately this workshop will not make you a top web app designer

---

title: HTML?

- Hyper-Text Markup Language
- A bit like LaTeX
- Gives structure (and style) to plain text
- Browser display HTML files
    - Without browser HTML *source code* is just a text file
    - Commonly used to present data (eg. MATLAB reports)

---

title: Structure of HTML file

<pre class="prettyprint" data-lang="html">
&lt;!DOCTYPE html>
&lt;html>
  &lt;head> ... &lt;/head>
  &lt;body> ... &lt;/body>
&lt;/html>
</pre>

- *DOCTYPE* declares HTML 'version' (this one means HTML 5)
- *head* contains meta information about the page
    - eg. Page title (on window title bar)
    - eg. Style definitions
    - eg. Javascript functions
- *body* is the main document
    - From top to bottom (except when applying styles, more on this later)

---

title: Inside &lt;body>

The basics:

- Structured by (invisible) blocks (or nested blocks)
    - Called 'tags'
    - eg. &lt;div>This is a block&lt;/div>
- Headings with different levels (like sections, subsections,
  subsubsections in latex)
    - eg. &lt;h1>Heading 1&lt;/h1>
- &lt;p>Paragraphs&lt;/p>
- &lt;img src='Images.jpg' />
- Can mark text as &lt;strong&gt;bold&lt;/strong> or &lt;em&gt;italics&lt;/em&gt;

---

title: Inside &lt;body>

<pre class="prettyprint" data-lang="html">
&lt;body>
  &lt;h1>Level 1 heading&lt;/h1>
    &lt;div>
      This is inside a block
      &lt;h2>Level 2 heading&lt;/h2>
      &lt;span>some more text&lt;/span>
      &lt;h3>Level 3 heading&lt;/h3>
      A tag should be &lt;strong>closed after &lt;em>all inner tags&lt;/em> are closed&lt;/strong>
      &lt;div>
        &lt;h6>Does not need to use heading level in sequence&lt;/h6>
      &lt;/div>
      &lt;h4>Level 4 heading &lt;span>You can have a span inside heading too!&lt;/span>&lt;/h4>
      &lt;img src="http://guardianexpressla.com/wp-content/uploads/2012/08/monkey.jpeg" />
    &lt;/div>
  Normal sized text
&lt;/body>
</pre>
<footer class="source">source: <a href="http://www.doc.ic.ac.uk/~cn06/gsa/workshop/blocks.html">http://www.doc.ic.ac.uk/~cn06/gsa/workshop/blocks.html</a></footer>

---

title: More HTML

- Tags with nothing between open and close<br/>Use this form &lt;img src='image.jpg'/&gt;
- Other HTML tags helpful:
    - &lt;address> Put your mailing address here </address>
    - &lt;small> small fonts </small> (use CSS instead)
    - &lt;big> big fonts </big> (use CSS instead)
- Help the browser to understand the meaning of the webpage

---

title: Cascading Style Sheets (CSS)
subtitle: Styling your webpage

- Giving colours or layout to boring HTML pages
- Three ways
    - Inline (in the HTML file)
    - Stylesheet (in the HTML file)
    - External stylesheet
- Inline bad, stylesheet good
    - Mixing styles with content
    - Very easy to get inconsistent style

This is what CSS looks like
<pre class="prettyprint" data-lang="css">
p { font-size: small; }
p.redtext { color: red; }
</pre>

---

title: Cascading Style Sheets (CSS)
subtitle: Styling your webpage

# My Awesome webpage
Normal sized text
<p style="font-size:small">Hi! this is some text</p>
<p style="font-size:small;color:red">And this paragraph is RED</p>

<pre class="prettyprint" data-lang="css">
&lt;style type='text/css'>
p { font-size: tiny; }
p.redtext { color: red; }
&lt;/style>
</pre>
<pre class="prettyprint" data-lang="html">
&lt;body>
  &lt;h1>My Awesome webpage&lt;/h1>
  Normal sized text
  &lt;p>Hi! this is some text&lt;/p>  &lt;p class="redtext">And this paragraph is RED&lt;/p>
&lt;/body>
</pre>

---

title: Cascading Style Sheets (CSS)
subtitle: What else can you do with CSS?

- Lots!
- Adjusting positions of you elements
- Rounded corners 

<pre class="prettyprint" data-lang="css">
p { position: absolute;
    left: 200px;
    top: 50;
}

div { border: 1px solid #000;
      border-radius: 15px;
      -moz-border-radius: 15px;
}
</pre>

---

title: CSS
subtitle: What if you want to reuse styles?

- Use CSS 'class'
- Gives group of CSS styles names, for example

<pre class="prettyprint" data-lang="css">
.small-fonts { font-size: tiny; }
.red-and-big-fonts { color: red; font-size: large; }
</pre>
<pre class="prettyprint" data-lang="html">
&lt;body>
  &lt;h1 class='red-and-big-fonts'>My Awesome webpage&lt;/h1>
  Normal sized text
  &lt;p class='red-and-big-fonts'>Hi! this is some text&lt;/p>  &lt;p class='small-fonts'>small text goes here&lt;/p>
&lt;/body>
</pre>
Note how the two &lt;p> classes have different style

---

title: Tools and tips

- View source (Ctrl+U in browser)
- Web development tools
    - [F12] in Google Chrome
    - [Firefox menu]->[Web development] in Mozilla Firefox
- Use [Twitter Bootstrap](http://twitter.github.com/bootstrap/) framework to style your webpage
    - They use HTML + CSS too
- Appropriate use of images
- Remember, HTML pages are universal
    - Desktop browsers and Mobile phones display the same file
    - Use relative positioning
    - In general, pixel-by-pixel design is not a good idea
- [W3schools](http://www.w3schools.com) http://www.w3schools.com/
