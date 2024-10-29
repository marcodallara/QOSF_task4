# Solution to Task 4: State Preparation Circuit for 5 Qubits

### Universal State Preparation Circuit
I start with the universal state preparation circuit based on the work from [arXiv:1003.5760](https://arxiv.org/abs/1003.5760) based on a Schmidt decomposition structure. 

However, this apprach require two CNOT gates between non-connected qubits. To address this problem, I decompose these two CNOT gates into other CNOT that are hardware realizable using an equality in [arXiv:2009.13247](https://arxiv.org/pdf/2009.13247).

This method results in a circuit depth of 127 with 47 CNOT gates.

### Circuit Simplification
Since we focus on a specific target state, I simplify the circuit structure to achieve better circuit depth and reduce the number of CNOT gates and parameters. This is achieved by systematically removing gates while preserving the overall structure, ensuring that the fidelity of the state preparation remains at one.

### Transpilation with Qiskit
I further simplify the circuit by applying Qiskit transpilation, which employs simple rules for circuit simplification, as outlined in the [PennyLane tutorial](https://pennylane.ai/qml/demos/tutorial_circuit_compilation/).

## Results
The final circuit achieve the target state with:
- **Fidelity**: 1
- **Circuit Depth**: 38
- **Number of CNOT Gates**: 16


## References
1. [arXiv:1003.5760](https://arxiv.org/abs/1003.5760)
2. [arXiv:2009.13247](https://arxiv.org/pdf/2009.13247)
3. [PennyLane Tutorial](https://pennylane.ai/qml/demos/tutorial_circuit_compilation/)
