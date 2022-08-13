# BrainAmp (BA) Measurement checklist

The following diagrams and checklists can help you setup your experiment consistently. If you have any observation or suggestion please open an issue or make a PR.


### Active electrodes and Impedances
Some relevant links
ActiCAP snap electordes: https://pressrelease.brainproducts.com/acticap-snap/ , https://pressrelease.brainproducts.com/active-electrodes-walkthrough-slim/
Using BrainAmp with BrainVision requires the actiCAP ControlSoftware. Source: https://sites.bu.edu/reinhartlab/files/2017/06/BrainVision_Recorder_UM-1.pdf Chapter 7.1.1 and https://www.nmr.mgh.harvard.edu/~tatiana/BrainVisionManuals/Recorder_and_VideoRecorder/20201109_Recorder.pdf Chapter 9

Default impedance threshold for slim active electrodes (source: https://pressrelease.brainproducts.com/active-electrodes-walkthrough-slim/):

![Default impdances for ActiCAP electrodes](./default_impedances.png)


### Connectivity diagram 

![Diagram for BrainAmp](./DiagramBrainAmp.jpg)

### Layouts

Different layouts can be designed to use with the EasycapM1 cap. This is the cap with predefined wholes for electrode placement. It looks as follows: 

![10-20 layout](./Layouts/Layout.svg)

No current default layout for BrainAmp.

### Preparation

- Print your EEG layout
- Charge batteries: 4 AA bateries available at the lab, plus battery of amplifier.
- Make sure electrodes are available and clean.
- Check you have the consumables you need:
  - Conductive gel and syringes
  - Alcohol and cotton swabs
  - *EOG stickers
  - *ECG stickers
  - Paper towels (to clean up extra gel)
  - *Masks and latex gloves if needed.
- Measure your participant's head. We have three cap sizes: 54, 56, 58
- Prepare the adequate cap with the electrodes.
- Check the necessary USBs are available: HASP key for software (Purple/Blue)

Optional Ext:
- Prepare your external electrodes: ECG, GSR, etc.

### Measurement

- Place the cap:
  1. Measure the distance from Nasion to Inion. Cz should be in the middle.
  2. Measure the distance from ear to ear. Cz should be in the middle.
  3. Look at the participant from the front. Does it look symmetric?
  4. Connect the ControlBox and turn it on.
- Place gel in electrodes. With the ControlBox' impedance mode (Z) active, use the syringes to place a bit of gel in the cap. Correct until impedance levels are low enough that the LEDs of of the electrodes are all green. Start placing gel in ground GND and reference REF electrodes.
- Connect the ControlBox to the BrainAmp and turn on the amplifier. Do not set a specific mode on the ControlBox - just leave it turned on.
- Start the software:
  - BrainVision Recorder (Requires HASP key): This software reads data from the BrainAmp. In preferences, RemoteDataAccess and Passive Electrodes should be enabled. Make sure your layout is set correctly in the workspace.
  - BrainVisionRDA: This sends data from BVRecorder through an LSL stream.
  - LSLRecorder: Records LSL streams into XDF format.
  - Your Paradigm: the experiment you prepared for presenting stimuli and instructions to your participants.
- Check the signals in the BrainVision Recorder at 20 uV. Do they look like normal EEG? is there noise from the power line? Is there muscle noise?
- Ask your participant to produce artefacts: teeth clenching, blinking, moving eyes, swallowing.
- Leave the signals visible on BVRecorder (otherwise BVRDA won't send data)
- (optional EXG): Setup your external electrodes.
- Link BVRDA.
- Start your protocol.
- Verify all your streams appear in LSL LabRecorder.
- Check any experiment requirements.
- Start recording.
- Monitor recording using LSL Viewer on the Alianware PC.


### Clean up
- Remove cap and ensure your participant has all they need to clean their hair.
- Take material upstairs to the sink:
  - Syringes and needles
  - Cap and electrodes
- Separate cap and electrodes.
- Disinfect cap.
- Wash electrodes with water and a toothbrush.
- Wash syringes and needles with water.
- Wash off disinfectant from cap, and dry with a towel.
- Bring everything back to the fNIRS/VR lab.
- Charge batteries (4 AA, BrainAmp battery).
