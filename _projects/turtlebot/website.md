---
layout: project
title: This Website
permalink: /projects/website
subtitle: 
rollover-text:
project-type: engineering
project-priority: 2
cover-img: W_0_sm.png
images:
 - image_path: /projects/website/W_0.png

---

I put this website together for two primary reasons: 1) to learn the rudiments of HTML/CSS development, and 2) to move my web presence/portfolio from the Swarthmore College Computing Society (SCCS) Wordpress instance to something a little more grown-up and robust. After my third time begging an undergraduate sysadmin to re-activate the SCCS instance so that I could continue hosting my site there as the instance's sole user, it was abundantly clear that it was time to move on. So I turned to GitHub's excellent [Pages system](https://pages.github.com/), which lets you host a static website on GitHub servers.

I'd already built a GitHub Page for Avery and my wedding in 2017, so I understood the rudiments of how to get a simple site up and running. However, I wanted to replicate more of my Wordpress site's functionality, including orienting the site around projects, but also providing basic blogging functionality. I wanted to continue to rely on the basics of Bootstrap that I'd picked up with my previous site, but was also intrigued by the capabilities of the [Jekyll](https://jekyllrb.com/) system that GitHub Pages uses. After a fair amount of poking around, I found a few different sites that provided inspiration and, in some cases, base code for my site:
- Noah MacMillan's [portfolio site](http://noahmacmillan.com/). I really liked the column & grid layout that Noah put together - I've parroted it on my site, albeit in a much less elegant fashion.
- Andrew Fong's [Hydeout theme](https://github.com/fongandrew/hydeout) for Jekyll.
- The Development's [Flex theme](https://github.com/the-development/flex)
- ExchangeRate-API's [rlstevenson theme](https://github.com/ExchangeRate-API/rlstevenson-jekyll-theme). This was my most important discovery - a Jekyll theme that used Bootstrap and could be modified to fit the column-and-grid layout I was looking for. I built my site around this code, and I'm very grateful to the author for making this theme available.

I had to modify the rlstevenson theme in a few important ways before I could get it to work for my purposes. I added the project grid to the main page, and incorporated the concept of "projects" to the site structure - pages that exist in their own directories, which auto-populate the project grid. I also made the site more mobile-friendly, taking advantage of Bootstrap's built-in capabilities to make the site snap between mobile and standard layouts. Finally, I added a new skin (which, in retrospect, looks a lot like the skin for our wedding website...) There is still a _lot_ of work to be done: I need to port over more content from my old website, add commenting, add analytics, make the grid work more cleanly, etc. But for now, I'm pretty happy with it.

Do you like my website? Would you like one of your own? Great news - you can have one too! My modified theme, which I've creatively called rlstevenson-mod, is available [on my GitHub](https://github.com/JulianLelandBell/rlstevenson_mod) under the MIT license. All I ask is that if you find something I've screwed up, or add some nice feature you think would be useful, please tell me about it! 



