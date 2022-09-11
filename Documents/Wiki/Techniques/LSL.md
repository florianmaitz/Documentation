# LabStreaming Layer
Network communication protocol for recording multiple sources with possible different sampling frequencies. 

Companies like [[BrainProducts]] or [[G-Tech]], or [[open source]] volunteers create plugins that broadcast devices' data through the network.

Collect and record data from LSL streams throughout the network in [[XDF]] format with [[LSL LabRecorder]]. We suggest you use [version 1.16](https://github.com/labstreaminglayer/App-LabRecorder/releases/tag/v1.16.2) or higher.

Your [[Paradigms]] should send instantaneous triggers (or markers) on [[LSL]] streams to be recorded for every time-locked event of your experiment.
