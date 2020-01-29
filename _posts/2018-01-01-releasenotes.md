---
title: "Release notes"
layout: post
permalink: /releasenotes/
thumbnail: "/assets/images/thumbnails/2019-10-feature-image.png"
categories: [Documentation]
---
Examples of release notes projects I worked on at [Quick Base](https://www.quickbase.com){:target="blank"} and [IBM](https://www.ibm.com){:target="blank"}. Samples include monthly blog-style release notes and compilations for major releases.

### Lotus Notes, Domino, and Domino Designer Release Notes
I was the writer, editor, and project manager for this release notes documentation for the IBM Lotus Notes suite of products. This document is the compilation of all the individual release notes entries. Each release note was written in a separate document in a content database application, which facilitated workflow and allowed for micro-consumption of the content as individual pieces, or the assembly of all the content into a complete document.

[![](/assets/images/R5-release-notes.png){: width="300"}](/assets/pdf/R5-release-notes.pdf){:target="blank"}

---

### Quick Base Release Notes
Here are examples of monthly release notes for Quick Base. I tracked all the enhancements and fixes and wrote all the entries. The voice and tone for these release notes are a blend of technical marketing and user guide material.

These samples were assembled in Wordpress and published as part of the company blog:
<div class="postrow">
  <div class="postcolumn">
  <p><b>August 2017</b></p>
  <a href="/assets/pdf/Quick-Base-August-2017-Release-Notes.pdf" target="blank"><img src="/assets/images/aug-17-rn.jpg.png"></a>
  </div>
  <div class="postcolumn">
  <p><b>Feedback form</b></p>
  <a href="/assets/images/feedbackform.png" target="blank"><img src="/assets/images/feedbackform.png"></a>
  </div>
</div>


These samples were assembled in [Madcap Flare](https://www.madcapsoftware.com/products/flare/){:target="blank"} and published as part of the help documentation:




The documentation team was notified about every submission so we could take action. I also would email customers,if they provided contact information, to ask further questions or to tell them we used their suggestions.

A set of feedback emojis appeared at the bottom of each user guide or API guide topic. Choosing an emoji opened a feedback form in a separate browser tab, so that users could provide more information.

<div class="postrow">
  <div class="postcolumn">
  <p><b>Emojis</b></p>
  <a href="/assets/images/feedbacklinks.png" target="blank"><img src="/assets/images/feedbacklinks.png"></a>
  </div>
  <div class="postcolumn">
  <p><b>Feedback form</b></p>
  <a href="/assets/images/feedbackform.png" target="blank"><img src="/assets/images/feedbackform.png"></a>
  </div>
</div>

The code to display the feedback emojis was some simple JavaScript that:
- Displayed the emoji images
- Included links to the feedback form in a Quick Base application
- Captured the page information for inclusion in the feedback document

Sample code:
```html
<p><b>Did this help you? Give us a rating:</b></p>
<p>	<script type="text/javascript">/*<![CDATA[*/
    /*]]>*//*<![CDATA[*/
    var feedbacklink1 = "https://team.quickbase.com/db/bguzysv2w?a=GenNewRecord&_fid_62=1&_fid_14=" + document.location.pathname;
    document.write('<a href=feedbacklink1 onclick="window.open(feedbacklink1); return false;" target="_blank"><img src="images/emo/1.png" height="36px" width="36px" title="Not at all" alt="1 not at all"></a>');
    /*]]>*//*<![CDATA[*/
  /*]]>*/</script>
  &#160;&#160;
  <script type="text/javascript">/*<![CDATA[*/
    /*]]>*//*<![CDATA[*/
    var feedbacklink2 = "https://team.quickbase.com/db/bguzysv2w?a=GenNewRecord&_fid_62=2&_fid_14=" + document.location.pathname;
    document.write('<a href=feedbacklink2 onclick="window.open(feedbacklink2); return false;" target="_blank"><img src="images/emo/2.png" height="36px" width="36px" title="Very little" alt="2 very little"></a>');
    /*]]>*//*<![CDATA[*/
  /*]]>*/</script>
  &#160;&#160;
  <script type="text/javascript">/*<![CDATA[*/
    /*]]>*//*<![CDATA[*/
    var feedbacklink3 = "https://team.quickbase.com/db/bguzysv2w?a=GenNewRecord&_fid_62=3&_fid_14=" + document.location.pathname;
    document.write('<a href=feedbacklink3 onclick="window.open(feedbacklink3); return false;" target="_blank"><img src="images/emo/3.png" height="36px" width="36px" title="Neutral" alt="3 neutral"></a>');
    /*]]>*//*<![CDATA[*/
  /*]]>*/</script>
  &#160;&#160;
  <script type="text/javascript">/*<![CDATA[*/
    /*]]>*//*<![CDATA[*/
    var feedbacklink4 = "https://team.quickbase.com/db/bguzysv2w?a=GenNewRecord&_fid_62=4&_fid_14=" + document.location.pathname;
    document.write('<a href=feedbacklink4 onclick="window.open(feedbacklink4); return false;" target="_blank"><img src="images/emo/4.png" height="36px" width="36px" title="Somewhat" alt="4 somewhat"></a>');
    /*]]>*//*<![CDATA[*/
  /*]]>*/</script>
  &#160;&#160;
  <script type="text/javascript">/*<![CDATA[*/
    /*]]>*//*<![CDATA[*/
    var feedbacklink5 = "https://team.quickbase.com/db/bguzysv2w?a=GenNewRecord&_fid_62=5&_fid_14=" + document.location.pathname;
    document.write('<a href=feedbacklink5 onclick="window.open(feedbacklink5); return false;" target="_blank"><img src="images/emo/5.png" height="36px" width="36px" title="Completely" alt="5 completely"></a>');
    /*]]>*//*<![CDATA[*/
/*]]>*/</script></p>
```

To include the feedback emojis on every page, I added the code to the existing [Madcap Flare](https://www.madcapsoftware.com/products/flare/){:target="blank"} snippet that already appeared on every page, as the footer material:
```html
<MadCap:snippetBlock src="Resources/Snippets/Copyright_and_GA.flsnp" />
```
