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
    For 1:1 Ratio:</br>
    Itotal=P/Vdd=1*10^-3/1.8=0.55mA</br>
    Itotal=Iref+Ix</br>
          =2Iref(Since ratio is 1:1)</br>
          Iref=Ix=0.275mA)</br>
##### Circuit:
![1_1ckt](https://github.com/user-attachments/assets/64689321-ce2d-4ffa-8a76-c933d8175abc)</br>
#### DC Analysis:
By Adjusting Width</br>
![1_1_ratio](https://github.com/user-attachments/assets/9b8a5cbf-144d-482c-a6f9-902903185359)

<u>So We can observe that both Iref and Ix are equal (Due to 1:1 Ratio)</u></br>
Current mirroring is ocurring as per the ratio</br>
#### Transient Analysis:
![1_1trans](https://github.com/user-attachments/assets/6d4b222e-7f86-49d2-8cac-7b0d8213e49f)

    Gain Calculation:</br>
    **Gain=Vout/Vin**</br>
    0.979-0.818/1-0.990</br>
    =16.1</br>
    **In dB Scale:**</br>
    dB=20log(Gain)=24.31</br>
#### AC Analysis:
![1_1ac](https://github.com/user-attachments/assets/8d6889ab-c541-4cc7-b569-76d2cdd1f022)

    -3dB Gain=15.82</br>
    Bandwidth=2.29GHz


      
