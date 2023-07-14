# Quantum Adder

This repository contains examples of quantum adder circuits implemented using Qiskit. The adder circuits included are the Full Adder, 4-bit Adder, and Carry Look Ahead Adder.

## Problem Statement

Alice wishes to perform the addition of two 4-bit numbers using Quantum Circuits.
Let those two numbers be a and b.
In classical digital electronics, this is achieved using the full-adder circuit, which inputs the bits a_i,b_i and carry bit C_(i-1) and returns the sum bit S_i and carry bit C_i. Hence, the result of the computation would be as follows:
Your task is to help Alice design a fully functional Quantum Adder using just CNOT and Toffoli Gates.

## Adder Circuits

### Full Adder

The Full Adder circuit adds two bits and a carry input to produce a sum and a carry output. It consists of the following gates:

- CNOT (Controlled-NOT) gate: Also known as the CX gate, it performs a NOT operation on the target qubit if the control qubit is in the state |1|. In the Full Adder circuit, CNOT gates are used to propagate the carry and calculate the sum.
- Toffoli (CCX) gate: The Toffoli gate is a controlled-controlled-X gate that performs a NOT operation on the target qubit if both control qubits are in the state |1|. In the Full Adder circuit, a Toffoli gate is used to calculate the carry output.

### 4-bit Adder

The 4-bit Adder circuit combines four full adders to perform addition on four-bit numbers. It takes two four-bit inputs and a carry input, and produces a four-bit sum output and a carry output. The gates used in the 4-bit Adder circuit are the same as those used in the Full Adder circuit.

### Carry Look Ahead Adder

The Carry Look Ahead Adder circuit is an optimized adder circuit that calculates the carry bits in parallel before performing the addition. It consists of the following gates:

- CNOT (Controlled-NOT) gate: The CNOT gate is used to propagate the carry and calculate the sum, similar to the Full Adder circuit.
- Toffoli (CCX) gate: The Toffoli gate is used to calculate the carry output, similar to the Full Adder circuit.
- C3X gate: The C3X gate is a custom gate that performs a controlled-controlled-controlled-X operation. It performs a NOT operation on the target qubit if all three control qubits are in the state |1|. In the Carry Look Ahead Adder circuit, the C3X gate is used to optimize the calculation of carry bits.
