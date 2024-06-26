---
layout: post
title:  Filco Zero Modding
date:   2023-04-17
updated: 
tags: blog
splash_img_source: /assets/img/blogs/Filco0/all_stab_wires_ok.jpg
splash_img_caption: They're not pretty but they do work and that's all I wanted.
permalink: /posts/:title/
---

# Filco Zero Modding

I've finally taken the plunge to start modding my Filco Zero. I was scared to mod it as there were not very many replacement parts when I looked into it a while back (read 6+ years ago). But now with the Matias stabilizers, the easy availability of Costar stabilizers, and new DCS Alps sets available, I wanted to get the Zero updated.

I did cover some of my mods in a geekhack modding log but I wanted to expand on this so I had a reference in the future. Also figured it might be an interesting read.

&nbsp;

## Goals
1) ~~I wanted to get the stabilizers working with the Cherry stem stabilizers that DCS uses.~~

2) ~~I want to address the stabilizer rattle.~~

3) ~~I want to get the DCS Alpine Winter set I have laying around working on to my keyboard.~~

4) ~~I want to address the ping on the upstroke.~~

5) ~~I want to get the Pegasus Hoof working on VIA.~~

6) I want to replace the cable with something detachable.

So far, I've succeeded in goals 1 through 4. Those were covered in my [modding log that I posted on geekhack](https://geekhack.org/index.php?topic=119951.0). Essentially I had to rebend the stabilizer wires, modify some of the stabilizer inserts, and sand downt he spacebar.

&nbsp;

## Tools 
It's really nice that my hobbies work together sometimes. I was able to use a lot of the mini painting tools for the modding work in the GH thread.

* Infini standing sticks
* Sanding swizzle sticks
* Busted army painter brush
* 2 regular ass needle nose pliers
* The same krytox 205g0 I've been using forever
* Painters Tape

&nbsp;

## Testing
There was a suggestion that there are issues with the DCS Alps sets not fitting correctly on Row 3 (homerow). People have reported that the caps might impact the wrong part of the switch and cause the travel to be shortened way more than it's supposed to. I did not encounter that issue with my caps.

&nbsp;

## Tape Modding
Something I really didn't like about this keyboard is the horrible upstroke ping when the switches were actuated. I was going to buy a foam mat or PE foam to put into the keyboard case but stumbled into the tape mod idea. Figured this was easy enough to try since I already had the tape on hand. I tried it out and it looks jank/10 but it works at like an 7/10. I expected nothing so I was very surprised. I am still interested in buying a foam mat or PE foam to see if I can remove the tape and just rely on those foam options. I just want to remove the ping though.

&nbsp;

## Upcoming Work
I do want to update this blog to include my adventures in DIY cable making and if I can get the Zero to work with Via/Vial. More to come.

&nbsp;

## Update Dec 24 2023 - Got Via Working and a Detachable Cable
Thanks to [speedycake in LightningKeyboard's Discord server](https://geekhack.org/index.php?topic=119951.msg3177357#msg3177357) I was able to get Via working on the Pegasus Hoof controller. The firmware was ported over to QMK earlier in 2023 but I didn't realize how to get it working. So essentially the steps I followed were:

1) Set the controller to DFU mode with the magnetic reset
   
2) Download the Pegasus Hoof firmware from [this website](https://www.caniusevia.com/docs/download_firmware)

3) Use the QMK toolbox tool to flash the firmware. I'd need to select the atmega32U2


I confirmed that I have a 2013 Pegasus Hoof [from my old build log when I modded my Zero](https://geekhack.org/index.php?topic=71855.0). And confirmed my controller was running an old [EasyAVR firmware](https://geekhack.org/index.php?topic=51252.0). So I grabbed the 2013 Pegasus Hoof firmware.

Next I booted up my Windows Virtual Machine and installed [QMK toolbox](https://github.com/qmk/qmk_toolbox). Then reset my controller with a magnet and passed the USB input into the VM. I set the MCU type to atmega32U2 and then flashed the hex file from Caniusevia.com. Once it's done, I just booted up Via and it worked! 

I'm very happy to have my decade old controller and keyboard in the modern age!

Lastly, thanks to some new interest in Filcos, some friends are putting together a little buy from [KeebStuff](https://keebstuff.com/) so that we can get a Filco cable that attaches into the Filco board connector and terminates into a female LEMO end. That way I can have one LEMO cable for all of my boards...wait, I need to figure out what to do with my Kishsaver now. That's another project for another day.