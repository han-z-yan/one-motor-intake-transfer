# One-motor intake and transfer drive

An interactive 3D model of an FTC intake and transfer drive that runs off a single motor and three one-way bearings.

- **Motor forward:** the intake and the transfer both run, in the same direction.
- **Motor reverse:** the intake keeps pulling in and the transfer is left free to spin.

Open `index.html` in a browser, or view the published page on GitHub Pages.

## How it works

- A belt copies the motor's direction. A gear pair flips it.
- Gear B and pulley A both ride on shaft 1 through one-way bearings. They always turn in opposite directions, so one of them is always turning the "pull in" way and driving the shaft.
- Pulley C rides on shaft 2 through a one-way bearing, so shaft 2 only turns in one motor direction.
- The one-way bearings need a round shaft, so shafts 1 and 2 are 8 mm round. The motor shaft and both roller shafts are 8 mm REX, and belts link the round shafts to the REX roller shafts.

## Speeds

With the default settings the motor turns at 6000 rpm, the two round shafts at 3000 rpm, and the rollers at 2000 rpm (3:1 total).

## Changing it

The settings are at the top of the script in `index.html`:

| Setting | What it does |
|---|---|
| `MOTOR_RPM` | Motor speed used for the readouts |
| `STAGE1` | Reduction from the motor to the round shafts |
| `STAGE2` | Reduction from the round shafts to the rollers |
| `SPIN` | `-1` or `+1`, which way the rollers turn |
| `POS` | Where each shaft sits |

The model uses three.js r128 from a CDN, so it needs an internet connection to load.
