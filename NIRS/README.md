# fNIRS setup

These are some config files found on the computer, where the fNIRS device was setup.
They seem to contain hardware configurations.

Default experimental layout is included in `channel_masking`, and it seems important.

There seems to be no Zebris montage file. This contains the 3D positions of the optodes (or channels, idk). It is useful for analysis with MNE.

Installation files are ordered in fNIRS computer.

## Calibration

Follow manual under `Manuals/NIRX/TroubleshootingStaticPhantom.pdf`

## Default layout

![NIRS/Montages/Default_16x22/Standard.png](https://raw.githubusercontent.com/WriessneggerLab/Protocols/main/NIRS/Montages/Default_16x22/Standard.png)

A default layout was created based on Wriessnegger 2018[^1]. Legacy files (`channel_masking/whole_head.hwc` and `channel_masking/TopoLayout_wholehead.tpl`) contained the masking and layout data: 16 sources and 22 detectors. A NIRStar configuration has been created to reproduce this setup with minimal setup. The folder including all files in usder `Montages/Default_16x22`.

Diagnostics executed on 2022-05-02. All tests passed.

Possible issues: Assumed equidistant optical distances:
```
Opt_Distance = "30	30	30	30	30	30	30	30	30	30	30	30	30	30	30	30	30	30	30	30	30	30	30	30	30	30	30	30	30	30	30	30	30	30	30	30	30	30	30	30	30	30	30	30	30	30	30	30	30	30	30	30	30	30	30	30	30	30	30	30	30\0D\0A"
```

[^1](Wriessnegger, S. C., Bauernfeind, G., Kurz, E. M., Raggam, P., & Müller-Putz, G. R. (2018). Imagine squeezing a cactus: Cortical activation during affective motor imagery measured by functional near-infrared spectroscopy. Brain and cognition, 126, 13-22.)