# CiS422-pj1-debug

 
## Description:

a system like Strava, MapMyRun, or RideWithGPS
The input will be a record consisting of a sequence of (latitude, longi-tude) pairs.
The output should be a list of turn-by-turn directions.
  

  
## Use:

download project, unzip files, run app.py from command line or IDE and it will open the page in your browser.
you can input your source co-ordination (latitude, longi-tude) pairs and find web app will help you to find direction,and showing path on map.

## Use:How to find co-ordination ?

You may see this webpage to find a way
https://support.google.com/maps/answer/18539?co=GENIE.Platform%3DDesktop&hl=en



## test

there is a geojson_example.json I downloaded from Official website. 

You can also use geojson_example.json provided coordinates to test, but if you expand the distance between the coordinates (like500 meters), a system prompt will pop up, showing an error.



## API limition
The API provided in openrouteservice has a radius limit, it can display any coordinates within a radius of 350 meters
But if the two coordinates exceed 350 meters, not for the erronous co-ordinates.




## source address

API :openrouteservice.org/dev/#/api-docs

STATICS:  LEFTLET: Leaflet 1.7.1, a JS library for interactive maps. http://leafletjs.com



## requirement venv

certifi==2020.6.20
chardet==3.0.4
click==7.1.2
Flask==1.1.2
idna==2.10
itsdangerous==1.1.0
Jinja2==2.11.2
MarkupSafe==1.1.1
requests==2.24.0
urllib3==1.25.10
Werkzeug==1.0.1

 
