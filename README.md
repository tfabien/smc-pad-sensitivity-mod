# M-Vave SMC-PAD: pad sensitivity mod

Your SMC-PAD pads feel dead and you have to hammer them to get a decent velocity? This is a ~20 minute fix: open the unit, stick a sheet of spacers on the transparent sheet that carries the black pads, close it. No soldering, no glue gun, no 15-minute video.

The spacers are **laser-cut** from self-adhesive vinyl sheets (what I used and tested), either as **one full sheet** covering all 16 pads at once (the easiest) or as 16 individual spacers. A **3D-printed** version is also provided (untested), and **strips of electrical tape** also work. Pick whichever you have.

> Inspired by Owl Muso's [M Vave SMC Pad Sensitivity Hack](https://www.youtube.com/watch?v=G5knDHVOgrA). Same idea, minus the video: ready-made spacer files and a step-by-step with annotated photos.

![Spacer sheet](images/00-spacer-sheet.jpg)

## What you need

- A **PH0** Phillips screwdriver
- A plastic pry tool, or a fingernail, to remove the rubber feet and the QR label
- **Spacers**, one of:
  - laser-cut self-adhesive vinyl, **full sheet** (recommended, one piece for all 16 pads), tested
  - laser-cut self-adhesive vinyl, 16 individual spacers, tested
  - 3D-printed spacers (STL / 3MF): untested, see below
  - no laser, no printer? Strips of electrical tape (see below)
