# Experiment 3 : Differential Amplifier – Design in LTspice using 180 nm technology lib.

## Aim : 
To Design a basic diffrential amplifier for the following specification Vdd=3.3V,P<=3mW,Vincm=1.72V,Vocm=1.8V,Vp=0.7V,Perform DC Analysis,Transient analysis,AC Analysis and extract the required parameters.
## Components Required  :
N-MOSFET(x3),Resistors(3,3k,0.77k),Power supply(3.3v,),Current source().

## Theory : 
A differential amplifier amplifies the difference between two input voltages while rejecting common-mode signals. It is widely used in analog circuits for its noise rejection and balanced input handling.
### Circuit Diagram :
![Screenshot 2025-03-04 221738](https://github.com/user-attachments/assets/16304869-efe0-41fd-a6e9-fc6ea74af1a2)</br>
Resistor Rss can be replaced by a current source or a NMOSFET also.</br></br>
#### About Circuit:
1.**Transistors M1 and M2** : These are the NMOS transistors forming the differential pair.</br>
2.**Resistors Rd**: These are the load resistors, typically used to convert the output current into a voltage.</br>
3.**Current Source Rss** :  Ensures a constant total current through M1 and M2.</br>
4.**Input Voltages (VINcm)**: VIN,cm is the common-mode input voltage.</br>
5.**Output Voltages (Vout1, Vout2)**: These are the output voltages at the drains of M1 and M2.</br>
#### Modes of operation:
1.Common mode :</br>
Common modes siganl : (V1 + V2)/2</br>

2.Diferential mode :</br>
The difference between two inputs : V1 - V2</br>

#### Working Principle:</br>
1.When Vin1 and Vin2 are equal then Current thorough both M1 and M2 are equal.(Vin1=Vin2=Vcm).</br>
2.If both sides of the perfectly matched the it can reject noise in Common mode.</br>
3.There should be no mismatch in Circuit elements like MOSFETs(M1,M2),Power supply(Vdd) and resistors(Rd,Rss).</br>
Vout1=(-gm X Rd X Vcm)/(1+2 X gm X Rs)</br>
Vout2=(-gm X Rd X Vcm)/(1+2 X gm X Rs)</br>

## Circuit 1 :
### Calculation:
    Iss=P/Vdd=(3x10^-3)/3.3=0.9mA</br>
    Id1=Id2=Iss/2=0.45mA</br>
    Rd=(Vdd-Vocm)/Id=(3.3-1.8)/0.45*10^-3=3.3kohm</br>
    Rss=Vp/Iss=0.7/0.9*10^-3=0.77kohm</br>
### Circuit:
![Screenshot 2025-03-04 231747](https://github.com/user-attachments/assets/f4b2c3e2-da96-48f4-91db-96fd70450ae9)
### Procedure:
#### DC Analysis:
1.Design the circuit as per the specification.</br>
2.Go for the Configure analysis option and select DC op pnt.</br>
3.Run Simulation.</br>
4.Adjust the Width of both Mosfet to get corresponding Iss and Vout in table.</br>
#### Result:
![Screenshot 2025-03-04 232402](https://github.com/user-attachments/assets/de5da78d-2fbb-489c-9691-d237dd9eb8e0)
#### Transient Analysis:
1.Go for the Configure analysis option and select select transient option.</br>
2.Modifiy V1 and V2 voltage sources by advanced options with SINE Wave.</br>
3.Run Simulation.</br>
4.Note down Vin and Vout waveforms.</br>
![Screenshot 2025-03-04 234452](https://github.com/user-attachments/assets/991c719c-b587-46eb-8b8c-f5b35ac1d4dd)
#### Result :
# ![Screenshot 2025-03-04 234013](https://github.com/user-attachments/assets/c0758c03-71e7-42ca-9fd3-345c9d444e33)
    Gain Calculation:
    Gain = Vout/Vin
         = (1.860-1.740)/(1.768-1.671)
         =1.23
    In dB:
    Gain=20log(1.23)
        =1.79dB
#### AC Analysis:
1.Go for the Configure analysis option and select select AC Analysis.</br>
2.Run Simulation.</br>
3.Note down gain and bandwidth.</br>
# ![Screenshot 2025-03-05 001134](https://github.com/user-attachments/assets/74afe3ab-4acb-4526-a0e5-e6994325d827)
#### Result :
# ![Screenshot 2025-03-05 001010](https://github.com/user-attachments/assets/26116dc1-504c-4b1f-adf3-179752d59f36)
    Bandwith=279MHz
    Gain in Midband Frequency=10.085
#### Rd Variation Analysis:
|Rd(kohm)|Vout(v)|Iss(mA)|
 | --- | --- | -- |
 |3.1|1.88|0.912|
 |3.2|1.843|0.910|
 |3.3|1.8|0.909|
 |3.4|1.75|0.907|
 |3.5|1.71|0.905|









