# altius docs


It's a simple and responsive Hugo theme built using Bootstrap and Javascript from start to finish.



If you want to use your own images for the carousel, you should specify image link in the markup of your post.



For example:



title: "Bootstrap karuselė Blogspot tinklaraščiui"
date: 2021-02-02T19:02:00+02:00
draft: false
tags: [newpost,bootstrap,carousel,for,blogspot,blog]
image: "image.png"

This is an example from an existing post. 



The template supports tags also. 



## Code editing



I made everything as simple as it was possible. You don't need to dig around all the time to make some changes. Just edit the partials. If you want facebook plugins and other features to work, just add the scripts that belong to you.



## PWA compatible



It is totally PWA ready and once published lets users to install it as an app. Isn't that cool?



## Service worker



It has a service worker script which helps to cache the resources used. It might cause some issues at the development environment, because you wont be able to see the changes from the first time even if you use -disableFastRender flag. Just disable the service worker on your browser.



## Responsive



It's mobile and pc friendly. One template to rule them all.



## Special parameters 



You don't need to actually worry about it. I'll add an example here.



baseURL = "https://www.nerdy.lt/"
languageCode = "en-us"
title = "Nerdy.lt"
theme = "altius"

DefaultContentLanguage = "en"
SectionPagesMenu = "main"
Paginate = 12 
googleAnalytics = ""
enableRobotsTXT = true
enableEmoji = true
disableKinds = ["taxonomy", "taxonomyTerm"]
summaryLength = 150

[author]
    name = "Nerdy Altius"
    email = ""

[params]
  favicon = "https://lh3.googleusercontent.com/-YCP7iCHdwf0/X6egYpNGYWI/AAAAAAAAE4o/pc-ILMmzG8g3KRUA2stRmw0rnv86okZiwCLcBGAsYHQ/s80/512.png"
  site_logo = "https://lh3.googleusercontent.com/-YCP7iCHdwf0/X6egYpNGYWI/AAAAAAAAE4o/pc-ILMmzG8g3KRUA2stRmw0rnv86okZiwCLcBGAsYHQ/s80/512.png"
  description = "AltiusDay antras tinklarastis | Programinis kodas | Ismaniuju irenginiu konfiguracija | Pravarcios pamokos ir dar daug visko"
  facebook = "https://www.facebook.com/altiusday"
  twitter = "https://twitter.com/AltiusDay"
  instagram = "https://www.instagram.com/_andrius_p_/"
  youtube = ""
  github = ""
  gitlab = ""
  linkedin = ""
  mastodon = ""
  slack = ""
  stackoverflow = ""
  rss = "https://nerdy.lt/sitemap.xml"
  background_color_class = "bg-white"
  featured_image = "/connection.jpg"
  recent_posts_number = 12
  post_navigation = true
  ogimage = "/connection.jpg"
  imgalt="altiusimage"

[taxonomies]
   tag = "tags"



## CSS



I made override.css file to make some improvements here and there. Upload it to your /static/ directory. 



## Let's talk about the images and where exactly to put them



Just upload new images to static directory. Try to use as light-weight images as you can. But keep in mind that they might appear on screen sizes. So use the big ones in pixels and tiny ones in size.



## SEO



I measured the site on Google's Lighthouse and it gave 100 out of 100 score. altius is not the fastest template around, but it sure is one of the most SEO friendly. 



## Disabling and enabling partials



I use all of the available partials, but I was way too lazy to make enable and disable parameters. So you'll have to:



1. Create these definitions yourselves
2. Use the partials
3. Or just delete the inner content of the partial you won't use



## Search



It was implemented using pure Javascript and XML parsing. It's a dumb search engine just to prove that it's possible to make some interesting things when you trully want to. It scans your generated sitemap.xml file and displays some results if a given word matches the same word on a post. But you don't need to worry about the little thingies I made it to work. Just copy and paste the search directory into the /content/ of yours.



## It's MIT



Use it for your own fun. Build it, break it or reimagine the whole concept. Try to make something wonderful out of this theme. It's totally yours now.



## Contacts



If you ever wondered how to contact me, just write an email to andrius@artefaktas.eu and I'll answer
