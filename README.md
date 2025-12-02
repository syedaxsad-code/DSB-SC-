# DSBSC


EX NO: 2	DSB-SC-AM MODULATOR AND DEMODULATOR

AIM:

To write a program to perform DSBSC modulation and demodulation using SCI LAB and study its spectral characteristics

EQUIPMENTS REQUIRED

•	Computer with i3 Processor
•	SCI LAB

Note: Keep all the switch faults in off position

Algorithm:

1.	Define Parameters:
•	Fs: Sampling frequency.
•	T: Duration of the signal.
•	Fc: Carrier frequency.
•	Fm: Frequency of the message signal.
•	Amplitude: Maximum amplitude of the message signal.
2.	Generate Signals:
•	Message Signal: A sinusoidal signal that will be modulated.
•	Carrier Signal: A high-frequency sinusoidal signal used for modulation.
3.	DSBSC Modulation:
•	Modulated Signal: Multiply the message signal by the carrier signal to produce the DSBSC signal.
4.	DSBSC Demodulation:
•	Multiplication: Multiply the modulated signal by the carrier signal to get the product of the message signal with itself (i.e., the original message signal plus high-frequency components).
•	Low-pass Filtering: Apply a Butterworth low-pass filter to remove the high- frequency components and recover the original message signal.
5.	Visualization:
Plot the message signal, carrier signal, DSBSC modulated signal, and the recovered signal after demodulation.
PROCEDURE

•	Refer Algorithms and write code for the experiment.
•	Open SCILAB in System
•	Type your code in New Editor
•	Save the file
 
•	Execute the code
•	If any Error, correct it in code and execute again
•	Verify the generated waveform using Tabulation and Model Waveform

Model Waveform

<img width="703" height="679" alt="image" src="https://github.com/user-attachments/assets/e7c7c7f8-ccf2-41ac-b1f3-325989941a6f" />

Program
```
ac=14.8;
Am=7.4;
fc=3100;
fm=310;
fs=31000;
t=0:1/fs:2/fm;
wc=2*3.14*fc;
wm=2*3.14*fm;
e1=(Am*sin(wm*t));
subplot(3,1,1);
plot(t,e1);
title("Modulating signal");
xgrid
e2=(ac*sin(wc*t));
subplot(3,1,2);
plot(t,e2);
title("Carrier signal");
xgrid
e3=(Am/2.*cos(wc*t-wm*t))-(Am/2.*cos(wc*t+wm*t));
subplot(3,1,3);
plot(t,e3);
title("Double side band suppressed carrier");
xgrid
```



Output Graph
![WhatsApp Image 2025-12-02 at 20 16 13_94d2033d](https://github.com/user-attachments/assets/8e8a593d-72b6-46a9-a547-d60ce1f20567)


Tablular Column

![WhatsApp Image 2025-12-02 at 20 29 08_d0fa94e6](https://github.com/user-attachments/assets/c173c32c-852c-483e-a6fc-7dde980421d7)



Result

Thus the DSB-SC-AM Modulation and Demodulation is generated.

