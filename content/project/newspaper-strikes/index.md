---
# Documentation: https://sourcethemes.com/academic/docs/managing-content/

title: "Technological Change in the American Newspaper Industry: 1960 - 1976"
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

You can download this paper [here](https://aniketpanjwani.com/file/newspaper-technology.pdf)

## Summary

Technological diffusion is often complex, slow and poorly understood. Technical superiority need not induce adoption on its own: researchers have also highlighted the role of competition, labor costs, unionization and more. This paper brings additional empirical evidence to bear on the determinants of technological diffusion and its consequences. We study the adoption of three technological innovations in the American newspaper industry in the 1960s and 1970s: phototypesetters, computers and offset printing. 

Phototypesetters helped compositors arrange the text for a page through the use of photography. They displaced linecasters, which newspapers had used since the 1880s. Computers augmented compositors’ productivity by automating justification and hyphenation. Offset printing substituted photolithography for letterpress. It was the biggest innovation in newspaper printing since the advent of the rotary press in the 1840s. Although it was more expensive than letterpress, it yielded neater copy and had complementarities with phototypesetting.

In this paper, we ask the following questions: what are the determinants of adoption of the three technologies, what is their impact on employment, and what is their impact on newspapers’ output? To answer these questions, we combine data on newspapers, their printing technology and their typesetting equipment from Editor & Publisher’s International Year Books with data on union membership and strike incidence from the yearly accounts of the International Typographical Union (ITU). We use these data to run descriptive regressions in which we control for observable characteristics of newspapers to make inferences about what drove technology adoption.

Our main findings are that:

1. Offset printing is associated with a 10% decrease in ITU journeymen employment.
2. Adoption of each technology (phototypesetters/computers/offset printing) increased circulation 3 - 4%
3. Unionization is negatively associated with technology adoption, but strikes are positively associated with technology adoption, indicating that strikes may have been the ITU's weapon of last resort.
4. Chained newspapers are more likely to adopt offset printing than independent ones by six percentage points, but no more likely to adopt phototypesetting or computers.[^1]

## Tools/Techniques Used

+ I use Python to process raw data digitized from newspaper yearbooks on newspaper technology. As an example, a typical example of the data on newspaper technology looks like this:

'''
Tapesetters 4AKI-Autofape; Teletype Setters- 4AKI; Cold Type &Photo Comp 2COM-2961 HS, 1COM-4961, 1COM-ACM-9000; 1COM-IV, JCOM-7200,: OCR Equipment 1 COM. PLATE","2C0M-2961, 2CD-4961
'''

+ Processed data of the above form is stored in a PostgreSQL database on AWS RDS.
+ Regression models are estimated using STATA.

[^1]:  Offset presses were large, one-time expenses for newspapers, while photocomposers and computers could be introduced gradually with little initial expense, so this result may reflect newspaper chains’ greater ability to finance purchases of expensive offset presses.
