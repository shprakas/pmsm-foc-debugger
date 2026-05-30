# PMSM FOC PWM Step Debugger

Interactive browser-based PMSM (Permanent Magnet Synchronous Motor) Field-Oriented Control (FOC) debugger and visualization tool.

---

## Overview

This project provides a graphical environment for understanding and debugging PMSM current control loops.

It combines:

- A continuous-time motor model
- A discrete-time current controller
- PWM-period stepping
- Internal variable inspection
- Interactive visualization of control errors

The simulator is intended for:

- Motor-control engineers
- Embedded software developers
- Control-system students
- FOC algorithm debugging and education

---

## Features

### Motor Model

- PMSM dq-axis model
- Continuous machine integration
- RK4 numerical solver

Configurable parameters:

- Stator resistance (R)
- d-axis inductance (Ld)
- q-axis inductance (Lq)
- Permanent magnet flux linkage (ψf)
- Pole pairs (p)

### Controller

- Discrete current PI controller
- Configurable Kp and Ki
- Configurable PWM frequency
- Back-EMF feedforward
- Selectable integration methods:
  - Forward Euler
  - Trapezoidal

### Visualization

- dq current vector scope
- dq voltage vector scope
- Dynamic autoscaling
- Command and measured current display
- Back-EMF visualization
- Torque visualization

### Time-Domain Analysis

- Current plots
- Voltage plots
- Torque plots
- Interactive cursors (C1/C2)
- Zooming and measurements

### Debugging

- PWM-period stepping
- Detailed computation trace
- Error-angle injection (Δθ)
- CSV export
- Data logging

---

## Mathematical Model

### Mechanical Speed

```math
\omega_m = \frac{\text{RPM}\cdot 2\pi}{60}
```

### Electrical Speed

```math
\omega_e = p\cdot\omega_m
```

### Back-EMF

```math
E = \omega_e\psi_f
```

### d-axis Voltage Equation

```math
u_d = Ri_d + L_d\frac{di_d}{dt} - \omega_eL_qi_q
```

### q-axis Voltage Equation

```math
u_q = Ri_q + L_q\frac{di_q}{dt} + \omega_eL_di_d + \omega_e\psi_f
```

### Electromagnetic Torque

```math
T_e = 1.5\,p\left(\psi_f i_q + (L_d-L_q)i_di_q\right)
```

---

## Usage

1. Set machine parameters.
2. Set controller gains.
3. Configure speed and angle error.
4. Set current references.
5. Press **Step** to execute one PWM period.
6. Use **Free Run** for continuous simulation.
7. Inspect vector scopes and waveforms.
8. Export CSV data if required.

---

## Browser Support

Tested with:

- Google Chrome
- Microsoft Edge
- Mozilla Firefox

No installation required.

---

## Live Demo

After enabling GitHub Pages:

```text
https://YOUR_USERNAME.github.io/pmsm-foc-debugger/
```

---

## License

MIT License

---

## Author

Astha Tiwari

Interactive educational and debugging tool for PMSM Field-Oriented Control development.
