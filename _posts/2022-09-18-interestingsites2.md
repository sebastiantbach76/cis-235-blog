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
<img src="https://raw.githubusercontent.com/sebastiantbach76/cis-235-blog/main/assets/images/mtr-wsi-desktop.png" title="WebSpeed Insights' Analysis of www.technologyreview.com (Desktop)" style="width:100%;" alt="A graphic depicting WebSpeed Insight's Analysis of www.technologyreview.com on Desktop Browsers: Accessibilty 82, Best Practices 92, Performance 48">
<figcaption>WebSpeed Insights&rsquo; Analysis of www.technologyreview.com on Desktop Browsers</figcaption>
</figure>
<figure>
<img src="https://raw.githubusercontent.com/sebastiantbach76/cis-235-blog/main/assets/images/mtr-wsi-mobile.png" title="WebSpeed Insights' Analysis of www.technologyreview.com (Mobile)" style="width:100%;" alt="A graphic depicting WebSpeed Insight's Analysis of www.technologyreview.com on Mobile Browsers: Accessibility 75, Best Practices 83, Performance 20">
<figcaption>WebSpeed Insights&rsquo; Analysis of www.technologyreview.com on Mobile Browsers</figcaption>
</figure>

<p>Clearly, MIT Technology Review earned some significantly low scores from WebSpeed Insights, so let&rsquo;s devote some space in this post to unpacking the major issues.</p>
<p>Desktop browsers registered a major dip in performance when accessing www.technologyreview.com. The primary rubrics that the site failed to meet are:
</p>
<ol>
  <li>Time to interactive: 5.6 s</li>
  <li>Speed index (a measure of how quickly elements of a page populate): 2.7 s</li>
  <li>Total blocking time: 460 ms</li>
  <li>Max Potential First Input Delay (a measure of how long the page takes to load before a user can begin entering input): 370 ms</li>
  <li>Reduces unused JavaScript: potential 762 KB reduction</li>
  <li>Avoids enormous network payloads: total size of 3,918 KB</li>
  <li>Reduces JavaScript execution time (typically reflective of how numerous or large the external JavaScript files used by the site are): 2.8 s</li>
  <li>Ensures text remains visible during webfont load: failed</li>
</ol>
<p>Based on these results, I would venture that the 10+ external JavaScript files that the site attempts to execute are chiefly responsible for the reduction in site performance. My browser console also displays several &ldquo;Uncaught (in promise)&rdquo; errors indicating problems with the site&rsquo;s code (namely, improperly handled exceptions) that go beyond the sheer volume of JavaScript loaded by the page. By all appearances, much of the external code is devoted to third-party site analytics, so the website administrators should consider how much value they derive from these measures and trackers and consider reducing their number to improve performance on desktop browsers.</p>
<p>Mobile browsers suffered a two-pronged reduction in accessibility and performance:</p>
<ol>
  <li>Time to interactive: 7.7 s</li>
  <li>Speed index: 6.2 s</li>
  <li>Total Blocking Time: 5,160 ms</li>
  <li>Defers offscreen images (typically indicates that the site does not employ lazy-loading of offscreen and hidden images): potential reduction of 1,062 KB</li>
  <li>Reduces unused JavaScript: potential reduction of 811 KB</li>
  <li>Serves images in next-gen formats (failure usually indicates the site relies exclusively on JPEGs and PNGs instead of graphic formats with higher compression ratios such as WebP): potential reduction of 76 KB</li>
  <li>Avoids serving legacy JavaScript to modern browser (failure typically means the site does not discriminate between older and newer browsers and, instead, pushes the same polyfills and transforms to both): potential reduction of 74 KB</li>
  <li>Avoids enormous network payloads: total size of 3,985 KB</li>
  <li>Reduces JavaScript execution time: 6.4 s</li>
  <li>Ensures text remains visible during webfont load</li>
  <li>Reduces the impact of third-party code: 3,820 ms</li>
  <li>Buttons do not have an accessible name</li>
  <li>Background and foreground colors do not have a sufficient contrast ratio</li>
  <li>&#96;[id]` attributes on active, focusable elements are not unique</li>
  <li>ARIA IDs are not unique</li>
  <li>Heading elements are not in a sequentially-descending order (typically indicates that nested headings skip over numeric levels from one header to the next, thereby muddling the semantic structure of the page for assistive devices)</li>
  <li>Links do not have a discernible name</li>
