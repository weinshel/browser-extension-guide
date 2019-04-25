---
title: What are extensions?
has_children: false
nav_order: 1
---

# Background: Web Browsers and Browser Extensions

Extensions are bits of code that modify the functionality of a web browser. They are written using standard web technologies - JavaScript, HTML, and CSS - plus some dedicated JavaScript APIs. Among other things, extensions can add new features to the browser or change the appearance or content of particular websites.

Browser extensions are one of the few things in the tech world that are _close_ to being cross-platform. Most of the major browsers (Chrome, Firefox, Microsoft Edge, Opera)[^1] have standardized (more or less) on the same toolset, which is based on the framework and APIs[^2] first implemented in Google Chrome. Firefox historically had an entirely different framework for add-ons, but recently implemented the toolset used by Chrome and phased out the other add-on formats. Microsoft and Opera have likewise made similar moves in recent years.

With some exceptions, most extensions written originally for Chrome will run unmodified on Firefox, Edge, and Opera. All of the browsers implement (more or less) the same APIs, though there are some differences between the browsers in terms of conventions about how to deal with asynchronous JavaScript. There are various names for what this toolset is called, including “Chrome extensions”, “WebExtensions”, “browser extensions”, and "add-ons" that are marginally different but basically can be used interchangeably. For reasons that we’ll get into later, the conventions used by Firefox WebExtensions are a bit easier to work with, and it’s possible to do things that way and have your extension also work with Chrome and other browsers without any modification.

[^1]: Safari has its own extension toolset, but it has its own set of frameworks and APIs that is a bit different and we won't cover that.

[^2]: Application Programming Interface, basically the set of standards for things like “this is how you ask the browser what the currently open tabs are”

# What can extensions do?

**Enhance or complement a website**: Use an add-on to deliver additional
in-browser features or information from your website. Allow users to
collect details from pages they visit to enhance the service you offer.

![](https://mdn.mozillademos.org/files/15808/Amazon_add_on.png)

Examples: [Amazon Assistant for
Firefox](https://addons.mozilla.org/en-US/firefox/addon/amazon-browser-bar/),
[OneNote Web
Clipper](https://addons.mozilla.org/en-US/firefox/addon/onenote-clipper/),
and [Grammarly for
Firefox](https://addons.mozilla.org/en-US/firefox/addon/grammarly-1/)

**Let users show their personality**: Browser extensions can manipulate
the content of web pages; for example, letting users add their favorite
logo or picture as a background to every page they visit. Extensions may
also enable users to update the look of the Firefox UI, the same way
standalone [theme
add-ons](https://developer.mozilla.org/en-US/Add-ons/Themes/Theme_concepts) do.

![](https://mdn.mozillademos.org/files/15809/MyWeb_New_Tab_add_on.png)

Examples: [MyWeb New
Tab](https://addons.mozilla.org/en-US/firefox/addon/myweb-new-tab/),
[Tabliss](https://addons.mozilla.org/en-US/firefox/addon/tabliss/), and
[VivaldiFox](https://addons.mozilla.org/en-US/firefox/addon/vivaldifox/)

**Add or remove content from web pages**: You might want to help users
block intrusive ads from web pages, provide access to a travel guide
whenever a country or city is mentioned in a web page, or reformat page
content to offer a consistent reading experience. With the ability to
access and update both a page's HTML and CSS, extensions can help users
see the web the way they want to.

![](https://mdn.mozillademos.org/files/15807/ublock_origin_add_on.png)

Examples: [uBlock
Origin](https://addons.mozilla.org/en-US/firefox/addon/ublock-origin/),
[Reader](https://addons.mozilla.org/en-US/firefox/addon/reader/), and
[Toolbox for Google Play
Store™](https://addons.mozilla.org/en-US/firefox/addon/toolbox-google-play-store/)

**Add tools and new browsing features**: Add new features to a
taskboard, or generate QR code images from URLs, hyperlinks, or page
text. With flexible UI options and the power of the [WebExtensions
APIs](/en-US/Add-ons/WebExtensions) you can easily add new features to a
browser. And, you can enhance almost any website's features or
functionality, it doesn\'t have to be your website.

![](https://mdn.mozillademos.org/files/15806/QR_Code_Image_Generator_add_on.png)

Examples: [QR Code Image
Generator](https://addons.mozilla.org/en-US/firefox/addon/qr-code-image-generator/),
[Swimlanes for
Trello](https://addons.mozilla.org/en-US/firefox/addon/swimlanes-for-trello/),
and [Tomato
Clock](https://addons.mozilla.org/en-US/firefox/addon/tomato-clock/)

**Games**: Offer traditional computer games with off-line play features,
or explore new game possibilities; for example, by incorporating
gameplay into everyday browsing.

 ![](https://mdn.mozillademos.org/files/15805/Asteroids_in_Popup_add_on%20.png)

Examples: [Asteroids in
Popup](https://addons.mozilla.org/en-US/firefox/addon/asteroids-in-popup/),
[Solitaire Card Game New
Tab](https://addons.mozilla.org/en-US/firefox/addon/solitaire-card-game-new-tab/),
and [2048
Prime](https://addons.mozilla.org/en-US/firefox/addon/2048-prime/).

**Add development tools**: You may provide web development tools as your
business or have developed a useful technique or approach to web
development that you want to share. Either way, you can enhance the
built-in Firefox developer tools by adding a new tab to the developer
toolbar.

![](https://mdn.mozillademos.org/files/15804/aXe_Developer_Tools_add_on.png)

Examples: [Web
Developer](https://addons.mozilla.org/en-US/firefox/addon/web-developer/),
[Web React Developer
Tools](https://addons.mozilla.org/en-US/firefox/addon/react-devtools/),
and [aXe Developer
Tools](https://addons.mozilla.org/en-US/firefox/addon/axe-devtools/)