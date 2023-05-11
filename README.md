# rmacc-hpc-symposium-2023

This repository is an accompaniment to my poster submission to the 2023 RMACC HPC Symposium entitled  "Recommended Libraries for Cyberinfrastructure Users Developing Jupyter Notebooks". This repo contains information about Jupyter Widgets and how they can be used to develop interactive workflows, data dashboards, and web applications that can be run on HPC systems and science gateways. Easy to build web applications are not only useful for scientists. They can also be used by software engineers and system admins who want to quickly create tools tools for file management and more!

> Abstract: Researchers are increasingly interested in using Jupyter Notebooks on HPC clusters, science gateways, and compostable platforms. In addition to using notebooks for scientific workflows, developers can use interactive browser controls, called widgets, to allow users to more easily interact with data and without editing code. In addition to simple widgets, such as sliders, checkboxes, and text inputs, more advanced features can be used to build standalone data dashboards and web applications. Many of these widgets and data visualizations are domain independent, though users may discover them in an ad hoc fashion, which can cause an onslaught of tickets to request particular libraries. To avoid frustration faced by users and system administrators alike, we present a recommended environment for scientists and research software engineers developing Jupyter Notebook on cyberinfrastructure platforms.

## Background

We have used  notebooks to build...
- Scientific workflows
- Training materials
- Data dashboards
- Web applications
- Data management tools

We have built several web applications intended to run on…
- HPC clusters
  - Open OnDemand
- composable platforms
  - Docker containers
- science gateways
- JupyterHub

## Problem

We had to continually submit tickets to system admins as we discovered new libraries.

## Solution

The [environment.yml](https://github.com/nicole-brewer/rmacc-hpc-symposium-2023/blob/main/environment.yml) file in this repository includes a curated set of recommendations for system administrators. This list contains only the most widely-use libraries (in my estimation). My repository [awesome-jupyter-widgets](https://github.com/nicole-brewer/awesome-jupyter-widgets) contains a more extensive list of Jupyter Widgets for scientists and software engineers.

## Current Work

- list of awesome Jupyter widgets
- scientific web application template
- tutorial for managing increasing complexity of workflows and web applications in Jupyter notebooks

## Future Work

- cookbook for building data dashboards and scientific web apps
- further reporting on benefits and drawbacks of different libraries for different scientific use-cases
