---
# Documentation: https://sourcethemes.com/academic/docs/managing-content/

title: "Active Area Coverage from Equilibrium"
authors: [I. Abraham, A. Prabhakar and T.D. Murphey]
date: "2018-07-01"
doi: ""

# Schedule page publish date (NOT publication's date).
publishDate: 2018-07-01

# Publication type.
# Legend: 0 = Uncategorized; 1 = Conference paper; 2 = Journal article;
# 3 = Preprint / Working Paper; 4 = Report; 5 = Book; 6 = Book section;
# 7 = Thesis; 8 = Patent
publication_types: ["1"]

# Publication name and optional abbreviated publication name.
publication: "Workshop on the Algorithmic Foundations in Robotics"
publication_short: "WAFR"

abstract: "This paper develops a method for robots to integrate stability into actively seeking out informative measurements through coverage. We derive a controller using hybrid systems theory that allows us to
consider safe equilibrium policies during active data collection. We show that our method is able to maintain Lyapunov attractiveness while still actively seeking out data. Using incremental sparse Gaussian processes, we define distributions which allow a robot to actively seek out informative measurements. We illustrate our methods for shape estimation
using a cart double pendulum, dynamic model learning of a hovering
quadrotor, and generating galloping gaits starting from stationary equilibrium by learning a dynamics model for the half-cheetah system from
the Roboschool environment."

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

url_pdf: https://murpheylab.github.io/pdfs/2018WAFRAbPrMu.pdf
url_code: https://github.com/i-abr/kle3
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
  caption: "Robot sampling a state space (for Bayesian optimization) while taking into account dynamic constraints (keeping the cart double pendulum inverted)."
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
