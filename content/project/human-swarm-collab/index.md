---
# Documentation: https://sourcethemes.com/academic/docs/managing-content/

title: "Shared Ergodic Control for Flexible Human-Swarm Collaboration under Pressure"
summary: "Developing autonomous ergodic swarm algorithms for human-swarm collaboration under dynamic, time-sensitive constraints"
authors: []
tags: []
categories: []
date: 2019-09-03T12:07:14-05:00

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

People often have to perform a variety of tasks-including search-and-rescue, target location, or exploration and terrain mapping- in unfamiliar environments. Drones deployed in the field with them have the ability to greatly improve their situational and perceptual awareness by providing feedback to aid in their task performance and safety. However, swarm deployment can be complicated, as drones can be difficult for a person to control and operate without greatly increasing their cognitive load, which can make task performance difficult and inefficient. With this in mind, I ask the question: *How can we design a human-swarm system to best accomplish a task under pressure?*

I lead the Northwestern team on the  DARPA FX-3 Urban Swarm Challenge project, exploring this idea. I developed a formulation for swarm control and high-level task planning that is dynamically responsive to
user commands and adaptable to environmental information. I designed an end-to-end pipeline from a tactile tablet interface for user commands to onboard control of robotic agents based on decentralized ergodic coverage. I conducted experiments with a robotic swarm at the DARPA OFFSET FX3 field tests, combining user inputs and task specifications to generate swarm behavior flexible to changing conditions and objectives in real-time. I also developed an experimental VR test bed to validate our approach in a simulation and conduct human subject studies investigating human-robot collaboration under pressure.

{{< video src="rss_2020_submission_small.mp4" controls="yes">}}

## Ergodic Specifications for Flexible Swarm Control and Dynamic Task Adaptation

I use decentralized ergodic control for reliable control of a swarm that is dynamically responsive to user and external inputs. We use ergodicity as a
concept for converting spatially distributed task information into temporally driving robot motion. Because ergodicity relates the time-averaged distribution of a trajectory proportionally to a target spatial distribution, we can use ergodic control to specify how long a single agent should spend time in particular regions of the exploration space.  In particular, we use the decentralized ergodic variation for a networked set of heterogenous agents to drive the swarm control such that it is robust to networking communication issues, changing numbers of agents in the field and evolving information distributions over time.
{{< figure src="usim_crop.gif" width="336" caption="Swarm of Quadrotors covering a Target  ''U'' Spatial Distribution " lightbox="true">}}



Ergodic specifications allow us to flexibly define task allocation and response using spatial distributions. We define each task as a spatial measure over the exploration space that can dynamically update based on user or external inputs. We can combine the different task specifications and user specifications to enable multimodal descriptions of where agents need to be spatially allocated over the workspace. 

{{< figure src="comb_sim.png" title="Simulation of a swarm dynamically adapting to the environment while also responding to user commands. (a) When the swarm discovers a DD, the agents cover the rest of the workspace while avoiding that location. (b) When a user inputs a bimodal distribution (shown as the dark region on the map), the swarm responds to the user commands, while continuing to avoid the DD location. (c) When the swarm finds an EE, it simultaneously converges on the EE, covers the user inputs, and avoids the DD location.  (d) shows the resulting target distribution for the combined tasks." lightbox="true" >}}

When defining task specifications for field missions (at the DARPA FX3 Field testing), we focus on two main scenarios: reallocating priority to a given region when an easter egg (EE) is discovered and generating a region of avoidance
if a disabling device (DD) is discovered. The location of these elements is represented in the specification by parametrizing the distribution as a multimodal sum of Gaussians to generate high importance regions where there is an EE and low regions (avoidance regions) where there is a DD. 

{{< figure src="tanvas_pic_cropped.png" title="The Tanvas tactile tablet allows the operator to communicate their preferences for coverage to the swarm." lightbox="true" >}}

User inputs are incorporated through a tablet interface we developed for communicating regions of interest by the user to a swarm in realtime using the TanvasTouch monitor. Using the TanvasTouch, the user can specify regions of exploratory interest by simply shading the regions of interest on the TanvasTouch. The tablet interface transmits a set of desired points on the workspace for the swarm to prioritize and the spatial distribution is generated by assigning the highest priority value at each of those points in a discretized workspace. The user-specified distribution is combined  with the task-based distribution to generate swarm control that is dynamically responsive to both task updates and user inputs.



## Experimental Systems

### Robotic Swarm at DARPA OFFSET Field Tests

The decentralized swarm control was tested on a swarm of 4 Aion Robotics R1 rovers at the DARPA OFFSET Sprint 3 field tests. Motion planning for each rover used the decentralized ergodic planner wrapped around an RT-RRT* planner for real-time path planning and local obstacle avoidance. The rovers communicated over a local LTE network using a Java interface to share information.

{{< video src="rover_urbanexplr.mp4" controls="yes">}}

We conducted field tests on an urban range, where we successfully deployed a swarm of ground rovers to explore a target region. The ergodic algorithm in conjunction with the RT-RRT* planner enabled exploration of the region (including the interior of a building) without any need for mode switching between indoor and outdoor exploration. 


### Virtual Reality System for Human-Subject Studies

We developed an experimental urban environment testbed using the Unity game engine and using an HTC Vive for controlling operator movement inside the virtual reality environment. As the operator moved within the VR environment, a swarm of simulated quadrotors running the ergodic swarm algorithm provided assisstane to the operator in real time.The swarm's behavior was governed by ergodic task specifications as described above, as well as using the TanvasTouch haptic interface to send commands for desired areas of explorations to the swarm.

{{< figure src="vr_system_architecture" width="336" caption="Experimental VR Urban Environment Testbed for User Studies on Shared Control " lightbox="true">}}

The VR environment was used to validate the full system architecture of the shared ergodic formulation with multiple two-way communication channels. In addition, we have conducted user studies using this testbed to analyze the impact of the shared ergodic swarm control approach compared to standard methods and analyzes the effects of different ergodic specifications within our framework on task performance under dynamic, time-sensitive constraints. 

