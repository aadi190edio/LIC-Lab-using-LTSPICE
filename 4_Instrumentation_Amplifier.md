# Experiment 4 : Instrumentation Amplifier
## Aim: 
Design an Instrumentation amplifier using 3 op amp configuration with following constraints R1=R3=10k,R2=R4=20K,R5=R6=10Kohm and Vcc=+/-15V 
 Calculate Adm for Rg=10,100,1k,10k,20kohms; Find Acm and calculate CMRR for each case using LTSPICE 
## Compnents Required :
op-amp(lm741.lib),resistors,DC Voltage supply.
## Theory:
An instrumentation amplifier (INA) is a very special type of differential input 
amplifier; its primary focus is to provide differential gain and high common-mode 
rejection. INAs offer high input impedance and low output impedance; newer devices 
will also offer low offset and low noise. The unique combination of a high common
mode rejection ratio (CMRR) and high accuracy make INAs especially attractive for 
applications with small error budgets such as motor controllers, battery test 
equipment, analog input modules, LCD test equipment and patient monitoring 
systems. The general definition of an INA is a circuit or device fitted with one to three 
internal operational amplifiers (op amps) to improve signal quality and increase 
common-mode rejection. The more common type of INA is the three op-amp 
configuration 
## Basic Circuit Diagram:
![Screenshot 2025-04-15 223919](https://github.com/user-attachments/assets/2016b5bd-02ee-485e-8f0f-708564a35c0f)

## Calculation 
     For Adm: </br>
     Adm= R2/R1(1+2*R5/RG) (To find theoretical Adm)</br> 
     1.For RG=10 ohm </br> 
        Adm=(20k/10k)(1+(20k/10)) </br>
           = 4002 v/v </br>
     2.For RG=100 ohm </br> 
         Adm=(20k/10k)(1+(20k/10)) </br>
            = 402 v/v </br>
     3.For RG=1k ohm </br> 
         Adm=(20k/10k)(1+(20k/1k)) </br>
            = 42 v/v </br>
     4.For RG=10k ohm </br> 
         Adm=(20k/10k)(1+(20k/10k)) </br>
            = 6 v/v </br>
     5.For RG=20k ohm </br> 
         Adm=(20k/10k)(1+(20k/20k)) </br>
            = 4 v/v </br>

     Finding Vid (Diffrential input) to be applied :
        
     
## Simulation:
![Screenshot 2025-04-15 234649](https://github.com/user-attachments/assets/16066d3b-b823-469e-a434-5f7a7603a3ff)

### Procedure :
1.Set up the circuit as above.</br>
2.Set Vin and Rg for each case.</br>
3.Perform transient analysis and find Adm.</br>

Analysis:
**1.For Rg=10 ohm.** </br>

**2.For Rg=100 ohm.** </br>
![rg2](https://github.com/user-attachments/assets/78cefd09-e47c-4cf6-a661-cb7f8d61e86b)

**3.For Rg=1k ohm.** </br>
![rg3](https://github.com/user-attachments/assets/b593dc3d-4734-442e-8b1f-fcac7aeba321)

**4.For Rg=10k ohm.** </br>
![rg4](https://github.com/user-attachments/assets/05de57a2-dc8f-41be-a08e-ebb1258bf6a2)

**5.For Rg=20k ohm.** </br>
![rg5](https://github.com/user-attachments/assets/3a2e5863-5728-4162-94a3-3d43eb7eb1d8)





| Resistance(RG in ohms) | Adm(Calculated) | Adm(Simulated) |
| :---         |     :---:      |          ---: |
| 10   | 4002   |      |
| 100  | 402    |      |
| 1k   | 42     |      |
| 10k  | 6      |      |
| 20k  | 4      |      |
