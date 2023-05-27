---
layout: post
title: Spotify Demo Music Player
description: For the final class project in my Objected-Oriented Programming class, my team and I chose to create a Spotify Music player, which can request music demos from the Spotify API and play them.
image: null
nav-menu: false
show_tile: false
---

## Project Specification
<ul>
  <li>Tools/Languages: Java, JavaFX, Spotify API (account required), Eclipse IDE (developed on this IDE, so you might have to use Eclipse to get it to work)</li>
  <li>Environment: Final Class Project, Group of 4</li>
  <li>Timeline: 3 weeks</li>
  <li>GitHub: https://github.com/namdo1225/20230526_DemoSpotifyPlayer/tree/main</li>
</ul>

## Description

For the final class project, we are tasked with putting the principles of object-oriented programming together to create a complex enough program. We chose to create a music player that could play certain songs from Spotify using the Spotify API. Spotify restricts which songs could be retrieved and played by the API, and thus, we were limited to certain 30-seconds demo of certain songs.

<img src="{% link images/projects_media/20230526_demospotify/00.png %}" alt="" data-position="center center" />

The music player could:
<ul>
  <li>Utilize Spotify API to request for an MP3 link of a song and request a list of songs be a certain search string.</li>
  <li>Make, save, and use playlists.</li>
  <li>Could play/stop music. Fast forward or slow down the song.</li>
</ul>

## My Contribution

To get the whole music player working in the first place, you need Java to be able to communicate with the Spotify API. I was the person responsible for doing the whole that as well as creating Java classes that could easily retrieve songs and get search results for my team members.

Thankfully, I know a bit about HTTP and web protocols. JavaFX comes with classes and methods to easily initiate an HTTP request. I had to create a class to send a POST request to the API. The request must have a Basic Authorization token which is the Base-64 encrypted key you would get from your Spotify user profile to get a Bearer token that would allow me to retrieve songs and search results. 

From there, I would use my Bearer token to send a GET request to either retrieve the songs' MP3 or the search results. Either way, the result is always in the form of a JSON object, meaning I need to parse it to find the content I am looking for.
