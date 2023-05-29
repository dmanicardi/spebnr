# SPEBNR: a Simple Python Environment for statistical estimation of Biochemical Network Robustness

SPEBNR is a simple Python tool that permits estimating the distance between two biochemical systems. 

Each system consists of two distinct components: 
  * a *process* describing the behaviour of the program in a specific step; 
  * an *environment evolution* describing the effect of the environment on the data space.

Two systems are compared via a (pseudo)metric, called the *evolution metric*. Thanks to the possibility of extrapolating process behaviour from that of the system typical of our model, this metric allows us to
  * verify how well a system is fulfilling its tasks by comparing it with its specification;
  * compare the activity of different biochemical systems;
  * compare the behaviour of one biochemical system with respect to different initial process and changes in the initial concentrations.

Via the metric we introduce a dependability property of a biochemical system, called *robustness*.

Robustness is the ability of the program to tolerate internal and external perturbation while preserving the original behaviour.

In [EnvZOmpR.py](./EnvZOmpR.py) createSystem is used to model a simple biochemical system in which the *EnvZ/OmpR Osmoregulatory Signaling System* regulates two proteins in the *Escherichia Coli* bacterium. We use our algorithm to evaluate the differences between the original EnvZ/OmpR system and two other systems which are obtained by perturbing its initial state. Then, we use our algorithm to evaluate the differences between the original EnvZ/OmpR system S and 50 systems which have an input distance in (eta_1-1,eta_1], for five different values for eta_1: 0.3, 0.4, 0.5, 0.6, 0.7.

In [createSystem.py](./createSystem.py) uses SPEBNR to create the biochemical system and model the biochemical species.

In [spebnr.py](./spebnr.py) is used in order to model the system and calculated the distance over systems and the distance between system distributions. Then, it calculates the robustness of the biochemical system.

## Download 

To download SPEBNR you have just to clone GitHub project:

```
git clone https://github.com/desimani/spebnr.git
```

Run this command in the folder where you want to download the tool.

## How to run experiments

To run experiments Python3 (>= 3.11) is needed. Moreover, the following Python packages must be available:
  * [numpy](https://numpy.org) >= 1.23.4
  * [scipy](https://scipy.org/) >= 1.10.1
  * [matplotlib](https://matplotlib.org) >= 3.6.2
  * [statistics](https://github.com/digitalemagine/py-statistics) >= 1.0.3.5
  
To install all the required packages you can just run:

```
pip install -r requirements.txt
```

If all the needed package are installed in your system, you have to execute:

```
EnvZOmpR.py
```
