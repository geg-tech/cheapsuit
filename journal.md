---
title: "Cheap Suits"
author: "egg_splats"
description: "A Hacker Card in the style and profile of a playing card"
created_at: "2025-07-10"
---
balala joker poker
## time spent: 9 hours
> thats a lot of drawing!

## 7/10/25 - cookin a card like no other
I had this concept cookin' for a while (since BakeBuild), and after seeing all of the Hacker Card PCBs being submitted recently, I was inspired to give my own take on the [guide](https://jams.hackclub.com/jam/hacker-card) with all of the new experience I've gained from my past hardware projects. <br/>
> warning: lore drop

I've had the idea of making some form of Hack Club playing card for a while (partly due to my crippling poker and balatro addiction), which I took with my BakeBuild submission a while back in April, making custom pixel art of Orpheus on a joker card inspired by Balatro. <br/>
Now looking back, I can definitely improve this idea through a Hacker Card, which contains a much slimmer form factor, custom graphics, and some form of interactivity with the NFC chip. I've improved my skills in hardware, art, and design across all of my projects, and I'm finally ready to give this idea it's due justice. <br/>

<img width="276" height="372" alt="hack-club-joker-large" src="https://github.com/user-attachments/assets/ca74f4df-6b7c-4f68-9005-ce93eb49842d" /> <br/>
> also inspired by the song ["Cheap Suits"](https://youtu.be/87i0RargAcA?si=6u_HbRG08Tu_UAo9) by mekaloton and OH MY GOD I LOVE THIS SONG SO MUCH AKJHDLSAHDASD I LOVE GAMBLING

To start off, I decided that the card will have the same dimensions as a Bicycle playing card, which is 2.5 inches wide and 3.5 inches tall (88.9mm tall and 63.5mm wide), with a 3mm fillet on the corners. I then went into my drawing software and made a quick mockup of how I wanted the card to look like. <br/>

<img width="826" height="543" alt="image" src="https://github.com/user-attachments/assets/f1a03013-6e23-4a20-be67-ddadbeaa4fcb" />

Since PCB manufacturers will make 5 copies of one PCB, I can't make 5 different cards with differing suits, so I'll have to merge all 4 into one cohesive design. I also want to design a hardcore electronic vibe with the card, using strong and sharp lines. <br/>
I plan on using *8* LEDs, but I also worry that the low power from the NFC will not be able to handle all of the LEDs at full power, which is why I also plan on having at *least* 4 LEDs to maintain symmetry and to match the suits. <br/>

From there, I started to brainstorm some more about the design, adding comments about how I wanted the card to look like. <br/>

<img width="1013" height="668" alt="image" src="https://github.com/user-attachments/assets/0d7bc46f-5821-47de-97e2-03bad54e5545" /> <br/>

I wanted to maintain a hardcore-cyberpunk aesthetic, but also incorporate some poker table or casino vibes with it, maybe using art-deco themes due to their similarity with cyberpunk of having sharp and defined lines. <br/>

but anyways i should work on the actual pcb <br/>

I'll be using EasyEDA for this project, since KiCad doesn't have many of the symbols/footprints of the components in the guide.
I followed the guide, but I swapped out the yellow 2V LEDs with [red ones](https://jlcpcb.com/partdetail/Hubei_KENTOElec-E6C0805UR/C2295), as well as adding 3 extra LEDs in parallel, resulting in 4 LEDs. <br/>

<img width="349" height="584" alt="image" src="https://github.com/user-attachments/assets/2a3404e7-d8ac-43ff-9109-668b2e801660" /> <br/>

I read on the NFC's datasheet that it can ideally output 2V and 5mA of current. The datasheets for the red LEDs were all in Chinese, but I read online that LEDs this size also work at about 1-2mA, so by Kirchhoff's Current Law it should be good (?? still unsure) <br/>

<img width="1054" height="585" alt="image" src="https://github.com/user-attachments/assets/5e964b00-5fa9-4ae4-9164-3a22a1981b13" /> <br/>

### hours spent: 2 hours planning and making schematic

## 7/11/25 - Importing to KiCad and drawing!!!!!!!
seven eleven day woohoo <br/>

Today I moved the PCB to KiCad since I'm more experienced in it (easyeda was also tweaking out on my browser). I imported all of the symbols and footprints to KiCad, so everything should also be the same. <br/>

I then asked whether or not my idea of having the 4 LEDs in parallel would work in *#electronics*, and was told that the LEDs would draw way too much current from the NFC chip, which would either leave me with very dim LEDs or damaging the NFC chip, so I just changed it to one LED <br/>
> very sad i know

<img width="1071" height="629" alt="image" src="https://github.com/user-attachments/assets/464ac35f-05a7-4176-9164-54c6c0051e9a" /> <br/>

Once I had the footprints imported, I moved into the PCB editor and routed the components. <br/>

<img width="899" height="616" alt="image" src="https://github.com/user-attachments/assets/d30efe3c-370b-46c4-9811-9e0846fb751f" />

After that, it was time to actuall design the card in Figma. <br/>
I took a screenshot of the PCB in orthographic mode and ported it to Figma, making a frame around the outline of the screenshot to hold the drawings in. I used the common card motif of having the rank and suit of the card in the corners, but instead of using a rank and suit, I used the Highway star and Hack Club's H logo, modified to fit the aesthetic of Undercity. <br/>

<img width="573" height="515" alt="image" src="https://github.com/user-attachments/assets/5034da1b-bf6e-4265-8f96-5033664bcccc" /> <br/>
> i spent a lot of time undercity-ifying the logo lol

Once I was happy with the corner, I worked on the center and suits. Using Figma's Stroke features, I made the checkered pattern found on poker chips with a couple circles and drew the suits with the Pen tool. I also made a small little square cutout to show the NFC chip that was going to be soldered on, which was specifically placed in the middle of the PCB. <br/>

<img width="938" height="1140" alt="image" src="https://github.com/user-attachments/assets/69aa95b9-9c56-4c85-9623-2eea4f8a246f" /> <br/>

The other corners of the face of the card looked a bit empty compared to the rest of the board, so I made a trim around the card, as well as adding cyberpunk-ish details to fill up the space and to add to the theme of the PCB. <br/>
To add variety, I made one side filled with white and the other an outline, which also nods at the corresponding suits they are near
> the white fill is next to the red/light suits (hearts and diamonds), the black fill is next to the dark/black suits (clubs and spades)

<img width="361" height="509" alt="image" src="https://github.com/user-attachments/assets/b0f287d4-0979-405a-9ac7-03a94967d3b1" /> <br/>

Once I was happy with the face, I quickly imported it into KiCad, exporting the suits as a separate file to make them shiny by making them exposed copper instead of just silkscreen. <br/>
After that, I started work on the back. I kept the cyberpunk theming with the trims, making two "tower" shapes with white and black fills, as well as adding extra details like stars or triangles to fill up the space. <br/>
I also added a small little via to serve as a possible lanyard hole for the extras :> <br/>

<img width="376" height="543" alt="image" src="https://github.com/user-attachments/assets/36c84ac8-72d9-4b39-9670-7177b29a7002" /> <br/>

anyways im tired <br/>
### time spent: 4 hours in KiCad and drawing

## 7/12/25 - MORE DRAWING!!!!! WOOO!!!!!!!
Today I spent the night drawing out the back side of the playing card. I didn't have as much of a vision for the back as the front (two general cyberpunk-ish towers vs 4 suits around the center), so I went back and forth spitballing ideas in Figma. <br/>

I decided to have some sort of circle in the middle for consistency and symmetry, and ended up making three different designs for the back (called *Moon*, *Compass*, and *Bicycle*) <br/>

<img width="1000" alt="image" src="https://github.com/user-attachments/assets/38dec45a-edde-437c-9403-73c13a54304e" /> <br/>

* The *Moon* was traced off an image of the moon, with lines radiating off like light. To fill the rest of the space, I used the Highway rainbow color thing from the magazine and pasted it in with the fill set to black and the outline to white.
* The *Compass* was made from the Highway star in the middle with a slash going through it, splitting it into black and white and north and south being marked. I was shooting for a "compass to Highway/Undercity" type theme, so I made the center look like a compass, with the rest inspired off a *literal Geometry Dash* level called *Azimuth* (go check it out it looks really pretty)
* The *Bicycle* was inspired largely by Bicycle playing cards, most notably having the three circles stacked on top of each other and intricate designs in the circles.

<img width="1280" height="720" alt="azimuth that geometry dash level" src="https://github.com/user-attachments/assets/97cbfbe7-a536-449b-8dfd-fc3f99336e37" /> <br/>
<img width="500" height="2000" alt="image" src="https://github.com/user-attachments/assets/2d5f674b-8645-4aa9-997d-e4882665cbc6" /> <br/>

I'm still unsure on what I'll pick for the final product, but I'm currently gravitating towards the bicycle design rn <br/>

There are also a bunch of ideas I have for this card, such as possibly adding 5mm copper pads to solder enamel pin posts (those poky bits) SMD style on to mount them on bags and such but that'll come later <br/>

### time spent: 2 hours drawing

## 7/13/25 - last time drawing then github stuff
i'll lock in today I PROMISE 🙏 :sob: <br/>

Today I asked more people on which backside I should use for my playing card and was met with more mixed opinions lmao <br/>
Many people on Slack (and myself) prefer the bicycle style, while my IRL friends on discord preferred the moon and compass style. I *could* try panelizing the cards into one of each design, but that could drive up costs by a ton. <br/>

In the meantime, I'm settling on the bicycle design :3 <br/>

<img width="520" height="610" alt="image" src="https://github.com/user-attachments/assets/50beb5de-7d81-45ed-b10b-1f260d801da1" /> <br/>

I also added a 5mm copper pad to hold a pin post (that poky thing i said yesterday) in the bottom corner. To help secure the card with pins, I can repurpose the lanyard hole to hole a small 3D printed enclosure for another pin post, creating two pin posts for the card to hold on by. <br/>
> here's a shitty sketch on what i'm talkin about

<img width="1080" height="430" alt="image" src="https://github.com/user-attachments/assets/a2799bda-cc09-4453-84eb-0596ad4ab928" /> <br/>

To add texture, I imported pictures of the four suits from Google into KiCad as copper, revolving them around the center using the *Array* function (command + T on mac). I also considered the Highway and Undercity logos, but I worry that it'll be too small for JLCPCB to manufacture as copper graphics. <br/>

<img width="542" height="355" alt="image" src="https://github.com/user-attachments/assets/632bbe74-4843-4f49-a0b6-0897fce2a0a1" /> <br/>
<img width="895" height="562" alt="image" src="https://github.com/user-attachments/assets/bf95f4ee-9d5d-4f77-91cb-8d5a6e97f870" /> <br/>

anyways here's the final pictures <br/>

<img width="574" height="592" alt="image" src="https://github.com/user-attachments/assets/11ccdfe9-7c66-4938-b542-31ec4582f9cc" />
<img width="493" height="591" alt="image" src="https://github.com/user-attachments/assets/28d92f0c-e426-4fca-b83b-9a9f73aad261" />

### time spent: 2 hour drawing, adding copper details, and finalizing the card

## 7/14/25 - cant sleep so im finishing this github
yeah i finished the github (its 3am i really cant be bothered to do ts rn 💔) <br/>
might render this stuff later idk <br/>

I filled out the rest of the GitHub, uploading the PCB gerbers and files to the repo and writing out the README.md <br/>

To calculate the costs, I went into JLCPCB and put in the card with the BOM for the assembly. I initially wanted red LEDs and all 5 of the PCBs to be assembled, but was *quickly* humbled by shipping and tax costs which shot the price well over the budget for a cheaper project ($10 + JLC coupon). <br/>

In the end, I had to sacrifice the red LEDs in favor of yellow LEDs due to the red ones being part of an "external library" which added a $3 dollar fee to PCBA. I also had to cut down on the amount of assembled boards to 2 PCBA in order to stay below 30 dollars. 
> also apparently the NFC chip in the tutorial is also part of an external library which is pretty weird; they were the most expensive component and had a $3 fee on top of that

I managed to get the cost under 30, but my order history on JLCPCB is now cooked (couldn't see the tax amount until after I "ordered" it, meaning I had to cancel each attempt right after adjusting to stay under 30 dollars) <br/>

anyways now I should be good for submitting :D
### time spent: 1 hour
