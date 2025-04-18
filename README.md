# Tracking Weather Balloons - Radiosondes 🎈
Outline / notes for presentation on radiosondes geared toward amateur radio operators

2024-04-17 - Presented to the Crowley's Ridge Amateur Radio Club via Zoom

## What is a weather balloon / radiosonde
* What - Measures conditions at various layers of the atmosphere.
  * Temperature, humidity, wind speed, etc.
* How
  * Balloon - Helium or Hydrogen filled. Provides lift. Expands during ascention until bursting.
  * Parachute - slows down the descent to safe speed
  * Payload - radiosonde. Uses GPS and sensors to collect data that is sent to a ground station with a radio transmitter. Most commonly 400-406 MHz
* Who - Weather agencies (NWS in US), educational/research, military
* Why - Develop weather models/forecasts. Monitor severe weather conditions.
* Where - Many, but not all NWS offices. Universities. Military bases.
* When - Regularly (twice daily, etc.), during specific weather conditions, before specific activities
* NWS Upper Air website has a lot of information

## SondeHub and how it works
* SondeHub.org - Tracker for radiosondes
* amateur.sondehub.org
* Data submitted by volunteer stations
* No login needed
* Looks a little different on mobile, but has the same features. Might have to rotate to landscape.
* Review settings area
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
  * Configuration
* Antenna
  * Homebrew 1/4 wave ground plane
  * Many dual-band verticals work well
  * Seen good results even with the diplole included with RTL kits
  * Collinear
  * Yagi
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
  * Doesn't scan the entire band
  * Hardware
    * Older 433 MHz Semtech LoRa boards
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
* Report your recovery

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

## Questions
* [SondeHub Discord](https://sondehub.org/go/discord)
  * Great for technical questions and also sonde information
* [FB Group: Radiosonde North America - NWS Weather Balloon](https://www.facebook.com/groups/444260440607754/)
  * Photos and stories of hunts and recoveries
* My email is [good on QRZ](https://www.qrz.com/db/ae5au)

## Links
* [NWS Upper Air](https://www.weather.gov/upperair/)
* [SondeHub](https://sondehub.org/)
* [SondeHub Amateur](https://amateur.sondehub.org/)
* [radiosonde_auto_rx](https://github.com/projecthorus/radiosonde_auto_rx/wiki)
* [1/4 ground plane calc](https://m0ukd.com/calculators/quarter-wave-ground-plane-antenna-calculator/)
* [Uputronics filter](https://store.uputronics.com/products/uputronics-filtered-preamps?variant=48292157325646)
* [Uputronics filter at Airspy.us](https://v3.airspy.us/product/upu-fp403s/)
* [Chasemapper](https://github.com/projecthorus/chasemapper)
* [RDZ TTGO Sonde GitHub](https://github.com/dl9rdz/rdz_ttgo_sonde)
* [RDZ TTGO Sonde Wiki](https://github.com/dl9rdz/rdz_ttgo_sonde/wiki)
* [LilyGo LoRa32 V2.1_1.6](https://lilygo.cc/products/lora3?variant=42272562249909)
* [LilyGo LoRa32 Amazon](https://www.amazon.com/LILYGO-LoRa32-433Mhz-Development-Paxcounter/dp/B0B45L398K)
* [LilyGo T-Beam](https://lilygo.cc/products/t-beam?variant=43059202654389)
* [RS41ng Firmware for radiosondes](https://github.com/mikaelnousiainen/RS41ng)
