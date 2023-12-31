---
layout: post
title: GitHub Visualizer
description: For a 4-member group project, we created a Windows program that can abstract many Git commands and provide a visual interface for these functionalities.
image: null
nav-menu: false
show_tile: false
---

## Project Specification
<ul>
  <li>Tools/Languages: C#, Windows Forms, Visual Studio IDE</li>
  <li>Environment: Class Project, Group of 4. Eventually forked by me.</li>
  <li>Timeline: 7+ weeks</li>
  <li>GitHub: <a href="https://github.com/namdo1225/visualizer-github">Repository</a></li>
</ul>

## Description

For a 4-member group project, we created a Windows program that can abstract many Git commands and provide a visual interface for these functionalities. The program also has the ability to work with the GitHub API and perform various functionalities with your remote repositories.

## My Contribution

I originally wrote the various methods to interact with the GitHub API and created the unit tests. However, after forking on it, I solely continued to develop the app, including working with Window Forms to polish the UI and working with other APIs to work with local repositories.

## Instructions to use:

1) If you want to work with your remote repositories on GitHub, login with GitHub. Otherwise, you can use the local workspace.

<img src="{% link images/projects_media/20231230_visualizer-github/00_setup.png %}" alt="" data-position="center center" />

2) A side panel should pop up. You should be presented with a user code. This is important. Enter that code in the browser that popped up.

<img src="{% link images/projects_media/20231230_visualizer-github/01_code.png %}" alt="" data-position="center center" />
<img src="{% link images/projects_media/20231230_visualizer-github/02_code.png %}" alt="" data-position="center center" />

3) Accept the permission once you have entered the user code. You should now be able to see your repositories.

<img src="{% link images/projects_media/20231230_visualizer-github/04_congrats.png %}" alt="" data-position="center center" />

4) You can create new repositories, clone remote repositories, and even track directories that contain your local repositories.

<img src="{% link images/projects_media/20231230_visualizer-github/05_repo.png %}" alt="" data-position="center center" />

5) You can go to the “Branches” tab and view your repository’s branches.

<img src="{% link images/projects_media/20231230_visualizer-github/06_branch.png %}" alt="" data-position="center center" />

6) You can go to the “Changes” tab, stage or unstage, and commit any changes you have made to your projects.

<img src="{% link images/projects_media/20231230_visualizer-github/07_changes.png %}" alt="" data-position="center center" />

7) If you have committed the changes, they should be reflected back in the “Branches” tab.

<img src="{% link images/projects_media/20231230_visualizer-github/08_committed.png %}" alt="" data-position="center center" />

8) You could click on the “Settings” tab to change some configurations and get more information about the app.

<img src="{% link images/projects_media/20231230_visualizer-github/09_settings.png %}" alt="" data-position="center center" />
