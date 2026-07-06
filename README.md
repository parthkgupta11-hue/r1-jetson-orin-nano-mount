# Unitree R1 – Jetson Orin Nano Mount

A 3D-printable, slide-in mount for attaching an NVIDIA Jetson Orin Nano (or Orin Nano Super) Developer Kit to the back of a Unitree R1 humanoid robot. The Nano slides into the mount and can be removed just as easily — no tools needed to swap the module in or out. The mount itself is secured to the R1's existing M4 attachment points.

![Assembled mount render](docs/images/assembly-render.png)

## Compatibility

Designed around the **NVIDIA Jetson Orin Nano Developer Kit** (4GB/8GB, carrier board form factor). This also fits the **Jetson Orin Nano Super Developer Kit** — NVIDIA has confirmed the Super kit uses the exact same carrier board and module hardware as the standard kit; the "Super" designation is a firmware/software update only, so the physical footprint and mounting holes are identical.

If you're using a bare SO-DIMM module on a different carrier board (rather than the official NVIDIA dev kit), double-check your board's dimensions before printing — this design is sized for the official reference carrier board.

## Parts

| File | Function | Attachment | Hole spec |
|---|---|---|---|
| `Part1_R1_Baseplate.stl` | Slide-rail bracket that bolts to the R1's back panel; the Nano sled slides into this | Mounts to R1's existing M4 screw holes | 4× 5.6 mm holes for M4 heat-set inserts |
| `Part2_Housing_Shell.stl` | Outer shell/cover around the Nano; has cutouts for the power button and Wi-Fi/BT antenna connectors | Joins to the end cap (below) with M4 screws | 4.4 mm clearance holes for M4 screws · 1× 12 mm hole for the Nano's power button · 6.5 mm holes for antenna connectors |
| `Part2_Housing_EndCap.stl` | End cap that closes the housing shell | Receives screws from the shell above | 5.6 mm holes for M4 heat-set inserts |

> Filenames above are suggestions — rename the exported STLs to something like this so the repo is understandable without opening OnShape. See "Before you post this" below.

## Bill of Materials

| Qty | Item | Notes |
|---|---|---|
| 4+ | M4 brass knurled heat-set inserts — [Zruosiniy 400-pc metric assortment kit](https://www.amazon.com/Zruosiniy-Brass-Threaded-Inserts-Nuts/dp/B0F2N8QY45) | For the 5.6 mm holes. Brass insert OD varies by brand (common M4 inserts range roughly 5.6–6.5 mm OD) — measure the actual inserts with calipers before printing your final parts to confirm 5.6 mm is a snug press fit, not loose |
| 4+ | M4 screws | Length depends on stack-up (housing wall + insert depth) — measure before ordering |
| — | Soldering iron / heat-set insert tool | For installing inserts. Install temp ≈ your print temperature + 10–20 °C |

## Print Settings (suggested — fill in what you actually used)

- **Material:** PETG recommended for durability on a moving/dynamic robot (PLA is more brittle under vibration/impact)
- **Layer height:** 0.2 mm
- **Infill:** 30–40%+ (this mount lives on a robot that runs, cartwheels, and falls — don't skimp on strength)
- **Supports:** note which parts need them and where (the rail geometry on the baseplate may need support — check your slicer preview)
- **Orientation:** note the recommended print orientation for each part

## Assembly

1. Print all three parts (see settings above).
2. Install M4 heat-set inserts into the 5.6 mm holes on the baseplate and end cap using a soldering iron.
3. Bolt the baseplate to the R1's back-mounted M4 attachment points.
4. Slide the Jetson Orin Nano into the baseplate's rails.
5. Fit the housing shell over the Nano, aligning the button and antenna cutouts.
6. Attach the end cap to the shell with M4 screws through the 4.1 mm clearance holes into the heat-set inserts.

## Source Files

Editable CAD (OnShape, parametric): [link to OnShape document](https://cad.onshape.com/documents/4870ae7b7abf8141c113cbe3/w/747d7f00118be55340bf33ef/e/ac8754d0635a8b6524a612b2)

## License

This project is licensed under **Creative Commons Attribution-ShareAlike 4.0 International (CC BY-SA 4.0)**. See [`LICENSE`](LICENSE) for details. In short: anyone can use, remix, and even sell derivatives of this design, as long as they credit Parth Gupta and share their own version under the same license.

## Credits

Designed by Parth Gupta.
