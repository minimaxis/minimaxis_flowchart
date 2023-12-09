# minimaxis_flowchart
🤏🧜‍♀️ Visualize Miniscript using Mermaid

![Build Status](https://img.shields.io/badge/Build-Passing-brightgreen)
![License](https://img.shields.io/badge/License-MIT-green)

## 🌐 Introduction

Flowchart for Miniscripts
This is a small suite of tools aimed to work with Miniscript. 

## 📂 Project File Tree

minimaxis_flowchart
├── minimermaid.py


#### minimaxis_flowchart

- minimermaid.py
    - Application flowchart for MiniScripts.
 
## 🛠 Tech Stack

### Technology
- Python

### External Packages 
- re
- json
- symbols, simplify, And, Or, printing

## Usage

```python
miniscript = 'or(pk(key_revocation),and(pk(key_remote),or(and(pk(key_local),hash160(H)),older(1008))))'
miniscript_to_mermaid(miniscript, True) # True for readability improvement through simplification,
                                        # False for auditability improvement through replication.

### Output: ###
# graph TD
# key_revocation -->|pk| or_0{Check 1/3}
# 1008 -->|older| and_0{Check 2/2}
# key_remote -->|pk| and_0{Check 2/2}
# and_0 --> or_0
# and_0{Check 2/2}
# H -->|hash160| and_1{Check 3/3}
# key_local -->|pk| and_1{Check 3/3}
# key_remote -->|pk| and_1{Check 3/3}
# and_1 --> or_0
# and_1{Check 3/3}
# or_0{Check 1/3}
# or_0 -->|yes|s((spend))
# or_0 -->|no|n((nothing))
```

## Contributing

Pull requests are welcome. For major changes, please open an issue first
to discuss what you would like to change.
