# Portable SquachWatch: Battery Case for the 2.8" CYD

> ## 🦶 A huge thank you to Talking Sasquach!
> This whole project exists because of **[Talking Sasquach](https://talkingsasquach.com)** and **SquachWatch**. Thank you for the firmware, for Squachy, for the [SquachWatch web flasher](https://squachwatch.com), and for making something this much fun to build around. This case is a thank-you back.

A compact, battery-powered 3D-printed case for running **[SquachWatch](https://github.com/skizzophrenic/SquachWatch-CYD)** on the 2.8" "Cheap Yellow Display" (ESP32-2432S028R). It holds a 3000 mAh LiPo with USB-C charging, an on/off switch and the touchscreen stylus, and runs for about 9–10 hours on a charge.

<!-- Preview picture: upload images/preview_v20.png and replace this line with ![Preview](images/preview_v20.png) -->

<!-- Add photos of the printed case here, e.g. ![Printed case](images/printed_front.jpg) -->

---

## Downloads

| I want… | Get it here |
|---|---|
| **The build guide (PDF)** | [SquachWatch_Portable_Build_Guide_v11.pdf](SquachWatch_Release_v20/SquachWatch_Portable_Build_Guide_v11.pdf) |
| **The Bambu Studio project** | [squachwatch_case_v20.3mf](SquachWatch_Release_v20/squachwatch_case_v20.3mf) |
| **STL files** for any slicer (all in one zip) | [SquachWatch_STL_v20.zip](SquachWatch_Release_v20/SquachWatch_STL_v20.zip) |
| **Release notes** | [RELEASE_NOTES.md](SquachWatch_Release_v20/RELEASE_NOTES.md) |
| **The SquachWatch firmware** | Flash it from your browser at **[squachwatch.com](https://squachwatch.com)** |

---

## Which file should I download?

It's the same case either way. Pick the file that matches your slicer.

### Bambu Lab printers (Bambu Studio or OrcaSlicer): `squachwatch_case_v20.3mf`
This is the easy one. It's a Bambu Studio project with **three plates already laid out** and the **colors already set**. Open it, click the plate you want, match the colors to your AMS, and print.

| Plate | What's on it | Pick it if you'll hold it… |
|---|---|---|
| **1: Horizontal** | Case, plain bezel, Squachy badge, SQUACHWATCH badge. Both badges go on the **back**, the lettering above Squachy | Sideways (landscape), USB end on the right. This is SquachWatch's default screen rotation |
| **2: Plain** | Case and bezel, no badges, no pockets | Any way. One color, no AMS needed |
| **3: Vertical** | Case, bezel, Squachy badge, SQUACHWATCH badge. Squachy goes on the back; the lettering sits on the **bezel** under the screen, in two big lines | Upright (portrait), USB cable at the bottom |

Plates 1 and 3 use 11 colors: the case color, 8 colors for Squachy, and cyan, pink and purple for the lettering. With fewer colors, you can merge similar ones when you map filaments, or print plate 2.

### Other printers and slicers (PrusaSlicer, Cura, etc.): the STL files
Download [SquachWatch_STL_v20.zip](SquachWatch_Release_v20/SquachWatch_STL_v20.zip) and unzip it. All parts are already turned the right way to print. Choose the set that matches the plates above:

| You want… | Print these STLs |
|---|---|
| **Horizontal** | `back_shell_horizontal_v20_stylus.stl`, `bezel_plain_v20_stylus.stl`, the 4 `text_*_horizontal_v20_stylus.stl` parts (SQUACHWATCH badge, goes on the back), the 8 `logo_*_v20_stylus.stl` parts (Squachy badge) |
| **Vertical** | `back_shell_vertical_v20_stylus.stl`, `bezel_vertical_v20_stylus.stl`, the 4 `text_*_vertical_v20_stylus.stl` parts (goes on the bezel), the 8 `logo_*_v20_stylus.stl` parts |
| **Plain** | `back_shell_plain_v20_stylus.stl`, `bezel_plain_v20_stylus.stl` |

Load each badge's parts together and answer **Yes** when your slicer asks to load them as one object with multiple parts. Then give each part its color using the filament table below. With a single-color printer, you can print the badges in one contrasting color or skip them. The plain set needs no badges at all.

**Filament slots** (the project file already has these set):

| Slot | Color | Parts |
|---|---|---|
| 1 | dark grey `#2B2B2B` | shells, bezels, `text_bg` (badge background) |
| 2 | dark brown `#3A1A06` | `logo_dark_brown` |
| 3 | brown `#7A3E10` | `logo_brown` |
| 4 | black `#111111` | `logo_black` |
| 5 | teal `#16505A` | `logo_teal` |
| 6 | tan `#F0B878` | `logo_tan` |
| 7 | white `#FFFFFF` | `logo_white` |
| 8 | red `#D22323` | `logo_red` |
| 9 | purple `#B967FF` | `logo_purple`, `text_purple` |
| 10 | cyan `#00FFF5` | `text_cyan` |
| 11 | pink `#FF71CE` | `text_pink` |

**Brim:** not needed. The project file has it turned off.

**Charging:** plug a USB-C charger into the charger module's port, the notch in the long side under the stylus tube. The CYD's own USB port is only for flashing firmware and doesn't charge the battery.

**Hardware for every version:** 4 × M4 × 6 × 6 mm brass heat-set inserts and 4 × M4 × 8 mm button-head screws. The badges glue in with a few drops of CA (super) glue.

---

## The build guide (PDF)

The [build guide](SquachWatch_Release_v20/SquachWatch_Portable_Build_Guide_v11.pdf) is written for people who have **never worked with electronics before**. Every step is explained in order, with photos and diagrams of the actual parts: what to buy, which tools you need, how the circuit works, how to set your multimeter (which dial setting, which socket the probes go in, and what reading to expect), how to flash SquachWatch onto the board, how to wire the battery, charger, switch and boost board, how to set the 5 V output, and how to put the case together. Every step has a checkbox and a test, so a mistake gets caught before it can damage anything. A troubleshooting table at the end covers the common problems. A few basic hands-on skills, like **tinning a wire** or using heat-shrink tubing, are easy to pick up from a quick YouTube search, and a two-minute video shows them better than any picture.

**Firmware:** the guide's first step flashes SquachWatch straight from your browser with the **[SquachWatch web flasher](https://squachwatch.com)**. No software to install.

---

## Customize
The case is made from a parametric Python model (every dimension is a setting you can change). The source files aren't posted here yet; open an issue on this repo if you'd like them.

---

## License

The case design, print files, build guide and source code are released under the **[MIT License](LICENSE)**.

- **Free to use.** Print it, share it, change it, remix it, and use it in your own projects.
- **Credit is required.** Anywhere you use, share or remix this design, credit **Dagromflomite** as the case designer, and keep the copyright notice from the [LICENSE](LICENSE) file with any copies.
- **No sales without Talking Sasquach's permission.** The case carries Talking Sasquach's Squachy artwork and the SquachWatch name. Those belong to Talking Sasquach and aren't covered by the MIT License. Because the case includes these logos, it **cannot be sold without express permission from Talking Sasquach**.
- **Font:** the SQUACHWATCH lettering uses the Orbitron font, which is under its own SIL Open Font License 1.1, not the MIT License.

## Credits
- **Squachy, the SquachWatch name and artwork:** Talking Sasquach ([talkingsasquach.com](https://talkingsasquach.com))
- **SquachWatch firmware:** [skizzophrenic/SquachWatch-CYD](https://github.com/skizzophrenic/SquachWatch-CYD) · web flasher at [squachwatch.com](https://squachwatch.com)
- **Font:** Orbitron by Matt McInerney, SIL Open Font License 1.1
- **Case design, build guide and source code:** Dagromflomite
