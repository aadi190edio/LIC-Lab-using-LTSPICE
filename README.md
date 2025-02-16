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

## Circuit 1 :
### DC Analysis :
#### Procedure :
1.After the Circuit Setup include the Library file(.lib tsmc018.lib) by SPICE Directive
2.In Configure analysis select DC Op pnt.
# ![Screenshot 2025-02-17 002651](https://github.com/user-attachments/assets/aceec8d5-e15d-4e72-a09b-644c3062df0b)
  Given P=100*10^-6 W
  W.K.T P=V*I
  By substituting values P=100*10^-6 W and V=1.8V
  We get I= 5.56 * 10^-5 A (Drain Current)

By adjusting width of the channel we can obtain approximate current to get the corresponding power
# ![Screenshot 2025-02-17 003523](https://github.com/user-attachments/assets/8f884108-93b7-44c6-b45b-501a34d9c882)
 here
 L=180n W=179n

Channel Width(W) vs Drain Current(Id)
155n:5.09*10^-5
160n:5.14*10^-5
165n:5.18*10^-5
170n:5.23*10^-5
175n:5.27*10^-5

### Transient Analysis :
#### Procedure :
1.In Configure analysis select Transient option.
2.Set the stop time 1m.
# ![Screenshot 2025-02-17 005211](https://github.com/user-attachments/assets/8d313ba9-1aa7-4e81-b5ad-a4c455db8b8f)

