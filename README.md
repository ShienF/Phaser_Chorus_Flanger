# Phaser_Chorus_Flanger
* VST3 plugin
* Juce framework

## Requirement
* Juce v6.1.2 
* VisualStudio 2019

## Building
1. Choose the branch to clone or download (phaser >> wei, chorus_flanger >> shien)
2. Open Fx_Project_jucer with projucer
3. Open exporter (VisualStudio 2019)
4. Build the project and you will get a vst3 file

## Phaser
### Introduction
* A six-stage phaser effect
* 
### Parameter
![image](https://user-images.githubusercontent.com/88203221/149050438-28f6c51f-1f5b-4147-9234-00b926f029d2.png)
* Feedback: Set the feedback from -1 to 1.
* Rate: Set LFO frequency from 1 to 20. 
* Depth: Set poles amplitude from 0.01 to 0.99.
* Cutoff: Set the cutoff frequency from 0 to 20000.
* Mix: Set the dry/wet ratio from 0% to 100%.

### If you want to customize parameter
* Choose your range corresponding to LFO frequency in Phaser.h 
``` cpp=
                for (int j = 0; j < numStages; ++j)
                    filters[j]->setCutoffFrequency(frequency[k] * 2000+ centreFrequency);
```
 
