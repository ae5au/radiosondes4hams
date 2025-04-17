# radiosondes4hams
Presentation on radiosondes geared toward amateur radio operators

# Tracking Weather Balloons - Radiosondes 🎈
2024-04-17 - Presented to the Crowley's Ridge Amateur Radio Club via Zoom

## What is a weather balloon / radiosonde
* What - Measures conditions at various layers of the atmosphere.
  * Temperature, humidity, wind speed, etc.
* How
  * Balloon - provides lift. Expands during ascention until bursting.
  * Parachute - slows down the descent to safe speed
  * Payload - radiosonde. Uses GPS and sensors to collect data that is sent to a ground station with a radio transmitter. Most commonly 400-406 MHz
* Who - Weather agencies (NWS in US), educational/research, military
* Why - Develop weather models/forecasts. Monitor severe weather conditions.
* Where - Many, but not all NWS offices. Universities. Military bases.
* When - Regularly (twice daily, etc.), during specific weather conditions, before specific activities

## SondeHub and how it works
* SondeHub.org - Tracker for radiosondes
* amateur.sondehub.org
* Data submitted by volunteer stations
* While in flight, provides forward predictions and reverse predictions
* Launch sites
  * Generates predictions for future launches
  * Shows historical data
* Chase and recovery reporting

## Stations for home
* Receiver - radiosonde_auto_rx
  * Python developed for Linux
  * Raspberry Pi (etc) and 1+ RTL-SDR dongle (TCXO required)
  * AirSpy or SDRplay - more bandwidth
* Antenna
  * Homebrew 1/4 wave ground plane
  * Many dual-band verticals work well
  * Seen good results even with the diplole included with RTL kits
* Filter / preamp
* Why run my own station if there are others?
  * Redundancy
  * Track closer to the ground for cold hunts
  * For fun!

## Stations for portable
* Chasemapper (with auto_rx)
  * Headless / browser-based / multi-user
  * Able to do __offline__ mapping and predictions
  * Update chase car position on SondeHub (GPS required)
  * Many options for hunting professional sondes or amateur payloads
* rdzTTGOsonde
  * Decodes many sonde types on LoRa ESP32 development boards
  * Display, web server, Android app, KISS TNC
  * Live predictions from SondeHub
  * With GPS and Wi-Fi, can update chase position to SondeHub
  * Hardware
    * Older 433 Semtech boards
    * LilyGo LoRa32 V2.1_1.6
        * Better RX
        * Display
        * BYO GPS, battery, , button(s), case
        * $15.60 + shipping from China
        * $30.50 Amazon Prime
    * LilyGo T-Beam
        * Not quite as sensitive, but usable
        * Can be ordered with display
        * Has button, GPS, and 18650 cell holder
        * BYO case
        * $31.99 + shipping from China
  * Could also use at home
* Antennas
  * Portable and mobile 70cm antennas


## Hunting tips / tricks
* Prepare
  * Predictions - ahead of time for days that you might be free
  * Re-run every day or two as the model updates
* Live tracking while the sonde is still transmitting
  * Use chase mode so others know you are hunting
  * On ground, you have to be fairly close
  * Get close enough, quick enough
  * Know how low your (and/or other) home stations can track in the target area
* Searching for cold cases
  * Research flight path and area ahead of time
  * Check flights for ones that were tracked low enough into areas with good chances of success
* Retrieval
  * Extension poles
  * Throw lines
  * Drone
  * Canoe

## What you can do with the sonde
* Collect
* Reuse - RS41ng on 70cm
  * Tracker for your own flight
  * RDF beacon
  * Modes
    * APRS
    * Horus 4FSK
    * CATS
    * CW
    * Others

## How this helps with ham radio balloon projects
* Learn the mechanics of stratospheric flight
  * How burst altitude, wind patterns, etc. affect flight
* Practice predictions
* Practice tracking
* Free hardware

## Links
https://sondehub.org/
https://github.com/projecthorus/radiosonde_auto_rx/wiki
https://m0ukd.com/calculators/quarter-wave-ground-plane-antenna-calculator/
https://store.uputronics.com/products/uputronics-filtered-preamps?variant=48292157325646
https://v3.airspy.us/product/upu-fp403s/
https://github.com/projecthorus/chasemapper
https://github.com/dl9rdz/rdz_ttgo_sonde
https://github.com/dl9rdz/rdz_ttgo_sonde/wiki
https://github.com/mikaelnousiainen/RS41ng

