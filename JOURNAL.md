# 10/23/2026: Initial setup and planning
So first I want to know what type of material the case shell is going to be. Swaying towards resin but I don't have a resin printer so sourcing it is going to be hella anoying. I want that translucent floating effect though, so has to be ultra dark resin. 
I'm going to use a transparent OLED display, someting like this but higher resolution: https://www.amazon.com/clp/B0B8N46G24

So its going to use an ESP32-wroom chip and some i2s DAC
I wanna use inspiration from this: https://www.google.com/search?q=sony+nw+e507&oq=sony+nw+e507&gs_lcrp=EgRlZGdlKgYIABBFGDkyBggAEEUYOTIHCAEQABiABDIHCAIQABiABDIHCAMQABiABDIHCAQQABiABDIHCAUQABiABDIICAYQABgWGB4yCAgHEAAYFhgeMggICBAAGBYYHtIBCDIwODFqMGo3qAIAsAIA&sourceid=chrome&source=chrome.ob&ie=UTF-8

And then, I'm prolly going to use a one-way mirror. So I need one way mirror film, and I have to design the case from that. But first, let's get teh PCB started.
This battery:  103040 Lithium-Polymer (LiPo) Battery Pack 
idk tho
<img width="659" height="672" alt="image" src="https://github.com/user-attachments/assets/b2f70d75-b39d-4fa9-ac92-ed0948901158" />

https://lapse.hackclub.com/timelapse/XvpUFCtiKgLS

**Total time spent: 1.25 hours**

# 11/10/2026: Some changes + schematic
So i want to change how the design works. Having a floating under-screen layout would be very hard and annoying to do, as well as expensive. BUT, if I sort of replicate the layout of the winamp screen, that would be realtively easier to do as well as still looking retro-stylish. Like, look at this: <img width="519" height="237" alt="image" src="https://github.com/user-attachments/assets/544eb950-3cd7-4c58-8f55-c8296caad476" />

of course, it won't be a full 1:1 copy due to copyright restrictions and everything, but you get the gist of it.
So then I'm continuing to work on the schematic. 
So, I worked on the schematic. I added resistors to the SUBc, connected like the Ap2112k voltasge regulator, wired the battery (its just  apin), programmed at 500mA discharge. added a load sharing circuit osoi that you can operate while charging. Decided we r going to use a esp32 n16r8. So we isolated the PSSRAM pins. I added the MicrfoSD card, and im planning to use the CIrrus CS43131 DAC because it gives good audio quality while not being a power hungry moster. Also relatively affordable at $18, which is concerning in mas production.
<img width="1577" height="1069" alt="image" src="https://github.com/user-attachments/assets/adc81582-c30a-4fda-8250-38d500689d25" />

https://lapse.hackclub.com/timelapse/q2PGdiHObc6c
https://lapse.hackclub.com/timelapse/f0RfLnmQCNTE
**Total time spent: 3 hours**
