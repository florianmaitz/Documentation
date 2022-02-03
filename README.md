# Protocols
Lab protocols for different devices.
The following are notes to consolidate into protocols.

## TODO
One folder for every device.
Add configuration files to folders.
Add default layout and workspace.
Add different layouts and workspaces with their respective usage.
Add connectivity diagrams.

## LiveAmp (LA) Measurement checklist

### Preparation

- Print your EEG layout
- Charge batteries: either LiveAmp via USB or powerbank.
- Make sure the LA electrodes are available and clean.
- Check you have the consumables you need: 
  - Conductive gel and seringes
  - Alcohol and Qtips
  - EOG stickers
  - ECG stickers
  - Paper towels (to clean up extra gel)
  - Masks and latex gloves if needed.
- Measure your participant's head. We have three cap sizes: 54, 56, 58
- Prepare the adequate cap with the electrodes.
- Check the two necesary USBs are available: HASP key for software and Bluetooth dongle for connectivity.

Optional Ext:
- Prepare your external electrodes: ECG, GSR, etc.
- Make shure the powerbank is charged.

### Measurement

- Place the cap: 
  1. Measure the distance from Nasion to Inion. Cz should be in the middle.
  2. Measure the distance from ear to ear. Cz should be in the middle.
  3. Look at the participant from the front. Does it look symetric?
  4. Connect the Amplifier and turn it on.
- Start the software:
 - BrainVision Recorder (Requires HASP key): This software reads data from the LiveAmp. In preferences, RemoteDataAccess should be enabled. Make sure your layout is set correctly in the workspace.
 - BrainVisionRDA: This sends data from BVRecorder through an LSL stream.
 - LSLRecorder: Records LSL streams into XDF format.
 - Your Paradigm: the experiment you prepared for presenting stimuli and instructions to your participants.
- Place gel in electrodes. With the impedance view open in BVRecorder, use the seringes to place a bit of gel in the cap. Correct until impedance levels on BVRecorder are lower than your selected threshold. Start placing gel in ground GND and reference REF electrodes.
- Check the signals at 20 uV. Do they look like normal EEG? is there noise from the power line? Is there muscle noise?
- Ask your participant to produce artifacts: teeth clenching, blinking, moving eyes, swallowing.
- Leave the signals visible on BVRecorder (otherwise BVRDA won't send data)
- (optional Exg): Setup your external electrodes.
- Link BVRDA
- Start your protocol.
- Verify all your streams appear in LSL LabRecorder.
- Check any experiment requirements.
- Start recording.
