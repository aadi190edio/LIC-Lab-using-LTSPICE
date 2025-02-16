# LIC-Lab-using-LTSPICE
Experiments related to  Linear Integrated Cicuits using LTSPICE.
# Experiment 1 : Basic CS amplifier Characterization in LTspiceusing 180nm technology lib
## Aim:
 To Perform DC,AC and Transient analysis of Single stage CS Amplifier by including necessary libraries for power rating of 100µW and Vary the Width of channel too see the changes in drain current.
## Components and Libraries Required :
 N-MOSFET(nmos4,pmos4),Resistor(),Power Supply(DC:1.8V and 0.9V)
 tsmc018.lib(Library File)
## Theory :
An NMOS single-stage amplifier amplifies small input signals by operating the NMOS transistor in the saturation region, where it behaves as a voltage-controlled current source. For proper amplification, the transistor must satisfy:
                          Vds=Vgs+Vth

This ensures that the drain current(Id)is controlled by the gate voltage(Vgs), allowing the amplified output voltage to develop across the drain resistor with a 180-degree phase shift relative to the input.  

Key Characteristics  
- Voltage Gain(Av=-gm*Rd): Depends on transconductance(gm)and drain resistance(Rd).  
- High Input Impedance: Minimizes signal source loading.  
- Phase Inversion: Output is inverted with respect to input.  
- Limited Voltage Swing: Constrained by biasing and power supply.  

