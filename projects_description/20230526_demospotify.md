---
layout: post
title: Java Spotify Music Player
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
  <li>GitHub: <a href="https://github.com/namdo1225/Java_Spotify_Player">Repository</a></li>
</ul>

## Description

For the final class project, we are tasked with putting the principles of object-oriented programming together to create a complex enough program. We chose to create a music player that could play certain songs from Spotify using the Spotify API. Spotify restricts which songs could be retrieved and played by the API, and thus, we were limited to certain 30-second demos of certain songs.

<img src="{% link images/projects_media/20230526_demospotify/00_login.png %}" alt="" data-position="center center" />

The music player could:
<ul>
  <li>Utilize the Spotify API to request an MP3 link of a song and request a list of songs using a certain search string.</li>
  <li>Make, save, and use playlists.</li>
  <li>Could play or stop music. Fast forward or slow down the song.</li>
</ul>

Note: The app is currently not working because my Spotify account has been deleted. Because you need an account to interact with the API, it is not safe for me to keep my account active for this app.

## My Contribution

To get the whole music player working in the first place, you need Java to be able to communicate with the Spotify API. I was the person responsible for developing the whole project, as well as creating Java classes that could easily retrieve songs and get search results for my team members.

Thankfully, I know a bit about HTTP and web protocols. Java comes with classes and methods to easily initiate an HTTP request. I had to create a class to send a POST request to the API. The request must have a Basic Authorization token, which is the Base-64 encrypted key you would get from your Spotify user profile, to get a Bearer token that would allow me to retrieve songs and search results. 

From there, I would use my Bearer token to send a GET request to either retrieve the songs' MP3 or the search results. Either way, the result is always in the form of a JSON object, meaning I need to parse it to find the content I am looking for. After parsing, I finally have the song's name, creator, date, and demo url to display to the user.

## 2023 Improvement

For 2023, to authorize with the Spotify API safely and continue searching for songs, I have decided to use Spotify's Authorization Code with PKCE Flow. With this flow, I have to generate a code verifier and a code challenge from that verifier. The challenge will be passed to the API while trying to get an authorization code. The code verifier will be passed to the API while trying to get the access token. The verifier recently passed in will be compared to the code challenge previously passed in so that the API can ensure that the recognized app is making the API request.

## Instructions to use:

1) Click "Login". You will be redirected to Spotify's website.

<img src="{% link images/projects_media/20230526_demospotify/00_login.png %}" alt="" data-position="center center" />

2) Login to Spotify and click "Agree".

<img src="{% link images/projects_media/20230526_demospotify/01_agree.png %}" alt="" data-position="center center" />

3) Grab the code from the URL.

<img src="{% link images/projects_media/20230526_demospotify/02_code.png %}" alt="" data-position="center center" />

4) Copy the code into the app.

<img src="{% link images/projects_media/20230526_demospotify/03_copy.png %}" alt="" data-position="center center" />

5) You can now search for tracks if the provided code is correct.

<img src="{% link images/projects_media/20230526_demospotify/04_search.png %}" alt="" data-position="center center" />

6) You can play songs, change playback speed, adjust volume, etc.

<img src="{% link images/projects_media/20230526_demospotify/05_play.png %}" alt="" data-position="center center" />

7) You can add songs to playlists.

<img src="{% link images/projects_media/20230526_demospotify/06_playlist.png %}" alt="" data-position="center center" />

8) The red icon at the top right has instructions that can help you navigate through the app.

<img src="{% link images/projects_media/20230526_demospotify/07_instruction.png %}" alt="" data-position="center center" />
