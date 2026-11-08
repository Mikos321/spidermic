# Spidermic
 ![Spidermic](img/spidermic_sphere.JPG)
Spidermic is an low cost circular microphone array. For use in audio measurement applications such as [ambisonics](https://github.com/AppliedAcousticsChalmers/ambisonics-for-insta360-pro).
## Features
* Low cost spherical microphone array with up to 15 omnidirection microphones.
* Plug and play compatible with [Minidsp MCHstreamer lite](https://www.minidsp.com/products/usb-audio-interface/mchstreamer-lite).
* 15 PDM Infineon M73D122V01 Microphones.
## Repository Organization
* [kicad/spider-array-main-v3](kicad/spider-array-main-v3) - KiCad schematic, layout and fabrication files for the main breakout board
* [kicad/spider-array-mic](kicad/spider-array-mic) - KiCad schematic, layout and fabrication files for the microphone boards
* [mounts/](mounts/) - STL Files for the ring mount.
## Documentation
### BOM
For an complete mic set you will need:

| Part          | Amount        |
| ------------- | ------------- |
| [Microphone board](kicad/spider-array-mic) |          15   |
| [GCT 0.5 mm pitch 6 pin oppside Flatflex cable 152mm](https://www.mouser.se/en/ProductDetail/640-506-D0152A4064T)  |          15   |
| [Main breakout board](kicad/spider-array-main-v3)  |           1   |
| [MiniDSP MCHstreamer lite](https://www.minidsp.com/products/usb-audio-interface/mchstreamer-lite)  |           1   | 

### Minidsp MCH-Streamer
The main board of the mic array is mounted on top of a MiniDSP MCH-Streamer connected to J2. 
Since the Infineon microphones work with 1.8v logic and the MCH-steamer only outputs 3.3v, I used Ti-SN74LVC8T245
level shifting from 3.3V to 1.8V of the data and clock signals to and from the MCH-streamer.
### Boards
Due to mems microphones being somewhat fragile, it is recommended to use [JLCPCB](https://jlcpcb.com/) board assembly when ordering boards.
Follow the [JLCpcb KiCAD file preperation guide](https://jlcpcb.com/help/article/how-to-generate-gerber-and-drill-files-in-kicad-9) and the [JLCPCB step by step ordering guide](https://jlcpcb.com/help/article/how-to-generate-gerber-and-drill-files-in-kicad-9)

![Microphones](img/spidermic_close.JPG)
