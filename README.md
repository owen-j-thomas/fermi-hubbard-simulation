# fermi-hubbard-simulation

This project served as a self directed proof of concept, demonstrating the simulation of a simplified fermi-hubbard interaction in a quantum circuit through J-W encoding and trotterised time dynamics using Cirq.

Quench dynamics in the 2-site Fermi-Hubbard model are simulated using Google's Cirq framework. The Fermi-Hubbard model is the canonical testbed for quantum simulation of correlated electrons, and a natural target for near-term quantum hardware.

A doubly-occupied initial state $|\uparrow\downarrow, 0\rangle$is prepared and evolved under the full Hubbard Hamiltonian. The simulation is built entirely at the circuit level: fermionic operators are mapped to qubit Pauli strings via the Jordan-Wigner transformation, and time evolution is approximated through first-order Trotter decomposition. The code file is well documented throughout.

The notebook proceeds in stages. First, the implementation is verified against the exact free-fermion solution ($U = 0$), where both spin species oscillate independently as $\cos^2(t)$. Having established confidence in the circuit, the on-site Coulomb repulsion $U$ is introduced and we observe how increasing $U/t$ progressively suppresses charge fluctuations and double occupancy.
