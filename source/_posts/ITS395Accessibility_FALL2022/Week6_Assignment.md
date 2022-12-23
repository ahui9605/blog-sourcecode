---
title: ITS395 Week6
date: October 9, 2022
tags:
  - Articles
  - Accessibility
categories: Accessibility Research

#阅读模式，右下角开启
readmode: true

#封面
cover: https://www.umaryland.edu/media/umb/cpa/accessibility/web-accessibility-page/accessibility.jpg

#版权
copyright_author: Zehui Liu
copyright_url: https://ahui9605.github.io/

description: ITS 395 Fall 2022 Week6
---

- 6.1 Describe the features of an accessible website (C?)
- 6.2 Describe how the web browser supports web accessibility (C?)

It is contingent on the website itself wanting what kind of accessibility, the WCAG2.1 showed numerous accessibility elements and allowed developers to design following them, but the type of accessibility desired is dependent on the website itself. However, it appears unfeasible to allow every website to have the same accessibility characteristics as those stated in WCAG2.1. Therefore, some of the content on the website needs to contain the basic elements of use for persons with disabilities, whether those disabilities involve the senses, the mind, or the body.

It is a standard procedure, and it is also one of the easiest methods, to provide alternative text for individuals who are visually impaired. Some of the images that are used for decoration on the website may be excluded by hiding them using CSS code. Since these images are only used for decoration, removing them will result in a slight shift in the visual presentation, but the text content itself will not change. CSS can use it as:

{% codeblock lang:CSS %}
.classname{display:none;}
{% endcodeblock %}

The name that is assigned from an HTML text is called {% label .classname blue %}, and it can be used to name any photos or material.

{% label display:none blue %} is used to hide the image in the browser; however, the content itself continues to exist and is saved in the HTML and CSS file. This material can be revealed at any moment by changing the layout's none property to either {% label block blue %}, {% label inline blue %}.

the following additional essential images are required to accompany the alt text:

{% codeblock lang:HTML %}
<img src="presentation.jpg" alt=" A google slide has the topic named Presentation written in the middle of the slide and an author's name John Doe in the bottom left corner of the slide.">
{% endcodeblock %}

This needs to be very particular and describe as much as is reasonably possible, and then convert those pictures into plain words to describe the vivid picture as best as possible without adding a lot of extra characters or effort.

Users who are colorblind have a requirement for the addition of high contrast and color; browser extensions provide the tools necessary to force the website backdrop or any sensitive color to the color that works best for you. Alternately, we can achieve it by adjusting the colors as necessary through the use of CSS. PSA offered developers with visual examples of what doing this for colorblind people looks like and also include the WCAG2.1 result so that developers can determine whether or not a photo or image is suitable for colorblind users.

Adjusting the font size and ensuring that the layout is well-fitted in the browser on both the computer and the mobile phone are also important for those individuals who have difficulty reading. These individuals find it difficult to keep track of what the content is about, and they require being in a concise place in order to follow the follow of the content because there is a lack of whitespace and clear linear pathways. To remedy this problem, we should steer clear of any repetitive or redundant texts and decorations as well as slash line reading text and information. Additionally, we should strive to be more straightforward, and we should alter the font text size appropriately.
