
# Practical 1: Docker Installation & Kubernetes Enablement (Windows)

## Objective

To install Docker Desktop on Windows and enable Kubernetes cluster for local development and DevOps practice.

---

## Prerequisites

* Windows 10/11 (64-bit)
* Virtualization enabled in BIOS (Intel VT-x / AMD-V)
* At least 4GB RAM (recommended 8GB+)

---

## Part A: Docker Installation Steps

### 1. Download Docker Desktop

* Go to official website: [https://www.docker.com/products/docker-desktop/](https://www.docker.com/products/docker-desktop/)
* Click **Download for Windows (WSL2/Hyper-V)**

---

### 2. Install Docker Desktop

* Run the downloaded installer (.exe)
* Enable the following options during installation:

  * Use WSL 2 instead of Hyper-V (recommended)
  * Add shortcut to desktop
* Click **OK / Install**

---

### 3. Restart System

* Restart your computer after installation

---

### 4. Verify Docker Installation

Open Command Prompt / PowerShell:

```bash
docker --version
```

Expected Output:

* Docker version xx.x.x

Check Docker is running:

```bash
docker run hello-world
```

---

## Part B: Enable Kubernetes in Docker Desktop

### 1. Open Docker Desktop

* Launch Docker Desktop application

---

### 2. Go to Settings

* Click ⚙️ Settings icon
* Navigate to **Kubernetes** tab

---

### 3. Enable Kubernetes

* Check the option:

  * ✔ Enable Kubernetes

<img width="943" height="238" alt="image" src="https://github.com/user-attachments/assets/f39d9332-5f1d-4985-ac29-58feebf96216" />

---
Cluster settings
Choose cluster provisioning method

<img width="702" height="428" alt="image" src="https://github.com/user-attachments/assets/77eb2ba1-cc5e-40f4-ac43-5485dbca47a9" />



* Click **Apply & Restart**
---

### 4. Wait for Setup

* Kubernetes components will be downloaded and configured
* This may take 5–15 minutes

---

### 5. Verify Kubernetes Installation

Open terminal:

```bash
kubectl version
```
<img width="1312" height="129" alt="image" src="https://github.com/user-attachments/assets/59c95a4a-7e76-4778-8910-18eaa07bb720" />

Check cluster nodes:

```bash
kubectl get nodes
```

Expected Output:

* One node named `docker-desktop` in Ready state

---

## Observations

* Docker installed successfully
* Kubernetes enabled inside Docker Desktop
* kubectl can communicate with local cluster

---

## Example Output

### Docker Version

```bash
docker --version
Docker 29.1.3
```
<img width="686" height="684" alt="image" src="https://github.com/user-attachments/assets/2a0dd534-358c-4ac1-b2dc-81a2122438ad" />


### Hello World Test

```bash
docker run hello-world
Hello from Docker!
```

### Kubernetes Nodes

```bash
kubectl get nodes
NAME             STATUS   ROLES
docker-desktop   Ready    control-plane
```

## Result

Successfully installed Docker Desktop and enabled Kubernetes cluster for local development environment.

---

## Conclusion

This practical demonstrates setting up a local DevOps environment using Docker Desktop and Kubernetes, which is essential for containerized application deployment and testing.
