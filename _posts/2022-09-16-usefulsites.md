---
title: "Two Useful Sites for Web Developers: Part 1"
date: 2022-09-16
---
<div class="sitetitle">

<h2>Can I Use... &#128279;</h2>

URL: <a href="https://www.caniuse.com" target="_blank">https://www.caniuse.com/</a>

</div>

<img src="https://raw.githubusercontent.com/sebastiantbach76/cis-235-blog/main/assets/images/caniuse_header.png" title="Can I use..." style="width:100%;" class="siteheader" alt="A graphic depicting the header of the caniuse.com website.">

<p><span class="dropcap">A</span>lexis &#8220;Fyrd&#8221; Deveria maintains this powerful reference website, which features a search engine that indexes HTML tags, CSS syntax, and JavaScript code within the context of their compatibility across various desktop and mobile browsers. For instance, if one wanted to determine which browsers currently support the <strong>&lt;iframe></strong> tag (which sparked some controversy early in its career), CanIUse.com will <a href="https://caniuse.com/mdn-html_elements_iframe">generate a table</a> displaying various browsers (grouped by their past and present versions) and their level of support for that DOM element.  Visitors to the site can organize the search results by current version, global usage, and version release date. Each report offers detailed notes about the query results and a link to <a href="www.browserstack.com" target="_blank">www.browserstack.com</a>, where users may simulate the experience of examining the queried item on a number of different browsers.  To continue with the example query above, one may learn from the search result&rsquo;s supplementary information that &#8220;Safari has a bug that prevents iframes from loading if the iframe element was hidden when added to the page&#8221; and that including &#8220;iframeElement.src = iframeElement.src should cause it to load the iframe.&#8221;<sup><a href="https://caniuse.com/mdn-html_elements_iframe">1</a></sup></p>
<p>
Personally, I find CanIUse.com invaluable for its ability to deliver data visualizations and historical views of support for the myriad tags, attributes, and commonplace code snippets that make up the basic building blocks of the modern World Wide Web. I cannot imagine rolling out a new site without first consulting CanIUse.com to determine the pros and cons of including, e.g., code from the latest ECMAScript standard that may or may not enjoy broad support on both desktop and mobile browsers. The site&rsquo;s excellent search engine allows me to conduct targeted, lightning-fast searches for this information and customize the formatting of the query results to my liking. Moreover, I can rely CanIUse.com to deliver the most current and authoritative compatibility information because the site draws down much of its data from <strong>MDN Web Docs</strong> (see below), the vast repository of web development knowledge trusted by countless developers worldwide. The site also strongly encourages user feedback and publishes a list of user-submitted feature requests (both filled and under consideration), thereby striving to improve an already terrific resource continuously. 
</p>

<p>Not only does CanIUse.com strike me as particularly user friendly, but it also presents itself as extremely browser friendly. A free mobile application for Android devices, <a href="https://play.google.com/store/apps/details?id=com.prodevutils.WebSpeed_Insights" target="_blank">WebSpeed Insights</a>, gives CanIUse.com high marks in the metrics of &#8220;Accessibility,&#8221; &#8220;Best Practices,&#8221; and &#8220;Performance&#8221; on both desktop and mobile browsers.</p>

<p><strong><em>Accessibility:</em></strong> WebSpeed Insights defines this category as &#8220;the inclusive practice of ensuring there are no barriers that prevent interaction with, or access to, websites on the World Wide Web by people with physical disabilities, situational disabilities, and socioeconomic restrictions on bandwidth and speed.&#8221; The app assigns sites an &#8220;Accessibility&#8221; score on a scale of 1-100 based on a great number of rubrics, including &#8220;&grave;[aria-*]&grave; attributes match their roles,&#8221; &#8220;Background and foreground colors have a sufficient contrast ratio,&#8221; and &#8221;Image elements have &grave;[alt]&grave; attributes.&#8221;</p>

