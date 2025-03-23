# Design and Analyze Current mirror circuit

## Aim:Design and analyze current mirror for given specification
## Part A:
### Aim: 
Design the Current mirror circuit for Av(Gain)>10,Vdd=1.8V,P<=1mw Design the current mirror ratio 1:1 and 1:2 perform transient and Ac Analysis.</br>
### Components and Libraries Required: 
CMOSP(x2),CMOSN(x1),Current source(Reference),Voltage sources , tsmc018.lib</br>
### Theory :
### Cascode Current mirror:
# ![Screenshot 2025-03-24 003654](https://github.com/user-attachments/assets/1b6d7118-2aad-46a0-a3e4-4c608eb9ac4f)

This circuit is a CMOS Current Mirror with Cascode Configuration, used to improve output resistance and accuracy. It consists of three MOSFETs:</br>
1.M1 and M3 forms basic current mirror.</br>
2.M2 and M3 acts cascode transistors for better performance.</br>

#### 1. Circuit Operation</br>

**A.Current Reference(Iref:Here 100uA in above figure)**</br>

1.A reference current Iref is provided at the source of M3.</br>
2.M3 is diode-connected (gate and drain shorted), forcing it to operate in saturation.</br>
3.Since M3 and M1 share the same VGS, they should ideally carry the same current.</br>

**B.Mirroring Mechanism**</br>
1.M1 is a mirror transistor that copies Iref.</br>
2.The gate of M1 is connected to M3, ensuring that both transistors have the same VGS.</br>
3.Thus, Iout ≈ Iref, assuming ideal matching conditions.</br>

**C.Role of M2 and Cascode Configuration**</br>
M2 and M3 create a cascode structure, which helps:</br>
->Increase output resistance (better current source behavior).</br>
->Reduce channel length modulation effects.</br>
->Improve accuracy of current mirroring.</br>

**Output Current (Ix)**</br>
The output current (Ix) is forced through M2.</br>
Since M2 is in saturation, it ensures that M1 and M3 operate correctly.</br>

#### Calculation:
    For 1:1 Ratio:
    Itotal= P/Vdd=1*10^-3/1.8= 0.55mA
    Itotal=Iref+Ix
          =2Iref(Since ratio is 1:1)
    Iref=Ix=0.275mA)
##### Circuit:
![1_1ckt](https://github.com/user-attachments/assets/64689321-ce2d-4ffa-8a76-c933d8175abc)</br>
#### DC Analysis:
By Adjusting Width</br>
![1_1_ratio](https://github.com/user-attachments/assets/9b8a5cbf-144d-482c-a6f9-902903185359)

<u>So We can observe that both Iref and Ix are equal (Due to 1:1 Ratio)</u></br>
Current mirroring is ocurring as per the ratio</br>
#### Transient Analysis:
![1_1trans](https://github.com/user-attachments/assets/6d4b222e-7f86-49d2-8cac-7b0d8213e49f)

    Gain Calculation:
    **Gain=Vout/Vin**
    0.979-0.818/1-0.990
    =16.1
    **In dB Scale:**
    dB=20log(Gain)=24.31
#### AC Analysis:
![1_1ac](https://github.com/user-attachments/assets/8d6889ab-c541-4cc7-b569-76d2cdd1f022)

    -3dB Gain=15.82 
    Bandwidth=2.29GHz

    For 1:2 Ratio:
    Itotal= P/Vdd=1*10^-3/1.8= 0.55mA
    Itotal=Iref+Ix
          =3Iref(Since ratio is 1:1)
    Iref=0.183mA
    Ix=2Iref=0.366mA
##### Circuit:
![1_2ckt (2)](https://github.com/user-attachments/assets/3b3c4e87-594d-4657-a225-499196cefe3e)</br>
#### DC Analysis:
By Adjusting Width</br>
![1_2ratio_](https://github.com/user-attachments/assets/6b798dd8-9b07-48ba-a3bc-f72511dd8d46)

<u>So We can observe that Ix is twice as Iref(Due to 1:2 Ratio)</u></br>
Current mirroring is ocurring as per the ratio</br>
#### Transient Analysis:
![1_2trans](https://github.com/user-attachments/assets/f33ba827-5546-4795-bfc8-fe644597c0ad)

    Gain Calculation:
    **Gain=Vout/Vin**
    0.774-0.595/1-0.990
    =17.9
    **In dB Scale:**
    dB=20log(Gain)=25.05
#### AC Analysis:
![1_2ac](https://github.com/user-attachments/assets/455a6f15-0b5e-4099-a9d9-c6759b4c4a27)


    -3dB Gain=16.22
    Bandwidth=1.15GHz


      
