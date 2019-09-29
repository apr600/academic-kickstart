---
# Documentation: https://sourcethemes.com/academic/docs/managing-content/

title: "Symplectic Integration for Optimal Ergodic Control"
authors: [A. Prabhakar, K. Flaskamp, and T.D. Murphey]
date: "2015-12-15"
doi: ""

# Schedule page publish date (NOT publication's date).
publishDate: ""

# Publication type.
# Legend: 0 = Uncategorized; 1 = Conference paper; 2 = Journal article;
# 3 = Preprint / Working Paper; 4 = Report; 5 = Book; 6 = Book section;
# 7 = Thesis; 8 = Patent
publication_types: ["1"]

# Publication name and optional abbreviated publication name.
publication: "IEEE Internation Conference on Decision and Control (2015)"
publication_short: "CDC"

abstract: "Autonomous active exploration requires search algorithms that can effectively balance the need for workspace coverage with energetic costs. We present a strategy for planning optimal search trajectories with respect to the distribution of expected information over a workspace. We formulate an iterative optimal control algorithm for general nonlinear dynamics, where the metric for information gain is the difference between the spatial distribution and the statistical representation of the time-averaged trajectory, i.e. ergodicity. Previous work has designed a continuous-time trajectory optimization algorithm. In this paper, we derive two discrete-time iterative trajectory optimization approaches, one based on standard first order discretization and the other using symplectic integration. The discrete-time methods based on first-order discretization techniques are both faster than the continuous-time method in the studied examples. Moreover, we show that even for a simple system, the choice of discretization has a dramatic impact on the resulting control and state trajectories. While the standard discretization method turns unstable, the symplectic method, which is structure-preserving, achieves lower values for the objective."

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

url_pdf: https://murpheylab.github.io/pdfs/2015CDCPrFlMu.pdf
url_code:
url_dataset:
url_poster:
url_project:
url_slides:
url_source:
url_video:

# Featured image
# To use, add an image named `featured.jpg/png` to your page's folder. 
# Focal points: Smart, Center, TopLeft, Top, TopRight, Left, Right, BottomLeft, Bottom, BottomRight.
image:
  caption: ""
  focal_point: ""
  preview_only: false

# Associated Projects (optional).
#   Associate this publication with one or more of your projects.
#   Simply enter your project's folder or file name without extension.
#   E.g. `internal-project` references `content/project/internal-project/index.md`.
#   Otherwise, set `projects: []`.
projects: []

# Slides (optional).
#   Associate this publication with Markdown slides.
#   Simply enter your slide deck's filename without extension.
#   E.g. `slides: "example"` references `content/slides/example/index.md`.
#   Otherwise, set `slides: ""`.
slides: ""
---
