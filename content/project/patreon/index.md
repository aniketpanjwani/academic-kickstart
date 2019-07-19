---
# Documentation: https://sourcethemes.com/academic/docs/managing-content/

title: "Subscription and Advertising Revenue in New Media: Evidence from the Patreon Hack"
summary: ""
authors: []
tags: ["Research"]
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

*07-18-19: Draft available in 2 - 3 weeks.*

## Summary

The media industry is a two-sided market. Typically, when media firms consider what type of content to produce, they must take into consideration both the tastes of consumers and the tastes of advertisers. However, technological constraints may prevent media firms from monetizing the subscription or advertising side of the market. For "old media" (i.e. newspapers, radio, and television), there are no such technological constraints. However, "new media" content creators - such as bloggers, podcasters, and YouTubers - have until recently only been able to easily monetize their content through advertising.

In the last five to ten years, platforms and technologies have been created which allow "new media" content creators to monetize people who consumer their content. In this paper, we study how the introduction of a subscription revenue stream affects online content creators' content creation decisions. To study this, we exploit a natural experiment in the history of Patreon, an online platform which makes it easy for online content creators to collect subscription payments. 

In October 2015, Patreon's database was hacked. Due to privacy concerns, many subscribers of content creators on Patreon cancelled their subscriptions. We treat the revenue loss due to canceled subscriptions as random across creators, and we use the revenue loss in a continuous difference-in-differences model to study how a negative shock to creators' subscription revenue affects their content creation behavior. We focus on YouTube content creators, because they are the largest group of creators on Patreon, and we are easily able to scrape details of their content creation behavior using the [Youtube Data API](https://google.com).

We find that negative subscription shocks

1. **increase** the amount of affiliate links in videos' descriptions.
2. **increase** the amount of brand mentions in videos.
3. **Have no effect** on the "clickbait"-iness of content.

Overall, our findings point at content creators attempting to replace lost subscription revenue with *native advertising*, or advertising disguised as content, but not drastically changing the quality of videos.

## Tools/Techniques Used

This project involves several distinct data collection/data munging tasks.

1. Using the Python *requests* and *BeautifulSoup* packages, I scraped and parsed [Graphtreon](https://graphtreon.com), a website which tracks Patreon creators, and their subscriber counts.
2. Using the Youtube Data API v3, I acquired all videos of a sample of Patreon video creators, the automatically-generated captions of those videos, and various other measures describing the videos (e.g. likes and dislikes).
3. I stored the captions in an AWS S3 Bucket. I stored all information about Patreon creators and their videos in a PostgreSQL database hosted on AWS RDS.
4. I used *nltk* to parse videos' captions before creating count measures of brand mentions in videos.
5. I used *scikit-learn* to implement a Naive Bayes model which predicts from a video's title whether a video is "clickbait".
6. We use STATA and R to construct descriptive statistics, tables, and estimate the difference-in-differences models.

