---
# Documentation: https://sourcethemes.com/academic/docs/managing-content/

title: "Dynamic Coverage for Active Learning From Equilibrium"
authors: [I. Abraham, A. Prabhakar and T.D. Murphey]
date: 2020-05-13T12:05:31-05:00
doi: ""

# Schedule page publish date (NOT publication's date).
publishDate: 2020-05-13T12:05:31-05:00

# Publication type.
# Legend: 0 = Uncategorized; 1 = Conference paper; 2 = Journal article;
# 3 = Preprint / Working Paper; 4 = Report; 5 = Book; 6 = Book section;
# 7 = Thesis; 8 = Patent
publication_types: ["2"]

# Publication name and optional abbreviated publication name.
publication: "IEEE Transactions on Automation Science and Engineering"
publication_short: "T-ASE"

abstract: "This paper develops KL-Ergodic Exploration from
Equilibrium (KL-E3), a method for robotic systems to integrate stability into actively generating informative measurements through ergodic exploration. Ergodic exploration enables robotic systems to indirectly sample from informative spatial distributions globally, avoiding local optima, and without the need to evaluate the derivatives of the distribution against the robot dynamics. Using hybrid systems theory, we derive a controller that allows a robot to exploit equilibrium policies (i.e., policies that solve a task) while allowing the robot to explore and generate informative data using an ergodic measure that can extend to high-dimensional states. We show that our method is able to maintain Lyapunov attractiveness with respect to the equilibrium task while actively generating data for learning tasks such, as Bayesian optimization, model learning, and off-policy reinforcement learning. In each example, we show that our proposed method is capable of generating an informative distribution of data while synthesizing smooth control signals. We illustrate these examples using simulated systems and provide simplification of our method for real-time online learning in robotic systems."

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

url_pdf:
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
