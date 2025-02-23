# Yijia_Sun_PS2: **System Configuration and Setup Guide**

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
```sh
python3.11 -m venv env
source env/bin/activate
```

Install dependencies from requirements.txt:
```sh
python --version
pip list
```

### **2.2 Verify Python and Package Installation**
Check if Python and required libraries are correctly installed:
```sh
python --version
pip list
```
Expected output:
```sh
Python 3.11.11
```

### **2.3 Configure Data Storage**
Ensure at least **100GB of free space** for data processing:
```sh
df -h
```
If needed, extend disk space before running large-scale computations.

### **2.4 Running the System**
Execute the comorbidity network analysis with:
```sh
python main.py --input data/prevalence_data.csv --output results/
```
Results will be stored in the results/ folder.

## **3. Cloud Deployment (AWS, GCP, or Azure)**

This section provides a step-by-step guide for deploying the comorbidity network analysis system on cloud platforms like **AWS EC2, Google Cloud Compute Engine (GCP), and Microsoft Azure Virtual Machines**.

---

### **3.1 Setting Up a Cloud Instance**

Select a **compute-optimized virtual machine (VM)** for optimal performance:

- **AWS EC2**: `c5.large` (2 vCPUs, 12 GB RAM)
- **Google Cloud Compute Engine**: `n2-standard-2`
- **Azure Virtual Machine**: `Standard_D2s_v3`

Create and launch the instance using the **Ubuntu LTS** image.

---

### **3.2 Install Required Dependencies**

After connecting to the instance via SSH, update system packages:

```sh
sudo apt update && sudo apt upgrade -y
```

Install Python and required system dependencies:
```sh
sudo apt install python3.11 python3.11-venv python3.11-dev -y
```

Clone the GitHub repository and navigate to the project directory:
```sh
git clone https://github.com/YOUR_REPO_NAME.git
cd YOUR_REPO_NAME
```

Create a virtual environment and install dependencies:
```sh
python3.11 -m venv env
source env/bin/activate
pip install -r requirements.txt
```

Verify Python and package installations:
```sh
python --version
pip list
```

### **3.3 Managing Large Datasets**
Since cloud instances may have limited storage, consider using cloud storage solutions:

#### **AWS S3**
```sh
aws s3 cp s3://your-bucket/prevalence_data.csv data/
```

#### **Google Cloud Storage (GCP)**
```sh
gsutil cp gs://your-bucket/prevalence_data.csv data/
```

### **3.4 Running the Analysis in Cloud**
Run the main script with cloud-based data:
```sh
python main.py --input data/prevalence_data.csv --output results/
```

Monitor processing logs:
```sh
tail -f logs/output.log
```

After execution, download results locally:
```sh
scp -r user@your-cloud-instance-ip:/path/to/results ./local_results/
```
