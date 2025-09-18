## AC-to-DC-Converter-Project
MATLAB Simulink Project: AC to DC Coverter with rectifier, non-inverting op-amp, RC low-pass filter for min. ripple

# Introduction

I executed this mini-project to apply and improve both electrical simscape and circuit theory knowledge by examining circuit components and relations between them. I aimed to study on combined circuits and concepts to reach my goal which is converting an AC signal to a DC signal. , full-wave rectifier bridge with four diodes, a resistor and a capacitor for converting. But when I converted AC to DC 

# Project in Detail

This project demonstrates the design of an AC to DC converter using:

- Transformer ==> I used a voltage transformer to represent voltage step down 220 V to 10 V.
  
- Full-wave rectifier ==> A full-wave rectifier bridge with four diodes, a resistor and a capacitor for converting.
   Diodes' forward voltage : 0.7 V (voltage drop)
   Resistor for rectifier : I would prefer 5 kOhm resistor, because in real life applications 1 kOhm- 10kOhm resistors are more desirable.
  
- Op-amp 
- RC low-pass filter

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
