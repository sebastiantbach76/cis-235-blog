---
title: "Welcome..."
date: 2022-09-09
---

<h2>...to my blog for CIS 235, Web Programming I!</h2>

I have a confession to make: This isn&rsquo;t your grandparents&rsquo; **HTML** (and, to be honest, my grandparents never heard of **HTML**, which wasn't invented until late in their lives). This blog is actually maintained in **Markdown**, which is a form of simplified markup language that is&mdash;<em>luckily!</em>&mdash;interoperable with **HTML** tags, **&Eta;&Tau;&Mu;L** &#345;&#279;&#349;&egrave;&#x01A6;&#x02123;&#x018F;&#x018C; & &#x01AF;&#x019E;&#x0197;&#x0186;&#x019F;&#x0189;&#x0190; &cent;haracters, and **CSS** housed within &lt;style&gt; tags. For instance, the following copy is responsible for styling the colors of this page&rsquo;s background and text.
<pre>
&lt;style>
body {
    background: peachpuff;
    color: black;
}
...
&lt;/style>
</pre>
One can even include inline graphics. (***Surf, Ferris, surf!***)

<figure>
<img src="https://raw.githubusercontent.com/sebastiantbach76/cis-235-blog/main/assets/images/ferris_surfing.png" title="Ferris surfs the Web!" style="width:500px;">
<figcaption style="text-align: center;">Ferris surfs the World Wide Web! Art Credit: Esther Arzola (2019). Reuse <a href="https://www.behance.net/gallery/89117181/Ferris-the-professional">explicitly permitted by artist</a>.</figcaption>
</figure>

As you probably know, **GitHub.com**, which hosts this blog site in one of my repositories, deploys **Jekyll**, a static site generator written in Ruby, to render **Markdown** as **HTML**. This architecture is responsible for most of the public-facing text you encounter in that site&rsquo;s repositories, and it makes it possible to host a blog site without setting up a database to flesh out the site content. Combining the stripped-down markup of **Markdown** with a sprinkling of **CSS** and a beaker full of **Jekyll** alchemy can lead to rapid drafting and publication of blog posts. In total, from blog site setup to blog post publication, this task probably consumed about 20 minutes of my time.

Other tools I used to construct this site include:
<ul>
<li><strong>IDE:</strong> JetBrains WebStorm</li>
<li><strong>VCS:</strong> Git/GitHub</li>
<li><strong>Static Content:</strong> Gimp</li>
</ul>

That&rsquo;s all for now.  I am off to conduct my search for seven websites to critique...

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

ul li {
  color: black;
}

p {
    background: peachpuff;
    color: black;
    text-align: justify;
    text-justify: inter-word;
    font-family: Times;
    font-size: 16px;
    font-weight: 400;
    line-height: 22px;
}

h1 {
    color: darkblue;
    font-weight: 800;
    font-family: Times;
    font-size: 45px;
}

h2 {
    color: darkblue;
    font-family: Georgia;
    font-style: italic;
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

</style>
