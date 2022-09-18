---
title: "Interesting Sites for Geeks: Pt. 1"
date: 2022-09-18
---
<div class="sitetitle">

<h2>Official Elm Language Playground &#128279;</h2>

URL: <a href="https://elm-lang.org/try" target="_blank">https://elm-lang.org/try</a>

</div>

<div>
<img src="https://raw.githubusercontent.com/sebastiantbach76/cis-235-blog/main/assets/images/epg_header.png" title="MDN Web Docs" style="width:100%;" class="siteheader" alt="A graphic depicting the header of the developer.mozilla.org website.">
</div>

<p><span class="dropcap">E</span><strong>LM</strong> is a novel, type-safe, domain-specific, and reactive functional programming language that compiles to and interoperates with JavaScript and abides by the mantra &ldquo;No runtime exceptions.&rdquo;<sup><a href="https://elm-lang.org/" target="_blank">1</a></sup> At first glance, Elm&rsquo;s syntax may appear fairly alien to programmers more familiar with procedural programming languages like C or objected-oriented programming languages like Java (unless, of course, one is also familiar with Haskell, one of the inspirations for the Elm programming language).
</p>
<pre>
import Html exposing (text)

main =
  text "Hello, Blog!"
</pre>
Compare the program above to the equivalent code in Java:
<pre>
class HelloBlog {
    public static void main(String[] args) {
        System.out.println("Hello, Blog!"); 
    }
}
</pre>
<p>By contrast, Java syntax is clearly more verbose and less legible as plain, spoken (English) language. In Java, at compile time, the Java compiler will translate the code above into a .class executable that can be invoked in a command line terminal and run on the Java Virtual Machine (JVM) in the Java runtime environment. In Elm, at compile time, the Elm compiler produces an HTML file (typically, &ldquo;index.html&rdquo;) by default; with the appropriate flag added to the compile command&mdash;e.g., &ldquo;<code>elm make src/Main.elm --output=main.js</code>&rdquo;&mdash;Elm produces clean, well-formed JavaScript that will not throw exceptions at runtime. This example illustrates Elm&rsquo;s domain specificity (as opposed to general purpose) as a programming pathway toward more stable web applications. It accomplishes this goal via an incredibly robust and programmer-friendly compiler that outputs extremely detailed and intuitive error messages at compile time. When I first began coding in Elm, I chuckled to myself when I received my first verbose, spot-on Elm compiler error that was nothing like the terse, sometimes inaccurate feedback I have received from the JavaScript interpreter at runtime. Here is a sample compiler error message:</p>
<pre>
-- TYPE MISMATCH ---------------------------- Main.elm

The 1st argument to &#96;drop` is not what I expect:

8|   List.drop (String.toInt userInput) [1,2,3,4,5,6]
^^^^^^^^^^^^^^^^^^^^^^
This &#96;toInt` call produces:

    Maybe Int

But &#96;drop` needs the 1st argument to be:

    Int

