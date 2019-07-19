---
# Documentation: https://sourcethemes.com/academic/docs/managing-content/

title: "Chomper"
summary: ""
authors: []
tags: ["Open Source"]
categories: []
date: 2019-07-18

# Optional external URL for project (replaces project detail page).
external_link: ""

# Featured image
# To use, add an image named `featured.jpg/png` to your page's folder.
# Focal points: Smart, Center, TopLeft, Top, TopRight, Left, Right, BottomLeft, Bottom, BottomRight.
image:
  caption: ""
  focal_point: ""
  preview_only: false

# Custom links (optional).
#   Uncomment and edit lines below to show custom links.
# links:
# - name: Follow
#   url: https://twitter.com
#   icon_pack: fab
#   icon: twitter

url_code: ""
url_pdf: ""
url_slides: ""
url_video: ""

# Slides (optional).
#   Associate this project with Markdown slides.
#   Simply enter your slide deck's filename without extension.
#   E.g. `slides = "example-slides"` references `content/slides/example-slides.md`.
#   Otherwise, set `slides = ""`.
slides: ""
profile: false
---

## Download

This is an open-source project hosted on [Github](https://github.com/aniketpanjwani/chomper). I discussed the project on [FLOSS Weekly](https://twit.tv/shows/floss-weekly/episodes/481).

## Description/Motivation

Many people in the digital era struggle with the healthy use of technology. We have a natural, evolutionary pressure to seek out dopamine hits, and technology firms are at the forefront of creating highly addictive feedback loops to take advantage of these biological mechanisms. As a consequence of years of participation in these feedback loops, many of us have found that our ability to concentrate on a task for more than a few minutes has greatly suffered.

Internet blockers are a useful tool to interrupt the cycle of going to a website (e.g. Facebook/Reddit), and getting a dopamine hit. They work by preventing access to a set of websites (i.e. a blacklist), and sometimes also have a functionality to only allow access to a set of websites (i.e. a whitelist). For many years, there have existed internet blockers for MacOS and Windows, but no Internet blocker for Linux.[^1]

So, I created Chomper - the first Internet blocker for Linux. It has both a "blacklist" and "whitelist" functionality. Additionally, typical Internet blockers are very easy to override. Simply uninstall or close the program, and you have full Internet use restored. Because of the flexibility of Linux, Chomper, can be relatively easily configured so that it becomes impossible to override an Internet block.

[^1]: There are browser-based Internet blockers which work for Linux, but I don't consider these, because you could always just use a different browser. They are also easy to disable, just like any other browser extension, and usually they are not enabled in Private/Incognito mode.
