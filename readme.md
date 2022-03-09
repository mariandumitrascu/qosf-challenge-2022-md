# QOSF Mentorship Program - 2022 Challenge - Marian Dumitrascu

## Task 3 - Encoding and Classifier

You can find task definition [here]('http://./Cohort 5 Screening Tasks.pdf').

## Approach and Solution


<br>
To approach this task I used PennyLane framework, and 7 types of encoding, making use of all out of the box PennyLane embedding functions (with the exception of basis encoding) as well as one angle encoding from scratch. I wanted to use this opportunity to go through all options available at this time regarding Variational Circuits Classifiers, and PennyLane framework provides this.


***
<!-- ### [Angle Encoding - 2 qubits - Custom Circuit](https://github.com/mariandumitrascu/qosf-challenge-2022-md/blob/main/task-02/md-task-02-angle-encoding-2-qubits.ipynb) -->
### Angle Encoding - 2 qubits - Custom Circuit

__Notebook__: [md-task-02-angle-encoding-2-qubits.ipynb](https://github.com/mariandumitrascu/qosf-challenge-2022-md/blob/main/task-02/md-task-02-angle-encoding-2-qubits.ipynb)
__Notebook__: [md-task-02-angle-encoding-2-qubits.ipynb](./task-02/md-task-02-angle-encoding-2-qubits.ipynb)
<br>
<br>
Circuit coding for angle encoding follows [pennylane technique](https://pennylane.ai/qml/demos/tutorial_variational_classifier.html), whch is also following the scheme in in [Schuld and Petruccione (2018)](https://link.springer.com/book/10.1007/978-3-319-96424-9). Controlled Y rotations are also decomposed using [Nielsen and Chuang (2010)](http://www.michaelnielsen.org/qcqi/)

<br>
<br>

References:
<br>
[Pennylane](https://pennylane.ai/qml/demos/tutorial_variational_classifier.html)<br>
[Schuld and Petruccione (2018)](https://link.springer.com/book/10.1007/978-3-319-96424-9)


***
### Angle Encoding - 4 qubits - using qml.AngleEmbedding
__Notebook__: [md-task-02-angle-encoding-4-qubits.ipynb](https://github.com/mariandumitrascu/qosf-challenge-2022-md/blob/main/task-02/md-task-02-angle-encoding-4-qubits.ipynb)
<br>
<br>
<br>
References:
<br>
[qml.AngleEmbedding](https://pennylane.readthedocs.io/en/stable/code/api/pennylane.AngleEmbedding.html)


***
### Amplitude Encoding - 2 qubits - using qml.AmplitudeEmbedding

__Notebook__: [md-task-02-amplitude-encoding-2-qubits.ipynb](https://github.com/mariandumitrascu/qosf-challenge-2022-md/blob/main/task-02/md-task-02-amplitude-encoding-2-qubits.ipynb)
<br>
<br>
<br>
References:
<br>
[qml.AmplitudeEmbedding](https://pennylane.readthedocs.io/en/stable/code/api/pennylane.AmplitudeEmbedding.html)

***
<!-- ### [IQP Encoding - 4 qubits - using qml.IQPEmbedding](https://github.com/mariandumitrascu/qosf-challenge-2022-md/blob/main/task-02/md-task-02-iqp-encoding-4-qubits.ipynb) -->
### IQP Encoding - 4 qubits - using qml.IQPEmbedding

__Notebook__: [md-task-02-iqp-encoding-4-qubits.ipynb](https://github.com/mariandumitrascu/qosf-challenge-2022-md/blob/main/task-02/md-task-02-iqp-encoding-4-qubits.ipynb)
<br>
<br>
Encodes n features into n qubits using diagonal gates of an IQP circuit.
<br>
This embedding has been proposed by [Havlicek et al. (2018)](https://arxiv.org/pdf/1804.11326.pdf).
<br><br>
References:
<br>
[qml.IQPEmbedding](https://pennylane.readthedocs.io/en/stable/code/api/pennylane.IQPEmbedding.html)


***
<!-- ### [Amplitude Displacement Encoding - 4 qubits - using qml.DisplacementEmbedding](https://github.com/mariandumitrascu/qosf-challenge-2022-md/blob/main/task-02/md-task-02-disp-amplitude-encoding-4-qubits.ipynb) -->
### Amplitude Displacement Encoding - 4 qubits - using qml.DisplacementEmbedding
__Notebook__: [md-task-02-disp-amplitude-encoding-4-qubits.ipynb](https://github.com/mariandumitrascu/qosf-challenge-2022-md/blob/main/task-02/md-task-02-disp-amplitude-encoding-4-qubits.ipynb)
<br>
<br>
This is working only on gaussian devices similar with Strawberry Fields photonic devices. Amplitude Displacement Encoding and Phase Displacement Encoding differ in only one line of code, but the results are very different. Amplitude Displacement perform much better for our data set achieving 95% accuracy very fast comparing with Phase Displacement. 
<br>
<br>
<br>
References:
<br>
[qml.DisplacementEmbedding](https://pennylane.readthedocs.io/en/stable/code/api/pennylane.DisplacementEmbedding.html)


***
<!-- ### [Phase Displacement Encoding - 4 qubits - using qml.DisplacementEmbedding](https://github.com/mariandumitrascu/qosf-challenge-2022-md/blob/main/task-02/md-task-02-disp-phase-encoding-4-qubits.ipynb) -->
### Phase Displacement Encoding - 4 qubits - using qml.DisplacementEmbedding

__Notebook__: [md-task-02-disp-phase-encoding-4-qubits.ipynb](https://github.com/mariandumitrascu/qosf-challenge-2022-md/blob/main/task-02/md-task-02-disp-phase-encoding-4-qubits.ipynb)
<br>
<br>
<br>
References:
<br>
[qml.DisplacementEmbedding](https://pennylane.readthedocs.io/en/stable/code/api/pennylane.DisplacementEmbedding.html)


***
<!-- ### [QAOA Encoding - 4 qubits - using qml.QAOAEmbedding](https://github.com/mariandumitrascu/qosf-challenge-2022-md/blob/main/task-02/md-task-02-qaoa-encoding-4-qubits.ipynb) -->
### QAOA Encoding - 4 qubits - using qml.QAOAEmbedding

__Notebook__: [md-task-02-qaoa-encoding-4-qubits.ipynb](https://github.com/mariandumitrascu/qosf-challenge-2022-md/blob/main/task-02/md-task-02-qaoa-encoding-4-qubits.ipynb)
<br>
<br>
This is using Hamiltonian embedding and is inspired by QAOA algorithms. **qml.QAOAEmbedding** function performs both learning and encodding.
<br>
<br>
References:
<br>
[qml.QAOAEmbedding](https://pennylane.readthedocs.io/en/stable/code/api/pennylane.QAOAEmbedding.html)



```python

```
