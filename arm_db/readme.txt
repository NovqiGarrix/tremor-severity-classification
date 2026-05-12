---Title---

A Study on the Essential and Parkinson’s Arm Tremor Classification - Arm Tremor Database

---Contributors---

Vasileios Skaramagkas, Institute of Computer Science, Foundation for Research and Technology Hellas (FORTH), Greece, ORCID: 0000-0002-3279-8016
George Andrikopoulos, Royal Institute of Technology KTH, Sweden, ORCID: 0000-0002-9399-7801
Zinovia Kefalopoulou, Neurology Department, Patras University Hospital, Patras, Greece
Panagiotis Polychronopoulos, Neurology Department, Patras University Hospital, Patras, Greece

---Corresponding Authors---

Vasileios Skaramagkas, vskaramagkas96@gmail.com
George Andrikopoulos, andrikopg@gmail.com

---DOI---

10.5281/zenodo.4772130

---Database Description---

Database including arm tremor data acquired via accelerometers from volunteers diagnosed with essential and Parkinson's tremor, as well as volunteers with no tremor diagnosis.

The uploaded files include:
1) "database.mat": the database in Matlab cell and struct-type format
2) "readme.txt": a text file providing more information on the database structure

Part of the dataset was used in the work accepted for publication in:
V. Skaramagkas, G. Andrikopoulos, Z. Kefalopoulou, and P. Polychronopoulos, "A Study on the Essential and Parkinson’s Arm Tremor Classification," in MDPI Signals, Special Issue on Biosignals Processing and Analysis in Biomedicine, vol.2, no.2, pp. 201-224, April 2021; DOI: 10.3390/signals2020016 2021.

Please refer to the above mentioned article for more information on the data acquisition protocol.

---Database Structure---

"database.mat": A matlab workspace file containing 'data' 1x37 cell-vector, which expands to
37 structs, each containing information and recordings from a single subject involved in the trial.
The included structs are organized as follows:

Version 1:
data{1} -- data{2}: subjects diagnosed with Essential tremor
data{3} -- data{10}: subjects diagnosed with Parkinson's disease
data{11} -- data{37}: subjects with no diagnosed tremor 

Each data struct contains the following two fields:

a) data{#}.info

Struct including the following subject information in struct format:

age: age in years
sex: female/male
hand: left/right (the hand where the accelerometers were placed - strong hand)
med: state of the medication - ON: has received medication over the last 12 hours/
			       OFF: has not received medication over the last 12 hours
tremor: years since tremor appeared
disease: years since disease/condition appeared
status: type of tremor (Parkinson's tremor, Essential tremor, no diagnosed tremor)  

b) data{#}.recordings

Struct including subject recordings in struct format according to the 
following four (4) experimental sequences:

i) rest: Measurement with hand at resting pose
ii) postural: Measurement with the hand at postural position 
iii) free_motion: The hand touches the table and then the nose. An oscillatory movement.
iv) motion_with_object: Same as free_motion,but this time the hand is holding a bottle.

Each of the above experimental sequences is a struct containing four (4) fields, each corresponding
to a accelerometer positioning:

1) index: Accelerometer placed on index finger
2) thumb: Accelerometer placed on thumb finger
3) metacarpal: Accelerometer place on the metacarpal area
4) wrist: Accelerometer placed on wrist

Each accelerometer positioning is a struct containing three (3) fields, each corresponding
to an accelerometer axis (x, y, z) and containing the acquired accelerometer measurements.
	- Sampling Frequency: 62.5 Hz
	- Units: m/s^2

For more information, please refer to the following article:
V. Skaramagkas, G. Andrikopoulos, Z. Kefalopoulou, and P. Polychronopoulos, "A Study on the Essential and Parkinson’s Arm Tremor Classification," in MDPI Signals, Special Issue on Biosignals Processing and Analysis in Biomedicine, vol.2, no.2, pp. 201-224, April 2021; DOI: 10.3390/signals2020016 2021.

Last Update: 2021/05/19