- Something to keep screws in, with two separate compartments: 9 case screws and 9 PCB screws (they're different)

## Files

| File | What it is |
|---|---|
| [`files/SMC-Pad_spacers_full_sheet.dxf`](files/SMC-Pad_spacers_full_sheet.dxf) | **One full sheet (136 x 136 mm)** covering all 16 pads at once, with rounded corners and notches, directly at the right size. Recommended |
| [`files/SMC-Pad_spacers_sheet_4x4.dxf`](files/SMC-Pad_spacers_sheet_4x4.dxf) | 16 individual spacers (27 x 27 mm each) on a 125 x 130 mm sheet |
| [`files/SMC-Pad_spacer_single.dxf`](files/SMC-Pad_spacer_single.dxf) | A single spacer (27 x 27 mm, with a round hole and a vertical slot) |
| [`files/SMC-Pad_spacers_LightBurn.lbrn2`](files/SMC-Pad_spacers_LightBurn.lbrn2) | Ready-to-run LightBurn project (sheets + title text + cut settings) |
| [`files/SMC-Pad_spacers_full_sheet.stl`](files/SMC-Pad_spacers_full_sheet.stl) | 3D-printable full sheet. **Not tested** |
| [`files/SMC-Pad_spacer_single.stl`](files/SMC-Pad_spacer_single.stl) | 3D-printable single spacer. **Not tested** |
| [`files/SMC-Pad_spacers_3Dprint.3mf`](files/SMC-Pad_spacers_3Dprint.3mf) | 3D-printing project (3MF), updated to the new design. **Not tested** |

All dimensions are in millimetres. In the previews below, blue is the spacer cut, green the title text and red the outline of the sheet.

<p>
<img src="images/dxf-full-sheet.png" width="360" alt="Full sheet">
<img src="images/dxf-sheet-4x4.png" width="340" alt="Individual spacers sheet">
<img src="images/dxf-single-spacer.png" width="200" alt="Single spacer">
</p>

### Making the spacers

**Laser-cut (self-adhesive vinyl sheet), tested**

Load `SMC-Pad_spacers_LightBurn.lbrn2`, or import one of the DXF files. The idea is to *kiss-cut*: cut through the vinyl but not through the backing.

![LightBurn project with the three DXF files](images/lightburn-project.png)

The LightBurn project uses 3 layers, run in this order:

1. Title text, light engrave (1-5 % power, 25 mm/s)
2. Spacers (round holes, slots and outlines), kiss cut: 10-15 % power, 16.7 mm/s (1000 mm/min)
3. Sheet outline, full cut: 30 % power, 16.7 mm/s (1000 mm/min)

Those numbers come from my machine (LightBurn device profile `LR4`). Run a small test first and tune power on your own laser, then make sure the backing survives.

**3D-printed (untested)**

STL and 3MF files are provided for the new design. I haven't printed them myself (the vinyl version is the one I tested), so treat them as a starting point and let me know how it goes.

**Electrical tape (no tools needed)**

Instead of the spacers, stick strips of electrical tape on the transparent sheet, in step 6, on each pad. Cheapest and quickest option.

## Step by step

> Work on a mat, keep the screws sorted per step, and don't force anything. Before you start, switch the pad off and unplug the USB cable.

### 1. Pull the knobs

Use a flat screwdriver and go **very slowly**. Slide it under the edge of a knob and lift a little, then move around the knob and lift from different angles. Never pull on one side only, or you'll bend the potentiometer. Repeat for all 8 knobs.

![Knobs off](images/01-knobs-off.jpg)

### 2. Undo the back screws

Flip the unit over.

- **1 to 4**: the four corner screws are hidden under the round rubber feet. Pry the feet off, then undo the screws.
- **5 to 8**: four uncovered screws, in the middle of each side.
- **9**: peel the QR label back to find the centre screw, and undo it.

That's 9 case screws in total.

![Back screws](images/02-back-screws.jpg)

Lift the bottom plate off. You now see the PCB (with the battery) sitting in the top shell.

### 3. Unplug the battery first

**Before you undo anything on the PCB, disconnect the battery.** Unplug the small white JST connector of the 3.7 V / 2000 mAh LiPo. Pull on the connector, not on the wires.

![Battery](images/03-battery-unplug.jpg)

### 4. Remove the 9 PCB screws

Undo the 9 black screws that hold the PCB. The photo shows the 9 screw holes, with the screws already out.

> **Careful: the case screws and the PCB screws are not the same.** Keep them in two separate piles. The hole in the middle of the PCB is not for a PCB screw: it lets the **case screw** (step 2, screw 9) go through the PCB. When you put the PCB back, don't screw anything into that hole.

![PCB screws](images/04-pcb-screws.jpg)

### 5. Lift out the PCB

Take the PCB out gently. The sheet with the black squares is a **separate, loose sheet**, not attached to the PCB or to the case. **Pay attention to its orientation**: it must go back the same way up and the same way round. The easy way: lay it down on the PCB as if you were opening the page of a book, so it keeps its orientation. The pad cavities in the top shell are now empty. Leave the sheet lying on the PCB for the next step.

![Empty cavities](images/06-cavities-empty.jpg)

### 6. Stick the spacers on the transparent sheet

The transparent sheet with the black pads is lying on the PCB (step 5). It's much easier to stick the spacers **directly on it** than into the case cavities.

> **Careful with the side:** stick the spacers on the **silicone-pad side** of the sheet (the side that faces the case), **not on the PCB side**. If you laid the sheet down like a book page, that's the side facing up.

1. Remove the round holes and the slots from the vinyl so they're open, then peel the full sheet off its backing.
2. Lay it over the 16 pads in one go, starting from one edge and going progressively to avoid bubbles. Each round hole goes over a LED, with the slot vertical, as in the photos.
3. Check that you can see the LED through each round hole and the black pad through each slot.

> Using the 16 individual spacers instead? Same thing, one spacer on each pad.

![Laying the spacer sheet](images/07-spacers-laying.jpg)

![Spacers stuck on the transparent sheet](images/08-spacers-stuck.jpg)

> **Want even more sensitivity?** Stack **two layers**: stick a second full sheet (or a second spacer on each pad) on top of the first, perfectly aligned. Do the same on all 16 pads so they stay even.

### 7. Close it up

Reverse the steps:

1. Close it like a book, the reverse of how you opened it: swing the PCB, with the transparent sheet and its spacers lying on it, back over the case. The sheet ends up against the silicone pads, the same way up as it came out. Take your time, this is where it's easy to flip it.
2. Check that the PCB is lined up on its posts.
3. Refit the 9 black PCB screws, and only those. Leave the centre hole empty (it's for the case screw, see step 4).
4. Plug the battery back in (last, once the PCB is screwed down).
5. Fit the bottom plate and refit the 9 case screws (4 corners, 4 mid-side, and the centre one, which goes through the PCB hole).
6. Put the rubber feet back, stick the QR label back, push the 8 knobs on.

Plug it in and power it on. Last step: calibrate the pads in software.

### 8. Calibrate the pads in MidiSuite

The mod fixes the hardware, but the pads still need to be calibrated in software, otherwise you won't get the full benefit.

1. Install **MidiSuite**, M-Vave's editor (v1.15.0 in the screenshot). All downloads are on the official page: [m-vave.com/download](https://www.m-vave.com/download). Direct links to the current version:
   - Windows: [MidiSuite_new.zip](https://yms-file-store.oss-cn-hongkong.aliyuncs.com/software/pc/MidiSuite_new.zip)
   - macOS: [MidiSuite_new.dmg](https://yms-file-store.oss-cn-hongkong.aliyuncs.com/software/pc/MidiSuite_new.dmg)
   - Mobile apps: [iOS](https://apps.apple.com/us/app/midi-suite/id6737530581) and [Android (APK)](https://resource.m-vave.com/software/app/MidiSuite.apk) (the mobile app lists the SMC-PAD Pocket, not the SMC-PAD, so use the desktop version)
2. Connect the SMC-PAD and open MidiSuite.
3. Click **Pad Calibration Mode**.
4. Every pad has its own sensitivity level, from **Level 1 to Level 8** (factory setting: **Level 4**). Changes are saved to the device immediately.
5. Hit a pad, adjust its level, hit it again. Repeat for each of the 16 pads until they all feel even.

![MidiSuite pad calibration](images/09-pad-calibration.jpg)

## Disclaimer

You're opening a device with a lithium battery inside. Do this at your own risk, don't puncture or bend the battery, and don't short anything. This will probably void your warranty. This project is not affiliated with M-Vave.

## License

Files and text: [CC BY-SA 4.0](LICENSE). Share your results and improvements, PRs welcome.
