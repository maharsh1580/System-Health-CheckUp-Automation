# 🖥️ System Health CheckUp Automation

A lightweight Python automation script for monitoring basic system health metrics such as **disk space** and **CPU usage**.

This project is a simple introduction to **system monitoring, automation, and Python's system-level libraries**.

## 🚀 Features

* 💾 Checks available disk space
* 🧠 Monitors current CPU usage
* ⚠️ Detects potentially unhealthy system conditions
* ⚡ Lightweight and easy to run
* 🐍 Built entirely with Python

## 🛠️ Technologies Used

* **Python**
* **psutil**
* **shutil**

`shutil` is used to retrieve disk usage information, while `psutil` is used to monitor CPU utilization.

## 📂 Project Structure

```text
System-Health-CheckUp-Automation/
│
├── system_checkup.py
└── README.md
```

## ⚙️ How It Works

The script performs two basic system health checks.

### Disk Usage Check

The program retrieves disk usage information using:

```python
shutil.disk_usage(disk)
```

It calculates the percentage of free disk space and considers the disk healthy when:

```text
Free Disk Space > 20%
```

### CPU Usage Check

CPU utilization is measured using:

```python
psutil.cpu_percentage(1)
```

The system is considered healthy when:

```text
CPU Usage < 75%
```

These thresholds can easily be modified inside the Python script.

## 📦 Installation

Clone the repository:

```bash
git clone https://github.com/maharsh1580/System-Health-CheckUp-Automation.git
```

Move into the project directory:

```bash
cd System-Health-CheckUp-Automation
```

Install the required dependency:

```bash
pip install psutil
```

## ▶️ Usage

Run the Python script:

```bash
python system_checkup.py
```

The health-check functions can also be imported into another Python automation or monitoring project.

Example:

```python
from system_checkup import check_cpu_usage, check_disk_usage

if check_cpu_usage():
    print("CPU usage is healthy.")
else:
    print("CPU usage is high.")

if check_disk_usage("C:\\"):
    print("Disk space is healthy.")
else:
    print("Disk space is running low.")
```

> On Linux or macOS, `/` can be used instead of `C:\` for the disk path.

## 🧩 Current Health Checks

| Check         | Healthy Condition   |
| ------------- | ------------------- |
| 💾 Disk Space | More than 20% free  |
| 🧠 CPU Usage  | Less than 75% usage |

## 🔮 Possible Future Improvements

The project could be expanded with:

* RAM usage monitoring
* CPU temperature monitoring
* Network usage monitoring
* Battery health monitoring
* Disk read/write monitoring
* Running process monitoring
* Automatic warning notifications
* Logging system health data
* Periodic background health checks
* System health dashboard

## 🎯 Purpose

This project was created as a simple experiment in **Python automation and system monitoring**.

It demonstrates how Python can interact with operating-system statistics and make automated decisions based on system resource usage.

## 👨‍💻 Author

**Maharsh Badheka**

GitHub: `@maharsh1580`

---

⭐ If you found this project useful, consider starring the repository!
