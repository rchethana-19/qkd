## Quantum Key Distribution (QKD) Simulation — BB84 Protocol

This project simulates the **BB84 quantum key distribution protocol** in Python. It models how Alice and Bob generate and share a secure key using quantum bits (qubits) — and how the presence of an eavesdropper (Eve) introduces errors in the key.

## What is BB84?

The BB84 protocol is the first quantum cryptography protocol. It uses:

* **Random bits** and
* **Random measurement bases (`+` or `x`)**

to generate a secret key over a quantum channel. If an eavesdropper (Eve) tries to intercept the communication, her actions introduce detectable errors.

## 📁 Project Structure

This script includes:

* **Bit & basis generation** for Alice
* **Qubit encoding**
* **Optional Eve interception**
* **Bob’s measurement of qubits**
* **Key extraction based on matched bases**
* **QBER (Quantum Bit Error Rate) calculation**
* **QBER Visualization with matplotlib**

---

## How to Run

1. **Install Dependencies**

   ```bash
   pip install matplotlib
   ```

2. **Run the script**

   ```bash
   python qkd_bb84_simulation.py
   ```

---

##  Features

* **Simulate Eve** by toggling the `simulate_eve` flag.
* **Visual output** of:

  * Alice's bits
  * Measurement bases
  * Basis match indicator
* **QBER Plot** to visually assess eavesdropping effect.

---

## Parameters

| Parameter      | Description                                |
| -------------- | ------------------------------------------ |
| `NUM_BITS`     | Number of bits/qubits to simulate          |
| `simulate_eve` | Set to `True` to simulate Eve interception |

---

## Sample Output

```
Alice Bits:   [1, 0, 1, 0, 1, ...]
Alice Bases:  ['+', 'x', 'x', '+', ...]
Bob Bases:    ['x', 'x', '+', '+', ...]
Basis Match:  ['❌', '✅', '❌', '✅', ...]

Raw Key (Alice): [0, 1, 1, ...]
Raw Key (Bob):   [1, 1, 0, ...]

Quantum Bit Error Rate (QBER): 28.57%
```

A bar chart of QBER is also plotted using `matplotlib`.

---





