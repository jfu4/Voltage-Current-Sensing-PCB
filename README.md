# Voltage and current measuring PCB for UBC Aerodesign
The purpose of this project was to design a small and inexpensive board to monitor voltage and current in the plane. 

# Voltage Sensing:  
<img width="476" height="353" alt="image" src="https://github.com/user-attachments/assets/417749fd-432a-4eae-b1f4-7cf69662f119" />  

**Description:**  

Designed for Lipo4s (12V - 16.8V), but can use other Lipo batteries as well.
In order to keep the board small and cheap, the design uses a simple voltage divider and amplifier. The voltage divider resistances are tailored to ensure the voltage range will be:
@ 16.8V, Vout = 3.20V
@ 12V, Vout = 2.28V
as the signal will be fed into a 3.3V MCU. A differntiator was considered to increase the resolution, but was ruled out in the end in order to save cost/space.

# Current Sensing  
<img width="479" height="231" alt="image" src="https://github.com/user-attachments/assets/a0e055e1-a50a-4aa1-8d2e-9c39540e78c2" />  

**Description:**  

Designed for high current applications (up to 60 A). This design uses a shunt resistor and current sense amplifier to sense current.
Calculations for determining shunt resistor value:  
<img width="975" height="493" alt="image" src="https://github.com/user-attachments/assets/e61cc531-d1b1-4e2d-9bb8-1b5ea66382db" />  
<img width="636" height="209" alt="image" src="https://github.com/user-attachments/assets/bba47377-e161-438a-baaf-9b4a46c6995d" />  
It was deemed that the accuracy was sufficent for our setup at 1 m&Omega;.
 

# LED  
<img width="139" height="249" alt="image" src="https://github.com/user-attachments/assets/4e258ecd-5776-48f0-ac66-d84a3a79e8ad" />  

**Description:**  

Turns on when board is connected to the main board (3.3V)

# Connectors
<img width="444" height="450" alt="image" src="https://github.com/user-attachments/assets/62d0aa46-5a7b-4c70-ae86-6132561a8c82" />  

Used XT-60 connectors for the LiPos and JST connectors for the MCU.

# PCB Layout:
<img width="1471" height="490" alt="image" src="https://github.com/user-attachments/assets/5421d2de-0d90-45c0-ba52-fac371fd8ef6" />  

**Description:**  
To reduce the overall board size, components were arranged in a compact layout with efficient routing. Since the design must measure currents up to ~60 A, high-current traces were left exposed so they can be reinforced with solder to reduce resistance and improve ampacity. A 4-layer PCB stackup was chosen to further increase current-carrying capability and ensure robust thermal and electrical performance.

3D Model:
<img width="1236" height="406" alt="image" src="https://github.com/user-attachments/assets/508c95b8-051b-4e3e-933d-c0e899c4fc12" />  

Finished dimensions were 2295 mils x 865 mils.
