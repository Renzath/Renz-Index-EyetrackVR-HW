# Gum Stick Remix V2 (GSRv2) Guide



---
---



## Disclaimer

This guide was entirely written by a human (me AstralFoxVR) and no AI was used to produce it.


---


## Special thanks

Special thanks goes to:
- Renzahth, the original creator of the GSRv2, for helping me out with all my questions on the GSRv2 even one year after he created it.
- Zani for helping me out with my questions at the beginning and compiling a list of the different messages of Renzath.
- Prohurtz for answering my questions at the beginning too and for creating the whole EyeTrackVR!
- And last but not least PhysicsDude for creating the original design the GSRv2 is based on.



---
---



## Parts needed 

* 1x V4 mini LED kit from ETVR 
	> The V5 is not supported yet, but feel free to submit support in the GSRv2  channel from the ETVR discord server.  

	> [ETVR Store](https://store.eyetrackvr.dev/products/v4-mini-fully-solderless-kit "ETVR Store link (11/2026)")


* 2x OV2640 160 degree 850nm 200mm  
	> [Aliexpress](https://aliexpress.com/item/1005003040149873.html "Aliexpress link (11/2026)") ( Choose "Color: 75MM-160 850nm" )


* 2x Seeedstudio XIAO ESP32S3
	> [Seeedstudio (probably cheaper)](https://www.seeedstudio.com/XIAO-ESP32S3-Sense-p-5639.html "Seeedstudio link (11/2026)"), [Amazon](https://amzn.eu/d/05A4ea8F "Amazon link (11/2026)")


* 30 or 28 AWG Wire (or lower if you want, but it will be easier with 30 or 28 AWG)
	> Soft and flexible wire with no solid core is **strongly** recommended!  
  
  >[Aliexpress](https://aliexpress.com/item/1005006350734418.html "Aliexpress link (11/2026)")


* 1x Adafruit CH334F Mini 4-Port USB Hub (to link all ESP32S3 to one USB-C Port)
	> [Adafruit](https://www.adafruit.com/product/5997 "Adafruit link (11/2026)")


* 1x USB-A to USB-C Adapter (to plug into the index)
	> [Aliexpress](https://aliexpress.com/item/1005010327462753.html "Aliexpress link (11/2026)"), [Amazon](https://amzn.eu/d/0iA2fFHk "Amazon link (11/2026)")


* 4x M3x8mm screws (if using heat inserts, not sure on nuts and bolts version)
	> I would recommended to get a pack of various sizes other than what you need.

	> [Aliexpress](https://aliexpress.com/item/1005007315319409.html "Aliexpress link (11/2026)")


* 4x M3x14mm screws (if using heat inserts, not sure on nuts and bolts version)
	> I would recommended to get a pack of various sizes other than what you need.
	
	> [Aliexpress](https://aliexpress.com/item/1005007315319409.html "Aliexpress link (11/2026)")


* 8x M3x5.7x4.6 heat inserts
	> I would recommended to get a pack of various sizes other than what you need.
	
	> [Aliexpress](https://www.aliexpress.com/item/1005011985841677.html "Aliexpress link (11/2026)")


* 2x 56k Ohm THT resistor (for extra USB-C port) (1/4W is enough)
	> [LCSC](https://www.lcsc.com/product-detail/C1373212.html "LCSC link (11/2026)"), [Aliexpress](https://aliexpress.com/item/32952657927.html "Aliexpress link (11/2026)")


* 2x Camera extension cables **24 pin 0.5mm pitch and A to A.** (If your camera cables are 75mm or less than 200mm)
	> I would recommend 200mm, if you have 75mm cameras. You can absolutely also get away with bigger ones and maybe also with 150mm cables.   
	>>  **Absolutely do not go under 150mm if you have 75mm cams!!**  
	  
	 > [LCSC (A to A 150mm)](https://www.lcsc.com/product-detail/C54560895.html "LCSC link (11/2026)"), [LCSC (A to A 200mm)](https://www.lcsc.com/product-detail/C54560899.html "LCSC link (11/2026)"), [Aliexpress](https://www.aliexpress.com/item/2255799835842411.html "Aliexpress link (11/2026)"), [ETVR Store (A to A)](https://store.eyetrackvr.dev/products/esp-camera-cable-extensions?variant=50422401892649 "ETVR Store link (11/2026)")  


* 2x Camera Extension Connectors **24 pin**. (If your camera cables are 75mm or less than 200mm)
	> [LCSC](https://www.lcsc.com/product-detail/C54423203.html "LCSC link (11/2026)"), [Aliexpress](https://www.aliexpress.com/item/3256804096715690.html "Aliexpress link (11/2026)"), [Adafruit](https://www.adafruit.com/product/4524 "Adafruit link (11/2026)"), [ETVR Store](https://store.eyetrackvr.dev/products/esp-camera-cable-extensions "ETVR Store link (11/2026)")


* 1x Adafruit 4090 USB Type C Breakout Board or similar looking board (to have a extra USB-C port. Eg for a fan or Vive Face Tracker or other face trackers) (**Optional**)
	> [Aliexpress](https://www.aliexpress.com/item/1005005691960336.html "Aliexpress link (11/2026)"), [Adafruit](https://www.adafruit.com/product/4090 "Adafruit link (11/2026)")


* Heat shrink tubes in various sizes. (For the Adafruit 4090 USB Type C Breakout Board or similar looking board and for the DIY mouth tracker.) (**Optional** but **STRONGLY** recommended if you plan to use a Adafruit 4090 USB Type C Breakout Board or similar looking board or you plan to do a DIY mouth tracker)
	> [Amazon](https://amzn.eu/d/0aKqZTNe "Amazon link (11/2026)")



### Additional parts needed for a DIY mouth tracker

* 1x OV2640 160 degree 850nm 200mm (So 3x in total with the 2x from before)
	> [Aliexpress](https://aliexpress.com/item/1005003040149873.html "Aliexpress link (11/2026)") ( Choose "Color: 75MM-160 850nm" )

	
* 1x Seeedstudio XIAO ESP32S3 (So 3x in total with the 2x from before)
	> [Seeedstudio (probably cheaper)](https://www.seeedstudio.com/XIAO-ESP32S3-Sense-p-5639.html "Seeedstudio link (11/2026)"), [Amazon](https://amzn.eu/d/05A4ea8F "Amazon link (11/2026)")

	
* 1x M4x20mm or M4x18 screw with nut (for face tracking hinge, but you can get away with a **ABSOLUTE MINIMUM** M3x16mm or M4x16mm if needed. M4 is **STRONGLY** recommended for more stability.  
	> You can also use a longer M4 screw than 20mm or 18mm.
	
	>[Aliexpress](https://aliexpress.com/item/1005005971756266.html
 "Aliexpress link (11/2026)")	


* 2x 160 Ohm THT resistor (for face tracking LEDs) (1/4W is enough)
	> [LCSC](https://www.lcsc.com/product-detail/C410672.html "LCSC link (11/2026)"), [Aliexpress](https://aliexpress.com/item/32952657927.html "Aliexpress link (11/2026)")


* 2x 5mm 850nm IR LEDs (for face tracking)
	> [LCSC (100° emitting angle)](https://www.lcsc.com/product-detail/C6081338.html "LCSC link (11/2026)"), [Aliexpress (30° emitting angle)](https://aliexpress.com/item/1005003946239993.html "Aliexpress link (11/2026)")   

	> If you take the 30° emitting angle IR-LED you will probably need to sand down the top of the IR-LED a bit to diffuse the light more.    


* 1x Perfboard with a absolute minimum recommended of 6 by 3 holes. I would recommend 6 by 6 holes. 
	> You can probably also get away without it and solder everything to each other, but it will be more difficult, less clean and this guide doesn't show how to do it.   

	> [Aliexpress](https://aliexpress.com/item/1005004865405791.html "Aliexpress link (11/2026)"), [Amazon](https://amzn.eu/d/058MUtYw "Amazon link (11/2026)") 


* 1x Camera Extension Cables **24 pin 0.5mm pitch** A to B or A to A. (If your camera cables are 75mm or less than 200mm) (So 3x in total with the 2x from before)
	> I would recommend getting one A to B (for DIY mouth tracker) and two A to A cables (for eye tracking), to have a cleaner look at the end.  

	> I would recommend 100mm or 150mm, if you have 75mm cameras. You can absolutely also get away with bigger ones.  
	>> **Absolutely do not go under 100mm if you have 75mm cams!!**  

	> [LCSC (A to B 150mm)](https://www.lcsc.com/product-detail/C54560896.html "LCSC link (11/2026)"), [LCSC (A to B 200mm)](https://www.lcsc.com/product-detail/C54560900.html "LCSC link (11/2026)"), [LCSC (A to A 150mm)](https://www.lcsc.com/product-detail/C54560895.html "LCSC link (11/2026)"), [LCSC (A to A 200mm)](https://www.lcsc.com/product-detail/C54560899.html "LCSC link (11/2026)"), [Aliexpress](https://www.aliexpress.com/item/2255799835842411.html "Aliexpress link (11/2026)"), [ETVR Store (A to A)](https://store.eyetrackvr.dev/products/esp-camera-cable-extensions?variant=50422401892649 "ETVR Store link (11/2026)") 

	
* 1x Camera Extension Connector **24 pin**. (If your camera cables are 75mm or less than 200mm) (So 3x in total with the 2x from before)
	> [LCSC](https://www.lcsc.com/product-detail/C54423203.html "LCSC link (11/2026)"), [Aliexpress](https://www.aliexpress.com/item/3256804096715690.html "Aliexpress link (11/2026)"), [Adafruit](https://www.adafruit.com/product/4524 "Adafruit link (11/2026)"), [ETVR Store](https://store.eyetrackvr.dev/products/esp-camera-cable-extensions "ETVR Store link (11/2026)")



#### Optional additional parts for disconnecting the DIY mouth tracker 
* 2x Female JST SM Connectors, or similar, **with crimp contacts!** (to disconnect the mouth tracker)
	> [Aliexpress (male & female housing + contacts)](https://aliexpress.com/item/1005007484988429.html "Aliexpress link (11/2026)"), [LCSC (female housing](https://www.lcsc.com/product-detail/C141767.html "LCSC link (11/2026)"), [LCSC (female contacts](https://www.lcsc.com/product-detail/C141769.html "LCSC link (11/2026)")

* 1x Male JST SM Connectors, or similar, **with crimp contacts!** (to disconnect the mouth tracker)  
	> [Aliexpress (male & female housing + contacts)](https://aliexpress.com/item/1005007484988429.html "Aliexpress link (11/2026)"), [LCSC (male housing](https://www.lcsc.com/product-detail/C141768.html "LCSC link (11/2026)"), [LCSC (male contacts](https://www.lcsc.com/product-detail/C246760.html "LCSC link (11/2026)")

* 1x Camera Extension Connectors (to disconnect the mouth tracker; So 4x in total with the 3x from before)
	> [LCSC](https://www.lcsc.com/product-detail/C54423203.html "LCSC link (11/2026)"), [Aliexpress](https://www.aliexpress.com/item/3256804096715690.html "Aliexpress link (11/2026)"), [Adafruit](https://www.adafruit.com/product/4524 "Adafruit link (11/2026)"), [ETVR Store](https://store.eyetrackvr.dev/products/esp-camera-cable-extensions "ETVR Store link (11/2026)")


* 1x Cable Strap (to glue the extension cable connector and the JST SM connector, or similar, to it) (See image below to see what it looks like)
	> You can also just glue the connectors to the USB-HUB directly if you want.

	> [Amazon](https://amzn.eu/d/0bGLY5of "Amazon link (11/2026)"), [Aliexpress](https://aliexpress.com/item/1005010123189793.html "Aliexpress link (11/2026)")

![Connectors glued to cable strap](./Images/Introduction_connectors_glued_to_cable_strap.jpg "Connectors glued to cable strap")


---
---



## What to print

> Files can be found on [Renzath github](https://github.com/Renzath/Renz-Index-EyetrackVR-HW "Renzath Github 11/26") or [Physics-Dude github](https://github.com/Physics-Dude/Phys-Index-EyetrackVR-HW/tree/main "Physics-Dude Github 11/26").

### USB-HUB files
> Gum Stick Remix for 3x ESPs plus USB Hub → Adafruit USB Hub (Latest Version)   
([link if files didn't move](https://github.com/Renzath/Renz-Index-EyetrackVR-HW/tree/812fad27340c4135f5993a12d5b7b82689a926fe/Gum%20Stick%20Remix%20for%203x%20ESPs%20plus%20USB%20Hub/Adafruit%20USB%20Hub%20(Latest%20Version) "Github link (11/2026)") (11/2026))

* 1x [GSR-Adafruit_INS-Base-Cover.3mf](https://github.com/Renzath/Renz-Index-EyetrackVR-HW/blob/812fad27340c4135f5993a12d5b7b82689a926fe/Gum%20Stick%20Remix%20for%203x%20ESPs%20plus%20USB%20Hub/Adafruit%20USB%20Hub%20(Latest%20Version)/GSR-Adafruit_ESP-Frame-Basic.3mf "Github link (11/2026)")
* 1x [GSR-Adafruit_INS-Hub-Frame.3mf](https://github.com/Renzath/Renz-Index-EyetrackVR-HW/blob/812fad27340c4135f5993a12d5b7b82689a926fe/Gum%20Stick%20Remix%20for%203x%20ESPs%20plus%20USB%20Hub/Adafruit%20USB%20Hub%20(Latest%20Version)/GSR-Adafruit_INS-Hub-Frame.3mf "Github link (11/2026)")
* 1x [GSR-Adafruit_Spacer-Frame.3mf](https://github.com/Renzath/Renz-Index-EyetrackVR-HW/blob/812fad27340c4135f5993a12d5b7b82689a926fe/Gum%20Stick%20Remix%20for%203x%20ESPs%20plus%20USB%20Hub/Adafruit%20USB%20Hub%20(Latest%20Version)/GSR-Adafruit_Spacer-Frame.3mf "Github link (11/2026)")
* 1x [GSR-Adafruit_ESP-Frame-Strong.3mf](https://github.com/Renzath/Renz-Index-EyetrackVR-HW/blob/812fad27340c4135f5993a12d5b7b82689a926fe/Gum%20Stick%20Remix%20for%203x%20ESPs%20plus%20USB%20Hub/Adafruit%20USB%20Hub%20(Latest%20Version)/GSR-Adafruit_ESP-Frame-Strong.3mf "Github link (11/2026)") **(Strong not Basic!)**
* 1x [GSR-Adafruit_Lid-Cover-USB (M3x14mm).3mf](https://github.com/Renzath/Renz-Index-EyetrackVR-HW/blob/812fad27340c4135f5993a12d5b7b82689a926fe/Gum%20Stick%20Remix%20for%203x%20ESPs%20plus%20USB%20Hub/Adafruit%20USB%20Hub%20(Latest%20Version)/GSR-Adafruit_Lid-Cover-USB%20(M3x14mm).3mf "Github link (11/2026)")
	> If you want a clean look and/or don't need a extra USB-C Port and/or if you didn't install the Adafruit 4090 USB Type C Breakout Board or similar:  
	
	* 1x [GSR-Adafruit_Lid-Cover-Fill (M3x14mm).3mf](https://github.com/Renzath/Renz-Index-EyetrackVR-HW/blob/812fad27340c4135f5993a12d5b7b82689a926fe/Gum%20Stick%20Remix%20for%203x%20ESPs%20plus%20USB%20Hub/Adafruit%20USB%20Hub%20(Latest%20Version)/GSR-Adafruit_Lid-Cover-Fill%20(M3x14mm).3mf "Github link (11/2026)")


### Index Camera and IR-LED Lens Frame with cable tidy wings
> ETVR ValveIndex Cam-LED Mount Rings     
([link if files didn't move](https://github.com/Renzath/Renz-Index-EyetrackVR-HW/tree/812fad27340c4135f5993a12d5b7b82689a926fe/ETVR%20ValveIndex%20Cam-LED%20Mount%20Rings "Github link (11/2026)") (11/2026))

* 2x [Index-EyetrackVRv4 (GSR_Alt).3mf](https://github.com/Renzath/Renz-Index-EyetrackVR-HW/blob/812fad27340c4135f5993a12d5b7b82689a926fe/ETVR%20ValveIndex%20Cam-LED%20Mount%20Rings/Index-EyetrackVRv4%20(GSR_Alt).3mf "Github link (11/2026)")
	> **The second print need to be mirrored.  
	And not the .f3d file but the .3mf one!**


### Index Frunk Frame
> Gum Stick Remix for 3x ESPs plus USB Hub → Frunk Holder (Use M3x14mm Lid)  
([link if files didn't move](https://github.com/Renzath/Renz-Index-EyetrackVR-HW/tree/812fad27340c4135f5993a12d5b7b82689a926fe/Gum%20Stick%20Remix%20for%203x%20ESPs%20plus%20USB%20Hub/Frunk%20Holder%20(Use%20M3x14mm%20Lid) "Github link (11/2026)") (11/2026))

* 1x [GSR-Frunk_Index-Frame.3mf](https://github.com/Renzath/Renz-Index-EyetrackVR-HW/blob/812fad27340c4135f5993a12d5b7b82689a926fe/Gum%20Stick%20Remix%20for%203x%20ESPs%20plus%20USB%20Hub/Frunk%20Holder%20(Use%20M3x14mm%20Lid)/GSR-Frunk_Index-Frame.3mf "Github link (11/2026)"))
* 1x [GSR-Frunk_Brace_WithCam.3mf](https://github.com/Renzath/Renz-Index-EyetrackVR-HW/blob/812fad27340c4135f5993a12d5b7b82689a926fe/Gum%20Stick%20Remix%20for%203x%20ESPs%20plus%20USB%20Hub/Frunk%20Holder%20(Use%20M3x14mm%20Lid)/GSR-Frunk_Brace_WithCam.3mf "Github link (11/2026)")
	> Handy to print too or if you don't want or don't use a mouth tracker:   
	* 1x [GSR-Frunk_Brace_NoCam.3mf](https://github.com/Renzath/Renz-Index-EyetrackVR-HW/blob/812fad27340c4135f5993a12d5b7b82689a926fe/Gum%20Stick%20Remix%20for%203x%20ESPs%20plus%20USB%20Hub/Frunk%20Holder%20(Use%20M3x14mm%20Lid)/GSR-Frunk_Brace_NoCam.3mf "Github link (11/2026)")

#### Optional if you want to install a fan
* 1x [GSR-Frunk_Index-FanCover.stl](https://github.com/Renzath/Renz-Index-EyetrackVR-HW/blob/812fad27340c4135f5993a12d5b7b82689a926fe/Gum%20Stick%20Remix%20for%203x%20ESPs%20plus%20USB%20Hub/Frunk%20Holder%20(Use%20M3x14mm%20Lid)/GSR-Frunk_Index-FanCover.stl "Github link (11/2026)")
> This guide doesn't cover putting on a fan because you don't really need it. So you will need to figure out yourself how to mount it.
	
### Babble Camera Case for DIY mouth tracking (not for the official babble module!)
> If you want to use the official babble module you just need the [GSR-Frunk_Brace_WithCam.3mf](https://github.com/Renzath/Renz-Index-EyetrackVR-HW/blob/812fad27340c4135f5993a12d5b7b82689a926fe/Gum%20Stick%20Remix%20for%203x%20ESPs%20plus%20USB%20Hub/Frunk%20Holder%20(Use%20M3x14mm%20Lid)/GSR-Frunk_Brace_WithCam.3mf "Github link (11/2026)") from above.

> Babble Face Tracker Cam-LED Mount → Gumstick Remix Mount (Alternative)   
([link if files didn't move](https://github.com/Renzath/Renz-Index-EyetrackVR-HW/tree/812fad27340c4135f5993a12d5b7b82689a926fe/Babble%20Face%20Tracker%20Cam-LED%20Mount/Gumstick%20Remix%20Mount%20(Alternative) "Github link (11/2026)") (11/2026))

* 1x [GSR_Babble_FaceCam_Left.3mf](https://github.com/Renzath/Renz-Index-EyetrackVR-HW/blob/812fad27340c4135f5993a12d5b7b82689a926fe/Babble%20Face%20Tracker%20Cam-LED%20Mount/Gumstick%20Remix%20Mount%20(Alternative)/GSR_Babble_FaceCam_Left.3mf "Github link (11/2026)")
* 1x [GSR_Babble_FaceCam_Right.3mf](https://github.com/Renzath/Renz-Index-EyetrackVR-HW/blob/812fad27340c4135f5993a12d5b7b82689a926fe/Babble%20Face%20Tracker%20Cam-LED%20Mount/Gumstick%20Remix%20Mount%20(Alternative)/GSR_Babble_FaceCam_Right.3mf "Github link (11/2026)")
* 1x [GSR_Babble_FaceCam_Base.3mf](https://github.com/Renzath/Renz-Index-EyetrackVR-HW/blob/812fad27340c4135f5993a12d5b7b82689a926fe/Babble%20Face%20Tracker%20Cam-LED%20Mount/Gumstick%20Remix%20Mount%20(Alternative)/GSR_Babble_FaceCam_Base.3mf "Github link (11/2026)")


---
---


## Preparation

1. Prepare the cameras like written in the EyeTrackVR docs.  
> You will probably need to remove the IR filters. If you want to be sure, remove them.

[Preparing Cameras section from the EyeTrackVR docs](https://docs.eyetrackvr.dev/how_to_build/preparing_cameras "Preparing Cameras section from the EyeTrackVR docs (11/26)")

2. Prepare the ESP32S3s like written in the EyeTrackVR docs.
> Don't do the wireless setup, just the wired one, so set the antennas aside.

[Preparing XIAO Sense ESP32 section from the EyeTrackVR docs](https://docs.eyetrackvr.dev/how_to_build/preparing_xiao#wired-configuration "Preparing XIAO Sense ESP32 section from the EyeTrackVR docs (11/26)")

3. Setup your V4 LED Kit according to the EyeTrackVR docs.

[V4 LED Kit Setup from the EyeTrackVR docs](https://docs.eyetrackvr.dev/how_to_build/led_v4_setup "V4 LED Kit Setup from the EyeTrackVR docs (11/26)")

4. Read the "Introduction" section from the "Firmware Guide" from the EyeTrackVR docs.

["Firmware Guide" "Introduction" from the EyeTrackVR docs](https://docs.eyetrackvr.dev/firmware_guide/firmware " \"Firmware Guide\" \"Introduction\" from the EyeTrackVR docs (11/26)")

5. Do the steps written in the "Flashing tool" section from the "Firmware Guide" from the EyeTrackVR docs.
> Select "seeed_studio_xiao_esp32s3" from the drop-down list.

["Flashing tool" section from the "Firmware Guide" from the EyeTrackVR docs](https://docs.eyetrackvr.dev/firmware_guide/flashing_tool "\"Flashing tool\" section from the \"Firmware Guide\" from the EyeTrackVR docs (11/26)")


6. You can now read through the "Installing and setting up the ETVR App" section from the "Software Guide" from the EyeTrackVR docs.
> **(Highly recommended):** If you want the newest updates and features or experience bugs in the stable software, you can download the beta instead:  
To do that you need to go to the [EyeTrackVR github release section](https://github.com/EyeTrackVR/EyeTrackVR/releases "EyeTrackVR github release section") and grab the latest beta version. (There is no documentation yet as of writing (11/26) for the EyeTrackApp 0.3.0 beta 10 (latest beta), but it should be clear what to do and if not, ask in the EyeTrackVR discord server.

["Installing and setting up the ETVR App" section from the "Software Guide" from the EyeTrackVR docs](https://docs.eyetrackvr.dev/software_guide/eyetrackvr_app_guide "\"Installing and setting up the ETVR App\" section from the \"Software Guide\" from the EyeTrackVR docs (11/26)")


---
---


## Assembly

Prepare all the parts and printed parts needed. (See Pictures)

![Parts](./Images/All_parts.jpg "All parts with the optional ones included")

![Printed parts](./Images/All_printed_parts.jpg "All printed parts with the optional ones included, except the fan cover")

---

### USB-HUB Assembly

1. Prepare all the parts needed for the USB-HUB. 
> Ignore the already inserted heat inserts in the base, the cameras already inserted into the ESPs and the IR-LEDs inserted into the V4 mini LED kit.

![USB-HUB_Parts](./Images/USB-HUB_parts.jpg "All USB-HUB parts")


2. Place the heat inserts into the holes of the base and heat them up with a soldering iron to melt them into the plastic.
> If you have a bit of plastic above the heat inserts, like I do in the image, and it causes it to not be flat, you can take a sandpaper or file to file the plastic down to make it flat.

![USB-HUB Heat inserts](./Images/USB-HUB-Base_heat_inserts.jpg "Heat inserts before and after melting into the plastic")


3. Place the Adafruit CH334F into the hub frame, so that the USB-C Port is looking down and is resting on the opening meant for it and the CH334F marking is looking at you. Then place the V4 mini board into its place.
> I would recommended to use tape to hold the two boards in place like in the image below.  
>> I used kapton tape because I had it near me.

![USB-HUB boards in hub frame](./Images/USB-HUB_boards_placed_in_hub_frame.jpg "Boards placed in the hub frame and secured with Kapton tape")


4. Flip the hub frame upside down and solder one wire from the 5V and one from the GND hole of the CH334F board to the VIN + (5V) and - (GND) pad of the V4 mini board respectively.
> I would **strongly** recommended to pre-tin the VIN pads as well as the wires beforehand and then solder the wires onto the pads.  
-> It is always good practice to pre-tin your wires and pads beforehand, so that you don't overheat the pads or board and its easier to solder them.

> I would **strongly** recommend using a red or similar wire as + and a black, brown or blue wire as - !

![USB-HUB power supply cables soldered](./Images/USB-HUB_power_supply_cables_soldered.jpg "5V soldered to VIN + and GND to VIN -")


5. **Skip this step if you don't plan on having a extra USB-C Port.**   
Now solder wires into the pins of "PORT3".
> I would **strongly** recommend to use red or similar for 5V; black, brown or blue for GND; and to use different colors for D- and D+.   
I would also **strongly** recommend to keep this color combination for the specific pads, for the rest of the project.

![USB-HUB wires soldered into port3](./Images/USB-HUB_port3_soldered.jpg "Wires soldered into PORT3")

6. **Skip this step if you don't plan to do a DIY mouth tracker.**   
Solder now a second pair of wires to the 5V and GND of the CH334F board pads. 
> I would **strongly** recommend to have these wires long because you can always trim them down later, and these go to the mouth tracker.

![USB-HUB second power supply wire pair](./Images/USB-HUB_second_power_supply_wires.jpg "Second pair of power supply wires soldered onto 5V and GND of the CH334F board")

7. **Skip to step 11 if you don't plan on having a extra USB-C Port.**  
Get your Adafruit 4090 USB Type C Breakout Board or similar board and desolder the two little resistors on the side, marked in red in the image.

![USB-HUB USB-C board resistors](./Images/USB-HUB_USB-C_board_resistors.jpg "Resistors not removed (left image) and resistors removed (right image)")

8. Solder the D+, D- and GND wire from PORT3 from the CH334F board to the USB-C breakout board pins as well as both 56kΩ resistors into the CC1 and CC2 pins respectively.

![USB-HUB USB-C board wires and resistors soldered](./Images/USB-HUB_USB-C_board_wires_and_resistors_soldered.jpg "D+, D- and GND Wires as well as 56kΩ resistors soldered into the pins")

9. Solder both other non soldered resistor legs to each other and then the 5V wire from the CH334F board to them, as well as a new 5V wire to the same place.
> I would **strongly** recommend before soldering them together, putting on both of the resistors as well as on the 5V wire, of the CH334F board, heat shrink tubes so they cant accidently connect to something else!

> I would also recommend bending the resistors like in the image below.

![USB-HUB CC Resistors and wires soldered](./Images/USB-HUB_USB-C_board_cc_resistors_and_wire_soldered.jpg "Step by step guide on how to solder the resistors and wires")

10. Shrink the heat shrink tubes, if not already done, and solder the new 5V wire, from the resistor connection, to the VBUS pin on the USB-C breakout board.
> **In the next pictures and until the end you will not see this USB-C breakout board stick out on the sides because I just figured out when I was done building that the wires on the left side in the next few pictures were meant for the USB-C breakout board.**

![USB-HUB USB-C breakout board VBUS soldered](./Images/USB-HUB_USB-C_board_VBUS_soldered.jpg "5V wire soldered to VBUS")

11. Flip the hub frame upside down again.  
* If you plan to have a DIY mouth tracker solder wires into the pins of PORT1, PORT2 and PORT3.   
PORT4 should already be soldered if you plan to have a extra USB-C port, else let it free.
* If you **don't** plan to have a DIY mouth tracker solder wires into the pins of PORT1 and PORT2 and let PORT3 free.   
PORT4 should already be soldered if you plan to have a extra USB-C port, else let it free.    

*(Please ignore how my board looks like, it took me several attempts to figure it all out, because there was not really a documentation before this one. (There were just images with a few instructions) )* 

> I **strongly** recommend again to use a red or similar wire for 5V; black, brown or blue wire for GND; and to use the same wire color you used for PORT3 on the other side (on this side its named PORT4, don't ask me why) for D+ and D-.   
**If you didn't do step 5**, then use different colors for D+ and D-!

> I also recommend to keep these wires long, because you can always trim them later. (They go to the ESPs)

> Please ignore the wires coming out on the left, it was before I realized they were meant for the USB-C breakout board.

> If you **don't** plan on having a DIY mouth tracker, ignore the long black and red wire pair coming out at the bottom left of the CH334F board, **they will exist for the rest of the guide!**

![USB-HUB wire spider, all usb ports soldered](./Images/USB-HUB_wire_spider_all_usb_ports_soldered.jpg "All USB-Ports soldered on the CH334F")


12. **Skip to step 14 if you don't plan on having a extra USB-C Port.**  
Put the wires through the spacer frame, then place it on-top of the hub frame and flip it upside down.  
Afterwards place the USB-C breakout board into the hole designed for it. (You can also optionally press a bit down on the resistor bridge, to get it a little closer to the hub frame)
Additionally if you plan on having a DIY mouth tracker, route the black and red wire pair out from the bottom of the hub frame, like in the picture.
> Please ignore that the hub frame is placed in the base in the left picture because like I mentioned before, I didn't know the wires were for the USB-C breakout board. *(And I didn't want to disassemble the whole thing again for new pictures)*

> Again ignore the wires coming out at the left side who I put through the hole in the left picture.

![USB-HUB USB-C board placement](./Images/USB-HUB_USB-C_board_placement.jpg "Placement of the USB-C breakout board")


13. Place the frame upside down, so that the smooth surface looks at you, onto the USB-HUB frame and spacer frame, so that its completely closed and flip it upside down.
> If you plan on having a DIY mouth tracker, the black and red wire pair should have a hole where they go through to the outside.

> Imagine like the wires coming out out of the hole on the left side is the USB-C breakout board.

> *And yes its the same picture as Step 12, I am sorry.*

![USB-HUB First half assembled](./Images/USB-HUB_first_half_assembled.jpg "First half of the USB-HUB assembled")


14. **Skip this step if you did step 12 to 13.**  
Put the hub frame into the base and then put the wires through the spacer frame and put the spacer frame on top of the hub frame.
> Again ignore the wires coming out of the hole on the left.

![USB-HUB First half assembled](./Images/USB-HUB_first_half_assembled.jpg "Fist half of the USB-HUB assembled")


15. Take the ESP frame and put your ESPs into them.   
> If you **don't** plan on using a DIY mouth tracker, put one ESP on the left and the other on the right, and leave the middle free.

> I got the image from Renzath because I forgot to take one myself.

> Ignore the wires coming out on the left.

![USB-HUB ESPs in position](./Images/USB-HUB_ESPs_in_position.jpg "ESPs in the ESP frame")


16. Tape The ESPs to the ESP frame, flip the ESP frame over and screw it with two screws through the spacer frame to the base, like in the image below.
> Ignore the wires coming out on the left again .

![USB-HUB ESP frame screwed](./Images/USB-HUB_esp_frame_screwed.jpg "Esp frame screwed with two screws to the base")


17. Solder the 5V, D+, D- and GND wires of the CH334F to the VUSB, D+, D- and GND pins of the ESPs. See the image below for a wiring diagram.
> Solder "PORT3" of the CH334F to the left ESP, "PORT2" to the middle ESP and "PORT1" to the right ESP.
>> If you **don't** plan on having a mouth tracker just solder "PORT3" and "PORT1".

> I **STRONGLY** recommend to put a bit of solder on the pads of the ESP and pretin the wires before you solder them down, so that you don't rip off the pads and have a smooth experience.

> I also recommend doing the 5V wires first, then the D+ and D- and at the end the GND wires.

> (You can also solder the GND wires to the GND pins instead of the square GND pads of the ESPs)

> And one last time, ignore the wires coming out on the left.


![USB-HUB ESPs wiring diagram](./Images/USB-HUB_wiring_diagram_ESPs.jpg "ESPs wiring diagram")

![USB-HUB ESPs wired](./Images/USB-HUB_ESPs_wired.jpg "All ESPs wired")


18. Unscrew the screws, flip the esp frame over, put it on-top of the spacer frame and screw all the four screws in or just two diagonally. After that put in the USB-C to USB-A adapter on the side and put the whole USB-HUB to the side.
> **Be careful when flipping the esp frame over, to not rip out the pads!**

> **Don't screw the screws in if it doesn't fit perfectly and wires are looking out on the sides! Put them all into the hub and just screw the screws in, when all the parts fit on top of each other without spaces in between!**


![USB-HUB finished](./Images/USB-HUB_USB-HUB_finished.jpg "USB-HUB is finished")

---

### Installing the camera and LEDs on the lens mount.

1. Prepare all the parts needed for the lens mounts.
> **Ignore the wrong lens mounts for the rest of the guide!**

![Lens mount parts](./Images/Lens_mount_parts.jpg "All lens mount parts")

2. **Skip this step if you have at least two V4 JST SUR 110mm wire harnesses.**  
You have two option if you don't have them:  
- You can buy some from the [ETVR store](https://store.eyetrackvr.dev/products/2x-110mm-replacement-wires "ETVR store V4 JST SUR 110mm wire harnesses link (11/26)") or  
- You do my method described below, where you will DIY these wires.   
**This is NOT A EASY METHOD and you will need good eyes or something to view it closer like a microscope, magnifying glass or phone camera!**     
	1. Disconnect the last cable that is too short and put it to the side. You should now have a disconnected IR-LED PCBs with a E at the end.   
	2. Solder a 30 (recommended) or 28 AWG wire to the middle leg of the connector (blue arrow) where a wire is still plugged in.  
	> **It needs to be the middle pin of that connector!!**
 
	> I **STRONGLY** recommend pretinning the wire so that you have a easier time soldering to the tiny middle leg of the connector!  

	3. Test with a Multimeter if there is a connection between the middle leg and the other legs right and left of it. (There shouldn't be one)

	4. Flip the PCB over and solder another 30 (recommended) or 28 AWG wire to the exposed copper pad above the EyeTrackVR logo. 
	> I recommend pretinning the copper pad and the wire to have a easier time soldering.  
	
	> You should now have two loose wires.

	5. Take your IR-LED PCB with a E at the end and solder the wire coming from the middle pin of the connector to the exposed copper pad above the EyeTrackVR logo of the IR-LED PCB with a E.  
	> I would recommend pretinning the copper pad and the wire to have a easier time soldering.  

	6. Finally take the other loose wire that is already attached to the copper pad above the EyeTrackVR logo of the non E PCB and solder it to the other exposed copper pad, above the E, of the IR LED PCB with the E on it.   
	> I would recommend pretinning the copper pad and the wire to have a easier time soldering.  

	7. Repeat the **exact** same process for the other side.
	
> - The blue arrow show the middle leg of the connector where you need to solder the wire to.
> - The pink arrow shows the pad where the other end of the soldered wire of the middle leg of the connector needs to be soldered to.
> - The red arrow shows the pad where the other end of the soldered wire of the copper pad above the logo of the non E board needs to be soldered to.

![Wire soldered to the middle leg of the connector](./Images/Lens_mount_wire_soldered_to_middle_leg.jpg "Wire soldered to the middle leg of the connector")

![All wires soldered to their spot](./Images/Lens_mount_wires_soldered_fully.jpg "All wires soldered to their spot")

3. Plug both complete wire harnesses with all the leds into the connectors of the USB-HUB so that when you look at the connectors of the cables its:  
No cable, cable, cable and then no cable, cable, cable again (Like in the picture below)    
Then, plug the USB-HUB into your PC or power it through the USB-C Port without the USB-C to USB-A adapter, take a phone, open the camera and you should be able to see the IR-LEDs shining on the camera screen.  
Disconnect the wire harnesses after testing.
> X is no wire connected and O is wire connected.  

> If you don't see the IR-LEDs shining, do not panic yet, it can mean that you have a too good phone that filters out the IR light, like most modern phones. If you have a old or cheap phone use that or you should also be able to faintly see a pink or similar color dot on the IR-LEDs with the naked eye, if they are working.

> The second and third picture is from Renzath, because I forgot to take a picture of the shining IR-LEDs.

![Wire harnesses connected to USB-HUB](./Images/Lens_mount_wire_harnesses_connected_to_USB-HUB.jpg "Wire harnesses connected to USB-HUB")

![IR-LEDs shining](./Images/Lens_mount_IR-LEDs_shining.jpg "IR-LEDs shining")

4. Put the cameras onto the lens mount so that the ribbon cables go around the round edges and not the straight edge. After that put onto the IR-LED holders the IR-LED PCBs.  
You are then finished with the lens mounts  and can put them to the side for now.
> I **strongly** recommend to glue the camera in place as well as the IR-LED PCBs because they will probably fall out if you don't!

> - The yellow arrows show cable tidy ways to have the cable cleaner around the lens mounts. (Credit goes to Renzath for the ideas!)
> - The red dots show where to glue the cams into their holders.
> - The pink arrows show the direction of the ribbon cables of the cams.

![Places to tug the cable away](./Images/Lens_mount_cable_tidy_ways.jpg "Places to tug the cable away")

![Glue spots for the camera](./Images/Lens_mount_glue_spots_camera.jpg "Glue spots for the camera")

![Finished lens mounts](./Images/Lens_mount_both_finished.jpg "Finished lens mounts")

---

### Routing the cables through the headset

**UNPLUG YOUR INDEX FROM POWER BEFORE CONTINUING!!!**

1. Follow the ifixit guide on how to replace the eye tube till step 21. You can skip step 3 and 4 if you want.  
[ifixit guide link](https://www.ifixit.com/Guide/Valve+Index+Headset+Eye+Tube+Replacement/150426 "ifixit guide")
> On step 19 and 20 you can heat up the two places marked in red in the image below with a hair dryer to loosen the glue a bit and let it retain more stickiness as well as having a easier time removing the piece.

![Index places to heat to loosen the glue](./Images/Index_places_to_heat_for_glue.jpg "Index places to heat to loosen the glue")

2. Take the index so that the lenses look at you and locate the metal bar that is above the lenses. (You will need to look from the bottom of the index to see it)   
> The hidden metal bar is marked with a pink dashed line.

![Hidden metal bar shown with a pink dashed line](./Images/Index_hidden_metal_bar.jpg "The hidden metal bar is shown in a pink dashed line")

3. Take one extension cable and make sure that the silver pads are looking **downwards** and insert it **ABOVE** the metal bar, to the right from the yellow thing (marked with a red arrow). It should then come out on the other side, **left** of the metal wire ribbon cable (marked with a green arrow) (if you look from the exposed motherboard side onto the index) and look similar to the image below.
> It will probably be a bit tricky to get it **above** the metal bar and there will be resistance. To help out you can use your finger or something else, but finger recommended, to apply a bit more force just before the metal bar to help it slide **above** it.

> - The metal bar is marked with pink arrows.   
> - How the extension cable is inserted is marked with blue arrows.  
> - The yellow thing is marked with a red arrow.  
> - The metal wire ribbon cable is marked with a green arrow.

![How to put in the extension cable](./Images/Index_extension_cable_above_metal_bar.jpg "Extension cable is above the metal bar")

4. Now take your other extension cable and do the same things as in step 3 except that you insert the extension cable to the left of the yellow thing (marked with a red arrow) and let the cable come out to the right of the metal wire ribbon cable (if you look from the exposed motherboard side onto the index). It should then look similar to the image below.
> Use the same method as in step 3 if you can't get the extension cable **above** the metal bar.


> - The metal bar is marked with pink arrows.   
> - The paths of the extension cables are marked with blue arrows.  
> - The yellow thing is marked with a red arrow.  

![Both extension cables in place](./Images/Index_both_extension_cables_inserted.jpg "Both extension cables are in place")

![Both extension cables in place from the front](./Images/Index_both_extension_cables_inserted_view_from_the_front.jpg "View from the front with both extension cables in place.")

5. Take both connectors of the IR-LEDs and route them between the two lenses and out from the middle hole (marked in red) like in the image below. (Below the metal bar)
> - The purple arrow shows the path of the connector. 
> - The metal bar is marked with pink arrows.   
> - The paths of the extension cables are marked with blue arrows.  

> Ignore the installed lens mount on the right.

> Imagine like there are two connector cables in the image. I forgot to take a picture when both were inserted.

> Be careful not to pull on the extension cables and accidently removing one from their position.

![How to route the connector cable](./Images/Index_path_of_the_connector_cable.jpg "The purple arrow shows the path of the connector")

![View of all routed cables](./Images/Index_path_of_all_the_cables.jpg "View of all cables and how they are routed.")

![View of all routed cables from the front](./Images/Index_all_cables_inserted_front_view.jpg "Marked in red is the middle hole for the connector cables")

6. Do step 21 to step 14 backwards from the ifixit eye tube replacement guide, to put the front facia back on. And I would **STRONGLY** recommend to fix the cables with tape to the front facia so that they don't slip out in the next steps!  
[Link to the guide](https://www.ifixit.com/Guide/Valve+Index+Headset+Eye+Tube+Replacement/150426 "Link to the ifixit guide")
> Be careful that all cables stay in place and don't fall out of their position when putting the front facia back on.

> You can use whatever tape you want, I just had Kapton tape near me so I used that.

![Front facia back on with cables taped to it](./Images/Index_front_facia_back_on_with_taped_cables.jpg "Front facia back on with cables taped to it")

7. Flip the index over so that the lenses are looking at you again and make a loop with the extension cables, so that they route left and right around the lenses.
> The red arrows show the direction of the cables.

> Imagine there are the two black cables of the IR-Leds for the eyes and that the lens mount are there too. (I was trying the best placements for the extension cables when doing this picture and didn't route the IR-leds cables yet and forgot to take a new picture with them there)

![Extension cables routing closeup](./Images/Index_extension_cable_lenses_closeup.jpg "Extension cables routing closeup")

![Extension cables routing](./Images/Index_extension_cable_lenses.jpg "Extension cables routing full view")

8. Put back the eye tube gasket (step 9 backwards of the ifixit eye tube gasket replacement guide), while routing the part of the extension cable that are on the sides of the lenses **above** the gasket and the part above the lenses, **underneath** the gasket. (See Image)  
[ifixit guide link](https://www.ifixit.com/Guide/Valve+Index+Headset+Eye+Tube+Replacement/150426 "ifixit guide")
![Extension cables above eye gasket](./Images/Index_extension_cable_above_eye_tube_gasket.jpg "Extension cables above eye gasket")

9. Take the cameras of the lens mounts and put them into the camera extension connectors, while paying attention on which side the copper pads of the cable end are (Picture 1). Then put the extension cables into the camera extension connectors so that **both** - the camera extension connectors and extension cables - copper pads are **on the same side!!** **If that isn't the case you wont get a camera feed!**
> The pink arrows show the side of the copper pads of the cables.

![Extension and camera cables connected](./Images/Index_extension_cable_connected_to_camera_cable.jpg "Extension and camera cables connected")

10. Take the tape of the camera extension cables on the front facia off the index. Then take the camera extension connectors and push them with the camera extension cables to the top under the eye gasket, so that the camera extension connectors are barely visible under the eye gasket, while gently pulling the camera extension cables from the front facia, so that the cables length that got pushed under the eye gasket gets pulled out from the front facia.
> The pink circles show where the extension connectors are located. 

> Have the eye gasket under the plastic like in the second picture and not like in the first one on the left side!

![Camera extension connector placement](./Images/Index_camera_extension_connector_placement.jpg "Camera extension connector placement")

![Camera extension connector placement full view](./Images/Index_camera_extension_connector_placement_full_image.jpg "Camera extension connector placement full view")

![Extension cables pulled on the front facia](./Images/Index_front_facia_extension_cables_pulled.jpg "Extension cables pulled on the front facia")

11. Put the lens mounts onto the lenses, then the face gasket bezel back on, screw it in and put the tether cable back in. (step 8 to 5 backwards of the ifixit eye tube gasket replacement guide)  
> If you did step 4 and 3 of the ifixit eye tube gasket replacement guide, do them backwards too.

[Link to the guide](https://www.ifixit.com/Guide/Valve+Index+Headset+Eye+Tube+Replacement/150426 "ifixit guide")

![Face gasket bezel screwed back on with tether cable in place](./Images/Index_face_gasket_bezel_back_on.jpg "Face gasket bezel screwed back on with tether cable in place")

12. Now put the face gasket back on.   (After this you are done with this section and almost done with the guide, congrats!)
>I would recommend sliding the ipd eye slider to the minimum distance before putting the face gasket back, to make it easier to put it on.

![Face gasket put back into place](./Images/Index_face_gasket_back_on.jpg "Face gasket put back on")

---

### Installing the USB-HUB and connecting the camera extension cables

1. Take the 3D printed frunk frame, place the heat inserts into the holes of the frunk frame and heat them up with a soldering iron to melt them into the plastic.

> If you have a bit of plastic above the heat inserts, like I do in the image, you can optionally take a sandpaper or file to file the plastic down to make it flat.

![Frunk frame heat inserts](./Images/Index_frunk_frame_heat_inserts.jpg "Frunk frame heat inserts")

2. Take the index so that the lenses look away from you and you have the front facia looking at you.  
Remove the tape that holds down the black cables for the IR-leds, put them with the extension cables through the frunk frame hole on the top and screw the frunk frame into the front facia instead of the motherboard cover.

![Cables put through the frunk frame](./Images/Index_frunk_frame_cables_put_through.jpg "Cables put through the frunk frame")

![Frunk frame screwed in](./Images/Index_frunk_frame_screwed_in.jpg "Frunk frame screwed in")

3. Put the IR-leds cables into the connectors on the USB-HUB so that when you look at the connectors of the cables its:
No cable, cable, cable and then no cable, cable, cable again (Like in the picture below)
> X is no wire connected and O is wire connected.

![Closeup of the USB-HUB](./Images/Index_USB-HUB_IR-leds_cables_closeup.jpg "Closeup of the USB-HUB")

4. Now put the extension cables into the ESPs with the copper pads facing the ESP when inserting it. If you plan on having a DIY mouth tracker put a extension cable also into the middle ESP .
> **DO NOT PUT THE CABLES  LIKE I DID IN THE IMAGE!!!** Instead if you did like I told you in step 3 and 4 of the last section, put the cables into the ESP so that they don't do a loop and look like in the image of step 6!

>It can be difficult to insert the extension cables into the ESPs, that is normal. You can press down with something flat onto the extension cable just before the connector to get it more flat and closer to the ESPs connector and make the insertion easier.

![Extension cable inserted into the ESPs](./Images/Index_USB-HUB_extension_cables_inserted.jpg "Extension cable inserted into the ESPs")

5. Now unscrew the top screws of the USB-HUB, put on the top lid of the USB-HUB and screw all four screws into the holes, while paying attention that all the ESPs are in their right place and the hub is one continuos block, without spaces in between.

![USB-HUB completely finished with extension cables inserted](./Images/Index_USB-HUB_top_lid_screwed_on.jpg "USB-HUB completely finished with extension cables inserted")

6. Now put the USB-HUB into the frunk frame, while inserting the USB-A male port into the index's USB-A female port.

![USB-HUB inserted into the index](./Images/Index_USB-HUB_USB-HUB_insearted.jpg "USB-HUB inserted into the index")

7. **This step is completely optional and you can skip to step 8 if you want.**  
If you have excess extension cable, which you will most probably have, and want a clean look like in the image of step 6, do the steps below:  
Take the USB-HUB out of the index, unscrew the frunk frame, put some of the extension cable under the frunk frame, optionally tape it together (see picture), then screw the frunk frame back on and put the USB-HUB back.
> I used kapton tape because I had it near me, but you can use whatever tape you want, as long as it can not conduct electricity. (Take kapton tape if you want to be safe)

> You can also unscrew the top part of the USB-HUB and remove the extension cables from the ESPs, to make it easier. But be careful that the USB-HUB doesn't fall apart and that afterwards you insert the cables back and screw the USB-HUB back together.

![Extension cables taped together to make them shorter](./Images/Index_USB-HUB_extension_cables_taped_together_to_make_them_shorter.jpg "Extension cables taped together to make them shorter")

8. **If you plan on having a mouth tracker DIY or non DIY, you can skip this step.**  
Take the frunk brace without cam and screw it on with four screws into the heat inserts of the frunk frame.   
After that you are done with this guide and your setup is complete, congrats and have fun! (Hope this guide helped you out :3 )

![Frunk brace without cam screwed into the frunk frame](./Images/Index_frunk_frame_brace_without_cam_screwed_in.jpg "Frunk brace without cam screwed into the frunk frame")

9. Take the frunk brace with cam and screw it on with four screws into the heat inserts of the frunk frame.
> If you plan on having a DIY mouth tracker, put the extension cable and the wire pair **above** the frunk brace!

> If you **don't** plan on having a DIY mouth tracker, ignore the wire pair and the extension cable above the frunk brace.

![Frunk brace with cam screwed into the frunk frame](./Images/Index_frunk_frame_brace_with_cam_screwed_in.jpg "Frunk brace with cam screwed into the frunk frame")

10. **If you plan on using a DIY mouth tracker skip this step.**  
Now take your mouth tracker, position the attachment holes of the tracker with the ones from the brace, put a screw (M4) through all of them and screw a nut onto the screw. Then connect the cable from the tracker, if you have one, to the USB-C port that looks out of the USB-HUB.  
After that you are done with this guide and your setup is complete, congrats and have fun! (Hope this guide helped you out :3 )
> The loops around the brace (not available in the picture below) are there to optionally secure the cable with cables ties in place.

> The picture is from Renzath because I don't have a mouth tracker.

![Mouth tracker attached to the frunk brace](./Images/Index_mouth_tracker_attached_to_frunk_brace.jpg "Mouth tracker attached to the frunk brace")

11. **If you DON'T plan on doing a detachable DIY mouth tracker, skip to step 15.**  
Take your extension cable, put it into a camera extension connector, fold the cable back up to the spot you want and then tape the cable together, so that it stays in that position. **DO NOT MAKE A CREASE IN THE CABLE!!! IT SHOULD STILL HAVE A ROUND BEND AND NOT A 180° ONE WHERE IT TOUCHES ITSELF!!!** (See picture 2 on the left).   
Then put the camera temporarily  into the babble face cam prints and attach it temporarily to the holes at the end of the frunk brace. If you bend the cable down it should still be able to connect to the camera ribbon cable. If not, do the tape lower till it works. (Picture 2 right)
> I personally bend it to the middle of the USB-HUB.

> If you have a A to B cable like mentioned in the part list it will work perfectly fine and look very clean. If you don't have one, depending on your cable length, you can do the taping together or not, because you need to do a loop to insert the camera cable the other way so that both copper pins face the same direction.

> You can also tape the connector to the spot you selected to make it easier to tape the cable together. I used kapton tape for it but you can use whatever you want.

> The pink arrows show the direction of the copper pins of the cables.
 
![Extension cable put into the extension connector](./Images/Index_extension_cable_attached_to_extension_connector.jpg "Extension cable put into the extension connector")

![Extension cable taped together and check if ribbon cable of the camera can still attach to the extension connector](./Images/Index_extension_cable_placement_and_check_for_detachable_diy_mouth_tracker.jpg "Extension cable taped together and check if ribbon cable of the camera can still attach to the extension connector")

12. Take your JST SM connectors, or similar, crimp the cable pair and put the crimped cable pair into your **male** connector.
> I would recommend that you have enough cable so that the male connector can reach all the way to the top of the babble face cam print.

> Ignore all the stuff around the babble face cam print, I installed the JST SM connector after I finished the build.

![Wire pair crimped and connected to JST SM female connector](./Images/Index_JST_SM_connector_crimped.jpg "Wire pair crimped and connected to JST SM female connector")

13. You can now glue the extension connector and a **female** JST SM connector, or similar, to your desired place.
> I used a cable strap that I glued to the USB-HUB and then another strap to a extension connector and a JST SM connector, to be able to move it or remove it. See images below. 
>>You can also glue it directly to the USB-HUB if you want.

> When gluing the extension connector down, be careful to not glue the black latch, so that you can still open and close it, to slide and lock or unlock the extension cable.   
The pink arrow shows this latch.

![Cable strap cut into pieces](./Images/Index_cable_strap_cut_up.jpg "Cable strap cut into pieces")

![Connectors glued to the cut cable strap](./Images/Index_connectors_glued_to_the_cable_strap.jpg "Connectors glued to the cut cable strap")

![Cut cable strap glued to the USB-HUB and connector cable strap put onto it](./Images/Index_connectors_glued_to_the_USB-HUB.jpg "Cut cable strap glued to the USB-HUB and connector cable strap put onto it")

14. Crimp two new wires of the same color and put them into a **female** JST SM connector, or similar, **while paying close attention that if you connect the female and male connector, the wire colors match up!**  
(For the next steps, when the wire pair is mentioned, its referring to the new wires you just cut.)
> I would recommend keeping the new wires moderately long because you can always trim them later.

![Both JST SM connector_crimped and connected](./Images/Index_both_JST_SM_connector_crimped_and_connected.jpg "Both JST SM connector_crimped and connected")

15. Put the wire pair through the designed hole of the babble face cam left print. 
> The pink arrow shows the hole.

![Wire put through the babble face cam left print](./Images/Babble_wire_pair_trough_hole.jpg "Wire put through the babble face cam left print")

16. Take your perfboard and solder the black, brown or blue wire from the USB-HUB into the middle hole and then take your red or similar color wire from the USB-HUB and solder it to the rightmost hole. After that solder two other black, brown or blue wires, one left and one right of the middle wire and solder two red or similar color wires into the holes that are left. (See image below)
> You can now trim the USB-HUB wires down, before soldering, if you want. **There should still be enough wire that there is a bit of slack and its not completely stiff!**  
Alternatively you can also just stuff the excess wires into the babble face came print when closing it up.

> The pink arrows show the two wires coming from the USB-
HUB

> I would recommend pretinning the wires before soldering them to have a easier time soldering them.

> Ignore the two resistors for now.

![Top view of the perfboard](./Images/Babble_perfboard_top_view_USB-HUB_wires_marked.jpg "Top view of the perfboard")

17. Solder the resistors into the perfboard like in the image below. (Its the same image as above yes)

![Top view of the perfboard](./Images/Babble_perfboard_top_view.jpg "Top view of the perfboard")

18. Turn the perfboard 180° and follow the steps below: 
	1.  Bend the leftmost and second leftmost resistor leg to the leftmost soldered hole at the bottom. (red line)
	2. Bend the rightmost resistor leg to the rightmost soldered hole. (cyan line)
	3. Bend the second rightmost resistor leg to the second rightmost soldered hole. (green line)
	4. Solder the legs to their soldered holes.
		> **Pay attention that the wires soldered in the 				holes don't fall out while soldering the 					resistor legs to them!**
	5. Cut the resistor legs above the solder and don't throw them away just yet!
	6. Take one cut resistor leg, trim it to the size of three holes and solder it so that all three soldered hole that are left are soldered to it. (black line)
	7. (You can now throw the leftover resistor legs away.)
	
> This is the way I did it and is the easiest in my opinion, but you can also do it differently. (The wiring diagram is below)

> You can ignore the IR-LEDs in the wiring diagram if you want, they just show what the lose wires will be used for.

> - The red line are the parts that are connected to the red or similar wire of the USB-HUB.  
> - The black line are the parts that are connected to the black, brown or blue wire of the USB-HUB.
> - The green line are the parts that are connected to the second rightmost red or similar wire in this view.
> - The cyan line are the parts that are connected to the rightmost red or similar color wire in this view.
> - The yellow dashed lines show the placement of the two resistors.
> - The pink arrows show the two soldered holes where the wires coming from the USB-HUB are soldered to.

![Bottom view of the perfboard](./Images/Babble_perfboard_bottom_view.jpg "Bottom view of the perfboard")

![Wiring diagram](./Images/Babble_wiring_diagram.jpg "Wiring diagram")

19. Flip the perfboard 180° again. Take one black, brown or blue and one red or similar color loose wire you soldered onto the perfboard and put it through one of the holes on the side of the babble face cam mount prints. 
> I would recommend taking the leftmost red or similar color and the leftmost black, brown or blue loose wire for the left babble face cam print and the rightmost red or similar color and the rightmost black, brown or blue loose wire for the right babble face cam print.
> The pink arrow shows the direction the wires come out of the hole.

> (In the picture I took the rightmost red and black wire and put it through the hole of the right babble face came print.)

![Right IR-LED wires put through the babble face cam hole](./Images/Babble_IR-LED_wires_hole.jpg "Right IR-LED wires put through the babble face cam hole")

20. Cut two heat shrink tubes, put them onto both wires and solder the red or similar color wire to the longer leg of the IR-LED and the black, brown or blue wire to the shorted leg of the IR-LED. After that put the heat shrink tubes above the legs and the wire, and shrink them.
> I would recommend pretinning the wires before soldering them to the IR-LED to make it easier to solder them to it.
 
![Wires soldered to the IR-LEDs](./Images/Babble_IR-LED_soldered.jpg "Wires soldered to the IR-LEDs")

21. Do step 19 to 20 for the other side again, except that you don't flip the perfboard 180°.

![Both IR-LEDs soldered](./Images/Babble_both_IR-LEDs_soldered.jpg "Both IR-LEDs soldered")

22. Put the perfboard and the camera into the babble face cam mount.
> If you have a recommended 6 x 6 hole perfboard it will fit exactly into the space.

> Ignore the already in place IR-LED

![Perfboard and cam put into place](./Images/Babble_perfboard_and_cam_in_place.jpg "Perfboard and cam put into place")

23. Close the babble face cam mount print, slide in the babble face cam base and place the IR-LEDs into the holes right and left of the babble face cam mount print.
> If the base is loose and doesn't hold well, you can take a soldering iron at ~250°C and melt the edges of the face cam mount upwards towards the base. (See picture below)

> If the IR-LEDs don't fit, what will probably be the case, you can make the holes bigger by melting and forming them with a ~250°C soldering iron or you can sand the holes bigger.
>> If after that the IR-LEDs fit but don't hold in the holes anymore or you want to be extra sure, you can glue them to the holes.

> - The blue arrow shows the base.
> - The yellow arrows show the direction you need to melt and form the face cam mount.

![Modified babble cam mount](./Images/Babble_modified_cam_mount.jpg "Modified babble cam mount")

![Finished babble DIY mouth tracker](./Images/Babble_finished.jpg "Finished babble DIY mouth tracker")

24. Align the finished babble cam mount holes with the holes from the frunk brace, put a M4 screw through them and screw a nut onto it.   
After that you are done with this guide and your setup is complete, congrats and have fun! (Hope this guide helped you out :3 )
> The cam of the finished mount should look at your face if you are putting on the headset.

> I don't have a A to B extension cable so I need to make a loop with it to change the side of the copper pins so that both copper pins are on the same side.

![Finished GSRv2 build](./Images/Finished_GSRv2.jpg "Finished GSRv2 build")

![Full view of finished GSRv2 build](./Images/Full_view_of_finished_GSRv2.jpg "Full view of finished GSRv2 build")

---
---

## Hardware Troubleshooting
- **Not getting a camera feed**:
	1. Check if it isn't a software issue or misconfiguration on your side.
	2. If you have camera extension connectors, check that both copper pins look up or down, **but both need to be on the same side**.
	3. Check if you you put the copper pins facing down, to the ESP, into the ESP connector. (Don't ask me how I know...)
	4. Check the pads below the ESP if you didn't accidently solder D+ to D-  and D- to D+. (Don't ask me how I know...)
	5. Check if there are any shorts on the ESP pads.
	6. If you use a extension cable, change the extension cable of the not working feed.
	7. If it still doesn't work you probably damaged the ribbon cable of the OV2640 cam and you will need a new cam.
	8. If it still doesn't work after a change of camera, you probably somehow damaged the ESP and need to change it.
	9. If it **STILL** doesn't work then I don't know anymore and you are probably doing something wrong right now. (Let me know on Discord if you fixed it and its something not listed here and its not software but hardware and that can happen to others)

**If you have any other problem others might encounter and you fixed it and its not software but hardware, let me know on Discord so I can add it.**

---

## Software Troubleshooting
- **VRCFT with babble and EyeTrackVR do not work at the same time:**
	1. Change in VRCFT the **receive port** (not send port!!) to something else 			than 9001 - except 9000 - for example 9002.
	2. Check if port 9000, 9001 or your custom VRCFT receive port is used by 				something else on your system.
	3. Check the babble and VRCFT docs.
		> [Project babble docs](https://docs.babble.DIY/docs/intro "Project babble docs site (11/26)") and [VRCFT docs](https://docs.vrcft.io/docs/intro "VRCFT docs (11/26)")
	4. If you didn't find anything or couldn't fix it, ask in the EyeTrackVR or VRCFT discord server for help.
- **EyeTrackVR App is infinitely reconnecting to the cams:**
	1. Restart the app.
	2. If it didn't fix it, ask in the EyeTrackVR discord server for help.

**This section will probably never get updated again, but you can still send me on Discord the things you did to fix your problem, if it isn't listed here and if it isn't written somewhere and maybe I will put it on here.**