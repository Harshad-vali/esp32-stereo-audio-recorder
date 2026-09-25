# ESP32 Audio Device

Hardware design files for an ESP32-based audio recording device, including the KiCad project, PCB layout, schematic, manufacturing Gerbers, bill of materials, and design renders.

- **Revision:** v1.0
- **Date:** 10-03-2026
- **Designed by:** Harshad Vali
- **Organization:** Suretrust

## 3D Views

![3D Front View](https://github.com/Harshad-vali/esp32-stereo-audio-recorder/blob/a020a0ac3112970b35561fae102ded3ccc7f7b2d/front%203D%20view.png)
![3D Back View](https://github.com/Harshad-vali/esp32-stereo-audio-recorder/blob/cd2b9741f29df628836993a3b603f76e224dffac/back%203D%20view.png)
![3D Side View](side-3d-view.png)

## Overview

This board is an ESP32-based audio module designed around an **ESP32-WROOM-32** controller. The schematic integrates stereo digital microphone inputs, microSD storage, a real-time clock, and a regulated 3.3 V power system.

The PCB is approximately **62.5 mm × 44 mm** with a **1.6 mm board thickness**. The layout includes four mounting holes and dedicated areas for the antenna, microphone section, power circuitry, ESP32 module, and microSD card socket.

## Key Features

- **ESP32-WROOM-32** as the main controller
- **Two ICS-43434 I2S MEMS microphones** for stereo audio input
- **ST-TF-003A microSD socket** for removable storage
- **DS3232M RTC** for real-time clock functionality
- **TPS54331D** switching regulator for the 3.3 V power rail
- **Barrel-jack power input** with battery support
- **Push-button input** for the ESP32 control circuit
- Dedicated antenna keepout / antenna area
- Dedicated microphone section
- Four PCB mounting holes
- Manufacturing-ready Gerber and drill files

## Design Details

The schematic is divided into the following functional sections:

- **Power Circuit** — input power, filtering, protection, and 3.3 V regulation
- **ESP32 Controller** — ESP32-WROOM-32 and associated control circuitry
- **Microphone Section** — two ICS-43434 digital MEMS microphones
- **MicroSD Socket** — ST-TF-003A storage interface
- **RTC Circuit** — DS3232M real-time clock with battery backup

### Main Components

| Function | Component |
|---|---|
| Microcontroller | ESP32-WROOM-32 |
| Stereo audio input | 2 × ICS-43434 |
| Storage | ST-TF-003A microSD socket |
| Real-time clock | DS3232M |
| Power regulator | TPS54331D |
| Power protection | B340 Schottky diode |
| Power input | Barrel jack |
| Battery | Battery_Cell |
| User input | Push button |
| Inductor | 6.8 µH |

## PCB Layout

The PCB layout contains dedicated placement areas for the main functional blocks. The ESP32 is positioned near the upper portion of the board, with the microphone section located near the RF/antenna area and the microSD socket along the lower portion of the board.

The design screenshot shows **189 pads, 119 vias, 251 track segments, 53 nets, and 0 unrouted connections** in the displayed PCB state.

![PCB Layout](copper-layer-layout.png)

## Copper Layers

### Front Copper Layer

![Front Copper Layer](front-copper-layer.png)

### Back Copper Layer

![Back Copper Layer](back-copper-layer.png)

### All Copper Layers

![All Copper Layers](all-copper-layers.png)

## Assembly Layers

### Front Assembly

![Front Assembly Layer](front-assembly-view.png)

### Back Assembly

![Back Assembly Layer](back-assembly-view.png)

## Schematic

The complete design schematic contains the power circuit, ESP32 controller, microphone section, microSD interface, and RTC circuit.

![Schematic Preview](schematic.png)

## Board Dimensions

- **Board size:** approximately 62.5 mm × 44 mm
- **PCB thickness:** 1.6 mm
- **Mounting holes:** 4
- **Board outline:** Rounded corners

## Manufacturing

The `esp32 audio device gerber` folder contains the manufacturing outputs required for PCB fabrication:

- Front copper (`F_Cu`)
- Back copper (`B_Cu`)
- Front solder mask (`F_Mask`)
- Back solder mask (`B_Mask`)
- Front paste (`F_Paste`)
- Back paste (`B_Paste`)
- Front silkscreen (`F_Silkscreen`)
- Back silkscreen (`B_Silkscreen`)
- Edge cuts (`Edge_Cuts`)
- Plated-through-hole drill file (`PTH.drl`)
- Non-plated-through-hole drill file (`NPTH.drl`)
- Gerber job file (`job.gbrjob`)

## Files in This Repo

- `esp32 audio device main file/` — KiCad project files
  - `aduio device [roject.kicad_pro` — KiCad project
  - `aduio device [roject.kicad_sch` — schematic
  - `aduio device [roject.kicad_pcb` — PCB layout
  - `aduio device [roject.kicad_prl` — local KiCad project settings
  - `aduio device [roject-backups/` — KiCad backup archive
- `esp32 audio device gerber/` — PCB manufacturing Gerbers and drill files
- `esp32 audio device main bom.xlsx` — bill of materials
- `*.png` — PCB renders, layer views, assembly views, and schematic preview

## Tools Used

- **KiCad** — schematic capture and PCB layout
- **Excel / spreadsheet BOM** — component and manufacturing part information

## Opening the Project

Open the `.kicad_pro` file with **KiCad** to view and edit the complete project.

The project contains the schematic and PCB layout in KiCad-native formats, along with the generated manufacturing files.

## Notes

- The project files retain the original filenames from the supplied project archive.
- The Gerber files are generated from the supplied PCB layout.
- The BOM contains component references, values, footprints, quantities, manufacturer information, and part numbers.
- Backup archives are included in the supplied project and are not required for normal PCB editing.
