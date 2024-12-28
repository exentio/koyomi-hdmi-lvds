# Project Koyomi - HDMI-LVDS adapter

This is part of the development of Project Koyomi, read [this blog post](https://blog.exentio.sexy/2023/12/11/project-koyomi-planning.html)
for more.  
The purpose of this adapter is to test and play around with the display of the
Vaio P before further development of the motherboard and to be used in
hand-wired builds.  

**⚠️ WARNING: at the moment of writing, the board hasn't been tested.**  

The board uses Texas Instruments' SN75LVDS83B LVDS transmitter and TFP401 DVI
receiver to send video out to the display.  

The display connector is made by I-PEX, and the model numbers are
`20374-030E-31`/`20374-R30E-31`, they're the same but the 0 variant seems to be
more common.  
The display, in my case a LT080EE04100 by Toshiba (it should be the same for
all Vaio Ps), has no backlight driver, and for that the backlight pins are
broken out, allowing testing of different drivers.  

Reference timings from [this post on patters' blog](https://pcloadletter.co.uk/2012/07/06/iemgd-for-vaio-p/),
huge thank you!  

Pixel clock in Hz: `83600000`  
Horizontal active pixels: `1600`  
Horizontal front porch: `32`  
Horizontal sync time: `65`  
Horizontal back porch: `97`  
Horizontal blank time (HFP+HST+HBP): `194`  
Vertical active pixels: `768`  
Vertical front porch: `1`  
Vertical sync time: `1`  
Vertical back porch: `8`  
Vertical blank time (VFP+VST+VBP): `10`  

---

Huge thanks to Arya ([@CRImier](https://github.com/CRImier)) for her help during most phases of the design!
