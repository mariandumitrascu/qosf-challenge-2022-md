# QOSF Mentorship Program - 2022 Challenge

## Task 3 - Encoding and Classifier

### Problem Definition

<br>
Encoding the following files in a quantum circuit mock_train_set.csv and mock_test_set.csv in at least two different ways (these could be basis, angle, amplitude, kernel or random encoding
<br>
<br>
* Design a variational quantum circuit for each of the encodings, uses the column 4 as the target, this is a binary class 0 and 1.<br>
* You must use the data from column0 to column3 for your proposed classifier.<br>
* Consider the ansatz you are going to design as a layer and find out how many layers are necessary to reach the best performance. <br>

### Analyze and discuss the results

Feel free to use existing frameworks (e.g. PennyLane, Qiskit) for creating and training the circuits.<br><br>
This PennyLane demo can be useful: Training a quantum circuit with Pytorch,<br>
This Quantum Tensorflow tutorial can be useful: Training a quantum circuit with Tensorflow.<br>
For the variational circuit, you can try any circuit you want. You can start from one with a layer of RX, RZ and CNOTs.<br>

## Approach for Task 3 - Encoding and CLassifier 


<br>
To approach this task I used PennyLane framework, and 6 types of encoding, making use of all out of the box PennyLane embedding functions as well as one angle encoding from scratch. 