</ol>
<p>Obviously, www.technologyreview.com should revisit its JavaScript inclusions and do a better job of minimizing its impact on performance. There are also some simple steps the administrators could take to reduce the burden of static site assets: a quick batch conversion of graphics to a format like WebP (followed by some necessary HTML refactoring) should help reduce the file sizes of graphics dramatically. Finally, it would seem that the site requires serious revision to be more inclusive and hospitable to visitors with disabilities, in particular those affected by low vision. As the site currently stands, it risks forcing assistive devices to overlook large sections of content, leaving some visitors to the site in the dark about numerous articles.
</p>
<h2>lambdatest.com Results (a sample)</h2>

<!-- Images used to open the lightbox -->

<div class="row">
<h3>Google Chrome</h3>

<figure>
  <div class="column">
    <img src="https://raw.githubusercontent.com/sebastiantbach76/cis-235-blog/main/assets/images/mtr-galaxy-note-9-360x740.png" onclick="openModal();currentSlide(1)" class="hover-shadow" width=90px title="www.technologyreview.com on the Samsung Galaxy Note 9">
    <figcaption>Samsung Galaxy Note 9</figcaption>
  </div>
</figure>
<figure>
  <div class="column">
    <img src="https://raw.githubusercontent.com/sebastiantbach76/cis-235-blog/main/assets/images/mtr-google-pixel-3-412x695.png" onclick="openModal();currentSlide(2)" class="hover-shadow" title="www.technologyreview.com the Google Pixel 3">
    <figcaption>Google Pixel 3</figcaption>
  </div>
</figure>
<figure>  
  <div class="column">
    <img src="https://raw.githubusercontent.com/sebastiantbach76/cis-235-blog/main/assets/images/mtr-iphone-8-plus-414x736.png" onclick="openModal();currentSlide(3)" class="hover-shadow" title="www.technologyreview.com on the Apple iPhone 8 Plus">
    <figcaption>Apple iPhone 8 Plus</figcaption>
  </div>
</figure>
<figure>
  <div class="column">
    <img src="https://raw.githubusercontent.com/sebastiantbach76/cis-235-blog/main/assets/images/mtr-galaxy-tab-s4-10-5-610x808.png" onclick="openModal();currentSlide(4)" class="hover-shadow" title="www.technologyreview.com on the Samsung Galaxy Tab S4">
    <figcaption>Samsung Galaxy Tab S4</figcaption>
  </div>
</figure> 

<figure>
  <div class="column">
    <img src="https://raw.githubusercontent.com/sebastiantbach76/cis-235-blog/main/assets/images/mtr-ipad-(6th-generation)-768x1024.png" onclick="openModal();currentSlide(5)" class="hover-shadow" title="www.technologyreview.com on the Apple iPad 6th Generation">
    <figcaption>Apple iPad 6th Generation</figcaption>
  </div>
</figure>

</div>

<br />

<div class="row">
<div><h3>Mozilla Firefox</h3></div>
<figure>
  <div class="column">
    <img src="https://raw.githubusercontent.com/sebastiantbach76/cis-235-blog/main/assets/images/mtr-galaxy-note-9-firefox-360x740.png" onclick="openModal();currentSlide(6)" class="hover-shadow" width=90px title="www.technologyreview.com on the Samsung Galaxy Note 9">
    <figcaption>Samsung Galaxy Note 9</figcaption>
  </div>
</figure>
<figure>
  <div class="column">
    <img src="https://raw.githubusercontent.com/sebastiantbach76/cis-235-blog/main/assets/images/mtr-google-pixel-3-firefox-412x695.png" onclick="openModal();currentSlide(7)" class="hover-shadow" title="www.technologyreview.com on the Google Pixel 3">
    <figcaption>Google Pixel 3</figcaption>
  </div>
</figure>
<figure>  
  <div class="column">
    <img src="https://raw.githubusercontent.com/sebastiantbach76/cis-235-blog/main/assets/images/mtr-iphone-8-plus-firefox-414x736.png" onclick="openModal();currentSlide(8)" class="hover-shadow" title="www.technologyreview.com on the Apple iPhone 8 Plus">
    <figcaption>Apple iPhone 8 Plus</figcaption>
  </div>
