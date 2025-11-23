# -Frequency-Modulation-and-Demodulation-using-NumPy-and-Matplotlib-

__Aim:__

To implement and analyze frequency modulation (FM) using Python's NumPy and Matplotlib libraries.

__Apparatus Required:__ 

1. Software: Python with NumPy and Matplotlib libraries
   
2. Hardware: Personal Computer

 
__Theory:__

Frequency Modulation (FM) is a method of transmitting information over a carrier wave by varying its 
frequency in accordance with the amplitude of the input signal (message signal). The frequency of the carrier 
wave is varied according to the instantaneous amplitude of the message signal.

__Algorithm:__

1. Initialize Parameters: Set the values for carrier frequency, message frequency, sampling frequency, and 
   frequency deviation.
   
2. Generate Time Axis: Create a time vector for the signal duration.
    
3. Generate Message Signal: Define the message signal as a cosine wave.
    
4. Compute the Integral of the Message Signal: Calculate the integral of the message signal over time.
    
5. Generate FM Signal: Apply the FM modulation formula to obtain the modulated signal.
 
6. Plot the Signals: Use Matplotlib to plot the message signal, carrier signal, and modulated signal.

__Programme:__
```
import numpy as np
import matplotlib.pyplot as plt

Ac = 37.7
fc = 8900

Am = 18.9
fm = 890

fs = 89000
beta = 3.6

# Time Vector
t = np.arange(0, 2/fm, 1/fs)

# Message Signal
Em = Am * np.cos(2 * np.pi * fm * t)

# Carrier Signal
Ec = Ac * np.cos(2 * np.pi * fc * t)

# FM Signal
Efm = Ac * np.cos(2 * np.pi * fc * t + beta * np.sin(2 * np.pi * fm * t))

# Plotting
plt.figure(figsize=(10, 6))

plt.subplot(3, 1, 1)
plt.plot(t, Em)
plt.title("Message Signal")
plt.grid()

plt.subplot(3, 1, 2)
plt.plot(t, Ec)
plt.title("Carrier Signal")
plt.grid()

plt.subplot(3, 1, 3)
plt.plot(t, Efm)
plt.title("FM Signal")
plt.grid()

plt.tight_layout()
plt.show()

```
CALCULATION:

<img width="859" height="1254" alt="image" src="https://github.com/user-attachments/assets/8b5ba332-0849-4160-b521-7cea946e3336" />

<img width="1080" height="861" alt="image" src="https://github.com/user-attachments/assets/aaf8a14b-52eb-42d8-ae6e-7d350a52efd5" />


__Output:__

<img width="630" height="469" alt="image" src="https://github.com/user-attachments/assets/ca2c712c-7201-4d58-b2eb-844ef110150e" />


RESULT:

<img width="1280" height="445" alt="image" src="https://github.com/user-attachments/assets/e9632f4d-7207-4b80-8fa1-ca0df5fcb904" />


__Result:__
