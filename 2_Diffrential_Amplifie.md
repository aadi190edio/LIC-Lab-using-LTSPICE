# Experiment 3 : Differential Amplifier – Design in LTspice using 180 nm technology lib.

## Aim : 
To Design a basic diffrential amplifier for the following specificationVdd=3.3V,P<=3mW,Vincm=1.72V,Vocm=1.8V,Vp=0.7V,Perform DC Analysis,Transient analysis,AC Analysis and extract the required parameters.
## Components Required :
N-MOSFET(3),Resistors(3,3k,0.77k),Power supply(3.3v,),Current source().

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

