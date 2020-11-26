# web-app
openrouteservice.org/dev/#/api-docs

Overview
Hikers, runners, and cyclists often record their activites using a phone, fitness watch, or dedicated GPS device. They may upload data from their devices to a system like Strava, MapMyRun, or RideWithGPS, which typically provide analysis, map display, and optional social media sharing.

Existing services like Strava provide a variety of analyses and record keeping, but they typically do not provide a fully automated way to extract turn-by-turn directions from a recorded activity. For hikers and runners and some cyclists who travel off-road, this might be very difficult … there may be no suita-ble database from which to extract suitable cues. For road cyclists, however, it should be possible to extract turn-by-turn directions (a “cue sheet”) from a recording.

That is what our system will do. The input will be a record consisting of a sequence of (latitude, longi-tude) pairs, possibly with other information. The output should be a list of turn-by-turn directions,
Tracks
Runners, hikers, and cyclists often use GPS devices to log their outings. The GPS device might be a mobile phone, a fitness watch like those from Apple, Fitbit, and Garmin, or a cy-cling computer like the Garmin Edge series or the Wahoo Elemnt series. Many people log their activities to a web application like MapMyRun or Strava. A record that includes a se-ries of locations along with time, often with additional data such as heart rate, is called a track.
Tracks may be stored in any of several formats. Many web applications support download-ing tracks in the GPX format. GPX is an XML encoding, and looks like this:
<?xml version="1.0" encoding="UTF-8"?>
<gpx xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://www.topografix.com/GPX/1/1" xmlns:gpxdata="http://www.cluetrust.com/XML/GPXDATA/1/0" xsi:schemaLocation="http://www.topografix.com/GPX/1/1 http://www.topografix.com/GPX/1/1/gpx.xsd http://www.cluetrust.com/XML/GPXDATA/1/0 http://www.cluetrust.com/Schemas/gpxdata10.xsd" version="1.1" crea-tor="http://ridewithgps.com/">
  <metadata>
    <name>09/27/20</name>
    <link href="https://ridewithgps.com/trips/56855290">
      <text>09/27/20</text>
    </link>
    <time>2020-09-27T11:31:19Z</time>
  </metadata>
  <trk>
    <name>09/27/20</name>
    <trkseg>
      <trkpt lat="44.587662" lon="-123.256691">
        <ele>67.3999999</ele>
        <time>2020-09-27T18:31:19Z</time>
      </trkpt>
      <trkpt lat="44.587662" lon="-123.256691">
        <ele>67.3999999</ele>
        <time>2020-09-27T18:31:20Z</time>
      </trkpt>
      ...
The sample above was downloaded from Ride With GPS, a popular web application for cy-clists. 
