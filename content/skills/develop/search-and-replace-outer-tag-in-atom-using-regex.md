---
title: "Search and Replace Outer Tag in Atom Using Regex"
date: 2020-03-19T10:40:29+08:00
url: /skills/search-and-replace-outer-tag-in-atom-using-regex.html
type: "skills"
image: "https://cdn.jsdelivr.net/gh/Rhinocros/minorpatch-static@pics/uPic/wTzf3q.jpg"
categories:
  - "Develop Tools"
tags:
  - Atom
  - HTML
  - solution
  - replaced result
keywords:
- Atom
- HTML
- solution
- replaced result
description: "Using Atom, I'm trying to replace the outer tag structure for multiple different texts within a document. Also using REGEX, which I'm not versed enough to come up with my own solution"
comments: true
---


Using Atom, I'm trying to replace the outer tag structure for multiple different texts within a document. Also using REGEX, which I'm not versed enough to come up with my own solution

HTML to be searched `<span class="klass">Any text string</span>`

Replace it with `<code>Any text string</code>`

My REGEX `(<?span class="klass">)+[\w]+(<?/span>)`

Is there a wildcard to "keep" the `[\w]` part into the replaced result?


<br/>
<br/>
<script async src="https://pagead2.googlesyndication.com/pagead/js/adsbygoogle.js"></script>
<ins class="adsbygoogle"
     style="display:block; text-align:center;"
     data-ad-layout="in-article"
     data-ad-format="fluid"
     data-ad-client="ca-pub-8746275014476192"
     data-ad-slot="5144997159"></ins>
<script>
     (adsbygoogle = window.adsbygoogle || []).push({});
</script>
<br/>
<br/>


You can use a capture group to capture the text in between the `<span>` tags during the match, and then use it to build the `<code>` output you want. Try the following find and replace:

Find:

`<span class="klass">(.*?)</span>`

Replace:

`<code>$1</code>`

Here `$1` represents the quantity `(.*?)` which we captured in the search. One other point, we use `.*?` when capturing between tags as opposed to just `.*` . The former `.*?` is a "lazy" or tempered dot. This tells the engine to stop matching upon hitting the first closing `</span>` tag. Without this, the match would be greedy and would consume as much as possible, ending only with the final `</span>` tag in your text.
