# Decomposition-Algorithm
Decomposition algorithm decomposes a MCT quantum circuits of any Boolean function expressed in a Positive Polarity Reed-Muller PPRM expansion. 

Input of decomposition algorithm is a MCT quantum circuit that is written in circuit.txt file. Each line in circuit.txt file represent one MCT quantum gate in form “n c1 c2 .. cn t” where n is a number of controls, c1 c2 .. cn are control qubits of a quantum gate and t is target qubit of a quantum gate. For example, we consider a MCT quantum circuit with the gates “cnot(x1, x2, x3, x4), cnot(x1, x2, x3) and not(x3) that can written in circuit.txt file as follows:

3 1 2 3 4 

2 1 2 3

0 3

 Decomposition algorithm consists of the following major methods:
 
1-	get_circuit_from_file: read a quantum circuit from circuit.txt file and represent its gates into array.

2-	decomposition_ciruit_into_toffoli_gates: decompose array of quantum gates into toffoli gates such that all cnot gates have two controls as maximum number of controls.

3-	decomposition_into_elementry_gates: decompose array of gates of the previous method into NCV quantum gates.

4-	optimization: apply a set of simplification rules to simplify the quantum circuit.

