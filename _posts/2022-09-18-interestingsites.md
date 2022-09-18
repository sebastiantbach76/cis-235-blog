---
title: "Interesting Sites for Geeks: Pt. 1"
date: 2022-09-18
---
<div class="sitetitle">

<h2>Official Elm Language Playground &#128279;</h2>

URL: <a href="https://developer.mozilla.org/en-US/" target="_blank">https://developer.mozilla.org/en-US/</a>

</div>

<div>
<img src="https://raw.githubusercontent.com/sebastiantbach76/cis-235-blog/main/assets/images/mdnwebdocs_header.png" title="MDN Web Docs" style="width:100%;" class="siteheader" alt="A graphic depicting the header of the developer.mozilla.org website.">
</div>

<p><span class="dropcap">M</span><strong>DN</strong> (<em>formerly</em> <strong>Mozilla Developer Network</strong>) <strong>Web Docs</strong> is <strong><em>the</em></strong> authoriative source for all things World Wide Web. This comprehensive website, launched in 2005, maintains detailed, technical reference documents and tutorials on a wide variety of topics, including HTML5, CSS3, Django (a Python web development framework), JavaScript, MathML, Node.js (a popular JavaScript runtime environment), as well as Web APIs, Extensions, and Technologies. MDN Web Docs&rsquo; knowledge repositories represent the collaborative contributions of web development and telecommunications experts from industry giants Mozilla, Google, Microsoft, and Samsung, as well as thousands of amateur and professional independent developers who are part of the MDN community worldwide.<sup><a href="https://www.zdnet.com/article/developers-rejoice-microsoft-google-mozilla-are-putting-all-their-web-api-docs-in-one-place/" target="_blank">1</a></sup> In addition to providing articles on web technology topics, the site also features a soup to nuts, self-paced course on web development in its &ldquo;MDN Learning Area&rdquo; (under &ldquo;Guides&rdquo;). In short, MDN Web Docs delivers on its mission statement: &ldquo;to <u>provide a blueprint for a better internet</u> and empower a new generation of developers and content creators to build it.&rdquo;<sup><a href="https://developer.mozilla.org/en-US/about" target="_blank">2</a></sup>
</p>

<p>One of the features that I find extremely useful about MDN Web Docs is its table of contents-style navigation. I can visit the site with a general topic in mind, e.g., CSS pseudo-classes, and then drill down to more specific topics as I traverse the TOC tree from root to leaves. Before I browse more specific topics, MDN Web Docs warns me if the selected topic is &ldquo;Experimental&rdquo; by placing a beaker icon to the left of the topic name. The left-side navigation tree breaks down topics at the macroscopic level; once I reach the article I desire, a second navigation bar appears stickied to the upper-right side of the browser window that links to subtopics within that article. I appreciate having these dual navigation bars accessible at every turn because I tend to venture down hyperlinked rabbit holes while browsing this veritable hypertext Library of Alexandria&mdash;relying solely on the Back button to return from Wonderland would prove incredibly tiresome. If what I find in the article seems incomplete or in need of correction, I can locate links to the official MDN Web Docs GitHub repository at the bottom of the article and submit issues or suggested revisions on that companion site. In summation, MDN Web Docs accentuates its usefulness as a web development resource by incorporating ease of navigation and methods of user contribution into the ever-growing bodies of knowledge hosted on a generally streamlined, minimalistic site.</p>
<p>Let&rsquo;s see how MDN Web Docs fares after taking some objective measurements.
</p>
<h2>WebSpeed Insights Analysis:</h2>
<h3>Test Conditions:</h3>
<div class="conditions">
<strong>Device:</strong> Samsung Galaxy A13 5G<br/>
<strong>OS:</strong> Android 12<br/>
<strong>Cellular Network:</strong> Boost Mobile 5G
</div>

