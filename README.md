RMIS provides a suite of Matlab files that implement the "Relaxed Multirate Infinitesimal Step" method, an up-to-fourth order method that utilizes an explicit Runge--Kutta method for "slow" dynamics, and either an explicit (ERK), diagonally-implicit (DIRK), or fully-implicit (IRK) Runge--Kutta method for the "fast" dynamics, in an additively-split multirate problem:
   y'(t) = f_slow(t,y(t)) + f_fast(t,y(t)),
   y(t_0) = y_0
This software is designed for instructional use and has been implemented to be easily understood and modified.  As a result, certain efficiency-related optimizations have been omitted.

This implementation focuses on fixed-size time steps for both the fast and slow dynamics, however the single-rate codes in this repository (ERK, DIRK, IRK) also support adaptive time stepping.

To support exploration of the RMIS implementation, we provide a large number of Butcher tables (over 70), holding the coefficients for existing single-rate methods in each of these categories.

We note that this repository has been forked off of another public Git repository,
     https://drreynolds@bitbucket.org/drreynolds/rklab.git
that is used for classroom instruction and exploration of one-step Runge--Kutta methods (including additive Runge--Kutta, ARK, methods for mixed implicit-explicit time integration).

We provide two example problems that may be used to test different methods, and that may be used as a template for creating new problems.  These test problems include:
(a) a non-stiff variant of the Van der Pol oscillator (two-component
    nonlinear ODE system).
(b) a stiff Brusselator problem (three-component nonlinear ODE
    system), and

These codes require Matlab v2016b or newer.
