---
# Documentation: https://sourcethemes.com/academic/docs/managing-content/

title: "Ergodic Exploration using Binary Sensing for Non-Parametric Shape Estimation"
authors: [I. Abraham, A. Prabhakar, and T.D. Murphey]
date: "2017-09-01"
doi: ""

# Schedule page publish date (NOT publication's date).
publishDate: "2017-09-01"

# Publication type.
# Legend: 0 = Uncategorized; 1 = Conference paper; 2 = Journal article;
# 3 = Preprint / Working Paper; 4 = Report; 5 = Book; 6 = Book section;
# 7 = Thesis; 8 = Patent
publication_types: ["2"]

# Publication name and optional abbreviated publication name.
publication: "IEEE Robotics and Automation Letters"
publication_short: "R-AL"

abstract: "Current methods to estimate object shape—using
either vision or touch—generally depend on high-resolution
sensing. Here, we exploit ergodic exploration to demonstrate
successful shape estimation when using a low-resolution binary
contact sensor. The measurement model is posed as a collisionbased tactile measurement, and classification methods are used
to discriminate between shape boundary regions in the search
space. Posterior likelihood estimates of the measurement model
help the system actively seek out regions where the binary sensor
is most likely to return informative measurements. Results show
successful shape estimation of various objects as well as the ability
to identify multiple objects in an environment. Interestingly, it
is shown that ergodic exploration utilizes non-contact motion
to gather significant information about shape. The algorithm is
extended in three dimensions in simulation and we present two
dimensional experimental results using the Rethink Baxter robot."

# Summary. An optional shortened abstract.
summary: ""

tags: []
categories: []
featured: false

# Custom links (optional).
#   Uncomment and edit lines below to show custom links.
# links:
# - name: Follow
#   url: https://twitter.com
#   icon_pack: fab
#   icon: twitter

url_pdf: https://murpheylab.github.io/pdfs/2017RALAbPrHaMu.pdf
url_code:
url_dataset:
url_poster:
url_project: https://murpheylab.github.io/projects/HapticLanguages
url_slides:
url_source:
url_video: https://murpheylab.github.io/videos/2017RALAbPrHaMu.mp4

# Featured image
# To use, add an image named `featured.jpg/png` to your page's folder. 
# Focal points: Smart, Center, TopLeft, Top, TopRight, Left, Right, BottomLeft, Bottom, BottomRight.
image:
  caption: "Shape Estimation using Binary Sensing and Ergodic Exploration"
  focal_point: "Center"
  preview_only: false

# Associated Projects (optional).
#   Associate this publication with one or more of your projects.
#   Simply enter your project's folder or file name without extension.
#   E.g. `internal-project` references `content/project/internal-project/index.md`.
#   Otherwise, set `projects: []`.
projects: [high-dim-learning]

# Slides (optional).
#   Associate this publication with Markdown slides.
#   Simply enter your slide deck's filename without extension.
#   E.g. `slides: "example"` references `content/slides/example/index.md`.
#   Otherwise, set `slides: ""`.
slides: ""
---
