---
title: Test
subtitle: Test
category:
  - About Awake
author: Daniel Kelly
date: 2020-02-29T19:24:13.182Z
featureImage: /uploads/about-hero.jpg
---
framework it's built on (Nuxt.js) as well as includes some intentional optimizations to improve the end user experience when it comes to speed. 

The JAM Stack
The JAM stack is a way of building websites that compile down basically to html, css, and javascript and then is served over a CDN. API's are then sprinkled in to add more advanced functionality where needed. Because there is no server, no computations to run, initial response time is like lightening. 

Nuxt.js
﻿Nuxt.js has the ability to generate static sites that are served on the JAM Stack, building plain old html files... but those html files are super-powered with Vue.js. What this means, is that pages have content "hard coded" into the html files for top-rate SEO scores but after initial page load behave as a traditional SPA with smooth page transitions, minimal data served between requests, etc. This means Awake is fast both on both the first page visitors hit and even faster on subsequent pages.

Purge CSS
Awake uses the Bulma framework for a starting place for styles but certainly doesn't use every style the Bulma framework provides. Purge CSS minimizes the css sent to the browser by removing any unused styles at compile time. You can read more about how Awake uses Purge CSS in this post.

Opti-Image + Responsive Loader
﻿Opti-Image is a little vue component I wrote to be able to serve images in the most performant way possible. It supports webp's for browser's that support it (though not using the webp functionality for Awake, yet...), lazy loading out of the box, and easy srcset management. Responsive Loader (the Nuxt Flavor) auto optimizes image quality for best performance in the browser and creates multiple sizes for different devices. Combine these 2 together and all image on Awake are basically guaranteed to fly. 

Font Awesome 5
Awake comes with Font Awesome 5 support out of the box, so you have a wealth of free quality icons at your finger tips. However, if you're used to using Font Awesome in the more traditional manner without a build step you may be thinking: "What about all those icons I don't actually use? Aren't they just bloat?" Not so with Awake, with webpack we can bundle only the icons we're using. This does mean an extra step of registering a new icon when you want to use it, but that's as easy as adding it to an array in config/modules.js like so: 

﻿