<p><strong><em>Best Practices:</em></strong> WebSpeed Insights examines web pages to determine if they adhere to sixteen different industry standards for HTML formatting, user privacy, and website security. Some of these standards include &#8220;Uses HTTPS,&#8221; &#8220;Avoids front-end JavaScript libraries with known security vulnerabilities,&#8221; &#8220;Serves images with proper resolution,&#8221; and &#8220;Avoids requesting the notification permission on page load.&#8221; Once again, the application assigns the website in question a score from 1-100 in this category.
</p>

<p><strong><em>Performance:</em></strong> This metric takes into consideration the speed with which analyzed pages download and render and assigns those pages a score on a scale of 1-100.  The multitude of rubrics for this measure includes &#8220;Time to interactive,&#8221; &#8220;Total Blocking Time,&#8221; &#8220;Properly sizes images,&#8221; &#8220;Minifies CSS,&#8221; &#8220;Uses passive listeners to improve scrolling performance,&#8221; and &#8220;Reduces unused JavaScript.&#8221;
</p>

<figure>
<img src="https://raw.githubusercontent.com/sebastiantbach76/cis-235-blog/main/assets/images/ciu-wsi-desktop.png" title="WebSpeed Insights' Analysis of CanIUse.com (Desktop)" style="width:100%;" alt="A graphic depicting WebSpeed Insight's Analysis of CanIUse.com on Desktop Browsers">
<figcaption>WebSpeed Insights&rsquo; Analysis of CanIUse.com on Desktop Browsers</figcaption>
</figure>
<figure>
<img src="https://raw.githubusercontent.com/sebastiantbach76/cis-235-blog/main/assets/images/ciu-wsi-mobile.png" title="WebSpeed Insights' Analysis of CanIUse.com (Mobile)" style="width:100%;" alt="A graphic depicting WebSpeed Insight's Analysis of CanIUse.com on Mobile Browsers">
<figcaption>WebSpeed Insights&rsquo; Analysis of CanIUse.com on Mobile Browsers</figcaption>
</figure>

<p>I am genuinely impressed by the extensive list of website metrics that WebSpeed Insights examines, and I plan to use its analyses as a means of evaluating all of the web pages that I review on this blog site. I also plan to provide sample test results from <a href="https://www.lambdatest.com" >lambdatest.com</a>, which simulates precisely how websites render on different mobile devices (see below).</p>

<h2>lambdatest.com Results (a sample)</h2>

<!-- Images used to open the lightbox -->

<div class="row">
<h3>Google Chrome</h3>
<figure>
  <div class="column">
    <img src="https://raw.githubusercontent.com/sebastiantbach76/cis-235-blog/main/assets/images/ciu-galaxy-note-9-360x740.png" onclick="openModal();currentSlide(1)" class="hover-shadow" width=90px title="CanIUse.com on the Samsung Galaxy Note 9">
    <figcaption>Samsung Galaxy Note 9</figcaption>
  </div>
</figure>
<figure>
  <div class="column">
    <img src="https://raw.githubusercontent.com/sebastiantbach76/cis-235-blog/main/assets/images/ciu-google-pixel-3-412x695.png" onclick="openModal();currentSlide(2)" class="hover-shadow">
    <figcaption>Google Pixel 3</figcaption>
  </div>
</figure>
<figure>  
  <div class="column">
    <img src="https://raw.githubusercontent.com/sebastiantbach76/cis-235-blog/main/assets/images/ciu-iphone-8-plus-414x736.png" onclick="openModal();currentSlide(3)" class="hover-shadow">
    <figcaption>Apple iPhone 8 Plus</figcaption>
  </div>
</figure>
<figure>
  <div class="column">
    <img src="https://raw.githubusercontent.com/sebastiantbach76/cis-235-blog/main/assets/images/ciu-galaxy-tab-s4-10-5-610x808.png" onclick="openModal();currentSlide(4)" class="hover-shadow">
    <figcaption>Samsung Galaxy Tab S4</figcaption>
  </div>
