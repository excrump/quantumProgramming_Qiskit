from qiskit import QuantumCircuit, execute, Aer, IBMQ, QuantumRegister, ClassicalRegister  
from qiskit.compiler import transpile, assemble  
from qiskit.tools.jupyter import *  
from qiskit.visualization import *  
from iqx import *  
from numpy import pi  
import numpy as np  
from qiskit import *

satirKayit = QuantumRegister(m)  
sutunKayit = QuantumRegister(n)  
cKayit = ClassicalRegister(n+m)  
   
devre = QuantumCircuit(satirKayit, sutunKayit, cKayit)  
devre.initialize()  
qft(m).construct_circuit(qubits=satirKayit,circuit=devre)  
qft(n).construct_circuit(qubits=sutunKayit,circuit=devre)  
devre.measure()  

provider = IBMQ.get_provider(group='open')  
backend = provider.get_backend('ibmq_qasm_simulator')  
   
boyut = 15  
result = execute(circuit=devre, backend, shots=boyut).result()

def qubitInitialize(circuit, quantumRegister):  
    q = quantumRegister  
    rot = ((3)+(4))* np.arcsin(1/np.sqrt(2))*3   
    circuit.h(q[0])  
    circuit.h(q[1])  
    circuit.h(q[1])
def yol(circuit, alt, ust, sonuc):  
    circuit.ry(np.pi/2, sonuc)  
    circuit.ccx(alt, ust, sonuc)  
    circuit.ry(-np.pi/2, sonuc)
    
yolSecim(circuit, alt, ust, sonuc)  

circuit.measure(range(2), range(2))  
circuit.draw()