<figure>
<img src="https://raw.githubusercontent.com/sebastiantbach76/cis-235-blog/main/assets/images/mdn-wsi-desktop.png" title="WebSpeed Insights' Analysis of CanIUse.com (Desktop)" style="width:100%;" alt="A graphic depicting WebSpeed Insight's Analysis of CanIUse.com on Desktop Browsers: Accessibilty 100, Best Practices 92, Performance 93">
<figcaption>WebSpeed Insights&rsquo; Analysis of developer.mozilla.com on Desktop Browsers</figcaption>
</figure>
<figure>
<img src="https://raw.githubusercontent.com/sebastiantbach76/cis-235-blog/main/assets/images/mdn-wsi-mobile.png" title="WebSpeed Insights' Analysis of CanIUse.com (Mobile)" style="width:100%;" alt="A graphic depicting WebSpeed Insight's Analysis of CanIUse.com on Mobile Browsers: Accessibility 100, Best Practices 92, Performance 52">
<figcaption>WebSpeed Insights&rsquo; Analysis of developer.mozilla.com on Mobile Browsers</figcaption>
</figure>

<p>As you can see from the gauges above, MDN Web Docs scores well in terms of &ldquo;Accessiblily&rdquo; and &ldquo;Best Practices&rdquo; on both desktop and mobile platforms. However, the test results reveal a stark difference between desktop and mobile platforms in terms of &ldquo;Performance.&rdquo; The mobile platform test, in particular, reveals a number of surprising issues found on a site devoted to the best and latest information about web technologies. For instance, MDN Web Docs loses points on rubrics such as &ldquo;First Contentful Paint&rdquo; (2.6 s), &ldquo;Time to interactive&rdquo; (5.6 s), &ldquo;Elimination of render-blocking resources&rdquo; (with a potential savings of 1,640 ms), and &ldquo;First Contentful Paint (3G)&rdquo; (5730 ms). While these lower marks do not suggest that the site is a miserable failure on mobile devices, they do raise questions concerning the site&rsquo;s intended audience, especially given that fixes to some of these issues, e.g., removal/replacement of a render-blocking CSS file, strike me as fairly simple to execute.</p>

<h2>lambdatest.com Results (a sample)</h2>

<!-- Images used to open the lightbox -->

<div class="row">
<h3>Google Chrome</h3>

<figure>
  <div class="column">
    <img src="https://raw.githubusercontent.com/sebastiantbach76/cis-235-blog/main/assets/images/mdn-galaxy-note-9-360x740.png" onclick="openModal();currentSlide(1)" class="hover-shadow" width=90px title="CanIUse.com on the Samsung Galaxy Note 9">
    <figcaption>Samsung Galaxy Note 9</figcaption>
  </div>
</figure>
<figure>
  <div class="column">
    <img src="https://raw.githubusercontent.com/sebastiantbach76/cis-235-blog/main/assets/images/mdn-google-pixel-3-412x695.png" onclick="openModal();currentSlide(2)" class="hover-shadow">
    <figcaption>Google Pixel 3</figcaption>
  </div>
</figure>
<figure>  
  <div class="column">
    <img src="https://raw.githubusercontent.com/sebastiantbach76/cis-235-blog/main/assets/images/mdn-iphone-8-plus-414x736.png" onclick="openModal();currentSlide(3)" class="hover-shadow">
    <figcaption>Apple iPhone 8 Plus</figcaption>
  </div>
</figure>
<figure>
  <div class="column">
    <img src="https://raw.githubusercontent.com/sebastiantbach76/cis-235-blog/main/assets/images/mdn-galaxy-tab-s4-10-5-610x808.png" onclick="openModal();currentSlide(4)" class="hover-shadow">
    <figcaption>Samsung Galaxy Tab S4</figcaption>
  </div>
</figure> 

<figure>
  <div class="column">
    <img src="https://raw.githubusercontent.com/sebastiantbach76/cis-235-blog/main/assets/images/mdn-ipad-(6th-generation)-768x1024.png" onclick="openModal();currentSlide(5)" class="hover-shadow">
    <figcaption>Apple iPad 6th Generation</figcaption>
  </div>
</figure>

</div>

<br />

