PMSM FOC PWM Step Debugger
Interactive browser-based PMSM (Permanent Magnet Synchronous Motor) Field-Oriented Control (FOC) debugger and visualization tool.
Overview
This project provides a graphical environment for understanding and debugging PMSM current control loops. It combines a continuous-time motor model with a discrete-time current controller and allows users to step through PWM periods, inspect internal variables, and visualize the effect of control errors.
The simulator is intended for:
•	Motor-control engineers
•	Embedded software developers
•	Control-system students
•	FOC algorithm debugging and education
Features
Motor Model
•	PMSM dq-axis model
•	Continuous machine integration
•	RK4 numerical solver
•	Configurable machine parameters:
o	Stator resistance (R)
o	d-axis inductance (Ld)
o	q-axis inductance (Lq)
o	Permanent magnet flux linkage (ψf)
o	Pole pairs (p)
Controller
•	Discrete current PI controller
•	Configurable:
o	Kp
o	Ki
o	PWM frequency
•	Back-EMF feedforward option
•	Selectable integrator methods:
o	Forward Euler
o	Trapezoidal
Visualization
•	dq current vector scope
•	dq voltage vector scope
•	Dynamic autoscaling
•	Command and measured current display
•	Back-EMF visualization
•	Torque visualization
Time-Domain Analysis
•	Current plots
•	Voltage plots
•	Torque plots
•	Interactive cursors (C1/C2)
•	Cursor measurements
•	Plot zooming
Debugging
•	PWM-period step execution
•	Detailed computational trace
•	Error-angle injection (Δθ)
•	Numerical inspection of intermediate variables
•	Data logging
•	CSV export
Mathematical Model
Electrical speed:
ωe = p · ωm
Mechanical speed:
ωm = RPM · 2π / 60
Back-EMF:
E = ωe · ψf
d-axis equation:
ud = R·id + Ld·(did/dt) − ωe·Lq·iq
q-axis equation:
uq = R·iq + Lq·(diq/dt) + ωe·Ld·id + ωe·ψf
Electromagnetic torque:
T = 1.5 · p · [ ψf·iq + (Ld − Lq)·id·iq ]
Usage
1.	Set motor parameters.
2.	Set controller gains.
3.	Configure speed and angle error.
4.	Select current references.
5.	Press Step to advance one PWM period.
6.	Use Free Run for continuous simulation.
7.	Use cursors and zoom tools for analysis.
8.	Export CSV data when required.
Browser Compatibility
Tested with:
•	Google Chrome
•	Microsoft Edge
•	Mozilla Firefox
No installation required.
License
MIT License
Author
PMSM FOC PWM Step Debugger Interactive educational and debugging tool for motor-control development.