</figure>
<figure>
  <div class="column">
    <img src="https://raw.githubusercontent.com/sebastiantbach76/cis-235-blog/main/assets/images/mtr-galaxy-tab-s4-10-5-firefox-610x808.png" onclick="openModal();currentSlide(9)" class="hover-shadow" title="www.technologyreview.com on the Samsung Galaxy Tab S4">
    <figcaption>Samsung Galaxy Tab S4</figcaption>
  </div>
</figure> 

<figure>
  <div class="column">
    <img src="https://raw.githubusercontent.com/sebastiantbach76/cis-235-blog/main/assets/images/mtr-ipad-(6th-generation)-firefox-768x1024.png" onclick="openModal();currentSlide(10)" class="hover-shadow" title="www.technologyreview.com on the Apple iPad 6th Generation">
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
  <img src="https://raw.githubusercontent.com/sebastiantbach76/cis-235-blog/main/assets/images/mtr-galaxy-note-9-360x740.png" style="width:100%">
</div>

<div class="mySlides">
  <div class="numbertext">2 / 10</div>
  <img src="https://raw.githubusercontent.com/sebastiantbach76/cis-235-blog/main/assets/images/mtr-google-pixel-3-412x695.png" style="width:100%">
</div>

<div class="mySlides">
  <div class="numbertext">3 / 10</div>
  <img src="https://raw.githubusercontent.com/sebastiantbach76/cis-235-blog/main/assets/images/mtr-iphone-8-plus-414x736.png" style="width:100%">
</div>

<div class="mySlides">
  <div class="numbertext">4 / 10</div>
  <img src="https://raw.githubusercontent.com/sebastiantbach76/cis-235-blog/main/assets/images/mtr-galaxy-tab-s4-10-5-610x808.png" style="width:100%">
</div>

<div class="mySlides">
  <div class="numbertext">5 / 10</div>
  <img src="https://raw.githubusercontent.com/sebastiantbach76/cis-235-blog/main/assets/images/mtr-ipad-(6th-generation)-768x1024.png" style="width:100%">
</div>

<div class="mySlides">
  <div class="numbertext">6 / 10</div>
  <img src="https://raw.githubusercontent.com/sebastiantbach76/cis-235-blog/main/assets/images/mtr-galaxy-note-9-firefox-360x740.png" style="width:100%">
</div>

<div class="mySlides">
  <div class="numbertext">7 / 10</div>
  <img src="https://raw.githubusercontent.com/sebastiantbach76/cis-235-blog/main/assets/images/mtr-google-pixel-3-firefox-412x695.png" style="width:100%">
</div>

<div class="mySlides">
  <div class="numbertext">8 / 10</div>
  <img src="https://raw.githubusercontent.com/sebastiantbach76/cis-235-blog/main/assets/images/mtr-iphone-8-plus-firefox-414x736.png" style="width:100%">
</div>

<div class="mySlides">
  <div class="numbertext">9 / 10</div>
  <img src="https://raw.githubusercontent.com/sebastiantbach76/cis-235-blog/main/assets/images/mtr-galaxy-tab-s4-10-5-firefox-610x808.png" style="width:100%">
</div>

<div class="mySlides">
  <div class="numbertext">10 / 10</div>
  <img src="https://raw.githubusercontent.com/sebastiantbach76/cis-235-blog/main/assets/images/mtr-ipad-(6th-generation)-firefox-768x1024.png" style="width:100%">
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
  <img class="demo" src="https://raw.githubusercontent.com/sebastiantbach76/cis-235-blog/main/assets/images/mtr-galaxy-note-9-360x740.png" onclick="currentSlide(1)" alt="Samsung Galaxy Note 9 (Google Chrome)">
</div>

<div class="column">
  <img class="demo" src="https://raw.githubusercontent.com/sebastiantbach76/cis-235-blog/main/assets/images/mtr-google-pixel-3-412x695.png" onclick="currentSlide(2)" alt="Google Pixel 3 (Google Chrome)">
</div>

