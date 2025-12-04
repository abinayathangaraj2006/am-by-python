AM-USING-PYTHON-
AIM

To generate an amplitude-modulated (AM) signal using Python.

EQUIPMENTS REQUIRED

• Computer with i3 Processor

• Colab

THEORY:

Amplitude Modulation (AM) is a process used in analog communication where the strength (amplitude) of a high-frequency carrier wave is varied in accordance with the instantaneous value of a low-frequency message signal. The main purpose of modulation is to enable the transmission of information signals over long distances without significant loss or distortion.

In AM, the carrier frequency remains constant, but its amplitude changes as per the variations in the message signal. This results in a new waveform that carries the original information within its envelope. The modulated signal occupies a specific range of frequencies around the carrier, known as the bandwidth.

The AM signal contains the carrier and two additional components called sidebands, which carry the actual information. The upper and lower sidebands are symmetrically located around the carrier frequency.

Amplitude Modulation is widely used in radio broadcasting, aircraft communication, and public address systems because of its simplicity and ease of generation and reception. However, it is less efficient in terms of power and bandwidth compared to other modulation techniques like FM and PM.

Algorithm

Start the program.

Set the values for carrier frequency, message frequency, modulation index, sampling rate, and duration.

Generate a time vector for the given duration.

Create the message signal (low-frequency waveform).

Create the carrier signal (high-frequency waveform).

Vary the amplitude of the carrier signal according to the message signal to obtain the AM wave.

Plot the message, carrier, and modulated signals.

Display the results.


program :
import numpy as np
import matplotlib.pyplot as plt

Am = 4.3
fm = 324
Ac = 8.6
fc = 3240
fs = 32400
t = np.arange(0, 2/fm, 1/fs)
m = Am * np.cos(2 * np.pi * fm * t)
plt.subplot(3, 1, 1)
plt.plot(t, m)
plt.title('Message Signal')
plt.xlabel('Time (s)')
plt.ylabel('Amplitude')
c = Ac * np.cos(2 * np.pi * fc * t)
plt.subplot(3, 1, 2)
plt.plot(t, c)
plt.title('Carrier Signal')
plt.xlabel('Time (s)')
plt.ylabel('Amplitude')
s = (Ac + m) * np.cos(2 * np.pi * fc * t)
plt.subplot(3, 1, 3)
plt.plot(t, s)
plt.title('AM Signal')
plt.xlabel('Time (s)')
plt.ylabel('Amplitude')

plt.tight_layout()
plt.show()
 outputwave form:
 <img width="812" height="606" alt="Screenshot 2025-12-04 190151" src="https://github.com/user-attachments/assets/24a0958e-deeb-4a0b-9d3b-7ab83a47169d" />
 tabulation:
 ![WhatsApp Image 2025-12-04 at 19 03 29_670b121e](https://github.com/user-attachments/assets/9f7d8333-a9bf-44ff-a241-3c198496e841)
 Calculation

ma (Theory) = am/ac =0.5

ma(Practical) = (Emax-Emin)/(Emax+Emin) =15.1

RESULT:

Thus the amplitude modulation and demodulation is experimentally done and the output is verified.


Stop the program.

