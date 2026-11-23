# One-motor intake and transfer with a swing arm

A 3D animation of an FTC intake and transfer driven by one motor through three one-way bearings. It shows a swing-down intake arm, three static intake rollers, the transfer, and four held balls.

Everything is in `index.html`. Open it in a browser, or publish the folder with GitHub Pages. It loads three.js r128 from cdnjs, so it needs an internet connection the first time.

## How the drive works

- **Motor reverse:** gear B locks, pulleys A and C slip. Only the intake runs. The transfer freewheels, so the intake pushes the row of balls through it until the first ball reaches the stop.
- **Motor forward:** pulleys A and C lock, gear B slips. Intake and transfer both run and the balls feed up and out.
- The intake rollers turn the same way in both motor directions.

Speeds with a 6000 rpm motor: the intake runs at about 1950 rpm forward and 2000 rpm in reverse, and the transfer at 2000 rpm.

## Controls

- **Reverse: collect / Forward: feed up** switch the motor direction.
- **Arm down / Arm up** swing the outer intake roller out past the frame or fold it back inside.
- **Whole robot / Gearbox close-up** change the view. Drag to rotate, and use + and − to zoom.

## Changing the layout

The settings are at the top of the script in `index.html`. Positions are (x, y) in millimetres in the side master sketch.

| Setting | What it is |
| --- | --- |
| `M`, `S1`, `X` | Motor shaft, shaft 1, transfer middle shaft |
| `R1`, `R2`, `RS` | Static intake rollers. `RS` is the one the arm pivots on |
| `TL`, `TU`, `TR`, `TS` | Transfer rollers |
| `ARM_L`, `ARM_DOWN`, `ARM_UP` | Arm length, and its angle down and folded up |
| `W` | Gap between the side plates |
| `pathAt` | The ball path: floor, ramp, bend, straight up |

## What is assumed

- Positions were read off a screenshot of the master sketch, so they are good to about 1 mm.
- The gap between the side plates, the gearbox sitting outside one plate, and the order of parts along each shaft are placeholders.
- The stop for the first ball (the red bar) is assumed. Something on the real robot has to do that job.
- The gearbox is fitted roughly. In the current sketch the motor overlaps the small 32 mm roller, so the motor position still has to be settled.
