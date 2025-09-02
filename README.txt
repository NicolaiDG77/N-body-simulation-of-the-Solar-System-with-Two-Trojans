Animation:

In order to get a correct animation referring to this Solar System simulation, it is necessary to disable the following functions:

energy_drift()

Orbits()

Rotational()

Note: This can be done by commenting out the method call lines.

-----------------------------------------------------------------------------------------------------------------------------


Algorithm:

A numerical simulation of the N-body problem for our Solar System and two Trojans using a Runge–Kutta integrator and Newtonian mechanics.

energy_drift(): Computes the energy drift of the system.

Orbits(): Computes the orbital trajectories.

Rotational(): Computes the rotational speed profile of the system with respect to displacement from the Sun.

h: a variable used for the dynamic time step in the integration process, note a great value leads to numerical errors.

Note: For complete derivations, see the attached report.

-------------------------------------------------------------------------------------------------------------------------------

Dependency (Tested with Python 3.13.5):

NumPy 2.3.2 — vectorized arrays and math for the N-body state and updates.

Matplotlib 3.10.6 — plots/animation for orbits, energy drift, rotational profile.

jplephem 2.23 — Importing astronomical data on planets in our Solar System (the de430.bsp data).

tkinter (built-in) — used to display animation in an external GUI window

Planet300 (file): Some of the planetary data is extracted from this file and it is thus required that this file remains in the same folder as the code 'handin_code' by default.

Note: Other dependencies appearing in `requirements.txt` (e.g., Jupyter-related libraries, utility packages, etc.) are included automatically via `pip freeze`. They are pinned for reproducibility but are not directly used in this notebook.


---------------------------------------------------------------------------------------------------------------------------------

Risk assessment

While dependencies are pinned for full reproducibility in requirements.txt, the longevity of reproducibility might be affected by updates to the Jupyter libraries associated with the project like NumPy, Matplotlib, jplephem, and tkinter. Thus, it is recommended to check the related documentation if there are syntax changes. In terms of visualization method, tkinter was found to be the most stable for displaying the animation, but there are many alternatives which could be selected, for example through the backend feature in Spyder. Note, however, that this may require modification of the code in the animation function. This algorithm uses a manually coded Runge–Kutta integrator function and therefore does not depend on any external integration libraries. This algorithm was created in a Python 3.13.5 environment.

