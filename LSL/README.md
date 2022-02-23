# Working with LSL
We make extensive use of the [Lab Streaming Layer framework](https://labstreaminglayer.readthedocs.io/index.html). This allows us to create, record, and communicate data and event markers from a wide range of devices and programming languages.

For Psychopy paradigms we use [pylsl](https://github.com/chkothe/pylsl).
For Unity paradigms you can try [LSL4Unity](https://github.com/labstreaminglayer/LSL4Unity).
For BrainProducts devices we use [BrainVisionRDA](https://github.com/brain-products/LSL-BrainVisionRDA).
In matlab you can make use of the [liblsl-Matlab](https://github.com/labstreaminglayer/liblsl-Matlab) library.

## Lab Recorder

The [LSL LabRecorder](https://github.com/labstreaminglayer/App-LabRecorder) collects all streams available in the local network and records them in XDF format. From version v1.14 onward, your XDF files also are stored in a BIDS format. We suggest you use LabRecorder from this version onwards.

## Snippets

Python
```python
from pylsl import StreamInfo, StreamOutle
info = StreamInfo(name='PsychoPy',
    type='Markers',
    channel_count=1,
    channel_format='string',
    source_id='PsychopyMarkersID321654'
)
outlet = StreamOutlet(info)
outlet.push_sample(["A string marker"])
```

## Online visualization
To check both data and marker streams online we use the BrainVision LSLViewer. It's free from the official page, but you have to register, so don't. It should already be installed on the computers at the lab. 
This software is slow and can produce sapmle drops on low resource machines, so use it in a different computer from the one recording your data.

## Offline inspection
For visual inspection of your XDF files, we suggest [sigviewer](https://github.com/cbrnr/sigviewer). For programmatic inspection use the [XDF library of your prefered language](https://github.com/sccn/xdf)
