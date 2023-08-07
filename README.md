<h1 align="center">
    <img src="docs/images/MMlogo3.png" alt="Logo" width="100" height="100">
    <br />
    Mosaic system design guidelines
  </a>
  
</h1>

<div align="center">
  <br />
    <img align="center" src="docs/images/MM 02.JPG" alt="MM system" width="600" height="400">
  <br />
</div>



---

## About

Design files for use with the open source Mosaic system. All the footprints are verified and fully tested.
For more info, please visit <a href="https://mosaicsynth.com/index.php/system-info/">Mosaicsynth.com</a>

## Workflow

1. In kicad file -> new project from template -> user templates and select the one you need. (See getting started on how use the custom templates in kicad)
2. Start with the schematic and design your circuit. I have included some commonly used symbols so you can just copy and paste them to get started. It is good practice to make your schematic clean and easy to read. A few tips:
   -Always make sure you have at least a 2 space wire between components. This avoids having to connect components directly and makes it easier to move things around later.
   -Avoid points where 4 wires connect. This can be confusing when it's not quite clear wich wires connect to wich.
   -Only use right angle wires and space your symbols enough to make it easily readable.
   -Ground symbols always point down and power symbols always point up. (negative voltages like -12V are the exception and they point down)
   -Use standard symbols as much as possible, this helps with compatability. There are only a few Mosaic specific symbols like the input, output and power connector.
3. After your design is done you can delete any of the unused spare symbols and decide on the options on the lower part of the schematic template. You can include the logo and some JLCPCB specific parts like a production number placeholder or tooling holes for automated assembly.
4. When your schematic is fully done, triple check everything and move on to assigning footprints.
5. Create a PCB from the schematic and place the components off to the side for now. The template comes with the standard design rules for the JLCPCB 2 layer boards and some common trace widths and via sizes.
6. Start by placing your inputs,outputs, controls and power connector. I like to use a course grid of 2.5mm for this. The spacing between banana sockets should be at least 10mm, leaving you room for 4 sockets in the 50mm size.
7. Place the rest of your components on the bottom. I use 0805 and SOIC packages for some simpler modules but when you have a lot of components you can choose to go to 0402 and have your boards assembled. I generally find that with good component placement and some planning most designs will fit in the space between the bigger components. PCB design is kind of a dark art and there are so many ways to approach it so do your own research and look at lots of examples.
8. The groundfill on the top and bottom is always connected with vias around the mounting holes but it never hurts to add some extra vias to make sure both groundplanes are connected in several spots.
9. When you're done with placing and routing all the components on the bottom you can focus on the graphics on the frontpanel. You have 4 colours at your disposal, soldermask(generally black), silkscreen(generally white), uncovered surface finish(generally silver) and the bare FR4 board. I recommend keeping the graphics quite bold to make it readable.
10. Don't forget the scale that you're working on, a 50x50 module can get cramped quite quickly. Make sure you have enough space to use all the different functions and still be able to read any text or graphics. Going to a 50x100 or 100x100 is always an option.
11. Check footprints, component availability, routing, clearance and silkscreen legend. Repeat. Repeat. This part of designing a module requires a lot of back and forth and it's so easy to miss something. I always recommend to leave it for a day and check everything again.
12. Solder, assemble, make incredible music.
13. Share your project and let other know what you've made.


## Getting Started
Copy the content of the templates folder to the user templates folder:

    Unix: ~/kicad/template/

    Windows: C:\Documents and Settings\username\My Documents\kicad\template or C:\Users\username\Documents\kicad\template

    Mac: ~/Documents/kicad/template/

Go to <b> File → New Project → New Project from Template </b> and select the template you want from the user templates tab.

The templates come with all of the design rules and settings needed to design your mosaic system modules and have them manufactured by JLCPCB. If you use another manufacturer please make sure to check the design rules. 

All of the symbols have the preferred footprint already assigned so you can just duplicate the ones you need and after you have finished your design delete all the unwanted parts. 

Please make sure to <b>include the Mosaic logo and a link to the mosaicsynth.com website</b>. 

If you made something cool, please send us a picture. We would love to see what you have made!

## Support
<a href = "https://mosaicsynth.com/index.php/contact/"> contact form </a>

## Authors & contributors

Original files and system designed by [Mosaic modular synthesizers](https://github.com/Mosaic-modular).

## License

This project is licensed under the <a href="https://ohwr.org/cern_ohl_w_v2.pdf">CERN OHL v2 W</a> license. 

See [LICENSE](LICENSE) for more information.