<div class="column">
  <img class="demo" src="https://raw.githubusercontent.com/sebastiantbach76/cis-235-blog/main/assets/images/mtr-iphone-8-plus-414x736.png" onclick="currentSlide(3)" alt="Apple iPhone 8 Plus (Google Chrome)">
</div>

<div class="column">
  <img class="demo" src="https://raw.githubusercontent.com/sebastiantbach76/cis-235-blog/main/assets/images/mtr-galaxy-tab-s4-10-5-610x808.png" onclick="currentSlide(4)" alt="Samsung Galaxy Tab S4 (Google Chrome)">
</div>

<div class="column">
  <img class="demo" src="https://raw.githubusercontent.com/sebastiantbach76/cis-235-blog/main/assets/images/mtr-ipad-(6th-generation)-768x1024.png" onclick="currentSlide(5)" alt="Apple iPad 6th Generation (Google Chrome)">
</div>

<div class="column">
  <img class="demo" src="https://raw.githubusercontent.com/sebastiantbach76/cis-235-blog/main/assets/images/mtr-galaxy-note-9-firefox-360x740.png" onclick="currentSlide(6)" alt="Samsung Galaxy Note 9 (Mozilla Firefox)">
</div>

<div class="column">
  <img class="demo" src="https://raw.githubusercontent.com/sebastiantbach76/cis-235-blog/main/assets/images/mtr-google-pixel-3-firefox-412x695.png" onclick="currentSlide(7)" alt="Google Pixel 3 (Mozilla Firefox)">
</div>

<div class="column">
  <img class="demo" src="https://raw.githubusercontent.com/sebastiantbach76/cis-235-blog/main/assets/images/mtr-iphone-8-plus-firefox-414x736.png" onclick="currentSlide(8)" alt="Apple iPhone 8 Plus (Mozilla Firefox)">
</div>

<div class="column">
  <img class="demo" src="https://raw.githubusercontent.com/sebastiantbach76/cis-235-blog/main/assets/images/mtr-galaxy-tab-s4-10-5-firefox-610x808.png" onclick="currentSlide(9)" alt="Samsung Galaxy Tab S4 (Mozilla Firefox)">
</div>

<div class="column">
  <img class="demo" src="https://raw.githubusercontent.com/sebastiantbach76/cis-235-blog/main/assets/images/mtr-ipad-(6th-generation)-firefox-768x1024.png" onclick="currentSlide(10)" alt="Apple iPad 6th Generation (Mozilla Firefox)">
</div>

</div>

</div>

<div>

<br/>

<p>lambdatest.com detected the JavaScript exceptions problem noted above, so the impact of that misbehaving code on site functionality across browsers remains unknown. With the exception of minor variations in how different browsers display certain colors used on www.technologyreview.com, lambdatest.com reported no other significant differences in functionality across various browsers.</p>

<h2>The Bottom Line:</h2>

<p>WebSpeed Insights returned some troubling reports regarding malformed or missing ARIA elements on www.technologyreview.com. Accordingly, I feel uncomfortable recommending the site to a general audience. Otherwise, I would recommend it to readers who typically browse the web using a desktop client. Setting aside these performance and accessibility concerns, I <em>do</em> think readers who are interested in today&rsquo;s latest technology news would enjoy browsing the articles available on MIT Technology Review. In my experience, science and technology journalists often inadvertently betray limited writing and proofreading skills, especially on online-only STEM media outlets. MIT Technology Review writers have proven themselves to be the exception to that trend, and I value their ability to convey often complex technological details in polished prose.</p>
</div>

</div>

<div class="endrow">
    <div class="col-l"><strong>Previous:</strong> <a href="https://sebastiantbach76.github.io/cis-235-blog/2022/09/18/interestingsites.html">&#9754;
    &ldquo;Interesting Sites<br>for Geeks: Part 1&rdquo; </a>
    </div>
    <div class="col-r"><strong>Next: </strong><a href="https://sebastiantbach76.github.io/cis-235-blog/2022/09/19/tgtbtu1.html">&ldquo;The Good, the Bad,<br>and the Ugly: Part 1&rdquo;&#9755;
    </a></div>
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

.endrow {
  display: flex;
  justify-content: space-between;
}

.col-l {
  font-weight: 800;
  font-size: 16px;
}

.col-r {
  font-weight: 800;
  font-size: 16px;
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