Hint: Use Maybe.withDefault to handle possible errors.
</pre>
<p>At this point, you may be thinking to yourself, &ldquo;Hold it right there, buddy! I thought this was supposed to be a blog that reviews other websites and not an infomercial for Elm.&rdquo; Thanks for your patience with my Elm preamble. Allow me to turn my attention to the website in question right now.</p>
<p>For web developers curious about Elm, the creator of the language, Evan Czaplicki, and the Elm Software Foundation maintain an official Elm Playground (https://https://elm-lang.org/try), an online editor coupled with a preview window of the compiled code product/s. Visitors to the site may experiment with Elm code in the left panel and see the compiled results in the right panel (similar to <a href="https://codepen.io/" target="_blank">codepen.io</a> or <a href="https://jsfiddle.net/" target="_blank">jsfiddle.net</a>) without installing a single piece of Elm code on their respective systems. Upon navigating to the site, visitors receive the option of working from boilerplate code such as the obligatory &ldquo;Hello, World!&rdquo; program (nearly identical to the variant used above) or an application that represents and draws playing cards from a virtual deck (depicted in the page header above). Alternatively, the user may simply begin writing Elm code in the left panel and click the &ldquo;Rebuild&rdquo; button at the bottom of the left panel to replace the boilerplate options listed in the right panel with the compiled HTML and JavaScript. The Elm Playground also provides a helpful link to the <a href="https://guide.elm-lang.org/">official Elm Guide</a> so that programmers may refer to it as they explore the Elm Playground. For ease of use, the Elm Playground editor also provides buttons for light and dark modes and an Elm package manager (so that your code in the left panel can import the necessary code modules without throwing compiler errors).</p>
<p>To begin with, one of the most interesting things about the Elm Playground site is that its functionality is available to the open-source coding public as an Elm package: <a href="https://package.elm-lang.org/packages/evancz/elm-playground/1.0.3">elm-playground</a> (v. 1.0.3). Consequently, beginner Elm programmers could use this code package to host <em>their own</em> Elm playgrounds, which is often untrue of other online code editing sites. Unlike some other online code editors, the Elm Playground does not suffer from functional limitations: given that Elm is a domain specific programming language and that its domain is web development, anything one can do in Elm offline can be accomplished in the Elm Playground. By contrast, some other online code editors balk at, e.g., blocks that solicit user input because they lack the infrastructure to translate the Ruby syntax <code>userInput = gets.chomp</code> into a web-serviceable input prompt (in other words, those sites are unwilling to generate the front-end GUI to accompany one&rsquo;s back-end code&mdash;not an unreasonable position to hold, by the way). Of course, Elm&rsquo;s raison d&rsquo;être is to compile to a product that is browser-friendly and ready to render, hence the unbridled potential of the Elm Playground. After test driving Elm code on the Elm Playground, one can copy and paste the working code into a text editor or IDE (<a href="https://atom.io/">Atom</a>, <a href="https://code.visualstudio.com/">Virtual Studio Code</a> and <a href="http://lighttable.com/">LightTable</a> provide support for Elm code through highlighting and linting plugins; support for Elm in JetBrains IDE plugins is fairly limited as of this writing and may be incompatible with the current versions of those IDEs) for later editing or compiling. I will add that, because all of this functionality is available on a website, one could try out Elm coding on either a desktop or mobile browser.</p>
<p>Speaking of mobile browsers, let&rsquo;s see how WebSpeed Insights scores the Elm Playground:
</p>
<h2>WebSpeed Insights Analysis:</h2>
<h3>Test Conditions:</h3>
<div class="conditions">
<strong>Device:</strong> Samsung Galaxy A13 5G<br/>
<strong>OS:</strong> Android 12<br/>
<strong>Cellular Network:</strong> Boost Mobile 5G
</div>

<figure>
<img src="https://raw.githubusercontent.com/sebastiantbach76/cis-235-blog/main/assets/images/tep-wsi-desktop.png" title="WebSpeed Insights' Analysis of elm-lang.org/try (Desktop)" style="width:100%;" alt="A graphic depicting WebSpeed Insight's Analysis of elm-lang.org/try on Desktop Browsers: Accessibilty 87, Best Practices 100, Performance 100">
<figcaption>WebSpeed Insights&rsquo; Analysis of elm-lang.org/try on Desktop Browsers</figcaption>
</figure>
<figure>
<img src="https://raw.githubusercontent.com/sebastiantbach76/cis-235-blog/main/assets/images/tep-wsi-mobile.png" title="WebSpeed Insights' Analysis of elm-lang.org/try (Mobile)" style="width:100%;" alt="A graphic depicting WebSpeed Insight's Analysis of elm-lang.org/try on Mobile Browsers: Accessibility 95, Best Practices 100, Performance 89">
<figcaption>WebSpeed Insights&rsquo; Analysis of elm-lang.org/try on Mobile Browsers</figcaption>
</figure>

<p>Most of these scores seem fairly excellent, so let&rsquo;s examine areas where the desktop browsing experience took a hit on accessibility and where the mobile browsing experience underperformed. According to WebSpeed Insights, three rubrics account for the drop in the site&rsquo;s accessibility:</p>
<ol>
  <li>'&#60;frame>' or '&#60;iframe>' elements do not have a title</li>
  <li>Form elements do not have associated labels</li>
  <li>Links do not have a discernable name</li>
</ol>
<p>All of these oversights will directly impact assistive technologies and, in turn, a desktop user with, e.g., low vision&rsquo;s ability to make use of the Elm Playground and its minimalist layout. While an accessibility score of 89 does not seem disastrous, on a relatively bare-bones site like the Elm Playground, these omissions could prove costly.</p>
<p>In terms of performance, the mobile browsing experience does not meet the expectations for the following rubrics:</p>
<ol>
  <li>Ensures text remains visible during webfont load</li>
  <li>Reduces unused JavaScript</li>
  <li>First Contentful Paint (3G)</li>
</ol>
<p>Items 1 and 3 could be directly related, for a slow-loading webfont with no alternate could delay the first contentful paint <em>AND</em> make the site illegible until 5,190 ms have elapsed. Item 2 might also be contributing to the delay in the first contentful paint, for it refers to a JavaScript file, &ldquo;editor-codemirror.js,&rdquo; whose code could be pruned to reduce the file size from 79 KB to 50 KB. I will also note that a quick glance at the page source reveals that the <code>&#60;script></code> tag that loads the external JavaScript file carries neither the <code>async</code> nor the <code>defer</code> attribute, either of which could help improve page loading times.
</p>
<h2>lambdatest.com Results (a sample)</h2>

<!-- Images used to open the lightbox -->

<div class="row">
<h3>Google Chrome</h3>

<figure>
  <div class="column">
    <img src="https://raw.githubusercontent.com/sebastiantbach76/cis-235-blog/main/assets/images/tep-galaxy-note-9-360x740.png" onclick="openModal();currentSlide(1)" class="hover-shadow" width=90px title="elm-lang.org/try on the Samsung Galaxy Note 9">
    <figcaption>Samsung Galaxy Note 9</figcaption>
  </div>
</figure>
<figure>
  <div class="column">
    <img src="https://raw.githubusercontent.com/sebastiantbach76/cis-235-blog/main/assets/images/tep-google-pixel-3-412x695.png" onclick="openModal();currentSlide(2)" class="hover-shadow" title="elm-lang.org/try on the Google Pixel 3">
    <figcaption>Google Pixel 3</figcaption>
  </div>
</figure>
<figure>  
  <div class="column">
    <img src="https://raw.githubusercontent.com/sebastiantbach76/cis-235-blog/main/assets/images/tep-iphone-8-plus-414x736.png" onclick="openModal();currentSlide(3)" class="hover-shadow" title="elm-lang.org/try on the Apple iPhone 8 Plus">
    <figcaption>Apple iPhone 8 Plus</figcaption>
  </div>
</figure>
<figure>
  <div class="column">
    <img src="https://raw.githubusercontent.com/sebastiantbach76/cis-235-blog/main/assets/images/tep-galaxy-tab-s4-10-5-610x808.png" onclick="openModal();currentSlide(4)" class="hover-shadow" title="elm-lang.org/try on the Samsung Galaxy Tab S4">
    <figcaption>Samsung Galaxy Tab S4</figcaption>
  </div>
</figure> 

<figure>
  <div class="column">
    <img src="https://raw.githubusercontent.com/sebastiantbach76/cis-235-blog/main/assets/images/tep-ipad-(6th-generation)-768x1024.png" onclick="openModal();currentSlide(5)" class="hover-shadow" title="elm-lang.org/try on the Apple iPad 6th Generation">
    <figcaption>Apple iPad 6th Generation</figcaption>
  </div>
</figure>

</div>

<br />

<div class="row">
<div><h3>Mozilla Firefox</h3></div>
<figure>
  <div class="column">
    <img src="https://raw.githubusercontent.com/sebastiantbach76/cis-235-blog/main/assets/images/tep-galaxy-note-9-firefox-360x740.png" onclick="openModal();currentSlide(6)" class="hover-shadow" width=90px title="elm-lang.org/try on the Samsung Galaxy Note 9">
    <figcaption>Samsung Galaxy Note 9</figcaption>
  </div>
</figure>
<figure>
  <div class="column">
    <img src="https://raw.githubusercontent.com/sebastiantbach76/cis-235-blog/main/assets/images/tep-google-pixel-3-firefox-412x695.png" onclick="openModal();currentSlide(7)" class="hover-shadow" title="elm-lang.org/try on the Google Pixel 3">
    <figcaption>Google Pixel 3</figcaption>
  </div>
</figure>
<figure>  
  <div class="column">
    <img src="https://raw.githubusercontent.com/sebastiantbach76/cis-235-blog/main/assets/images/tep-iphone-8-plus-firefox-414x736.png" onclick="openModal();currentSlide(8)" class="hover-shadow" title="elm-lang.org/try on the Apple iPhone 8 Plus">
    <figcaption>Apple iPhone 8 Plus</figcaption>
  </div>
</figure>
<figure>
  <div class="column">
    <img src="https://raw.githubusercontent.com/sebastiantbach76/cis-235-blog/main/assets/images/tep-galaxy-tab-s4-10-5-firefox-610x808.png" onclick="openModal();currentSlide(9)" class="hover-shadow" title="elm-lang.org/try on the Samsung Galaxy Tab S4">
    <figcaption>Samsung Galaxy Tab S4</figcaption>
  </div>
</figure> 

<figure>
  <div class="column">
    <img src="https://raw.githubusercontent.com/sebastiantbach76/cis-235-blog/main/assets/images/tep-ipad-(6th-generation)-firefox-768x1024.png" onclick="openModal();currentSlide(10)" class="hover-shadow" title="elm-lang.org/try on the Apple iPad 6th Generation">
    <figcaption>Apple iPad 6th Generation</figcaption>
  </div>
</figure>
</div>

<div>
<!-- The Modal/Lightbox -->
<div id="myModal" class="modal">
  <span class="close cursor" onclick="closeModal()">&times;</span>
  <div class="modal-content">

<div class="mySlides">
  <div class="numbertext">1 / 5</div>
  <img src="https://raw.githubusercontent.com/sebastiantbach76/cis-235-blog/main/assets/images/tep-galaxy-note-9-360x740.png" style="width:100%">
</div>

<div class="mySlides">
  <div class="numbertext">2 / 5</div>
  <img src="https://raw.githubusercontent.com/sebastiantbach76/cis-235-blog/main/assets/images/tep-google-pixel-3-412x695.png" style="width:100%">
</div>

<div class="mySlides">
  <div class="numbertext">3 / 5</div>
  <img src="https://raw.githubusercontent.com/sebastiantbach76/cis-235-blog/main/assets/images/tep-iphone-8-plus-414x736.png" style="width:100%">
</div>

<div class="mySlides">
  <div class="numbertext">4 / 5</div>
  <img src="https://raw.githubusercontent.com/sebastiantbach76/cis-235-blog/main/assets/images/tep-galaxy-tab-s4-10-5-610x808.png" style="width:100%">
</div>

<div class="mySlides">
  <div class="numbertext">5 / 5</div>
  <img src="https://raw.githubusercontent.com/sebastiantbach76/cis-235-blog/main/assets/images/tep-ipad-(6th-generation)-768x1024.png" style="width:100%">
</div>

<div class="mySlides">
  <div class="numbertext">6 / 10</div>
  <img src="https://raw.githubusercontent.com/sebastiantbach76/cis-235-blog/main/assets/images/tep-galaxy-note-9-firefox-360x740.png" style="width:100%">
</div>

<div class="mySlides">
  <div class="numbertext">7 / 10</div>
  <img src="https://raw.githubusercontent.com/sebastiantbach76/cis-235-blog/main/assets/images/tep-google-pixel-3-firefox-412x695.png" style="width:100%">
</div>

<div class="mySlides">
  <div class="numbertext">8 / 10</div>
  <img src="https://raw.githubusercontent.com/sebastiantbach76/cis-235-blog/main/assets/images/tep-iphone-8-plus-firefox-414x736.png" style="width:100%">
</div>

<div class="mySlides">
  <div class="numbertext">9 / 10</div>
  <img src="https://raw.githubusercontent.com/sebastiantbach76/cis-235-blog/main/assets/images/tep-galaxy-tab-s4-10-5-firefox-610x808.png" style="width:100%">
</div>

<div class="mySlides">
  <div class="numbertext">10 / 10</div>
  <img src="https://raw.githubusercontent.com/sebastiantbach76/cis-235-blog/main/assets/images/tep-ipad-(6th-generation)-firefox-768x1024.png" style="width:100%">
</div>

<!-- Next/previous controls -->
<a class="prev" onclick="plusSlides(-1)">&#10094;</a>
<a class="next" onclick="plusSlides(1)">&#10095;</a>

<!-- Caption text -->
<div class="caption-container">
  <p id="caption"></p>
</div>



<!-- Thumbnail image controls -->
<div class="column">
  <img class="demo" src="https://raw.githubusercontent.com/sebastiantbach76/cis-235-blog/main/assets/images/tep-galaxy-note-9-360x740.png" onclick="currentSlide(1)" alt="Samsung Galaxy Note 9 (Google Chrome)">
</div>

<div class="column">
  <img class="demo" src="https://raw.githubusercontent.com/sebastiantbach76/cis-235-blog/main/assets/images/tep-google-pixel-3-412x695.png" onclick="currentSlide(2)" alt="Google Pixel 3 (Google Chrome)">
</div>

<div class="column">
  <img class="demo" src="https://raw.githubusercontent.com/sebastiantbach76/cis-235-blog/main/assets/images/tep-iphone-8-plus-414x736.png" onclick="currentSlide(3)" alt="Apple iPhone 8 Plus (Google Chrome)">
</div>

<div class="column">
  <img class="demo" src="https://raw.githubusercontent.com/sebastiantbach76/cis-235-blog/main/assets/images/tep-galaxy-tab-s4-10-5-610x808.png" onclick="currentSlide(4)" alt="Samsung Galaxy Tab S4 (Google Chrome)">
</div>

<div class="column">
  <img class="demo" src="https://raw.githubusercontent.com/sebastiantbach76/cis-235-blog/main/assets/images/tep-ipad-(6th-generation)-768x1024.png" onclick="currentSlide(5)" alt="Apple iPad 6th Generation (Google Chrome)">
</div>

<div class="column">
  <img class="demo" src="https://raw.githubusercontent.com/sebastiantbach76/cis-235-blog/main/assets/images/tep-galaxy-note-9-firefox-360x740.png" onclick="currentSlide(6)" alt="Samsung Galaxy Note 9 (Mozilla Firefox)">
</div>

<div class="column">
  <img class="demo" src="https://raw.githubusercontent.com/sebastiantbach76/cis-235-blog/main/assets/images/tep-google-pixel-3-firefox-412x695.png" onclick="currentSlide(7)" alt="Google Pixel 3 (Mozilla Firefox)">
</div>

<div class="column">
  <img class="demo" src="https://raw.githubusercontent.com/sebastiantbach76/cis-235-blog/main/assets/images/tep-iphone-8-plus-firefox-414x736.png" onclick="currentSlide(8)" alt="Apple iPhone 8 Plus (Mozilla Firefox)">
</div>

<div class="column">
  <img class="demo" src="https://raw.githubusercontent.com/sebastiantbach76/cis-235-blog/main/assets/images/tep-galaxy-tab-s4-10-5-firefox-610x808.png" onclick="currentSlide(9)" alt="Samsung Galaxy Tab S4 (Mozilla Firefox)">
</div>

<div class="column">
  <img class="demo" src="https://raw.githubusercontent.com/sebastiantbach76/cis-235-blog/main/assets/images/tep-ipad-(6th-generation)-firefox-768x1024.png" onclick="currentSlide(10)" alt="Apple iPad 6th Generation (Mozilla Firefox)">
</div>

</div>

</div>

<div>

<br/>

<h2>The Bottom Line:</h2>

<p>As the test results from lambdatest.com show, the Elm Playground probably is not the easiest site to use on a small mobile device such as a cellular phone. Tablets, on the other hand, offer greater screen width to better accommodate the two vertical panels displayed in the playground. To improve the mobile browsing experience, I would recommend to the site administrators that they offer users the option of reorienting the two panels so that the screen splits horizontally: the output panel could relocate to the top of the screen while the code editor panel could move to the bottom of the screen. Realizing this panel shift would allow users to see each horizontal line of code better and prevent the output panel from obscuring the ends of code lines. Aside from this limitation of the site, I would highly recommend it to anyone interested in exploring additional programming languages for web development. Elm provides a powerful alternative to the typical ways developers work with HTML, CSS, and JavaScript, and the Elm Playground allows curious users to discover the capabilities of the language without making any significant changes to their systems locally.</p>
</div>

</div>




<style>
body {
    background: peachpuff;
    color: black;
    text-align: justify;
    text-justify: inter-word;
    font-family: Times;
    font-weight: 400;
    line-height: 22px;
}

figcaption {
    font-weight: 800;
    text-align: center;
}

p {
    background: peachpuff;
    color: black;
    text-align: justify;
    text-justify: inter-word;
    font-family: Times;
    font-size: 16px;
    font-weight: 400;
    line-height: 20px;
}

a {
    color: darkblue;
}

h1 {
    color: darkblue;
    font-weight: 800;
    font-family: Times;
    font-size: 45px;
}

h2 {
    color: black;
    font-family: Georgia;
    font-size: 20px;
}

img {
    width: 500px;
    display: inline-block;
}

div {
    background: peachpuff;
    color: black;
}

pre {
    background: black;
    color: white;
    padding: 10px 0px 10px 15px;
    border: 5px solid #f05023;
}
    
code {
    background: black;
    color: white;
}
 
.language-html .highlighter-rouge .highlight {
    background: black;
    color: white;
}
.highlight {
    background: black;
    color: white;
}

.post-meta {
    color: black;
}

.site-header {
    border-top: 5px solid #424242;
    border-bottom: 2px solid #f05023;
    min-height: 55.95px;
    position: relative;
}

.site-footer {
    border-top: 2px solid #f05023;
    padding: 30px 0px 30px 0px;
}

.siteheader {
    border-radius: 0 0 25px 25px;
    border-left: solid 2px;
    border-right: solid 2px;
    border-bottom: solid 2px;
    min-width: 50%;
    max-width: 99.5%;
}

.sitetitle {
    background: #ffffff;
    padding: 10px 10px 5px 10px;
    border-radius: 25px 25px 0 0;
    font-weight: 800;
    border-left: solid 2px;
    border-right: solid 2px;
    border-top: solid 2px;
    min-width: 50%;
    max-width: 100%;
}

.sitetitle .url {
    padding-left: 15px;
    background: #ffffff;
    font-weight: 800;
}

.section-split {
    font-size: 44px;
    color: purple;
    font-weight: 800;
    margin: 5px 0 30px 0;
    text-align: center;
}

.dropcap {
    font-size: 64px;
    line-height: 1;
    float: left;
    font-weight: 800;
    margin-right: 3px;
    margin-top: -4px;
}

.wsi {
    min-width: 50%;
    max-width: 100%;
}

.row > .column {
  padding: 0 8px 8px 8px;
}


.row:after {
  content: "";
  display: table;
  clear: both;
}

/* Create four equal columns that floats next to eachother */
.column {
  float: left;
  width: 15%;
  padding: 0 15px 0px 15px;
}

/* The Modal (background) */
.modal {
  display: none;
  position: fixed;
  z-index: 1;
  padding-top: 100px;
  left: 0;
  top: 0;
  width: 100%;
  height: 100%;
  overflow: auto;
  background-color: black;
}

/* Modal Content */
.modal-content {
  position: relative;
  background-color: #fefefe;
  margin: auto;
  padding: 0;
  width: 90%;
  max-width: 1200px;
}

/* The Close Button */
.close {
  color: white;
  position: absolute;
  top: 10px;
  right: 25px;
  font-size: 35px;
  font-weight: bold;
}

.close:hover,
.close:focus {
  color: #999;
  text-decoration: none;
  cursor: pointer;
}

/* Hide the slides by default */
.mySlides {
  display: none;
}

/* Next & previous buttons */
.prev,
.next {
  cursor: pointer;
  position: absolute;
  top: 50%;
  width: auto;
  padding: 16px;
  margin-top: -50px;
  color: white;
  font-weight: bold;
  font-size: 20px;
  transition: 0.6s ease;
  border-radius: 0 3px 3px 0;
  user-select: none;
  -webkit-user-select: none;
}

/* Position the "next button" to the right */
.next {
  right: 0;
  border-radius: 3px 0 0 3px;
}

/* On hover, add a black background color with a little bit see-through */
.prev:hover,
.next:hover {
  background-color: rgba(0, 0, 0, 0.8);
}

/* Number text (1/3 etc) */
.numbertext {
  color: #f2f2f2;
  font-size: 12px;
  padding: 8px 12px;
  position: absolute;
  top: 0;
}

/* Caption text */
.caption-container {
  text-align: center;
  background-color: white;
  padding: 2px 16px;
  color: black;
}

img.demo {
  opacity: 0.6;
}

.active,
.demo:hover {
  opacity: 1;
}

img.hover-shadow {
  transition: 0.3s;
}

.hover-shadow:hover {
  box-shadow: 0 4px 8px 0 rgba(0, 0, 0, 0.2), 0 6px 20px 0 rgba(0, 0, 0, 0.19);
}

figcaption {
    line-height: 1.25em;
}

.conditions {
    padding-left: 15px;
}

ol li {
  color: black;
}

</style>

<script>
// Open the Modal
function openModal() {
  document.getElementById("myModal").style.display = "block";
}

// Close the Modal
function closeModal() {
  document.getElementById("myModal").style.display = "none";
}

var slideIndex = 1;
showSlides(slideIndex);

// Next/previous controls
function plusSlides(n) {
  showSlides(slideIndex += n);
}

// Thumbnail image controls
function currentSlide(n) {
  showSlides(slideIndex = n);
}

function showSlides(n) {
  var i;
  var slides = document.getElementsByClassName("mySlides");
  var dots = document.getElementsByClassName("demo");
  var captionText = document.getElementById("caption");
  if (n > slides.length) {slideIndex = 1}
  if (n < 1) {slideIndex = slides.length}
  for (i = 0; i < slides.length; i++) {
    slides[i].style.display = "none";
  }
  for (i = 0; i < dots.length; i++) {
    dots[i].className = dots[i].className.replace(" active", "");
  }
  slides[slideIndex-1].style.display = "block";
  dots[slideIndex-1].className += " active";
  captionText.innerHTML = dots[slideIndex-1].alt;
}
</script>
