# 🔍 TRACE FORGE
### Digital Forensics & Incident Response Toolkit

---

## 📘 Overview
TRACE FORGE is a modular **Digital Forensics and Incident Response (DFIR)** toolkit designed to simplify the process of analyzing multiple types of forensic evidence including memory dumps, disk images, log files, and network captures in all under one unified interface.

This project was built as part of my cybersecurity research to demonstrate an end-to-end incident response framework capable of rapid artifact collection, analysis, and case reporting.

---

## 🎯 Project Goals
- Develop modular forensic components for memory, disk, log, and network analysis.  
- Implement automated metadata generation (hashes, timestamps) for evidence integrity.  
- Build a unified CLI that auto-discovers available modules.  
- Ensure extensibility for plugin-based future modules.  
- Maintain accuracy, transparency, and usability for investigators.

---

## ❓ Why TRACE FORGE?
During real-world incident response, analysts often rely on multiple separate tools to gather and analyze evidence.  
TRACE FORGE aims to bring these capabilities together into **one streamlined and extensible toolkit**, built in Python, where every analysis result is automatically hashed, logged, and stored for proper chain-of-custody tracking.

---

## 🧱 Current Project Phases

### **Phase 1 – Planning and Design**
In this phase, I defined:
- The scope and objectives of the toolkit.  
- The core architecture for a modular DFIR tool.  
- The initial folder structure and technology stack (Python 3, Volatility3, pytsk3, Scapy, SQLite).  
- A high-level workflow diagram describing data flow between modules.

---

### **Phase 2 – Framework Skeleton and Architecture**
In this phase, I structured the entire toolkit by setting up its module placeholders, creating the base folder layout, and developing the initial CLI menu system.

The focus of Phase 2 was on environment setup, CLI integration, and ensuring all dependencies were installed correctly before module implementation.


**Key Achievements:**
- Created the full directory hierarchy under `/traceforge/`.  
- Added base Python module skeletons (`memory.py`, `disk.py`, `logs.py`, `network.py`, `report.py`).  
- Developed the initial interactive CLI (`cli.py`).  
- Locked dependencies using `requirements.txt`.  
- Documented environment setup and testing in `/docs/Phase2_Architecture.md`.

---


## 🗂️ Project Structure (planned)

```
traceforge/
├─ cli.py
├─ modules/
│ ├─ memory.py
│ ├─ disk.py
│ ├─ logs.py
│ ├─ network.py
│ └─ report.py
├─ reports/
├─ data/
├─ samples/
└─ docs/
├─ Phase1_Planning.md
├─ Phase2_Architecture.md
├─ Phase3_BuildUp.md
└─ diagrams/
├─ phase1_diagram.png
├─ phase2_architecture.png
└─ phase3_workflow.png
```

---


---

## 📊 Phase 1 Deliverables
- Project concept and objectives  
- Tool architecture overview  
- Initial planning diagram  
- Repository setup and documentation structure  

---

## 📊 Phase 2 Deliverables
- Environment setup and package installation  
- CLI banner and menu integration  
- Module skeleton structure  
- Architecture documentation  
- Workflow diagram  

---
### **Phase 3 – Build-Up (Implementation and Testing)**
In this phase, I implemented all the core functional modules and verified their performance under the unified CLI environment.  
Each module was tested with sample data to ensure reliable evidence processing, metadata generation, and output consistency.

The primary focus was completing the functional build and confirming each component produced correct, hashed, and timestamped results.

**Key Achievements:**
- Implemented all five forensic modules (`memory.py`, `disk.py`, `logs.py`, `network.py`, `report.py`)  
- Integrated each module with the unified CLI (`cli.py`)  
- Added SHA-256 evidence hashing and timestamp metadata for integrity verification  
- Verified outputs across all modules using structured test cases  
- Produced successful case reports and consistent logs  
- Established a stable operational foundation for future optimization

**Test Case Summary**

| Module | Input | Expected Output | Result |
|:--|:--|:--|:--|
| Memory | Invalid image path | `[!] Memory image not found` | ✅ Passed |
| Disk | Valid image | Timeline CSV generated | ✅ Passed |
| Logs | Authentication log | Extracted failed logins | ✅ Passed |
| Network | PCAP file | DNS/HTTP summary created | ✅ Passed |
| Report | Combined evidence | JSON report & DB entry | ✅ Passed |

**Outcome:**  
Phase 3 marks the transformation of TRACE FORGE from a design prototype into a fully functional DFIR toolkit capable of producing verified forensic outputs through a unified, reliable interface.

---

## 📊 Phase 3 Deliverables
- Completed functional implementation of all core modules  
- Added metadata hashing and reporting capability  
- Conducted structured test validation for each module  
- Created unified CLI integration and documentation  

---

## 🧩 Next Steps
- Phase 4 – Optimization, plugin integration, and logging automation  
- Phase 5 – Performance evaluation and research publication  

---


## 📜 License
MIT License — free to use, modify, and distribute with attribution.

---

## 👤 Author
**PIYUSH KUMAR SAHOO**  
Cybersecurity Researcher & Student
