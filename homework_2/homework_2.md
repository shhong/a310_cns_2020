# Homework 2 (Due: Mar 27, 2020)

## 1.  Summation of excitatory synaptic inputs

Use the simulation in the **1 Pyramidal cell + 2 stimuli** part of Tutorial 2 (part 2) that simulates a cortical pyramidal neuron with the passive membrane and two synapses, managed by two point process managers. Both synapses activate at _t_=50 ms, and both are set to excitatory ones (e = 0 mV).

Run three simulations and record the EPSP traces at the soma: 1) Both synapses are active (EPSP<sub>1+2</sub>), 2) only the first synapse is active (set `nc[1].weight[0]`= 0 to turn off the second synapse; EPSP<sub>1</sub>), 3) only the second synapse is active (set `nc[0].weight[0]`= 0 to turn off the first; EPSP<sub>2</sub>).

Do they sum linearly (approximately) , i.e., EPSP<sub>1+2</sub> ≈ EPSP<sub>1</sub> + EPSP<sub>2</sub>? By moving two synapses around, find out in which situation the the summation is approximately linear or not.

**Note:** Before you run simulations, make sure that you properly rescale synaptic conductances (as you did in "Synaptic scaling") each time so that the EPSP sizes of two synapses are similar.

## 2.  Summation of excitatory and inhibitory synaptic inputs

Here we ask you to reproduce a version of Fig 5.1 in the Koch for the transient synaptic inputs. Use the **1 Pyramidal cell + 2 stimuli**, but make one of the synapses inhibitory by changing the reversal potential (`e`) to -76 mV (Note that this is the same as the resting membrane potential and threfore the synapse will deliver _shunting inhibition_). Also change `tau2`=100 ms and `stim[1].start`=0 ms so that it should activate slowly like GABA<sub>B</sub> synapses from the beginning of the simulation.

1. __(Proximal inhibition)__ Place the excitatory synapse to a distal part of a basal dendrite and the inhibitory synapse close to soma. Run simulations with different conductance values, make a plot for the EPSP amplitude as Fig. 5.1A.
2. __(Distal inhibition)__ Now move the inhibitory synapse also to a distal part in the _same dendrite_ as the excitatory synapse, and make a plot as 1 (i.e., Fig. 5.1B).
3. __(Different branch)__ Move the inhibitory synapse to a different dendrite than the excitatory synapse, and make a similar plot as 1 and 2.
4. It is known that parvalbumin (PV)-expressing inhibitory interneurons prefer making synapses close to a soma of a pyramidal neuron, whereas other interneurons such as somatostatin (SOM)-expressing neurons are known to prefer dendrites ([Thomson and Lamy, Front. Neurosci., 2007](http://journal.frontiersin.org/article/10.3389/neuro.01.1.1.002.2007)). Discuss what you can predict about the computational roles of different interneurons based on your simulation results (e.g. [Wilson et al., Nature, 2012](http://www.nature.com/nature/journal/v488/n7411/full/nature11347.html)).

## 3. Channel dynamics during spike generation

Here we use the current clamp simulation of a single compartment neuron with the Hodgkin-Huxley mechanism to observe how ion channels activate during an action potential firing, triggered by a brief current injection.

Set up the same current clamp simulation as the part 1 of the NEURON tutorial 3, but with two differences:
* the neuron has the Hodgkin-Huxley mechanism (`hh`) instead of the Morris-Lecar,
* the duration of the injection (`ic.dur`) is short (1 ms).

1. Discuss how the channel activates during spike generation in a similar way to Fig. 6.5 in the textbook, by recording and showing how the channel gating variables, `m_hh`, `h_hh`, and `n_hh`, evolve in time.
2. __(Anode break excitation)__ Set the injected current (`ic.amp`) to -0.2 nA, run the simulation, and explain the result.
3. Plot the 2D phase plots of voltage and other gating variables. For example, `v` vs `n_hh`, `n_hh` vs `m_hh`, etc. In each plot, draw several trajectories with different injected currents, particularly including the negative ones (as in 2). Which pair of variables are most helpful to understand the system's behavior and how? Is your answer to the question 2 consistent with the phase plots?
