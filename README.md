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

We had to continually submit tickets to system admins as we discovered new libraries. Many of these libraries are relatively common interactive visualizations and other interactive components called widgets. Here are some examples. The first shows an interactive visualization achieved using Jupyter Widgets (ipywidgets) in conjunction with matplotlib.

![Screen Shot 2023-04-17 at 11 34 06 PM](https://github.com/nicole-brewer/rmacc-hpc-symposium-2023/assets/20686935/7b591bbc-2745-4ade-8cb5-8d37fe0e0d66)

The second shows an HPC usecase where plotly is used to create a visualization to monitor the status of nodes in a cluster.

![IMG_4209](https://github.com/nicole-brewer/rmacc-hpc-symposium-2023/assets/20686935/38913293-460c-4d87-8e6e-7fdb736b9333)

Finally, the following graphic shows a standalone web application made with Voilà. Voilà strips away code cells from Jupyter Notebooks leaving only an interactive user interface. Tools and apps made with  Voilà can be deployed on a variety of systems.

![anova](https://github.com/nicole-brewer/rmacc-hpc-symposium-2023/assets/20686935/587efff1-2286-4d73-a512-f96be11d95ec)

## Solution

The [environment.yml](https://github.com/nicole-brewer/rmacc-hpc-symposium-2023/blob/main/environment.yml) file in this repository includes a curated set of recommendations for system administrators. This list contains only the most widely-use libraries (in my estimation). 
To create this environment with conda, use the command...

```bash
conda create -f environment.yml
```

This environment includes the following libraries:

- libraries for scientific python including numpy, scipy, and pandas
- jupyterlab: preffered user-interface for most users (users not logging in from a preferred remote IDE)
- matplotlib: common static plotting library
- [ipympl](https://github.com/matplotlib/ipympl): enables interactive features for matplotlib
- [plotly](https://plotly.com/python/getting-started/): interactive plotting library
- [ipywidgets](https://ipywidgets.readthedocs.io/en/latest/): Jupyter Widgets: Find a comprehensive list at https://github.com/nicole-brewer/awesome-jupyter-widgets
  - [jupyter-scatter](https://github.com/flekschas/jupyter-scatter): 2D scatter plots that scale to millions of points
  - [ipyleaflet](https://github.com/jupyter-widgets/ipyleaflet): interactive map visualizations
  - [ipycytoscape](https://github.com/cytoscape/ipycytoscape): interactive network visualizations
- [voila](https://github.com/voila-dashboards/voila): turns notebook into standalone application by hiding code cells


To explore more libraries, visit my repository [awesome-jupyter-widgets](https://github.com/nicole-brewer/awesome-jupyter-widgets),
 which contains a more extensive list of Jupyter Widgets for scientists and software engineers.

## Current Work

- [a list of awesome Jupyter widgets](https://github.com/nicole-brewer/awesome-jupytr-widgets)
- [scientific web application template](https://github.com/nicole-brewer/jupyter-web-app-template)
- [a SciPy'23 tutorial](https://github.com/nicole-brewer/scipy23-jupyter-web-app-tutorial) for managing increasing complexity of workflows and web applications in Jupyter notebooks
- hiring and mentoring full time students to experiment an report on their experiences with Jupyter widgets

## Future Work

- cookbook for building data dashboards and scientific web apps
- further reporting on benefits and drawbacks of different libraries for different scientific use-cases

## Acknowledgements

The majority of my experience using Jupyter Notebooks for research applications comes from my time as 
a member of the [Scientific Solutions Group](https://communityhub.purdue.edu/groups/ssg) in Research Computing at Purdue University where I spent 
over three years as research software engineer.
I'd like to thank Carol Song, Rajesh Kalyanam, and Rob Campbell for their continued support of my outreach work in this area.   
I'd also like to thank my co-advisors Manfred Laubichler and Jane Maienschein for their support for my 
continued and extensive participation in the research software engineering and HPC communities. 
Finally, I'd like to thank Jason Yalim from Research Computing at ASU for encouraging me to submit to 
the Symposium and providing me with images of Jupyter widgets used for HPC applications. 

<img width="200" align="left" alt="BSSw-logo" src="https://github.com/nicole-brewer/rmacc-hpc-symposium-2023/assets/20686935/e834056f-7169-4ce8-90ed-24bb878ab993">

This work was supported by the [Better Scientific Software Fellowship Program](https://bssw.io/fellows/nicole-brewer), funded by the Exascale Computing Project (17-SC-20-SC), a collaborative effort of the U.S. Department of Energy (DOE) Office of Science and the National Nuclear Security Administration; and by the National Science Foundation (NSF) under Grant No. 2154495.
Any opinions, findings, and conclusions or recommendations expressed in this material are those of the author(s) and do not necessarily reflect the views of the DOE or NSF.
