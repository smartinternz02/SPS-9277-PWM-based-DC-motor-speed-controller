# SPS-9277-PWM-based-DC-motor-speed-controller
PWM based DC motor speed controller


DC motors are widely and very commonly used motors. From battery operated power tools, CPU fans, toy cars, mixers, even in Industrial use for conveyors etc. When it comes to controlling the speed of these motors it becomes a bit tricky. In order to do that, we have to design a circuit that can regulate the power getting delivered to the motor. Thus by increasing or decreasing the power the speed of the motor gets increased or decreased. This can be done by using variable resistor, but to achieve that high power variable resistors are needed so that it can dissipate plenty amount of power as heat. Since it dissipates power as heat which is use less and gets wasted, this technique is very inefficient and creates a huge power loss. 
An efficient way to do that is by Pulse Width Modulation(PWM). 
This PWM circuit is built using a Timer 555 IC and some complementary components. The power is controlled using a potentiometer. And described below in the circuit.

Working Principle
The IC 555 in this circuit is being operated in astable mode, which produces a continuous HIGH and LOW pulses. Now if we change the width of this HIGH and LOW pulse without changing the frequency we call it as Pulse Width Modulation. 
By shorting the pin 2(trigger) and 6(threshold) pin of IC 555 making it to run in astable mode, and in turn connected to ground via 0.1µF capacitor, which determines the frequency of the pulses. Now the 100k potentiometer with the fast switching diodes 1N4148, determines the charging time and discharging time of the capacitor. Due to the involvement of the diodes the charging time and the discharging time of the capacitor is equal thus there is no change in frequency. By varying the potentiometer knob the ton  increases or decreases which in turn changes the duty cycle since 
Duty Cycle(D) = ton /(ton + toff).
And as we know
Output Voltage = Duty Cycle * Vcc.
By varying the output voltage, it increases or decreases the delivering power to the Motor, thus increasing or decreasing the speed of the Motor.


Here's a link how I created the PCB layout and a small description for the project.
https://drive.google.com/file/d/1GSkcuYEkGf2wB12m3sBFJlwohxd9rQKm/view?usp=sharing

:)
