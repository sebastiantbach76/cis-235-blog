---
title: "Interesting Sites for Geeks: Pt. 2"
date: 2022-09-18
---
<div class="sitetitle">

<h2>MIT Technology Review &#128279;</h2>

URL: <a href="https://www.technologyreview.com/" target="_blank">https://www.technologyreview.com/</a>

</div>

<div>
<img src="https://raw.githubusercontent.com/sebastiantbach76/cis-235-blog/main/assets/images/mtr_header.png" title="MIT Technology Review" style="width:100%;" class="siteheader" alt="A graphic depicting the header of the www.technologyreview.org website.">
</div>

<p><span class="dropcap">M</span><strong>IT TECHNOLOGY REVIEW</strong> has published twice monthly since at least 1998 (when it shed the name <em>The Technology Review</em> for a humbler, more accurate title); however, it is remarkable to note that the magazine has been in publication since 1899.<sup><a href="https://www.technologyreview.com/supertopic/about/" target="_blank">1</a></sup> Prior to the name change, the magazine catered to a much narrower, strictly academic audience; since adopting the new title, MIT Technology Review features articles intended for a more general audience interested in the latest developments in cutting-edge technologies. The review regularly covers stories on current and emerging technologies understood broadly, including aerospace technology, artificial intelligence, automobiles, biotechnology, personal computing, engineering, environmental science, information security, IoT/wearable devices, practical and theoretical physics, technology policy, programming, remote sensing, robotics, social media, telecommunications, and the general World Wide Web. The magazine&rsquo;s articles feature interviews with movers and shakers within the various technology industries, editorials, technical report digests, and reviews of products recently released or soon-to-be released. Beyond its presence as both a print publication and companion website, MIT Technology Review also publishes a number of podcasts and organizes in-person and virtual events at which technology industry leaders present on timely subjects. 
</p>
<p>My abiding interest in MIT Technology Review derives from my desire to stay informed about evolving trends in various technologies without feeling the need to read several academic texts to understand the magazine&rsquo;s pieces (though I am sometimes moved to do so to satisfy personal curiosity). In my experience, contributors to the magazine write for an audience that splits the difference between the highly technical expert and the casual enthusiast, so I feel that the writing is never too abstruse nor too elementary. The review also consistently challenges the limitations of my perspectives on what the margins of technology are, repeatedly demonstrating how pervasive modern technologies have become in humans&rsquo; everyday lives. As a (paid subscription) website, MIT Technology Review presents a simple, clean design (built using the React.js framework) with only moderate reliance on large graphics set to downsize for smaller screens on demand.  The navigational header and related story sidebar are stickied to the top and right of the browser window, respectively, but unobtrusive, so the site keeps content legible while also facilitating ease of transition to a different department or topic from the current article. This unostentatious design allows readers to focus on the articles without being distracted by unrelated advertisements or additional features competing for attention.
</p>
<p>With these broad strokes in mind, let&rsquo;s examine some objective measures of MIT Technology Review&rsquo;s site design:
</p>
<h2>WebSpeed Insights Analysis:</h2>
<h3>Test Conditions:</h3>
<div class="conditions">
<strong>Device:</strong> Samsung Galaxy A13 5G<br/>
<strong>OS:</strong> Android 12<br/>
<strong>Cellular Network:</strong> Boost Mobile 5G
</div>

<figure>
<img src="https://raw.githubusercontent.com/sebastiantbach76/cis-235-blog/main/assets/images/mtr-wsi-desktop.png" title="WebSpeed Insights' Analysis of www.technologyreview.com (Desktop)" style="width:100%;" alt="A graphic depicting WebSpeed Insight's Analysis of www.technologyreview.com on Desktop Browsers: Accessibilty 87, Best Practices 100, Performance 100">
<figcaption>WebSpeed Insights&rsquo; Analysis of www.technologyreview.com on Desktop Browsers</figcaption>
</figure>
<figure>
<img src="https://raw.githubusercontent.com/sebastiantbach76/cis-235-blog/main/assets/images/mtr-wsi-mobile.png" title="WebSpeed Insights' Analysis of www.technologyreview.com (Mobile)" style="width:100%;" alt="A graphic depicting WebSpeed Insight's Analysis of www.technologyreview.com on Mobile Browsers: Accessibility 95, Best Practices 100, Performance 89">
<figcaption>WebSpeed Insights&rsquo; Analysis of www.technologyreview.com on Mobile Browsers</figcaption>
</figure>

<p>The majority of these scores seem superb, so let&rsquo;s examine areas where the desktop browsing experience proved less than ideal on accessibility and where the mobile browsing experience underperformed. According to WebSpeed Insights, three rubrics account for the drop in the site&rsquo;s accessibility:</p>
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

<p>With the exception of minor variations in how different browsers display certain colors used on www.technologyreview.com, lambdatest.com reports no significant differences in functionality across various browsers.</p>

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