</figure> 

<figure>
  <div class="column">
    <img src="https://raw.githubusercontent.com/sebastiantbach76/cis-235-blog/main/assets/images/ciu-ipad-(6th-generation)-768x1024.png" onclick="openModal();currentSlide(5)" class="hover-shadow">
    <figcaption>Apple iPad 6th Generation</figcaption>
  </div>
</figure>
</div>

<div class="row">
<div><h3>Mozilla Firefox</h3></div>
<figure>
  <div class="column">
    <img src="https://raw.githubusercontent.com/sebastiantbach76/cis-235-blog/main/assets/images/ciu-galaxy-note-9-360x740.png" onclick="openModal();currentSlide(6)" class="hover-shadow" width=90px title="CanIUse.com on the Samsung Galaxy Note 9">
    <figcaption>Samsung Galaxy Note 9</figcaption>
  </div>
</figure>
<figure>
  <div class="column">
    <img src="https://raw.githubusercontent.com/sebastiantbach76/cis-235-blog/main/assets/images/ciu-google-pixel-3-412x695.png" onclick="openModal();currentSlide(7)" class="hover-shadow">
    <figcaption>Google Pixel 3</figcaption>
  </div>
</figure>
<figure>  
  <div class="column">
    <img src="https://raw.githubusercontent.com/sebastiantbach76/cis-235-blog/main/assets/images/ciu-iphone-8-plus-414x736.png" onclick="openModal();currentSlide(8)" class="hover-shadow">
    <figcaption>Apple iPhone 8 Plus</figcaption>
  </div>
</figure>
<figure>
  <div class="column">
    <img src="https://raw.githubusercontent.com/sebastiantbach76/cis-235-blog/main/assets/images/ciu-galaxy-tab-s4-10-5-610x808.png" onclick="openModal();currentSlide(9)" class="hover-shadow">
    <figcaption>Samsung Galaxy Tab S4</figcaption>
  </div>
</figure> 

<figure>
  <div class="column">
    <img src="https://raw.githubusercontent.com/sebastiantbach76/cis-235-blog/main/assets/images/ciu-ipad-(6th-generation)-768x1024.png" onclick="openModal();currentSlide(10)" class="hover-shadow">
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
  <div class="numbertext">1 / 10</div>
  <img src="https://raw.githubusercontent.com/sebastiantbach76/cis-235-blog/main/assets/images/ciu-galaxy-note-9-360x740.png" style="width:100%">
</div>

<div class="mySlides">
  <div class="numbertext">2 / 10</div>
  <img src="https://raw.githubusercontent.com/sebastiantbach76/cis-235-blog/main/assets/images/ciu-google-pixel-3-412x695.png" style="width:100%">
</div>

<div class="mySlides">
  <div class="numbertext">3 / 10</div>
  <img src="https://raw.githubusercontent.com/sebastiantbach76/cis-235-blog/main/assets/images/ciu-iphone-8-plus-414x736.png" style="width:100%">
</div>

<div class="mySlides">
  <div class="numbertext">4 / 10</div>
  <img src="https://raw.githubusercontent.com/sebastiantbach76/cis-235-blog/main/assets/images/ciu-galaxy-tab-s4-10-5-610x808.png" style="width:100%">
</div>

<div class="mySlides">
  <div class="numbertext">5 / 10</div>
  <img src="https://raw.githubusercontent.com/sebastiantbach76/cis-235-blog/main/assets/images/ciu-ipad-(6th-generation)-768x1024.png" style="width:100%">
</div>

<div class="mySlides">
  <div class="numbertext">6 / 10</div>
  <img src="https://raw.githubusercontent.com/sebastiantbach76/cis-235-blog/main/assets/images/ciu-galaxy-note-9-360x740.png" style="width:100%">
</div>

<div class="mySlides">
  <div class="numbertext">7 / 10</div>
  <img src="https://raw.githubusercontent.com/sebastiantbach76/cis-235-blog/main/assets/images/ciu-google-pixel-3-412x695.png" style="width:100%">
