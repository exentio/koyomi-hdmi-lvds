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

### Forking guidelines
I hope that this design will inspire people to work on similar projects, and
that they'll be used as references to learn how to work on similar projects!  
If you want to make any contribution, you're welcome to fork and send a pull
request, as long as LLMs are not directly involved and you understand your
changes!  

You're also welcome to make changes to any part of this project to implement
different design choices, without having to send a pull request; however, if
your fork takes a completely different direction from Koyomi and breaks
compatibility, I kindly ask you to drop the name "Koyomi" from your project.
Please also remove every art on the PCB, if possible (wouldn't make sense to
have my face on a completely different project anyway).  
This can't and won't be enforced, so I'm just asking informally to please
respect this request, if you want to use my designs.  

### Commercial use
I purposely decided to allow commercial use for this project for two reasons: I
would be happy if modernized Vaio Ps and Koyomi were to be used in professional
contexts, and to let people distribute PCBs so everyone can build their own,
without having to sell parts myself, which is not something I can handle.  

If you plan to sell boards and parts, I only have these simple requests:  
- Please make them reasonably affordable and don't mark them up absurdly, I
want this project to be approachable from every point of view.  
- If you're profiting from reselling my designs, please donate something back
to the people who made the designs you're selling.  
- Don't remove any drawings/art on the PCBs, but you're allowed to add your own.  

None of these can and will be enforced, so I'm just asking you to respect the
time and hard work the other contributors and I have poured into designing
Koyomi.

---

Huge thanks to Arya ([@CRImier](https://github.com/CRImier)) for her help during most phases of the design!
