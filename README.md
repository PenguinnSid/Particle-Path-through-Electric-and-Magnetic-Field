# Particle-Trajectory-through-Electric-and-Magnetic-Field-Plot

Calculates and plots the path taken by a charged particle through a uniform Electric and Magnetic Field.

Variables Needed:
  1) t -> Total Sampling time
  2) t0 -> Initial Time
  3) delta_t -> Timestep
  4) m -> Mass of the particle
  5) q -> Charge on the particle

Vectors Needed:
  1) S -> Initial Position of the particle
  2) V -> Initial Velocity of the particle
  3) B -> Magnetic Field Vector
  4) E -> Electric Field Vector
  5) F -> Lorentz Force
  6) positions -> Holds positions of the particle at each timestep

Calculation:

  1) This process works on the basis of Lorentz Force.
    F = q(E + vxB)  [Force = Charge * (Electric Field + velocity x Magnetic Field)]

  2) After finding the force acting on the particle, we can find the momentum at that instant.
    Pf = P0 + F.dt  [Final Momentum = Initial Momentum + Change in Momentum]

  3) And finally, the position can be found.
    Sf = S0 + v.dt  [Final Position = Initial Position + Change in Position]
    where v = Pf/m  [New Velocity = Final Momentum/mass of the body]

  This entire process is done in a while loop for calculating the positions at 10^4 instants of time.
  The velocity is put back into the Lorentz Force equation to calculate the force at the next timestep.
  The Positions are appended into a vector that stores the x,y and z positions of the particle at each timestep.

The position vector is then plotted in 3D space to provide the actual path of the particle under the influence of the electric and magnetic field.

How to use:
  Download the ipynb file and upload it in a google colab notebook(simpler)/jupyter notebook.
  Tune the vectors to your liking.
  Run the program (Ctrl+F9).
  Select the particle you want to simulate the trajectory of(1/2/3).