</div>

<div class="mySlides">
  <div class="numbertext">8 / 10</div>
  <img src="https://raw.githubusercontent.com/sebastiantbach76/cis-235-blog/main/assets/images/ciu-iphone-8-plus-414x736.png" style="width:100%">
</div>

<div class="mySlides">
  <div class="numbertext">9 / 10</div>
  <img src="https://raw.githubusercontent.com/sebastiantbach76/cis-235-blog/main/assets/images/ciu-galaxy-tab-s4-10-5-610x808.png" style="width:100%">
</div>

<div class="mySlides">
  <div class="numbertext">10 / 10</div>
  <img src="https://raw.githubusercontent.com/sebastiantbach76/cis-235-blog/main/assets/images/ciu-ipad-(6th-generation)-768x1024.png" style="width:100%">
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
  <img class="demo" src="https://raw.githubusercontent.com/sebastiantbach76/cis-235-blog/main/assets/images/ciu-galaxy-note-9-360x740.png" onclick="currentSlide(1)" alt="Samsung Galaxy Note 9">
</div>

<div class="column">
  <img class="demo" src="https://raw.githubusercontent.com/sebastiantbach76/cis-235-blog/main/assets/images/ciu-google-pixel-3-412x695.png" onclick="currentSlide(2)" alt="Google Pixel 3">
</div>

<div class="column">
  <img class="demo" src="https://raw.githubusercontent.com/sebastiantbach76/cis-235-blog/main/assets/images/ciu-iphone-8-plus-414x736.png" onclick="currentSlide(3)" alt="Apple iPhone 8 Plus">
</div>

<div class="column">
  <img class="demo" src="https://raw.githubusercontent.com/sebastiantbach76/cis-235-blog/main/assets/images/ciu-galaxy-tab-s4-10-5-610x808.png" onclick="currentSlide(4)" alt="Samsung Galaxy Tab S4">
</div>

<div class="column">
  <img class="demo" src="https://raw.githubusercontent.com/sebastiantbach76/cis-235-blog/main/assets/images/ciu-ipad-(6th-generation)-768x1024.png" onclick="currentSlide(5)" alt="Apple iPad 6th Generation">
</div>

<div class="column">
  <img class="demo" src="https://raw.githubusercontent.com/sebastiantbach76/cis-235-blog/main/assets/images/ciu-galaxy-note-9-360x740.png" onclick="currentSlide(6)" alt="Samsung Galaxy Note 9">
</div>

<div class="column">
  <img class="demo" src="https://raw.githubusercontent.com/sebastiantbach76/cis-235-blog/main/assets/images/ciu-google-pixel-3-412x695.png" onclick="currentSlide(7)" alt="Google Pixel 3">
</div>

<div class="column">
  <img class="demo" src="https://raw.githubusercontent.com/sebastiantbach76/cis-235-blog/main/assets/images/ciu-iphone-8-plus-414x736.png" onclick="currentSlide(8)" alt="Apple iPhone 8 Plus">
</div>

<div class="column">
  <img class="demo" src="https://raw.githubusercontent.com/sebastiantbach76/cis-235-blog/main/assets/images/ciu-galaxy-tab-s4-10-5-610x808.png" onclick="currentSlide(9)" alt="Samsung Galaxy Tab S4">
</div>

<div class="column">
  <img class="demo" src="https://raw.githubusercontent.com/sebastiantbach76/cis-235-blog/main/assets/images/ciu-ipad-(6th-generation)-768x1024.png" onclick="currentSlide(10)" alt="Apple iPad 6th Generation">
</div>

</div>

</div>

<div>

<br/>

<h2>The Bottom Line:</h2>

<p>In my humble opinion, CanIUse.com should occupy a special place in any web developer&rsquo;s bookmark collection. </p>
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
  background-color: black;
  padding: 2px 16px;
  color: white;
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
