# Monkey hear, monkey do what? An application of Automated Behavioural Response systems for hypothesis testing in the world’s smallest monkey

This repository contains the code used to perform the analysis in the manuscript titled "Monkey hear, monkey do what? An application of Automated Behavioural Response systems for hypothesis testing in the world’s smallest monkey"

Theses datasets contain the behavioural responses (vocalisations, fleeing, eating and vigilance) of pygmy marmosets to various audio playback treatments (avian predator vocalisations, human speech, motor boats and control audios) in order to test two behavioural hypotheses.

<br />

Experimental Design

We deployed automated behavioural response (ABR) systems recording the feeding trees of 9 pygmy marmoset groups during the 5-week study. Once the camera trap in the ABR system detects movement it starts recording a 2-minute long video and then 10 seconds after the recording begins a 30 or 60 second audio recording was triggered (see stimuli details below) and started playing on an attached speaker. We were able to generate enough successful trials with five of these groups so that their responses to the stimuli could be evaluated for both experiments. Overall, we recorded 1,268 videos and 128 successful experimental trials over two experiments. The first experiment tested the risk-disturbance hypothesis and the playback audio stimuli consisted of avian predator vocalisations, human speech, motor boat and controls (cicadas and blue and yellow macaws) it consisted of 54 playback videos and 70 control videos where no audio was played (124 videos in total) that were analysed. The second experiment explored the distracted prey hypothesis, which postulates that animals are distracted by any stimulus they can perceive, and this distraction can cause them to become more susceptible to predation. We played audio recordings of motor boats and human speech that were spliced with the calls of birds of prey and control audios. Experiment 2 consisted of 74 playback videos. All videos from successful playback experiments from the 5 groups were analysed in the software BORIS (version 7.13), an event logging software for video coding.

#### File: Experiment1.csv

**Description:** the dataset used for the analysis of the first experiment looking at the risk disturbance hypothesis (n=124)

##### Variables

* Audio: playback type (factor: “Predator” avian predator call, “Motor Boat”, “Control” cicada or blue and yellow macaws, “Human Speech”, “None” no audio played in the video)
* Group: the pygmy marmoset group the focal individual is in (factor: CV denotes the group is near el Chino community, TL denotes the group is near Tahuayo lodge)
* Eat: total duration (seconds) the focal individual spent eating in the video
* Look: total duration (seconds) the focal individual spent looking at the camera trap in the video
* Speaker: total duration (seconds) the focal individual spent looking at the speaker in the video
* Vigilance: total duration (seconds) the focal individual spent being vigilant in the video
* Relaxed: total duration (seconds) the focal individual spent hunting, interacting with other marmosets and grooming in the video
* Calls: total number of vocalisations the focal individual emitted in the video
* Flee: if the focal individual fled in the video a binary response variable (0= no, 1=yes)
* TIF: the total duration (seconds) the focal individual was in the video frame in seconds (Time In Frame)
* TOF: the total duration the focal individual was out of the video frame in seconds (Time Out of Frame)

#### File: Experiment2.csv

**Description:** the dataset used for the analysis of the second experiment looking at the distracted prey hypothesis (n=74)

##### Variables

* Audio Type: anthropogenic noise playback type (factor: “Human Speech”, “Motor Boat”)
* Splice Audio: the audio that was spliced into the audio described in audio type (factor: “Predator” avian predator call, “Control” cicada or blue and yellow macaws)
* Group: the pygmy marmoset group the focal individual is in (factor: CV denotes the group is near el Chino community, TL denotes the group is near Tahuayo lodge)
* Eat: total duration (seconds) the focal individual spent eating in the video
* Look: total duration (seconds) the focal individual spent looking at the camera trap in the video
* Speaker: total duration (seconds) the focal individual spent looking at the speaker in the video
* Vigilance: total duration (seconds) the focal individual spent being vigilant in the video
* Relaxed: total duration (seconds) the focal individual spent hunting, interacting with other marmosets and grooming in the video
* Calls: total number of vocalisations the focal individual emitted in the video
* Flee: if the focal individual fled in the video a binary response variable (0= no, 1=yes)
* TIF: the total duration (seconds) the focal individual was in the video frame in seconds (Time In Frame)
* TOF: the total duration the focal individual was out of the video frame in seconds (Time Out of Frame)

#### File: PredatorCalls.csv

**Description:** the dataset used for the analysis looking at the impact of predator vocalisation playbacks on marmoset vocalisations behaviour across experiment 1 and 2 (n=67)


##### Variables

* Audio: playback type (factor: “Predator” just avian predator call, “Motor Boat Predator” motor boat audio with an avian predator call spliced in, “Human Speech Predator” human speech audio with an avian predator call spliced in)
* Group: the pygmy marmoset group the focal individual is in (factor: CV denotes the group is near el Chino community, TL denotes the group is near Tahuayo lodge)
* Calls: total number of vocalisations the focal individual emitted in the video

#### File: Experiment1PCA.csv

**Description:** the full behavioural dataset used for the PCA analysis looking at the correlation between behaviours from the videos analysed in experiment 1 (n=124)

##### Variables

* Audio: playback type (factor: “Predator” avian predator call, “Control” cicada or blue and yellow macaws, “None” no audio played in the video, “Anthropogenic Noise” includes both “Human Speech” and “Motor Boat” playbacks)
* Group: the pygmy marmoset group the focal individual is in (factor: CV denotes the group is near el Chino community, TL denotes the group is near Tahuayo lodge)
* Eat: total duration (seconds) the focal individual spent eating in the video
* Look: total duration (seconds) the focal individual spent looking at the camera trap in the video
* Speaker: total duration (seconds) the focal individual spent looking at the speaker in the video
* Vigilance: total duration (seconds) the focal individual spent being vigilant in the video
* Groom: total duration (seconds) the focal individual spent grooming in the video 
* Interact: total duration (seconds) the focal individual interacting with other marmosets in the video
* Hunt: total duration (seconds) the focal individual spent hunting insects in the video

#### File: Manuscript_Analysis.Rmd

**Description:** Code used to run the models outlined in the manuscript using the csv files outlined

#### File: Manuscript-Analysis.html

**Description:** the knitted r markdown file of the rmd file

#### Code/software
Raw video recordings were transcribed into behavioural observations in the event logging software BORIS (7.13) and then aggregated into summary variables (e.g., total durations and counts per trial) in R (4.3.2). All analyses were conducted in R (4.3.2). Script used for the statistical analyses as well as all included packages are provided in Manuscript_Analysis.Rmd as a R markdown file. 

