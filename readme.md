# QOSF Mentorship Program - 2022 Challenge - Marian Dumitrascu

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

## Approach for Task 3 - Encoding and Classifier 


<br>
To approach this task I used PennyLane framework, and 7 types of encoding, making use of all out of the box PennyLane embedding functions (with the exception of basis encoding) as well as one angle encoding from scratch. I wanted to use this opportunity to go through all options available at this time regarding Variational Circuits Classifiers, and PennyLane framework provides this.


***
### [Angle Encoding - 2 qubits - Custom Circuit](https://github.com/mariandumitrascu/qosf-challenge-2022-md/blob/main/task-02/md-task-02-angle-encoding-2-qubits.ipynb)

__Notebook__: [md-task-02-angle-encoding-2-qubits.ipynb](https://github.com/mariandumitrascu/qosf-challenge-2022-md/blob/main/task-02/md-task-02-angle-encoding-2-qubits.ipynb)
<br>
<br>
Circuit coding for angle encoding follows [pennylane technique](https://pennylane.ai/qml/demos/tutorial_variational_classifier.html), whch is also following the scheme in in [Schuld and Petruccione (2018)](https://link.springer.com/book/10.1007/978-3-319-96424-9). Controlled Y rotations are also decomposed using [Nielsen and Chuang (2010)](http://www.michaelnielsen.org/qcqi/)



***
### [Angle Encoding - 4 qubits - using qml.AngleEmbedding](https://github.com/mariandumitrascu/qosf-challenge-2022-md/blob/main/task-02/md-task-02-angle-encoding-4-qubits.ipynb)

__Notebook__: [md-task-02-angle-encoding-4-qubits.ipynb](https://github.com/mariandumitrascu/qosf-challenge-2022-md/blob/main/task-02/md-task-02-angle-encoding-4-qubits.ipynb)
<br>
<br>
<br>
[qml.AngleEmbedding](https://pennylane.readthedocs.io/en/stable/code/api/pennylane.AngleEmbedding.html)


***
### [Amplitude Encoding - 2 qubits - using qml.AmplitudeEmbedding](https://github.com/mariandumitrascu/qosf-challenge-2022-md/blob/main/task-02/md-task-02-amplitude-encoding-2-qubits.ipynb)

__Notebook__: [md-task-02-amplitude-encoding-2-qubits.ipynb](https://github.com/mariandumitrascu/qosf-challenge-2022-md/blob/main/task-02/md-task-02-amplitude-encoding-2-qubits.ipynb)
<br>
<br>
<br>
[qml.AmplitudeEmbedding](https://pennylane.readthedocs.io/en/stable/code/api/pennylane.AmplitudeEmbedding.html)

***
### [IQP Encoding - 4 qubits - using qml.IQPEmbedding](https://github.com/mariandumitrascu/qosf-challenge-2022-md/blob/main/task-02/md-task-02-iqp-encoding-4-qubits.ipynb)

__Notebook__: [md-task-02-iqp-encoding-4-qubits.ipynb](https://github.com/mariandumitrascu/qosf-challenge-2022-md/blob/main/task-02/md-task-02-iqp-encoding-4-qubits.ipynb)
<br>
<br>
Encodes n features into n qubits using diagonal gates of an IQP circuit.
<br>
This embedding has been proposed by [Havlicek et al. (2018)](https://arxiv.org/pdf/1804.11326.pdf).
<br><br>
[qml.IQPEmbedding](https://pennylane.readthedocs.io/en/stable/code/api/pennylane.IQPEmbedding.html)


***
### [Amplitude Displacement Encoding - 4 qubits - using qml.DisplacementEmbedding](https://github.com/mariandumitrascu/qosf-challenge-2022-md/blob/main/task-02/md-task-02-disp-amplitude-encoding-4-qubits.ipynb)

__Notebook__: [md-task-02-disp-amplitude-encoding-4-qubits.ipynb](https://github.com/mariandumitrascu/qosf-challenge-2022-md/blob/main/task-02/md-task-02-disp-amplitude-encoding-4-qubits.ipynb)
<br>
<br>
<br>
[qml.DisplacementEmbedding](https://pennylane.readthedocs.io/en/stable/code/api/pennylane.DisplacementEmbedding.html)


***
### [Phase Displacement Encoding - 4 qubits - using qml.DisplacementEmbedding](https://github.com/mariandumitrascu/qosf-challenge-2022-md/blob/main/task-02/md-task-02-disp-phase-encoding-4-qubits.ipynb)

__Notebook__: [md-task-02-disp-phase-encoding-4-qubits.ipynb](https://github.com/mariandumitrascu/qosf-challenge-2022-md/blob/main/task-02/md-task-02-disp-phase-encoding-4-qubits.ipynb)
<br>
<br>
<br>
[qml.DisplacementEmbedding](https://pennylane.readthedocs.io/en/stable/code/api/pennylane.DisplacementEmbedding.html)


***
### [QAOA Encoding - 4 qubits - using qml.QAOAEmbedding](https://github.com/mariandumitrascu/qosf-challenge-2022-md/blob/main/task-02/md-task-02-qaoa-encoding-4-qubits.ipynb)

__Notebook__: [md-task-02-qaoa-encoding-4-qubits.ipynb](https://github.com/mariandumitrascu/qosf-challenge-2022-md/blob/main/task-02/md-task-02-qaoa-encoding-4-qubits.ipynb)
<br>
<br>
<br>
[qml.QAOAEmbedding](https://pennylane.readthedocs.io/en/stable/code/api/pennylane.QAOAEmbedding.html)



