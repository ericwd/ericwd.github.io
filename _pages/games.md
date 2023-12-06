---
title: "Game Development"
permalink: /games 
date: 2023-12-04 # Says "updated on DATE" in footer
#classes: wide
toc: true


# single image galleries
gallery:
  - url: /assets/images/astro/gallery/2023-07-29-Veil-21hr.jpg
    image_path: /assets/images/astro/gallery/2023-07-29-Veil-21hr-thumb.jpg
    title: Veil Nebula

---
<!-- Page title shows here, left aligned, defined in front matter -->
<hr>

# Summary

Using the Unity ML Agents Toolkit, a neural network was trained to control a charater who gathers donuts as quickly as possible while avoiding spikes. 

For details on this package see the [official Unity documentation](https://github.com/Unity-Technologies/ml-agents).

To view the C# code I wrote to control the agent and environment see my [unity-ml-agent donut-collector](https://github.com/ericwd/unity-ml-agents-donut-collector/tree/main/Assets/Pacman/Scripts) repo.

{% include figure image_path="/assets/images/games/unity-ml-agents-donut-collector/ml-agents-01.png" caption="An agent encountering their first Blender donut and spike box." %}

# Live Demo
<!-- https://www.w3schools.com/tags/tag_iframe.ASP -->
<iframe src="https://ericwd.github.io/unity-ml-agents-donut-collector/Builds/github/index.html" width="1000" height="700" allowfullscreen = true style="border:none;">
</iframe>



# How to Use

This is not a video -- it's interactive and the agent is solving it's environment in real time.

To interact with the WebGL:
1. Click the environment or the fullscreen button to focus the window.
2. Press `<spacebar>` to reset the enironment objects and have the agent begin a new run.


# Details
- **Setting:** A closed environment where agent can move forwards, backwards, and turn.
- **Goal:** Collect all the donuts while avoiding spikes.

## Agent Reward Function
- Donut collision: +10 per collision.
- Spike collision: -100 per collision. Three collisions end the session. 
- Orientation: On each frame, gives (orientation factor * 0.001), where orientation factor is +1 when facing nearest donut and -1 when facing away. Calculated with dot product between vector to donut and forwards vector. Encourages agent to face a donut.
- Nearst donut distance: On each frame, gives -1 when donut is MAX_DISTANCE away, and +0 when close. Encourages agent to move towards nearst donut. 
- Hustle factor: On each frame, gives -1 for standing still and +0 when moving at max speed. Ecourages agent to move quickly.
- Hazard proximity: On each frame, gives -0.1 if a short forwards raycast collides with a hazard. Discourages getting stuck close to spikes.

{% include figure image_path="/assets/images/games/unity-ml-agents-donut-collector/ml-agents-02.png" caption="An agent using raycasts and other input information to learn how to navigate to the goal." %}

## Observations (Input Values)
- Character's forwards vector (x, z components).
- Vector from character to nearest donut (x, z components).
- Distance to nearest donut.
- Five "vision" raycasts in a 180° forwards facing cone. Can detect when a donut or spike is in front or to the sides of the character.

{% include figure image_path="/assets/images/games/unity-ml-agents-donut-collector/ml-agents-03.png" caption="Visualizations for hustle factor (tailing green line), forwards vector (white line), and vector to nearst donut (fronting green line)." %}


## Actions (Output Values)
- Turn: -1 to turn CCW, +1 to turn CW.
- Move: -1 to move backwards, +1 to move forwards.

## Training 
The neural network, observations vector, and reward function have undergone 15 different versions throughout this project. The most recent version, described above, is playing in the game view window. It has been trained for ~ 14M iterations, which took several days of wall time on my machine. 

{% include figure image_path="/assets/images/games/unity-ml-agents-donut-collector/ml-agents-04.png" caption="Cumulative session reward vs training iterations. Certain reward functions allowed agents to gain task proficiency more quickly, while others plateaued earlier." %}


{% include figure image_path="/assets/images/games/unity-ml-agents-donut-collector/ml-agents-05.png" caption="Training was run with 16 instances of each world at 20X the normal Unity game timescale." %}


# Future Development 
Some features I have planned:
- edit environment menu -- make the board more or less harsh by choosing number of donuts and spikes. 
- competition mode -- test your own donut collecting skills against a trained model.