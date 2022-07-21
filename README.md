# EEG2brainvol
attempts to use resting/functional EEG to derive, via AI, a volume suitable for beamforming

## big picture
To achieve acceptable source-level resolution while keeping high time resolution with EEG, individual MRI images are needed.  
With this project I aim to test the feasibility of reconstructing a good-enough brain volume from EEG data alone.  
The question is, whether there is enough information in hdEEG dynamics to allow for brain model reconstruction.  

## basic logic
- Sensors on surface pick up electrical information from source
- Aspects of the electr. signal is changing depending on source distance from sensor (SDS)
- SDS changes cyclically with heart beat
- SNR of these aspects (ASDS), to be determined via AI, is high enough when integrating data across the same positions within a cycle
- first ASDS candidate: neural noise

## assumptions
- existence of ASDS, based on electrical measures, is not physically impossible
- heartbeat cycle detectable from EEG (can be tested)

## roadmap
- given: ~20 EEG data, 60 electrodes, labelled (i.e. with individual MRIs)
- for each individual, 2 states (sober and alcohol-intoxicated :)
- first blind test with AI model
- ...for more, see issues
