# Journal

# Information
- Title: "KeyboardV1"
- Author: An. D./its_kronos
- Description: A mechanical keyboard (*change later to be more specific*)
- Creation Date: 6/8/2025

# 6/8/2025
I started the general planning for the design criteria and also started sourcing some of the parts needed to create the keyboard. This took a lot longer than I expected, and I didn't realise how much actually had to go to making a full-sized keyboard, even after making a macropad before this.  

No images yet as it has mainly been a lot of researching and writing ideas, but here is what I have so far:  

* TKL layout (87 keys)
* One rotary Encoder with button (1 key, 2 additional GPIO)
* 10 macro buttons (10 keys)
* Total keys: 98
* Matrix size: 17x6
* total gpio for input keys (disregarding matrix): 10
* total gpio for input keys (regarding matrix): 23
* total gpio for input:25
* gpio for output: 2
* minimum gpio: 27  
  <br>
* USBC connectivity (JLCPCB part C2988369, costing 0.08)
* Cherry MX speed silver switches ([switches](https://www.aliexpress.us/item/3256802556025161.html?spm=a2g0o.productlist.main.3.5272XBJNXBJNCB&algo_pvid=733cf7a3-43e8-43cd-82f2-136f3680b36f&algo_exp_id=733cf7a3-43e8-43cd-82f2-136f3680b36f-2&pdp_ext_f=%7B%22order%22%3A%2260%22%2C%22eval%22%3A%221%22%7D&pdp_npi=4%40dis%21USD%215.97%215.77%21%21%215.97%215.77%21%402103244817494332643153371e9e82%2112000021935784957%21sea%21US%210%21ABX&curPageLogUid=iXUQrrv9lirg&utparam-url=scene%3Asearch%7Cquery_from%3A)) (for 47.67)
* white to light blue gradient keycaps ([keycaps](https://www.aliexpress.us/item/3256808583283524.html?spm=a2g0o.productlist.main.1.71ff517bRP8f6k&algo_pvid=5b86f0d0-7a3e-48a7-8888-0f7d0f246e88&algo_exp_id=5b86f0d0-7a3e-48a7-8888-0f7d0f246e88-0&pdp_ext_f=%7B%22order%22%3A%2249%22%2C%22eval%22%3A%221%22%7D&pdp_npi=4%40dis%21USD%2120.14%2119.94%21%21%2120.14%2119.94%21%40210312d517494334827192282e9b8e%2112000046593508858%21sea%21US%210%21ABX&curPageLogUid=8ZD65B0kDTa0&utparam-url=scene%3Asearch%7Cquery_from%3A#nav-specification)) (for 20.22)
* Diodes (JLC part C2099, costing 0.01 each), probable ordering via aliexpress (name: 1N4148W)  

Anyways, here are some goals that I have for the next session!!  
- Figure out a specific MCU to use and read the datasheets as well as sourcing all the parts required in this step
- Source some stabs
- Source a rotary encoder switch
- learn a bit more about a usb protection IC, should I get one, and if so, source it  

**Session length: 1 hour** (ish probably a couple minutes more excluding this journal entry)  

# 6/9/2025

Did a lot more research and sourced a LOT of components, and found out what remaining components i have to source before i can jump in (why is reading documentation so time consuming)  

* PCB mounted stabs [stabs](https://www.aliexpress.us/item/3256801500004993.html?spm=a2g0o.productlist.main.6.55e3UmS5UmS5rr&algo_pvid=cb85c6c7-b106-4f3e-9c36-baa96d7e8698&algo_exp_id=cb85c6c7-b106-4f3e-9c36-baa96d7e8698-6&pdp_ext_f=%7B%22order%22%3A%2224%22%2C%22eval%22%3A%221%22%7D&pdp_npi=4%40dis%21USD%215.26%215.06%21%21%215.26%215.06%21%402101c5b117495173725771833ed12f%2112000017133790601%21sea%21US%210%21ABX&curPageLogUid=SFQ0nj1x8eGF&utparam-url=scene%3Asearch%7Cquery_from%3A) (for 5.26 total)
* EC11 rotary encoder switch [rot](https://www.aliexpress.us/item/3256806989461658.html?spm=a2g0o.productlist.main.1.40763a52ybtfqK&algo_pvid=e489c4d5-419f-4c6c-acc1-da98479a699d&algo_exp_id=e489c4d5-419f-4c6c-acc1-da98479a699d-19&pdp_ext_f=%7B%22order%22%3A%2218%22%2C%22eval%22%3A%221%22%7D&pdp_npi=4%40dis%21USD%211.42%211.22%21%21%2110.17%218.74%21%402101ea7117495175123601420e8599%2112000039705433951%21sea%21US%210%21ABX&curPageLogUid=zXx0Y2mGFKb8&utparam-url=scene%3Asearch%7Cquery_from%3A#nav-specification) (for 1.42)
* RP2040, costing 1.11 on JLC (part number: C2040)
* ESD protection costing 0.11 on JLC (part number:C7519)
* ordering diodes via jlc with pcba since i'm VERY new to soldering  
  <br>
* must source voltage converter from 5v to 3v3
* 100nF capacitors required for power pins, SHOULD be close to the power pins (one per power) (9 needed)
* 1 uF capacitors required for internal voltage pin, SHOULD be close to respective pins (two needed)
* remaining for this stuff added to the "to source" list below  
  <br>
* Flash memory: JLC part "C97521" for 0.77
* Crystal oscillator: JLC part "C20625731" for 0.38
* Voltage converter: JLC part "C26537" for 0.26  
  <br>
* Oh yeah I also just learned about basic vs extended parts and now am double checking to see if i can find basic for anything that I didn't already
* Using JLC part "C2128" for diodes instead of other one as previous listed  

TO SOURCE:
* 100nF
* 1 uF
* 1x2 pin header
* 1k ohm
* 15 pF
* 27.4 ohm
* 10uF  

GOALS
* source stuff
* start wiring and pcb making so i can actually give some pictures!!!  

**Session length: 1 hour 30 minutes**

# 6/11/2025

Started this session with sourcing the parts as my goal was from last session

* 100nF - C1525
* 1 uF - C1848
* 1x2 pin header - [headers](https://www.aliexpress.us/item/3256804251926023.html?spm=a2g0o.productlist.main.3.6233P5h8P5h85F&algo_pvid=584f0c50-5b9e-4a9e-93a5-931e9de41a05&algo_exp_id=584f0c50-5b9e-4a9e-93a5-931e9de41a05-14&pdp_ext_f=%7B%22order%22%3A%2212%22%2C%22eval%22%3A%221%22%7D&pdp_npi=4%40dis%21USD%211.44%211.44%21%21%211.44%211.44%21%40210313e917496921766935236e1966%2112000029181612582%21sea%21US%210%21ABX&curPageLogUid=TUy5rYkuikyu&utparam-url=scene%3Asearch%7Cquery_from%3A) (for 1.44)
* 1k ohm - C85373
* 15 pF - C1548
* 27.4 ohm - C31439
* 10uF - C13585
* 5.1k - C23186

Yeah it became pretty easy for me to source parts after having done it for two days already, but at least i can now focus on the actual hardware!  
  
Finding information about the USB receptacle was pretty difficulty, and when I did it was pretty hard to digest, but I eventually figured it out (I needed a 5.1k ohm resistor pulled down to the cc pins)  
  
I was able to finish routing the usbc receptacle as well as the accompanying voltage convertor to the pi2040, but I still have to wire up the data and power lines to the pi before starting my key matrix  
  
routing progress:  

![image](https://github.com/user-attachments/assets/c3d5c06c-1677-47a1-b141-a4abd01a31d5)


GOALS:  
  
* finish routing RPI
* Finish key grid

**Session length: 1 hour 15 minutes**

# 6/12/2025

Started off this session with finishing up the wiring for the pi completely, and I eventually realized that I needed a 10K ohm resistor to be able to reset the mcu into BOOTSEL should I need to reflash it.

* 10k ohm - C25744
* usb protection IC replaced to C7419953 because it has a recommended usb layout in datasheet
* Switching USBC connector to C165948 because it has a footprint that is easier to recreate

The wiring was pretty simple since this was the second time reading the rp2040 hardware documentation (first time to source parts), so I pretty much just followed that to result in the following:

![image](https://github.com/user-attachments/assets/ede82057-66d4-47e3-ab64-acae1bc2f0ad)  

Afterwards, I worked on my switch matrix, which honestly took more time than I thought it would. Understanding the logic behind a switch matrix compared to just directly wiring distinct switches to a controller took quite a while and gave me a few mistakes when I made my first draft, but eventually I ended up with: 

![Matrix](https://github.com/user-attachments/assets/7c7ef2ac-0d3c-48f5-a162-43a891d877b2)

![image](https://github.com/user-attachments/assets/34949dcc-cf62-4eee-8960-09e636de5497)

After making the matrix, I decided that the keyboard would look better with the encoder on the right side of the macro keys, so I just switched it in the schematic sheet.  
  
At this point, my goal was to completely finish what I would have to do in the schematic side of things, so I could start the PCB, and the final step was to assign footprints.  
Assigning footprints to almost everything was a breeze, and locating which keys needed different sizings was pretty tedious, but when I tried to find a footprint for the USBC connection, I struggled.  

I spent a pretty long time researching to no avail, and eventually decided that my best option would be to just remake it in KiCad (which I decided to save for another time)

  (Note that the other time could be the same day, since these this process took 4.5 continuous hours)

GOALS:
- Custom footprint for usbc receptacle
- Double check the footprints for all components
- Start working on the PCB layout, start wiring if time permits

**session time 4:30**

Alright next session of the same day!

Made a footprint for the usbc receptacle!!! Took way too long to learn how to make my own footprint and match it exactly to the documentation (please add dimensioning kicad I'm begging you)

![image](https://github.com/user-attachments/assets/ba65efef-e31f-47ee-aa45-86a56dd34699)

GOALS:
- Add and create the custom schematic diagram for the usbc receptacle
- double check footprints for all components

**session time: 1:30**

# 6/13/2025

- remade pi2040 shape to include all power pins for decoupling
I was pretty surprised that the base shape for the pi2040 didn't include all the power pins, as this is a pretty important detail since each power pin requires decoupling capacitors.
However, I easily fixed this by just making the pins visible in the editor.

![image](https://github.com/user-attachments/assets/64b8f469-3d0b-455e-ab75-aa0c03692444)


- made usbc shape
This was overall pretty easy and didn't require much effort.

![image](https://github.com/user-attachments/assets/1fc4f043-7767-4354-9997-e80473bebffe)


- labeling key names
I decided that labeling every key and diode would make placing parts exponentially faster (it did), but it was pretty tedious and time-consuming.

![image](https://github.com/user-attachments/assets/040dc984-7e50-4862-bc84-9f6ab06013ac)


- triple checked all footprints and parts
Another big time dump was double checking all the footprints, but I did realize that some of my footprints for the cherry switches (like for the key for "\\") weren't the proper "U" sizing.

- started placing switches onto the pcb, but difficulty finding distance between the function keys
- used: https://keyboard-layout-editor.com/#/ to find distance in a standard layout
- finished placing every switch
- finished placing every diode
This by far was the most annoying part of the process, due to there being about 100 diodes to place. At least watching the switches line up so perfectly was pretty nice to watch.

![image](https://github.com/user-attachments/assets/2a956f54-ef34-40f7-abc0-6a3ffd0d8eb7)


GOALS:
- Place other components for PCB
- Start routing

**Session time 3:40**  

Session Two:
- Placed all of the other components 
- replacing 1uF with C52923 for smaller footprint

![image](https://github.com/user-attachments/assets/f6953bd4-07e7-4b4c-b7aa-6c84df0cb109)

- Attemped to route but failed horribly with the differential pair

GOALS:
- Change up the part layout
- replace data line protection part so I don't have to use vias

**Session Length: 1:30** (most of the time was spent on trying to make sure there's enough space, but I severely underestimated the size traces are)

# 6/14/2025

- Created a running list of all the parts used so far
* placed all of the parts again in a more organized way
* Tried to do differential pair routing but got confused with the wiring of the ESD protection, wondering if the impedence should be split among both sides.
* After quite a bit of research I realized that they are internally connected and was able to successfully route it
* Had some power symbols with 3v3 and 3.3 which made the nets slightly wrong
* wired all the rows and columns (but not to the chip)
* wired most (if not all) of the stuff for the chip

![image](https://github.com/user-attachments/assets/3d093d16-02ea-4f19-8420-6c927e3e8a14)

![image](https://github.com/user-attachments/assets/4473ea77-e7a5-404c-a7fb-a54bfa057573)

GOALS:
- double check the list for all running parts
- finish the routing and pcb

**time: 3 hours**

# 6/16/2025

* routed most of the rows and colums as well as rearranging the crystal so it can have a ground plane
* This was overall pretty easy, but sometimes the routing was a bit difficult, and I had to rearrange things so that the traces could fit properly
* I also sometimes had to think for a bit of a way to connect two tracks without boxing myself in for the other rows and columns.

![image](https://github.com/user-attachments/assets/9d4bcd47-f721-404b-a438-e6dccb867b57)

![image](https://github.com/user-attachments/assets/6a003983-ddbc-4f4a-8573-5da627815fea)


* learned about length matching for the USB port and did a bit of research about it as well as implementing it

![image](https://github.com/user-attachments/assets/5503a496-3a90-476a-9520-5c91d199b264)


GOALS:
- Finish the routing of the PCB
- Double check the list for all running parts

**TIME: 1 hour 15 minutes**

Next session:

- Completed the entire routing and ground planes for the PCB, and it looks pretty good in my opinion

![image](https://github.com/user-attachments/assets/429ff7d5-73bf-4d05-8168-fa9c0ca54332)

GOALS:
- Find and add 3d models for some of the footprints (key switches, ec11, stabs, usbc connector, etc.)
- Double check running list of parts (i'm too lazy to go back and read every journal entry again, but i'll have to do it before adding 3d models 😭 so I don't position the wrong one)

**TIME: 1 hour 45 minutes**

# 6/17/2025

* checked running list and footprints
* added 3d components
* wondered if the metal piece between stabs needed holes in the plate, so I researched about that using previous submissions for highway, but this wasn't enough so I researched more
* Found a youtube video showcases the removal of stabs from a plate, and found that it was mainly just for allowing easy of removal from plate-mount stabs, but since i'm using plate mount, it would be better to include them
* decided to include hotswap sockets from kailh in the build, and sourcing them here (they are the cheapest among amazon and aliexpress): [amazon hotswap](https://www.amazon.com/DUROCK-Mechanical-Keyboard-Switches-Hot-Swap/dp/B0B4W9YMGM?crid=2Y51HD288RY55&dib=eyJ2IjoiMSJ9.4jfJMBrnUtVfrD9ndIz5Dbi40PLToNJ99BfeLn_g7eB_ABNPZvI_Xcvj5FoM-rEzZp_zvr-HBeE7mUBm-gf11450UfCjV8KXsEJfF1trVdJL-xN9e6SvQqTDC5ccrEOQBiLsyrZ60dv400_XJG4TSNYdgsDcZObeIaZqZ1iRnndZd8XOcbHfX0cLM8CZALM-87yads8R6P6ZWO3rt93f3eIpi1l0SAIedWHgRYZ3cd8.GZ2YWH9UQ05T6cp9X6nW72pieisquQSfZQdeXucPvUs&dib_tag=se&keywords=kailh%2Bhotswap%2Bsockets&qid=1750200309&sprefix=kailh%2Bhotswap%2Bsockets%2Caps%2C105&sr=8-2&th=1)
* added footprints for hotswap
* sadly have to reroute pretty much every single row and column due to having slightly different plated through hole sizing (and underside pad/component placement)!

![image](https://github.com/user-attachments/assets/8ebd9eb1-bdd5-4c16-a18f-43938dc450fd)

**TIME: 2 hours**

*session 2*


* even after removing all row and column tracks, all the pins for the switches are reversed, so I also have to redo all the diodes, which means that it would most likely be faster to reroute the entire board rather than taking the time to find each individual track connected to a diode and remove it, as well as reposition the diode

![image](https://github.com/user-attachments/assets/f40cd1a3-7823-4c15-a6df-df678aa05e4d)

* was able to route all the columns to eachother (not the pi)
* moved each diode and connected it to each keyswitch
* routed up all the stuff near the pi except for the crystal (routing heavily depends on how tightly i can route the columns and rows)

![image](https://github.com/user-attachments/assets/c4147cc7-6c51-4e77-a30d-358028350199)

**time: 1h15m**

# 6/18/2025

* finished rerouting the entire board
* added courtyard to the usbc connector
* added some stuff to the silkscreen

![image](https://github.com/user-attachments/assets/5b092a67-7eba-4c54-8caf-365ffd6edfd9)

![image](https://github.com/user-attachments/assets/16c53832-31a3-4fa0-897d-7efc5f8b879a)

* generated the plate with a keyboard layout, and it'd be too big for most household 3d printers, so I'm asking if I'd be allowed to use JLC3DP

![image](https://github.com/user-attachments/assets/b93c3a6e-c6dd-40af-8136-d4e69358de97)

* had to scale down the plate since it was 10x bigger in fusion

![image](https://github.com/user-attachments/assets/fba323ab-72f3-4445-a322-fd802cea63f9)

**time: 3.5 hours**

*session 2*

* after checking the parts, replacing old stabs with [stabs](https://www.aliexpress.us/item/3256806342416791.html?spm=a2g0o.productlist.main.1.1f9130bdR4lI3e&algo_pvid=cf999406-4910-42b3-8749-b1a43b4eea55&algo_exp_id=cf999406-4910-42b3-8749-b1a43b4eea55-0&pdp_ext_f=%7B%22order%22%3A%22901%22%2C%22eval%22%3A%221%22%7D&pdp_npi=4%40dis%21USD%217.67%216.64%21%21%217.67%216.64%21%402103146f17502672974193867e9e69%2112000037543723482%21sea%21US%210%21ABX&curPageLogUid=G5Umy2OhrlOa&utparam-url=scene%3Asearch%7Cquery_from%3A) because the old ones had pictures that didn't look like plate mount, but in the product here it clearly says plate mounted
* Did some research on whether the pcb would need to be supported or not, but I decided it would be for the best if they were and found standoffs i could use [standoffs](https://www.aliexpress.us/item/3256807945933515.html?spm=a2g0o.productlist.main.1.707337b6g0g4X3&algo_pvid=264d64cd-d181-40d5-8715-bf0f00bebe19&algo_exp_id=264d64cd-d181-40d5-8715-bf0f00bebe19-0&pdp_ext_f=%7B%22order%22%3A%22625%22%2C%22eval%22%3A%221%22%7D&pdp_npi=4%40dis%21USD%211.93%211.66%21%21%211.93%211.66%21%40210318ec17502700244453566eedb7%2112000043917409280%21sea%21US%210%21ABX&curPageLogUid=U4VRdFXwYqE0&utparam-url=scene%3Asearch%7Cquery_from%3A#nav-specification)
* resized edge.cuts and adding mounting holes, and this part took way too long because theres no tool for distancing like there is in many cad programs, so I had to align everything perfect with the grids, which was pretty annoying (also had to reroute and reposition the USBC receptacle due to board resizing)

![image](https://github.com/user-attachments/assets/8c771ce3-d565-4801-8124-81c35a15bb03)

* Setup wakatime for kicad and fusion

**time 1h45m**

# 6/19/2025

* i'm pretty new to cad so making the case will take quite a bit
* finished the bottom part of the case with holes for screws

![image](https://github.com/user-attachments/assets/f029cd76-f0ca-4128-8e8e-adba002e5771)

* added bigger holes at the bottom for the head, with the following sourced M3 screws: [screws](https://www.aliexpress.us/item/3256808318392916.html?spm=a2g0o.productlist.main.9.b3bd48ab2IfbUm&algo_pvid=13938592-212d-450d-895e-c381feab57e0&algo_exp_id=13938592-212d-450d-895e-c381feab57e0-8&pdp_ext_f=%7B%22order%22%3A%22164%22%2C%22eval%22%3A%221%22%7D&pdp_npi=4%40dis%21USD%211.58%211.27%21%21%211.58%211.27%21%402101effb17503475022117786e4c80%2112000045477825083%21sea%21US%210%21ABX&curPageLogUid=zDcpBpa3QEWD&utparam-url=scene%3Asearch%7Cquery_from%3A)

![image](https://github.com/user-attachments/assets/dc3d22d6-1e64-4817-af40-dd03e69e3008)

* will be adding the hole for the usbc connector last, so i can align everything in the assembly and put the cutout accurately

**time: 45m**

* finished top part of the case, except for the spaces between escape and other keys, arrow keys, etc.
* I'll add that part after finishing up with the assembly

![image](https://github.com/user-attachments/assets/139ecbe4-8932-4bc3-9784-068b7946ec22)


* full assembly before keycaps, stabilizers, colouring, and polishing

![image](https://github.com/user-attachments/assets/a8ce2b20-449b-45a9-8aa4-b216989ab48f)


* couldn't find a stabilizer model i could use, so i'm going without it
* added all keycaps, but this took way too long since i was initially moving and copying them one by one before I learned I could use rectangular patterns

![image](https://github.com/user-attachments/assets/e3dadd19-bf5f-4815-a6b2-e75db6992d5c)

* polished up the top part of the case so that the gaps are filled

![image](https://github.com/user-attachments/assets/9ec47aee-a5ee-41a9-b643-846d041a359b)


**time 3h15m**

# 6/20/2025

* redoing all the keycaps because it is the only way for me to unlink all of them so i can apply the custom colors
* found different keycaps for all the u sizes after some searching
* the new models for the keycaps were all scaled up and meshes, so i decided to find other ones since i couldn't convert them prismatically (fusion free version sob)


![image](https://github.com/user-attachments/assets/99e01caf-16ad-4aff-be17-12c80b99accd)


* after doing some more digging i found different keycap models (we love reddit) which had everything for each row with the [link](https://github.com/ConstantinoSchillebeeckx/cherry-mx-keycaps) and this included keycaps for different rows, so I decided to restart again for the next session


**time:1h45m** (mainly because I spent so much time restarting and searching)

* turns out all the files i found before were just mesh-based too, which wasn't really helpful
* learned that all STL files are meshed based, so I will download the STEP file from the github repo instead
* Used the step file instead and it worked so much better, and i was able to get a lot of keys placed down, and the keyboard is starting to look really good

![image](https://github.com/user-attachments/assets/56596862-00d4-4fda-8ef8-40cfcbefd928)

**time: 45m**

# 6/21/2025

* finished putting all the keys and colouring, and imported my rotary encoder cap from another project (hackpad), but didn't know which ec11 rotary encoder type comes with hackpad, due to there being so many different variations, so I asked which specific type it is and tried to do some research
* the type is the ec11e 
* since the 3d model on the pcb in the assembly is not an ec11e (and since I couldn't find an ec11e model, just one for a general ec11 encoder) i had to carefully go by the measurements on the datasheet to design my cap
* spent quite a long time designing the hole for the USBC connector, making it pretty tight with some clearance just incase

![image](https://github.com/user-attachments/assets/625d0176-20c8-4747-a23c-d5aca68acc9e)

![image](https://github.com/user-attachments/assets/d2b17433-38c8-4fca-977b-42a6999e0e49)

**time: 1h30m** (excluding some time about asking details to improve my case)

* sourced some gorilla superglue gel I would use for the standoffs in the plastic after doing some research about which glue works well with PLA
* started splitting all the prints so they could be printed with printing legion

![image](https://github.com/user-attachments/assets/063d32d5-26c1-44ad-9836-c4277dfbb908)


* decided not to split the plate because splitting it would make it pretty difficult to print secure during shipping, so i'll probably use JLC3DP for this one part
* discovered that JLC3DP PLA print has to have a minimum of 1cm height and their capabilities don't support 1.5mm height, but after some research I discovered that many people use FR4 as material for their plates, so I did a big brain move and exported the plate sketch as a DXF and imported it into kicad and just exported as gerber!

![image](https://github.com/user-attachments/assets/08836b28-a7f4-4a25-8622-d8d2d5e98e23)



* turns out that JLCPCB is pretty expensive for getting plates, so instead I decided to just get it via a resin print, which can support 1.5mm thick prints
* replacing 1k ohm with C11702, since it's a basic part
* turns out that no matter what I do the weight will be over 1.5 KG for the board alone, so I have to pay about 40 dollars shipping to the US, which means that the rest of the board is unfeasable to design
* i will finish a draft of the code and create a BOM, but that's about it since I don't have the means to pay the exorbitant amount of money required


**time: 30m**



