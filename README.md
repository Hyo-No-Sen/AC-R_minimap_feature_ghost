# ACR_minimap_features_ghost_r0.6 Manual

The original is in Japanese.
Other languages are machine-translated. Sorry if anything is hard to read.

## Table of Contents

- [Quick Start](#quick-start)
- [How to Launch](#how-to-launch)
- [How to Create a Stage Map](#how-to-create-a-stage-map)
- [How to Display the Ghost Car](#how-to-display-the-ghost-car)
- [How to Hide the Ghost Car](#how-to-hide-the-ghost-car)
- [Other Operations](#other-operations)
- [Special Driving Tracks](#special-driving-tracks)
- [Notes](#notes)
- [Cautions](#cautions)
- [Disclaimer](#disclaimer)
- [Plans](#plans)

## Quick Start

As a sample, the `master_maps` folder contains driving tracks for the Col de Turini stages in Monte Carlo. If you want to check that it works right away, follow [How to Launch](#how-to-launch), then drive any Col de Turini stage in Time Attack. You can delete these samples when you no longer need them.

## How to Launch

1. Extract the zip file and place it in a folder of your choice (e.g. `c:\apps\ACR_MINIMAP`)
2. Launch `ACR_MF_GHOST.exe` (e.g. by double-clicking it)
3. Launch Assetto Corsa Rally

## How to Create a Stage Map

1. Follow [How to Launch](#how-to-launch)
2. Right-click the minimap window (the semi-transparent black square) and check "Record track"
   - It is checked by default
3. Select the stage you want to make a map of (in Time Attack, etc.) and start the race
4. Drive carefully so that you don't go off course, and finish the stage
5. Right-click the minimap window and click "End race" (**important**)
   - If you don't click "End race", the driving track will not be saved to a file
6. A JSONL file is saved in the `recorded_track` folder; copy it to the `master_maps` folder
7. From the next time you start the same stage, the course (driving track) is displayed on the minimap

## How to Display the Ghost Car

1. Follow [How to Create a Stage Map](#how-to-create-a-stage-map) and save a driving track to a file
   - Check that the driving track has been saved in the `recorded_track` folder
2. Start the same stage with the same car again
3. The ghost car is displayed in the minimap window
4. When the stage ends, click "End race" and the driving track of this run is saved to a file
5. From the next time you start the same stage with the same car, the driving track with the faster stage time is displayed as the ghost
   - In other words, you can always practice against your own course record
   - Whenever you set a new stage record, be sure to click "End race" (a way to detect the end of a race has not been found, so this operation is required)
   - If you know a way to detect the end of a race, please let me know

## How to Hide the Ghost Car

Right-click the minimap window and uncheck "Use ghost car".

## Other Operations

- Right-click the minimap window and choose "Exit" to save the current settings and quit
- Left-click and drag on the minimap window to move it
- Left-click and drag at the edge of the minimap window to resize it
- Left-click and drag the car icon to move it
- Turn the mouse wheel over the minimap window to zoom in and out
- If you pause Assetto Corsa Rally while driving a stage, you can scroll the map freely with middle-click and drag. Unpause, or click "Car position" at the top right of the minimap window, to return to the car's position

## Special Driving Tracks

Driving tracks stored in the `special_ghost` folder are displayed with the highest priority. In other words, it is the place to store your best driving tracks.

## Notes

- In short, driving tracks are displayed as a "stage map" and as a "ghost". Only the role changes depending on the folder you store them in.

## Cautions

- Set Assetto Corsa Rally to borderless window or windowed mode. Fullscreen does not work.
- If the right-click menu of the minimap window does not appear, left-click the minimap window once
- If you can no longer control Assetto Corsa Rally, left-click the game screen
  → Keep in mind which window is currently active
- The program is converted to an executable with PyInstaller, so it may be falsely detected by antivirus software

## Disclaimer

- There may be hidden bugs. Use at your own risk.

## Plans

- [ ] Display information about the loaded ghost car (player name, stage time, etc.)
- [ ] Enable "touge"-style battles with the ghost car (offset the ghost's start timing so you can do "lead and chase")
- [ ] Enable loading telemetry data from other tools
- [ ] Enable selecting a ghost (so a ghost of any car can be loaded, making "AE86 vs Lancer Evo" possible)
