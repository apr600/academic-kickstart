---
# Documentation: https://sourcethemes.com/academic/docs/managing-content/

title: "Learning Information-based Task Representations"
summary: ""
authors: []
tags: []
categories: []
date: 2019-09-03T12:04:05-05:00

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
---

People are extraordinarly good at crafting representations of tasks that takes into account the motion information necessary for successful task performance and filtering out the variable, extraneous motions from a single task execution. However, it can be difficult to construct similarly robust representations for robotics that can also be used to generate control signals for successful task performance. I use **distribution-based representations and information-theoretic measures to both represent the task information and generate motions that successfully accomplish the task** using standard model predictive control methods.

## Robotic Visual Rendering using Information-Theoretic Methods

Drawing is a classic example of tasks where the motions are used to successfully accomplish the task of communicating information. It falls into a unique subset of tasks where the motion is simultaneously essential for accomplishing the task, but there are many motion trajectories that can successfully accomplish it--- people may draw the same image completely different, but they ultimately result in the same image. I wanted to give the same level of robustness and generality to a robot's task performance.

To do this, I represent the task as the distribution over the state space representing the relevant task state information. By representing the task as an information distribution, the definition can be abstracted away from the specific motion trajectories. This representation naturally accommodates uncertainty due to trajectory variability and multiple task solutions. Using this representation, I use an information-based metric **ergodicity** to define an objective function with model-based predictive control to generate controls that successfully accomplishes the task with the most efficient motion, given the system dynamics and initial conditions.


## Learning from Variable, Imperfect Demonstrations using Ergodic Control

As robots become more ubiquitous in every day life, they will be interacting with people more and will need to learn from them. At the same time, as regular people are required to teach robots to perform more challenging tasks and provide demonstrations for complicated robotic systems that they may be unfamiliar with, they may provide demonstrations that are non-optimal or even unsuccessful. *How do we allow robots to learn a task representation from a set of human demonstrations that 1) can encompass varied solutions to the same task, and, perhaps more importantly, 2) can still generate optimal solutions from a set of imperfect demonstrations from a non-expert user?*

Here, I continue exploring the idea of representing the set of demonstrations as an information distribution over the task space. By considering each demonstration as adding information about the task, we can consider imperfect, and even unsuccessful, demonstrations as still adding valuable information about the task to the representation. As such, a set of imperfect demonstrations can collectively create a task representation from which we can generate controls for optimal task performance. Furthermore, this representation allows more flexibility in the demonstration set, allowing for multiple solution sets for the same task. By representing the task as information over the task space, multiple solutions can emerge from a demonstration set and variations that are irrelevant to task success will naturally be averaged out.

### LfD for Area Coverage Tasks

Consider a standard task such as cleaning a particular surface. In general, the specific motions and sequential order of task space visited does not matter to success. Instead, viewing the task as an *area coverage* over the task space, reflects this flexibility-- while also capturing specific regions that may require more time spent, such as around stovetops or corners.



### LfD for Dynamic Tasks

Even for more dynamically challenging tasks, such as the cart-pendulum inversion problem, this representation allows for successful controls. The cart-pendulum inversion problem is a classic problem that can be extremely challenging for people to demonstrate, due to the complicated dynamics of the system and the instability at the desired upright state. As such, a set of demonstrations from human demonstrators, especially non-expert ones, are highly imperfect, and rarely successfully stabilize in the upright position. 