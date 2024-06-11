---
title: "Modular Synthesis"
permalink: /synth 
date: 2023-12-08 # Says "updated on DATE" in footer
#classes: wide
toc: true

---
<!-- Page title shows here, left aligned, defined in front matter -->
<hr>

A collection of the synthesizer modules I've built and the overall project status.

[![](/assets/images/synth/synth_saw_scope-thumb.jpg)](/assets/images/synth/synth_saw_scope.jpg)
Front panels with scope showing a sawtooth wave.

[![](/assets/images/synth/synth-back-thumb.jpg)](/assets/images/synth/synth-back.jpg)
Back panels made out of stripboard and aluminum.

# Summary

I'm building a modular synthesizer to learn about analog circuits and electronic music. 
*"But why?"*, you ask. Or similarly, *"I thought you were a chemist?"*

I'm not *completely* unqualified for this -- I did take a 300-level electronics elective in college, though it was mostly just doing linear algebra rather than working with real components. My lab partner and I build an extremely poor potentiostat. I've also built a small, Altoids-can, signal processing circuit for my grad school lab, which, amazingly, it is still in use today.

Honestly, I'm not entirely sure. There is something aesthetically pleasing about the orderliness of a schematic and it's materialization onto stripboard. Witnessing a few components turn the chaos of electrons into something approximately musical was too alluring to not give it a try.


I'm essentially building these "educational" modules designed by Moritz Klein available at [Erica Synths](https://www.ericasynths.lv/shop/diy-kits-1/) -- but with my own parts rather than from a PCB kit. Sometimes I'll make small modifications to the design because I want more or less of something, or because of component tolerances.

# Sound Demo

{% include video id="AdAZ86ObckE" provider="youtube" %}

What you're hearing in this video is three modules interacting with each other:
- a step sequencer is generating a control voltage (CV) sequence
- a quantizer (the mess on the breadboard) is "rounding" the CV to discrete values on a musical scale (chromatic, C major, or C minor)
- a voltage controlled oscillator turns the CV into a sawtooth or square wave audio signal

# Module Status

| Module     | Description              | Status |
| ---------- | -----------              | -------|
| Case       | Not technically a module, but important! It's wood. | **Complete**{: style="color: green"} 
| Power      | Transforms 24 V AC wall wart into +/-12 V DC.       | **Complete**{: style="color: green"} [[PDF]](/assets/pdf/synth/PSU%20schematic.pdf)
| Noise      | White noise generator. Filtered into pink and blue flavors.    | **Complete**{: style="color: green"} [[PDF]](/assets/pdf/synth/Noise%20schematic.pdf)
| Step Sequencer | Creates CV and gate sequences.                  | **Complete**{: style="color: green"} [[PDF]](/assets/pdf/synth/8-Step%20Sequencer%20Schematic.pdf)
| Voltage Controlled Oscillator                                    | Turns CV into volt/octave saw, square, or triangle waves. | **Complete**{: style="color: green"} [[PDF]](/assets/pdf/synth/VCO%20schematic.pdf)
| Voltage Controlled Filter | Low-pass filters audio signal according to envelope CV | **Breadboarded**{: style="color: orange"}
| Quantizer     | Rounds CV to selected musical scale. | **Breadboarded**{: style="color: orange"}
| Sample and Hold  | Samples a voltage and holds it for selected time. | **Breadboarded**{: style="color: orange"}
| Envelope Generator | Creates CV envelope for other modules       | **Not started**{: style="color: red"}
| Voltage Controlled Amplifier | Amplified audio signal according to envelope CV | **Not started**{: style="color: red"}



# Design and Build Process

An outline of my process in a nutshell:

1. Preparation
    - Research and understand a module via Youtube and lots of Googling
    - Order any missing parts
2. Prototype
    - Breadboard it with real parts
    - Test modifications if needed
    - Layout front panel parts on graph paper and choose size
3. CAD 
    - draw schematic in [TinyCAD](https://www.tinycad.net/) and export netlist
    - import netlist to [VeeCAD](https://veecad.com/) and layout all the parts onto stripboard
    - print build diagrams
4. Build
    - Cut stripboard tracks
    - Solder ICs, large components, small components, and wires
    - Cut metal for front panel, drill holes, and paint
    - Assemble front and back panels
5. Debug
    - Plug it in and troubleshoot all the mistakes that were inevitably made. 
        - "I forgot it" --> return to Build phase
        - "I messed up" --> return to CAD phase
    - Adjust any tuning points using case power supply


# Example Schematics and Pictures

Here are some pictures from the step sequencer build. Eventually, they'll go in their own post.
![](/assets/images/synth/seq-1.png)
<br><br>
![](/assets/images/synth/seq-2.png)
<br><br>
![](/assets/images/synth/seq-3.jpg)

# Resources

- Visit the [Erica Synths](https://www.ericasynths.lv/shop/diy-kits-1/) product pages to see available modules. They have details manuals with schematics available for free.
- Watch [Moritz Klein's](https://www.youtube.com/@MoritzKlein0) Youtube channel for a treasure trove of DIY synth pedagogy.
- Watch [LOOK MUM NO COMPUTER's](https://www.youtube.com/@LOOKMUMNOCOMPUTER) Youtube channel to cultivate some, uh, *chaotic, creative energy.*