<div class="row">
<div><h3>Mozilla Firefox</h3></div>
<figure>
  <div class="column">
    <img src="https://raw.githubusercontent.com/sebastiantbach76/cis-235-blog/main/assets/images/mdn-galaxy-note-9-firefox-360x740.png" onclick="openModal();currentSlide(6)" class="hover-shadow" width=90px title="CanIUse.com on the Samsung Galaxy Note 9">
    <figcaption>Samsung Galaxy Note 9</figcaption>
  </div>
</figure>
<figure>
  <div class="column">
    <img src="https://raw.githubusercontent.com/sebastiantbach76/cis-235-blog/main/assets/images/mdn-google-pixel-3-firefox-412x695.png" onclick="openModal();currentSlide(7)" class="hover-shadow">
    <figcaption>Google Pixel 3</figcaption>
  </div>
</figure>
<figure>  
  <div class="column">
    <img src="https://raw.githubusercontent.com/sebastiantbach76/cis-235-blog/main/assets/images/mdn-iphone-8-plus-firefox-414x736.png" onclick="openModal();currentSlide(8)" class="hover-shadow">
    <figcaption>Apple iPhone 8 Plus</figcaption>
  </div>
</figure>
<figure>
  <div class="column">
    <img src="https://raw.githubusercontent.com/sebastiantbach76/cis-235-blog/main/assets/images/mdn-galaxy-tab-s4-10-5-firefox-610x808.png" onclick="openModal();currentSlide(9)" class="hover-shadow">
    <figcaption>Samsung Galaxy Tab S4</figcaption>
  </div>
</figure> 

<figure>
  <div class="column">
    <img src="https://raw.githubusercontent.com/sebastiantbach76/cis-235-blog/main/assets/images/mdn-ipad-(6th-generation)-firefox-768x1024.png" onclick="openModal();currentSlide(10)" class="hover-shadow">
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
  <img src="https://raw.githubusercontent.com/sebastiantbach76/cis-235-blog/main/assets/images/mdn-galaxy-note-9-360x740.png" style="width:100%">
</div>

<div class="mySlides">
  <div class="numbertext">2 / 5</div>
  <img src="https://raw.githubusercontent.com/sebastiantbach76/cis-235-blog/main/assets/images/mdn-google-pixel-3-412x695.png" style="width:100%">
</div>

<div class="mySlides">
  <div class="numbertext">3 / 5</div>
  <img src="https://raw.githubusercontent.com/sebastiantbach76/cis-235-blog/main/assets/images/mdn-iphone-8-plus-414x736.png" style="width:100%">
</div>

<div class="mySlides">
  <div class="numbertext">4 / 5</div>
  <img src="https://raw.githubusercontent.com/sebastiantbach76/cis-235-blog/main/assets/images/mdn-galaxy-tab-s4-10-5-610x808.png" style="width:100%">
</div>

<div class="mySlides">
  <div class="numbertext">5 / 5</div>
  <img src="https://raw.githubusercontent.com/sebastiantbach76/cis-235-blog/main/assets/images/mdn-ipad-(6th-generation)-768x1024.png" style="width:100%">
</div>

<div class="mySlides">
  <div class="numbertext">6 / 10</div>
  <img src="https://raw.githubusercontent.com/sebastiantbach76/cis-235-blog/main/assets/images/mdn-galaxy-note-9-firefox-360x740.png" style="width:100%">
</div>

<div class="mySlides">
  <div class="numbertext">7 / 10</div>
  <img src="https://raw.githubusercontent.com/sebastiantbach76/cis-235-blog/main/assets/images/mdn-google-pixel-3-firefox-412x695.png" style="width:100%">
</div>

<div class="mySlides">
  <div class="numbertext">8 / 10</div>
  <img src="https://raw.githubusercontent.com/sebastiantbach76/cis-235-blog/main/assets/images/mdn-iphone-8-plus-firefox-414x736.png" style="width:100%">
</div>

<div class="mySlides">
  <div class="numbertext">9 / 10</div>
  <img src="https://raw.githubusercontent.com/sebastiantbach76/cis-235-blog/main/assets/images/mdn-galaxy-tab-s4-10-5-firefox-610x808.png" style="width:100%">
</div>

