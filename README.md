# Yijia_Sun_PS1: **System Configuration and Setup Guide**

This document provides **detailed setup instructions** for running the **comorbidity network analysis system** on both **cloud** and **local** environments.

---

## **1. System Requirements**

### **1.1 Hardware Specifications**
| Component     | Minimum Requirements |
|--------------|----------------------|
| **CPU**      | Intel Xeon CPU @ 2.20GHz (x86_64) |
| **Cores**    | 2 Cores (Hyperthreaded) |
| **Memory**   | 12 GB RAM |
| **Storage**  | At least 100 GB disk space |
| **GPU**      | No GPU detected (CPU-based processing) |

### **1.2 Software Specifications**
| Component       | Version |
|----------------|---------|
| **Operating System** | Ubuntu-based (KVM Virtualized) |
| **Python Version**  | 3.11.11 |
| **Key Dependencies** | Listed in `requirements.txt` |

---

## **2. Local Setup**

### **2.1 Install Required Packages**
Ensure you have **Python 3.11+** installed. If not, install it via:

```sh
sudo apt update && sudo apt install python3.11 python3.11-venv python3.11-dev -y
```

Next, create and activate a virtual environment:
