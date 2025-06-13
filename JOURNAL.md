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




