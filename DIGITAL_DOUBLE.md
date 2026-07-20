# Fisher 500-C Digital Double — Component Manifest

A caseless, component-accurate 3D control model of the factory-original Fisher 500-C
(1964), built alongside the Bernard Edward's Signature Edition resto-mod model in
`Fisher_500C.blend`. The original sits at world X = +0.62 m; the resto-mod at X = 0.
Both stand on museum placards. Use this unit as the unmodified baseline for tracking
every Signature Edition change.

Sources: project reference PDF (`Fisher_500C_Reference.pdf`), Hudson Valley HiFi
pre-restoration photo set (top deck, underside, PSU corner), quadesl.com refurb notes,
Stereophile 500-C review/measurements.

## Real-unit facts encoded in the model

- Chassis: 17.5" W x 6" H (faceplate) x 13" D, steel pan with cadmium-gold top deck, no cabinet
- 18 tubes: 7x 12AX7, 4x 7591 (push-pull, 2/ch), 6HA5, 6HR6, 2x 6CW4 nuvistor, 3x 6AU6
- Fisher "Golden Synchrode" FM front end; 4-gang tuning capacitor; flywheel tuning
- Voltage-doubler power transformer (rear right), two output transformers (rear left)
- Four twist-lock electrolytic can caps on deck; dual 1000 uF bias filter under chassis
- Selenium bridge rectifier (early production) under chassis
- Spacexpander (K-10 reverb) jumper plugs on the top deck — unit is silent without them
- Rear: 6 stereo input pairs + tape out (RCA), Speaker A/B + center-channel screw
  terminals, antenna strip, fuse, 2 AC convenience outlets

## Scene organization (Blender collections)

| Collection | Contents |
|---|---|
| `Fisher500C_Custom` | The resto-mod Signature Edition model (unchanged) + its placard |
| `Fisher500C_Original` | Parent of all ORIG_* sub-collections below |
| `ORIG_Chassis` | Deck, pan walls, feet, faceplate (dial window cut), dial pane |
| `ORIG_PSU` | Power transformer, OPT L/R (shroud+lams+flange+bolts each), 4 filter cans, Spacexpander jacks+jumpers |
| `ORIG_Tubes` | 18 tubes (V1–V18) + a socket per tube; glass/base/plates/getter as material slots |
| `ORIG_Tuner` | Golden Synchrode box, 4-gang tuning cap (end plates, rods, 8 rotors, shaft), tuning shaft + brass flywheel, IF transformers 1–4, ratio detector, dial pointer |
| `ORIG_FrontPanel` | Dial artwork (THE FISHER, 88–108 + log scales, tick strip), Stereo Beacon, signal-strength window, all knobs/toggles/jack, faceplate lettering |
| `ORIG_RearPanel` | 14 RCA jacks, speaker terminal strips A/B/center, antenna strip, fuse, AC outlets, power cord |
| `ORIG_Underside` | MPX compartment walls, selenium rectifier stack, bias board, dual-1000uF axial can + strap, 5 terminal strips w/ lugs, socket undersides, 3 cloth wiring looms |
| `ORIG_Labels` | ~45 floating text labels (toggle this collection to show/hide) + placard |
| `Studio` | Cameras + lights. Original-unit cameras: `Camera_Original` (front), `Camera_Orig_Top34`, `Camera_Orig_Under`, `Camera_Both` (two-shot) |

## Tube map

| Object | Type | Role |
|---|---|---|
| ORIG_V1–V4 | 7591 | Output L1/L2/R1/R2 (push-pull) |
| ORIG_V5/V6 | 12AX7 | Phono L / R |
| ORIG_V7/V8 | 12AX7 | Tone L / R |
| ORIG_V9/V10 | 12AX7 | Phase inverter L / R |
| ORIG_V11 | 12AX7 | Multiplex |
| ORIG_V12–V14 | 6AU6 | IF amplifiers 1–3 |
| ORIG_V15 | 6HA5 | RF amplifier |
| ORIG_V16 | 6HR6 | Mixer |
| ORIG_V17/V18 | 6CW4 | Nuvistors (front end) |

## Conventions

- Every original-unit object is prefixed `ORIG_`; labels are prefixed `LBLDD_`.
- Hide/show all labels by toggling the `ORIG_Labels` collection.
- Renders: `renders/fisher_500c_original_front_v1.png`, `_top34_v1.png`,
  `_underside_v1.png`, `fisher_500c_units_both_v1.png`.
- When a Signature Edition modification is decided, change ONLY the
  `Fisher500C_Custom` unit and log the delta against this control model.
