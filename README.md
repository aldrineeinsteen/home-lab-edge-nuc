# home-lab-edge-nuc

Automated provisioning and hardening of a Windows-based Intel/GMKTec NUC for home labs, edge clients, or kid-friendly PCs using Ansible.

This project provides an opinionated baseline for setting up and managing a Windows NUC as a secure, always-updated, and remotely monitored edge device.
It’s designed to be reusable for:
	•	🏠 Home labs – edge nodes, dev/test boxes, monitoring clients
	•	👨‍👩‍👧 Family PCs – safe & locked-down setup for tweens/teens
	•	🌐 Edge workloads – monitored endpoints exposing metrics for Prometheus/Grafana
⸻

🚀 Features
	•	Automatic Software Install (via Winget/Chocolatey):
	•	Firefox, Thunderbird, VSCode, Python 3, Java JDK, 7-Zip, Blender, LibreOffice (Word/Excel replacement)
	•	User Management
	•	Creates a standard non-admin user for daily use
	•	Prevents local software installs & disables Microsoft Store
	•	Blocks running installers from Downloads/Temp (SRP rules)
	•	Security Hardening
	•	SmartScreen enabled (Explorer + Edge + apps)
	•	Windows Defender real-time protection enforced
	•	Hides Windows Security settings from standard users
	•	System Management
	•	Always-on Windows Update (auto download + scheduled install)
	•	Safe reboot every Sunday at 03:00
	•	Remote Monitoring
	•	Installs Prometheus windows_exporter → exposes CPU, disk, and memory metrics
	•	Opens firewall for metrics scraping (default http://<NUC_IP>:9182/metrics)
	•	Parental Controls Ready
	•	Compatible with Microsoft Family Safety (requires linking child’s Microsoft account post-setup)

⸻

🛠 Requirements
	•	Control machine with Ansible 2.12+ and Python 3
	•	Target NUC running Windows 10/11
	•	Network connectivity to the NUC (WinRM enabled on 5985/5986)
