---
title: "Two Useful Sites for Web Developers"
date: 2022-09-16
---
<div class="sitetitle">

<h2>Can I Use... &#128279;</h2>

URL: <a href="https://www.caniuse.com" target="_blank">https://www.caniuse.com/</a>

</div>

<img src="https://raw.githubusercontent.com/sebastiantbach76/cis-235-blog/main/assets/images/caniuse_header.png" title="Can I use..." style="width:100%;" class="siteheader" alt="A graphic depicting the header of the caniuse.com website.">

<p><span class="dropcap">A</span>lexis &#8220;Fyrd&#8221; Deveria maintains this powerful reference website, which features a search engine that indexes HTML tags, CSS syntax, and JavaScript code within the context of their compatibility across various desktop and mobile browsers. For instance, if one wanted to determine which browsers currently support the <strong>&lt;iframe></strong> tag (which sparked some controversy early in its career), CanIUse.com will <a href="https://caniuse.com/mdn-html_elements_iframe">generate a table</a> displaying various browsers (grouped by their past and present versions) and their level of support for that DOM element.  Visitors to the site can organize the search results by current version, global usage, and version release date. Each report offers detailed notes about the query results and a link to <a href="www.browserstack.com" target="_blank">www.browserstack.com</a>, where users may simulate the experience of examining the queried item on a number of different browsers.  To continue with the example query above, one may learn from the search result&rsquo;s supplementary information that &#8220;Safari has a bug that prevents iframes from loading if the iframe element was hidden when added to the page&#8221; and that including &#8220;iframeElement.src = iframeElement.src should cause it to load the iframe.&#8221;<sup><a href="https://caniuse.com/mdn-html_elements_iframe">1</a></sup></p>
<p>
Personally, I find CanIUse.com invaluable for its ability to deliver data visualizations and historical views of support for the myriad tags, properties, and commonplace code snippets that make up the basic building blocks of the modern World Wide Web. I cannot imagine rolling out a new site without first consulting CanIUse.com to determine the pros and cons of including, e.g., code from the latest ECMAScript standard that may or may not enjoy broad support on both desktop and mobile browsers. The site&rsquo;s excellent search engine allows me to conduct targeted searches for this information and customize the formatting of the query results to my liking. Moreover, I can rely CanIUse.com to deliver the most current and authoritative compatibility information because the site draws down much of its data from <strong>MDN Web Docs</strong> (see below), the vast repository of web development knowledge trusted by countless developers worldwide.
</p>

<p>Not only does CanIUse.com strike me as particularly user friendly, but it also presents itself as extremely browser friendly. A mobile application for Android devices, <a href="https://play.google.com/store/apps/details?id=com.prodevutils.WebSpeed_Insights" target="_blank">WebSpeed Insights</a>, gives CanIUse.com high marks in the categories of &#8220;Accessibility,&#8221; &#8220;Best Practices,&#8221; and &#8220;Performance&#8221; on both desktop and mobile browsers. WebSpeed Insight&rsquo;s documentation defines  &#8220;Accessibility&#8221; as &#8220;the inclusive practice of ensuring there are no barriers that prevent interaction with, or access to, websites on the World Wide Web by people with physical disabilities, situational disabilities, and socioeconomic restrictions on bandwidth and speed.&#8221; The app assigns sites an &#8220;Accessibility&#8221; grade on a scale of 1-100 based on rubrics such as &#8220;`[aria-*]` attributes match their roles,&#8221; &#8220;Background and foreground colors have a sufficient contrast ratio,&#8221; and &#8221;Image elements have `[alt]` attributes.&#8221;</p>

<figure>
<img src="https://raw.githubusercontent.com/sebastiantbach76/cis-235-blog/main/assets/images/ciu-wsi-desktop.png" title="WebSpeed Insights' Analysis of CanIUse.com (Desktop)" style="width:100%;" alt="A graphic depicting WebSpeed Insight's Analysis of CanIUse.com on Desktop Browsers">
<figcaption>WebSpeed Insight&rsquo;s Analysis of CanIUse.com on Desktop Browsers</figcaption>
</figure>
<figure>
<img src="https://raw.githubusercontent.com/sebastiantbach76/cis-235-blog/main/assets/images/ciu-wsi-mobile.png" title="WebSpeed Insights' Analysis of CanIUse.com (Mobile)" style="width:100%;" alt="A graphic depicting WebSpeed Insight's Analysis of CanIUse.com on Mobile Browsers">
<figcaption>WebSpeed Insight&rsquo;s Analysis of CanIUse.com on Mobile Browsers</figcaption>
</figure><br />


<div class="sitetitle">

<h2>MDN (Mozilla Developer Network) Web Docs &#128279;</h2>

URL: <a href="https://developer.mozilla.org/en-US/" target="_blank">https://developer.mozilla.org/en-US/</a>

</div>

<img src="https://raw.githubusercontent.com/sebastiantbach76/cis-235-blog/main/assets/images/mdnwebdocs_header.png" title="MDN Web Docs" style="width:100%;" class="siteheader" alt="A graphic depicting the header of the developer.mozilla.org website.">





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

</style>
