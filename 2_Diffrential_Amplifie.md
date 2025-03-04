# Experiment 3 : Differential Amplifier – Design in LTspice using 180 nm technology lib.

## Aim : 
To Design a basic diffrential amplifier for the following specification Vdd=3.3V,P<=3mW,Vincm=1.72V,Vocm=1.8V,Vp=0.7V,Perform DC Analysis,Transient analysis,AC Analysis and extract the required parameters.
## Components Required :
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
For the above specification</br> 
Iss=P/Vdd=(3x10^-3)/3.3=0.9mA</br>
Id1=Id2=Iss/2=0.45mA</br>
Rd=(Vdd-Vocm)/Id=(3.3-1.8)/0.45*10^-3=3.3kohm</br>
Rss=Vp/Iss=0.7/0.9*10^-3=0.77kohm</br>


