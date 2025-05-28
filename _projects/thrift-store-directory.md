---
layout: page
title: Thrift store directory
date: 2025-05-28
---

# Thrift store directory

*May 28, 2025*

Right now I will build the app with Tempo AI builder. It works on react framework, I can view the code, has a visual Figma-like interface integration, can export/import from and into GitHub. Honestly all of that seems too good to be true, but I'll see.
I've wanted to try out this builder for a while but I've been putting it off very bravely. Mostly because I am extremely put off by anything that seems too complex, which is funny because I've learned very complex things in my life, an example would be the video game Europa Universalis, which is exceedingly complex and there's no way in hell anyone can just sit down to play this bad boy and have a good time. I need to approach this as if it were a video game. So let's start playing.  

## Tempo Prompt:

### Goal

I want you to build me an MVP of an online directory for second hand stores in Prague.

### Crucial concepts to keep in mind

* minimalist, simple and visually pleasing, calm, non-distracting design
* mobile-friendly and responsive (majority of users are expected to come from mobile devices)
* lightning-fast load times, buttery smooth responses
* simplest possible techstack to minimize bloat and number of potential bugs

### Project goal

To give users easy, elegant and fast overview of Second Hand store locations in the city of Prague with the basic information about each store.

### Target demographic

Users who don't want to go through the search engine listings looking at individual store pages or through general directories that are not very user-friendly and visually attractive.

### Features & Requirements

1. Landing Page Design (visual reference in image landing_page.png):

    Block_A: Heading with the title
    * title: "Sekáče v Praze"

    Block_B: Carousel of thrift stores
    * pulled from a database of all the stores
    * 5 stores in a single row
    * a button on each side of the carousel, when clicked it moves the visible list by 5 stores (or less if not available) in the appropriate direction (in a smooth animation)
    * design of a single element of this list: border-less rectangular (taller than wide) image of the store with a store title in the bottom displayed on top of the image

    Block_C: Interactive area for Map and Store_Page
    * by default shows map of Prague (referred to as Map) zoomed to show about 3/4 of the Prague city area (Map)
    * on the Map are shown markers with the geolocation of each store in the database
    * clicking on a marker on the Map or a store from the Carousel (Block_B) opens up a Store_Page
    * whenever Store_Page is displayed the Block_C gets divided between the Map (left side, 30% of the area) and the Store_Page (right side, 70% of the area), this division happens in an animated fashion (both the Map and Store_page live inside the Block_C)

    Map
    * minimal tile design, fast load times and smooth transitions, movement and zooming are of utmost importance

    Store_Page
    * Store Image
    * Photo Gallery
    * Store Title
    * Opening Hours
    * Address
    * Description

2. Database
    * Only to keep the store data

3. Design and typography
    * for color and typography reference use visual_design.jpg image
    * use modern and minimal styling


---

*May 23, 2025*

I have instructed Cursor AI and had it make me a very simple webpage with plain HTML/CSS/JS and a JSON file and Leaflet integration (for a map) to get a feel for how difficult it is to vibecode something. It was easy at first but then I ran into some problems rather quickly. It managed to make a simple map with few markers, it worked correctly, but when I wanted Cursor to add couple of design changes it started to fall apart. Map was beginning to show erratic behaviour when zooming in and out, Cursor did not style exactly as I thought it would etc. I can't imagine trying to vibecode an actual complex webapp in this manner. I was thoroughly discouraged from further trying to instruct the agent to repair the bugs and make the changes as I have imagined them in my head. I must not let the discouragement affect me. Instead I have to learn to effectively communicate my vision. Communicate better. Minimize the potential for the agent's self-interpretation and minimize the chance of an error due to lack of imformation. These agents can scan through pictures, diagrams and screenshots. It is a must to include a diagram or UI mockup in my prompts to make sure the agent has the highest chance to code what I envision.

The sheer number of web development technologies is giving me a headache. I would love to have this project made in simplest possible way, but to make the website really compelling I will probably have to use a framework of some sort, because otherwise it will take forever to stitch together.  
Still haven't thought much about the name for this app, but just now I've thought "*Sekáče v Praze*" might be good, sekáč is a Czech slang term for second hand store.  
I need to think harder about what is it that I actually want to build here.  
An online directory list of Second Hand shops in Prague. Simple landing page that is visually pleasing. I want the map to be incorporated but not a fully fleshed out detailed map, just a simple representation of a map of Prague. The problem I am pondering now is how to style this and especially on mobile devices. Simplicity is key. I don't want a plain list 1-n. But if there are going to be large amounts of stores then how to make it so they all get some real-estate. I dislike the idea of just a boring ol' cartographic map with some markers. It needs to be better. Altough I myself am a map connonsieur most people, probably, don't like to scroll maps endlessly and god-knows how many of them don't even know how to use a map in the first place. 
So a simple map that is just a very rough shape. Now suppose I have fifty stores in my directory, how do I shove them on the map without forcing the user to scroll around endlessly? Should there be a featured stores? I just wonder if people use maps anyway.  
I think I should start by coming up with a UI/UX design first and then concern myself with the coding later, because it is hard to translate to the AI agent what I want it to build without knowing myself first. Right. 

---

*May 20, 2025*

I set out to create a simple web and mobile app that will list out local second hand stores in a pleasant, easy to view way. That's about it for now. I have more ideas on various features that could be added but for now I'll be happy if I manage to just produce this basic concept.  
Frankly I have no clue how app development works so I'll have to find that out.

ChatGPT prompt: 
I want to make a simple online directory app that will show local second hand stores in my area. The app should be available first only as a web app but later I'd like to do a mobile variant (IOS + Android). It will just be a zoomable map with the available shops placed in it. Once you click on a shop it will open a pop up window with some detail of the shop (opening hrs, address, phone number, description). I have no knowledge about app development and this serves as a learning project. I want you to write me a complete road map of how this is done, start to finish. Over-explain everything, if you use a technical jargon include an explanation of that particular term, approach this as you would instruct a person with no prior knowledge. I want to know how one should approach building such an app, debugging, making it live and available, maintaining it and expanding it with further features. This is a solo project, I will do everything myself, nothing will be delegated or made it a team. I want to know how much this will cost in terms of operational costs (servers, support etc.).

