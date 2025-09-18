## AC-to-DC-Converter-Project
MATLAB Simulink Project: AC to DC Coverter with rectifier, non-inverting op-amp, RC low-pass filter for min. ripple

# Introduction

I executed this mini-project to apply and improve both electrical simscape and circuit theory knowledge by examining circuit components and relations between them. I aimed to study on combined circuits and concepts to reach my goal which is converting an AC signal to a DC signal.  full-wave rectifier bridge with four diodes, a resistor and a capacitor for converting. But when I converted AC to DC 

# Project in Detail

This project demonstrates the design of an AC to DC converter using:

- Transformer ==> I used a voltage transformer to represent voltage step down 220 V to 10 V.
  
- Full-wave rectifier ==> A full-wave rectifier bridge with four diodes, a resistor and a capacitor for converting.
   Diodes' forward voltage : 0.7 V (voltage drop)
   Resistor's resistance : I preferred 5 kOhm resistor, because load is more preferred between 1 kOhm- 10 kOhm in real life applications. Also I wanted to see the ripple more clearly on the signal.
   Capacitans of the capacitor: I chose 100 uF (micro Farad). So time constant is 0.5 s from R*C. It means capacitor will be discharge in 500 ms. Since in Türkiye, the mains AC frequency is 50 Hz, I chose AC voltage source's frequency as 50 Hz. In full-wave rectifier, frequency is doubled because it converts all positive and negative half-waves to positive. So, capacitor would start to charge 50*2=100 Hz, 1/(100 Hz)= 0.01 s= 10 ms  after it starts to discharge. Therefore, 500 ms >> 10 ms. This creates a strong smoothing effect but since resistance is not that great, ripple will occur.
  Now, we have a DC signal but there are two problems. First one is, because of diode voltage drops output voltage is not 10 V ideally. In four diodes bridge, two diodes are active on the positive side of signals and other two are opened circut. Moreover, on the negative side, vice-versa. So, in both case we always have 0.7+0.7=1.4 V voltage drop. Therefore, 10-1.4=8.6 V for output voltage. But lets make it 10 V as we desired.
- A non-inverting Op-amp ==> In order to have a gain of 1.4, I chose R2 = 7 kOhm and R1 = 43 kOhm for Vout=Vin(1+(R2/R1)). So, we now have 10 V DC signal. But the second problem is there is still ripple. We want to make the signal more smooth and clean. Furthermore, a low-pass filter woul work to prevent high frequencies. 
- RC low-pass filter ==> First of all, why did not I prefer a serie RL low-pass filter? Since I wanted to consider real life conditions, inductors are generally more expensive and larger than capacitors. So, my choice depends on less cost and a proper design.  

## Purpose
The aim is to achieve ~10 V DC with minimized ripple for stable supply applications.

## Tools
- MATLAB Simulink
- Circuit Simulation Simscape
- Basic Circuit Theory

## Results  
- Full-wave rectifier: ~8.6 V DC with ~172 mV ripple  
- Op-amp used to restore voltage to 10 V  
- RC filter further reduced ripple