<div class="mySlides">
  <div class="numbertext">10 / 10</div>
  <img src="https://raw.githubusercontent.com/sebastiantbach76/cis-235-blog/main/assets/images/mdn-ipad-(6th-generation)-firefox-768x1024.png" style="width:100%">
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
  <img class="demo" src="https://raw.githubusercontent.com/sebastiantbach76/cis-235-blog/main/assets/images/mdn-galaxy-note-9-360x740.png" onclick="currentSlide(1)" alt="Samsung Galaxy Note 9 (Google Chrome)">
</div>

<div class="column">
  <img class="demo" src="https://raw.githubusercontent.com/sebastiantbach76/cis-235-blog/main/assets/images/mdn-google-pixel-3-412x695.png" onclick="currentSlide(2)" alt="Google Pixel 3 (Google Chrome)">
</div>

<div class="column">
  <img class="demo" src="https://raw.githubusercontent.com/sebastiantbach76/cis-235-blog/main/assets/images/mdn-iphone-8-plus-414x736.png" onclick="currentSlide(3)" alt="Apple iPhone 8 Plus (Google Chrome)">
</div>

<div class="column">
  <img class="demo" src="https://raw.githubusercontent.com/sebastiantbach76/cis-235-blog/main/assets/images/mdn-galaxy-tab-s4-10-5-610x808.png" onclick="currentSlide(4)" alt="Samsung Galaxy Tab S4 (Google Chrome)">
</div>

<div class="column">
  <img class="demo" src="https://raw.githubusercontent.com/sebastiantbach76/cis-235-blog/main/assets/images/mdn-ipad-(6th-generation)-768x1024.png" onclick="currentSlide(5)" alt="Apple iPad 6th Generation (Google Chrome)">
</div>

<div class="column">
  <img class="demo" src="https://raw.githubusercontent.com/sebastiantbach76/cis-235-blog/main/assets/images/mdn-galaxy-note-9-firefox-360x740.png" onclick="currentSlide(6)" alt="Samsung Galaxy Note 9 (Mozilla Firefox)">
</div>

<div class="column">
  <img class="demo" src="https://raw.githubusercontent.com/sebastiantbach76/cis-235-blog/main/assets/images/mdn-google-pixel-3-firefox-412x695.png" onclick="currentSlide(7)" alt="Google Pixel 3 (Mozilla Firefox)">
</div>

<div class="column">
  <img class="demo" src="https://raw.githubusercontent.com/sebastiantbach76/cis-235-blog/main/assets/images/mdn-iphone-8-plus-firefox-414x736.png" onclick="currentSlide(8)" alt="Apple iPhone 8 Plus (Mozilla Firefox)">
</div>

<div class="column">
  <img class="demo" src="https://raw.githubusercontent.com/sebastiantbach76/cis-235-blog/main/assets/images/mdn-galaxy-tab-s4-10-5-firefox-610x808.png" onclick="currentSlide(9)" alt="Samsung Galaxy Tab S4 (Mozilla Firefox)">
</div>

<div class="column">
  <img class="demo" src="https://raw.githubusercontent.com/sebastiantbach76/cis-235-blog/main/assets/images/mdn-ipad-(6th-generation)-firefox-768x1024.png" onclick="currentSlide(10)" alt="Apple iPad 6th Generation (Mozilla Firefox)">
</div>

</div>

</div>

<div>

<br/>

<h2>The Bottom Line:</h2>

<p>To be perfectly honest, I could probably spend all day browsing MDN Web Docs: the temptation to dive into this deep pool of WWW wisdom is seldom easy to resist. If there are web developers in the field who do not rely on MDN Web Docs as heavily as I do for day-to-day reference and long-term study, I would highly recommend that they at least acquaint themselves with this rich online resource. The web is a living, breathing creature always growing and moving in new directions. In my humble opinion, MDN Web Docs is one of the best web destinations allowing visitors to keep tabs on the web&rsquo;s changes and movements. It should not only be the first stop on a fledgling web developer&rsquo;s journey toward mastery but also a regular haunt for the more adept developer.</p>
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
