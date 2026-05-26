# 4.-Design-and-Simulation-of-Full-wave-rectifier-controlled-by-a-thyristor
## AIM
To design, simulate and analyse a full wave rectifier controlled by thyristors using MATLAB Simulink.
## APPARATUS REQUIRED
•	MATLAB
## PROCEDURE
1.	Open MATLAB and click on the icon for SIMULINK as shown below
 <img width="522" height="376" alt="image" src="https://github.com/user-attachments/assets/cc714a4d-8634-445d-b8af-21bb59f44617" />

Another way is to open is through START icon of MATLAB Start ⇒ Simulink ⇒ Library  browser. 

2.	Click on NEW MODEL or go to FILE ⇒ NEW ⇒ MODEL and a new blank model is created as shown below
 <img width="572" height="382" alt="image" src="https://github.com/user-attachments/assets/9af61610-084a-4f5d-8e67-0924fd22c890" />

3.	After creating a blank model you need to open the SIMULINK component storeroom/library by going to View ⇒ Library Browser. Select SIMPOWER SYSTEMS then select Power Electronics library and by right clicking on Thyristor and click on add to the model will add the Thyristor in the blank model. Alternatively you can drag the component directly in the model page as shown below
 <img width="940" height="361" alt="image" src="https://github.com/user-attachments/assets/59888715-c4ac-4bf8-8445-30c7c4bd6e31" />

4.	Similarly go to ELECTRICAL SOURCES ⇒ AC Voltage Source and add it to the model. Select Elements and select “SERIES RLC BRANCH” and add it to the model. Simulink do not perform simulation unless and until a measurement block is present in a system. Since we need to measure the input and output voltages and the load current. To add them select Measurement in SIMPOWER SYSTEMS and then add current measurement and voltage measurement blocks to the model. Oscilloscope is not included in SIMPOWER SYSTEMS and is present in the top most block of the left column that is SIMULINK ⇒ Sinks ⇒ Scope. Also add PWM generator from sourced. We can join various blocks by clicking
on their edges and then drag the wire till the other connection terminal.
5.	Construct the circuit by joining them together in the form as given below
 <img width="940" height="369" alt="image" src="https://github.com/user-attachments/assets/09311276-5e10-44b5-afc3-560959183850" />

6.	Now double click the voltage block to set the values of voltage and frequency.
 <img width="349" height="325" alt="image" src="https://github.com/user-attachments/assets/dd8ea140-ab78-482a-8c32-21c464e6b708" />

7.	Double click on Thyristor and you can set various parameters for Thyristor according to the specific data sheet.
8.	Double click on series RLC branch, Select the Branch type as R and set the values for R.
9.	Double click on PWM generator, set the parameter as per the requirement.
 <img width="377" height="443" alt="image" src="https://github.com/user-attachments/assets/4aa1bd69-0587-4063-9746-3507b0d0fdd8" />

10.	In the Scope menu “>” is shown which can only be connected to the inverse icon “<” in the measurement blocks.
11.	Double click on SCOPE and then click on parameter icon as shown
 <img width="838" height="377" alt="image" src="https://github.com/user-attachments/assets/3605a795-2cd1-4746-b5a7-3ab209cb8691" />

12.	Make the number of axes as required.
13.	Before simulation also adjust the data history of scope by following
 <img width="363" height="278" alt="image" src="https://github.com/user-attachments/assets/e8d9af71-b299-4eaa-89c5-d5a41867f375" />

14.	Before running the simulation, we have to configure the parameters. Go to Simulation ⇒ Configuration parameters as shown
 <img width="542" height="399" alt="image" src="https://github.com/user-attachments/assets/a81746fc-b597-42d0-bd2e-77b1dae3e489" />

15.	Select the ode23tb (Stiff/TR-BDF2) or ode15s (Stiff/NDS) or any suitable solver as
shown below 
 <img width="566" height="401" alt="image" src="https://github.com/user-attachments/assets/eedae68e-014b-4c0a-a0ad-fc9e351a4eec" />

16.	Start the simulation by either clicking on Start Simulation icon as shown in below or
by going to Simulation ⇒ Start
 <img width="770" height="308" alt="image" src="https://github.com/user-attachments/assets/4e8dffc2-d1d0-483a-9012-f27cc2cb61f9" />

17.	Double click on scope and observe the graphs.
18.	Left click on any graph and drag to make a rectangle to get the waveforms for a small period of time.
19.	Right click on each graph and select the axes properties and label each graph.
20.	Save the file. ( It should be noted that Simulink do not allow to save files with spaces therefore usually is included in between two words.)
21.	Analyze and record your inference.

## Task
Design, Simulate and analyse single phase full wave rectifier controlled by SCR with the following details 
Vm=100
Frequency = 50Hz
Resistance = 1 ohm
Phase delay or delay angle of Thyristor = 45 degree
After analysing the simulated output,
(i)Draw various simulated waveforms on the graph sheet
(ii) Change the value of resistance to 2 ohm, simulate and draw the current waveform on the graph sheet.
(iii) Change the firing angle to 90 degree, simulate and draw the Output voltage and current waveform on the graph sheet.
(iv)Write your inference.

## Simulation
<img width="1538" height="534" alt="image" src="https://github.com/user-attachments/assets/2b3b5e93-2658-4324-9f11-72ce96cdcce4" />

## Output
I <img width="1280" height="567" alt="image" src="https://github.com/user-attachments/assets/4e6facd7-4e9a-4ca0-8f6c-fc12f70a1f3d" />
II <img width="1280" height="574" alt="image" src="https://github.com/user-attachments/assets/bfdf5bd6-d37b-4ca4-9cc6-3683093a573d" />
III <img width="1280" height="562" alt="image" src="https://github.com/user-attachments/assets/dc33871e-652c-4d32-a3aa-a66ecc0f87b9" />
IV **Inference**
The single-phase full-wave SCR rectifier successfully converted AC input into controlled DC output.
With a firing angle of 45°, the output voltage and current were obtained after the SCR triggering instant, producing a partially controlled DC waveform.
When the load resistance was increased from 1 Ω to 2 Ω, the load current decreased according to Ohm’s law while the output voltage waveform remained nearly unchanged.
Increasing the firing angle from 45° to 90° reduced the average output voltage and current because the SCR conduction period decreased.
The simulation verified that the output of the SCR rectifier can be controlled effectively by varying the firing angle.
## Result
A full-wave thyristor-controlled rectifier was successfully designed and simulated in MATLAB/Simulink, and its output characteristics were analyzed for different firing angles.
