# Working with LSL
We make extensive use of the [Lab Streaming Layer framework](https://labstreaminglayer.readthedocs.io/index.html). This allows us to create, record, and communicate data and [[Event Markers]] from a wide range of [[Devices]] and programming languages.

For [[Psychopy]] [[Paradigms]] we use [pylsl](https://github.com/chkothe/pylsl).
For [[Unity]] paradigms you can try [LSL4Unity](https://github.com/labstreaminglayer/LSL4Unity).
For [[BrainProducts]] devices we use [BrainVisionRDA](https://github.com/brain-products/LSL-BrainVisionRDA).
In [[MATLAB]] you can make use of the [liblsl-Matlab](https://github.com/labstreaminglayer/liblsl-Matlab) library.

## Lab Recorder

The [LSL LabRecorder](https://github.com/labstreaminglayer/App-LabRecorder) collects all streams available in the local network and records them in XDF format. From version v1.14 onward, your XDF files also are stored in a BIDS format. We suggest you use LabRecorder from this version onwards.

Having problems finding your experiment streams? The wifi and ethernet [[Networks]] in the lab are not necesarily connected. If your laptop is connected via wifi you might not be able to see your streams on the ethernet (cable) network. For this we have an emergency LSL [[Router]] at the lab. Connect it and connect all the computers in your experiment to the router.

## Snippets

Python string marker
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

Python numeric marker
```python
from pylsl import StreamInfo, StreamOutlet

info = StreamInfo(name='PsychoPy',
    type='Markers',
    channel_count=1,
    channel_format='int32',
    source_id='PsychopyMarkersID321654'
)
outlet = StreamOutlet(info)
outlet.push_sample([1])
```

## Online visualization
To check both data and marker [[LSL Streams]] online we use the BrainVision [[LSL Viewers]] to read and visualize LSL streams live from the network. It's free from the official page, but you have to register, so don't. It should already be installed on the computers at the lab. 
This software is slow and can produce sapmle drops on low resource machines, so use it in a different computer from the one recording your data.

## Offline inspection
For visual inspection of your XDF files, we suggest [sigviewer](https://github.com/cbrnr/sigviewer). For programmatic inspection use the [XDF library of your prefered language](https://github.com/sccn/xdf)
