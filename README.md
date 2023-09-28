![image](https://github.com/spendierk/2023_CQE_QUANTX_quantinuum/assets/106914305/1c0a691a-cf9d-4398-9d0b-c1f29e473eb3)

<br>
<br>

# Quantinuum's repository for the 2023 BIG Q Hackathon by CQE and QuantX

![logo image](wordmark-01.png)

For the BIG Q Hackathon by CQE and QuantX Technical Phase, [Quantinuum](https://www.quantinuum.com/) provides the System Model H1-2E emulator, 20 qubits, and the TKET quantum SDK. 

Our System Model H1-2 Emulator is a cloud-based classical CPU simulator that uses identical I/O pathways, compilers, and high-fidelity error modeling that mimics our H1-2 QPU. This allows access to distinctive system model features such as all-to-all connectivity, qubit reuse, and mid-circuit measurement with conditional logic.

TKET is an advanced software development kit for the creation and execution of programs for gate-based quantum computers. It is platform-inclusive and offers state-of-the-art circuit optimization routines. TKET is open source and easily accessible through the `pytket` Python package, with extension modules providing compatibility with many quantum computers, classical simulators, and popular quantum software libraries.


## H1-2 Emulator access

You’ll be able to test your project on the [H1-2 emulator (20-qubits)](https://assets.website-files.com/62b9d45fb3f64842a96c9686/6398c899bb181e5138578789_Quantinuum%20H1%20Emulator%20Product%20Data%20Sheet%20v6%2001DEC22.pdf). Our System Model H1-2 Emulator is a cloud-based classical CPU simulator using identical I/O pathways, compilers, and high-fidelity error modeling. The emulator has the most accurate noise model of the 20-qubit Quantinuum H1-2 trapped ion quantum processor and features all-to-all connectivity and qubit reuse after mid-circuit measurement. Important note is that just as for a real backend your submitted job will be in a queue since the emulator is cloud-based. Hence you need to plan for emulator queue times when submitting your final jobs.

Participants paired up with the Quantinuum provider need to provide kathrin.spendier@quantinuum.com with an email address if different from the emails shared with me by the organizers to set up their emulator account. (NOTE: if you already have access to the H-series with an email address, you can't use the same email address; it must be different.) Once your email address is added to the system, you will receive an invitation email from QCadmin@quantinuum.com, (Likely early Friday morning), which you will need to open and follow the steps outlined. (Note: You will be asked to accept the Quantinuum “Policy & Terms of USE” https://um.qapi.quantinuum.com/static/media/user_terms_and_conditions.46957d35.pdf. 
You must accept the terms and conditions to unlock access to the Quantinuum emulator.) Please ensure you have access to the emulator by Friday early afternoon. If you need help signing up, please find me for help or email kathrin.spendier@quantinuum.com.

#### Note: please check your spam/junk email folder for the invitation email from QCadmin@quantinuum.com


### Supporting video for sign-up process

[Here](https://drive.google.com/file/d/1EEUQUnHMp-wvQJlWN-RTQUHElcsALF6U/view?usp=sharing) is the link to log in to the user portal after setting up your account.


### Exploiting Mid-circuit Measurement and Qubit Reuse using the Quantinuum H1-2 Emulator

The ability to perform measurements between, or simultaneous with, the application of quantum gates is known as mid-circuit measurement. Specifically in this process, you measure a qubit, reset it, and use it again in the middle of a circuit. Mid-circuit measurements important in several quantum information computing protocols. Mid-circuit measurements and resets can be used to:

 - Enable Quantum Error Correction
 - Measurement based quantum computing (MBQC)
 - Enables qubit reuse compilation - reduces the number of qubits required to execute some quantum algorithms.

Several commercially available quantum computers, such as Quantinuuum’s trapped-ion quantum computer, can perform mid-circuit measurements and qubit resets.


## TKET: Quantinuum’s Quantum SDK
To access the Quantinuum H1-2 emulator, you will be using [TKET](https://www.quantinuum.com/developers/tket), more specifically `pytket`, the python wrapper of TKET. To access the emulator, you will use the [pytket-quantinuum extension](https://cqcl.github.io/pytket-quantinuum/api/) in your python environment (i.e., jupyter notebook). Since TKET is language agnostic, you can develop your project using other languages like Qiskit, Criq, or Q# and then convert your circuit written in your favorite language to a pyTKET circuit to submit your job to the H1-2 emulator.


### Useful Links to get you started are:
 - [pyTKET User manual](https://cqcl.github.io/pytket/manual/index.html)
 - [pyTKET API docs](https://cqcl.github.io/tket/pytket/api/)
 - [pyTKET Notebook Examples](https://github.com/CQCL/pytket/tree/main/examples)
 - [pytket-quantinuum extension](https://cqcl.github.io/pytket-quantinuum/api/)

 
### TKET and H1-2 Emulator tutorial
This repository has sample notebooks you can use to get started. 

[Here](https://github.com/spendierk/2023_CQE_QUANTX_quantinuum/blob/main/TKET%20and%20Emulator%20tutorial/TKET%20and%20Emulator%20tutorial.ipynb) you will find a sample notebook that goes over the basics of circuit preparation and submission with `pytket`, outlines how to convert between `pytket` and other quantum SDKs like Qiskit, as well as how to perform the mid-circuit measurement and qubit reuse on the H1-2 emulator. [Here](https://quantinuum.zoom.us/rec/share/s3ihKrmgF2xfAwUdSpVkKMNa0xEOX8m-9piatNN2VEzvx9P9XM6cGHknBynffvGA.Z6rmrE9havkLXFvm?startTime=1695848624000) is a video going over this tutorial and the user portal (Passcode:6&5ibKY).

[Here](https://colab.research.google.com/drive/133TKFNCUKfS6zwL_PXgWJjedr7lxHUZg?usp=sharing) you will find a quick-start Google Colab notebook, guiding you through submitting and running a circuit on the H1-2 Emulator, including package installation, circuit definition, backend setup, job monitoring, and result retrieval.


### TKET help
In case you need help please reach out to Kathrin Spendier (in-person mentor). For online help, during UK business hours, you can join the [public slack channel](https://tketusers.slack.com/join/) for support and discussion.


## Eligibility
Quantinuum employees are not eligible to participate in this hackathon.
For the general rules on eligibility and hackathon participation, please refer to the official rules.
