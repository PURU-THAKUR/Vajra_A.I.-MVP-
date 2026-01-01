🛡️ Vajra AI - Intelligent Security Monitoring System
https://img.shields.io/badge/Vajra-AI-blue
https://img.shields.io/badge/Python-3.8%252B-green
https://img.shields.io/badge/License-MIT-yellow
https://img.shields.io/badge/Status-Active-brightgreen

📋 Table of Contents
Introduction

Features

System Requirements

Quick Installation

Step-by-Step Guide

How to Run

Understanding Dashboard

Detection Guide

Troubleshooting

FAQ

Support

🎯 Introduction
Vajra AI is an advanced AI-powered security monitoring system that provides real-time threat detection by analyzing system behavior. Unlike traditional antivirus software that relies on known signatures, Vajra AI uses machine learning to detect anomalies in system behavior, making it effective against zero-day attacks and unknown threats.

✨ Key Features
🔍 Real-time Monitoring
CPU Usage Tracking: Monitor processor utilization in real-time

Memory Analysis: Track RAM usage and detect memory leaks

Process Surveillance: Monitor running processes for suspicious activity

Network Monitoring: Track data transmission and reception

Disk Activity: Monitor read/write operations

🤖 AI-Powered Detection
Behavioral Analysis: Learns normal system patterns and flags deviations

Anomaly Detection: Uses Isolation Forest algorithm to detect outliers

Risk Scoring: Assigns threat levels based on severity

Automated Alerts: Real-time notifications for suspicious activities

📊 Interactive Dashboard
Live Metrics: Real-time system performance indicators

Threat Timeline: Visual timeline of detected threats

Module Status: Health check of all system components

Historical Data: Track system behavior over time

⚡ Advanced Capabilities
Multi-module Architecture: Modular design for easy expansion

Rule-based Fallback: Works even when AI model is unavailable

Auto-refresh: Automatic data updates every 5 seconds

Responsive Design: Works on all screen sizes

💻 System Requirements
Minimum Requirements
Operating System: Windows 10/11, macOS 10.14+, Ubuntu 18.04+

Python: Version 3.8 or higher

RAM: Minimum 4GB (8GB recommended)

Storage: 2GB free space

CPU: Dual-core processor or better

Recommended Requirements
OS: Windows 11 / macOS Monterey / Ubuntu 20.04+

Python: Version 3.10+

RAM: 8GB or more

Storage: 5GB free SSD space

CPU: Quad-core processor

⚡ Quick Installation
Option 1: One-Line Install (For Experienced Users)
bash
# Clone and run in one command
git clone https://github.com/PURU-THAKUR/Vajra_A.I.-MVP-.git && cd vajra-ai && pip install -r requirements.txt && streamlit run main_app.py
Option 2: Step-by-Step (Recommended for Beginners)
Follow the detailed guide below.

📥 Step-by-Step Installation Guide
Step 1: Download the Project
Method A: Download ZIP (Easiest)

Click the "Code" button on GitHub

Select "Download ZIP"

Extract the ZIP file to your desired location

Windows: Right-click → "Extract All"

Mac: Double-click the ZIP file

Linux: unzip vajra-ai.zip

Method B: Git Clone

bash
git clone https://github.com/PURU-THAKUR/Vajra_A.I.-MVP-.git
cd vajra-ai
Step 2: Install Python
Check if Python is installed:

bash
python --version
# Should show Python 3.8 or higher
If Python is not installed:

Windows: Download from python.org

Mac: brew install python or download installer

Linux: sudo apt install python3 python3-pip

Verify installation:

bash
python --version
pip --version
Step 3: Install Dependencies
Navigate to the extracted folder and run:

bash
# Method 1: Using requirements.txt
pip install -r requirements.txt

# Method 2: Manual installation (if Method 1 fails)
pip install streamlit==1.28.0
pip install psutil==5.9.0
pip install joblib==1.3.0
pip install numpy==1.24.0
pip install pandas==2.0.0
pip install scikit-learn==1.3.0
Step 4: Verify Installation
Create a test script to verify all dependencies:

python
# test_installation.py
import streamlit as st
import psutil
import joblib
import numpy as np
import pandas as pd
from sklearn.ensemble import IsolationForest

print("✅ All dependencies installed successfully!")
print(f"Streamlit: {st.__version__}")
print(f"Psutil: {psutil.__version__}")
Run the test:

bash
python test_installation.py
🚀 How to Run the Application
Method 1: Standard Launch
bash
# Navigate to the project folder
cd vajra-ai

# Run the main application
streamlit run main_app.py
Method 2: Custom Port
bash
# Use a different port if 8501 is busy
streamlit run main_app.py --server.port 8502
Method 3: Run in Background
bash
# For Linux/Mac
nohup streamlit run main_app.py --server.port 8501 &

# For Windows (using Command Prompt)
start /B streamlit run main_app.py
What Happens After Running:
Terminal will show: You can now view your Streamlit app in your browser.

Browser will automatically open at http://localhost:8501

If browser doesn't open automatically, manually go to the URL

📊 Understanding the Dashboard
1. Sidebar Navigation
text
🛡️ Vajra AI
────────────
Navigate to:
○ Dashboard
○ AI Monitor
○ Live Threats
○ Modules
○ Settings
────────────
Live Metrics
CPU: 45% 🟢
Memory: 67% 🟡
────────────
AI Status
✅ Model Loaded
2. Dashboard Tab (Main Interface)
text
📊 Real-time Metrics
┌─────────────┬─────────────┬─────────────┬─────────────┐
│ CPU Usage   │ Memory      │ Processes   │ Threats     │
│ 45.2% 🟢    │ 67.8% 🟡    │ 142         │ 0 ✅        │
└─────────────┴─────────────┴─────────────┴─────────────┘

📈 Performance Charts
├── CPU & Memory Trend (Line Chart)
└── Active Threats List

🚨 Threat Detection
├── Current Status: ✅ All Clear
└── Last Scan: 2 minutes ago
3. AI Monitor Tab
Prediction Status: Normal/Anomaly

Confidence Level: 85%

Feature Analysis: Individual metric breakdown

Risk Score: 0-100 scale

4. Live Threats Tab
text
┌──────────┬─────────────────────┬────────┬─────────────┐
│ Time     │ Type                │ Level  │ Action      │
├──────────┼─────────────────────┼────────┼─────────────┤
│ 14:30:15 │ High CPU Usage      │ HIGH   │ Investigate │
│ 14:25:10 │ Memory Spike        │ MEDIUM │ Monitor     │
│ 14:20:05 │ Unknown Process     │ LOW    │ Review      │
└──────────┴─────────────────────┴────────┴─────────────┘
5. Color Coding System
🟢 Green: Normal (0-60%)

🟡 Yellow: Warning (60-80%)

🔴 Red: Critical (80-100%)

🔍 How It Detects Attacks
Detection Methodology
1. Behavioral Baseline
Learns your system's normal patterns

Creates a baseline of expected behavior

Flags deviations from this baseline

2. Real-time Analysis
python
# Example detection logic
if cpu_usage > 85%:
    threat_level = "HIGH"
elif memory_usage > 80%:
    threat_level = "MEDIUM"
elif unusual_process_count > 5:
    threat_level = "LOW"
3. Attack Types Detected
Attack Type	Symptoms	Detection Method
Cryptominer	CPU at 90%+ for extended periods	CPU monitoring + Process analysis
Ransomware	High disk write activity	Disk I/O monitoring
Spyware	Unusual network traffic	Network monitoring
DDoS Bot	High outbound traffic	Network + Process correlation
Memory Leak	RAM usage constantly increasing	Memory trend analysis
4. AI Model Working
Algorithm: Isolation Forest

Training: Uses your system's historical data

Prediction: Binary classification (Normal/Anomaly)

Confidence: Probability score for each detection

🛠️ Troubleshooting
Common Issues and Solutions
Issue 1: "ModuleNotFoundError"
Symptoms: ModuleNotFoundError: No module named 'streamlit'

Solution:

bash
# Reinstall all dependencies
pip uninstall streamlit psutil joblib numpy pandas scikit-learn -y
pip install streamlit psutil joblib numpy pandas scikit-learn

# Or use requirements.txt
pip install -r requirements.txt --force-reinstall
Issue 2: Port Already in Use
Symptoms: Port 8501 is already in use

Solution:

bash
# Method 1: Use different port
streamlit run main_app.py --server.port 8502

# Method 2: Kill existing process
# Windows:
netstat -ano | findstr :8501
taskkill /PID [PID] /F

# Linux/Mac:
lsof -ti:8501 | xargs kill -9
Issue 3: Browser Doesn't Open Automatically
Symptoms: Terminal shows URL but browser doesn't open

Solution:

Copy the URL from terminal (usually http://localhost:8501)

Open your browser manually

Paste the URL in address bar

Issue 4: "vajra_model.pkl not found"
Symptoms: AI features not working

Solution:

bash
# Run the trainer to create model
python trainer.py

# Or create a dummy model
python -c "import joblib; from sklearn.ensemble import IsolationForest; model = IsolationForest(); joblib.dump(model, 'vajra_model.pkl')"
Issue 5: High CPU Usage by Vajra AI
Symptoms: Vajra AI itself uses too much CPU

Solution:

python
# Edit main_app.py and increase refresh interval
# Change time.sleep(5) to time.sleep(10)  # Refresh every 10 seconds instead of 5
Performance Optimization
For Low-End Systems:

Reduce refresh rate in Settings tab

Close unnecessary browser tabs

Run in headless mode:

bash
streamlit run main_app.py --server.headless true
❓ Frequently Asked Questions
Q1: Is this an antivirus replacement?
A: No, Vajra AI is a complementary tool, not an antivirus replacement. It detects behavioral anomalies while antivirus detects known malware signatures.

Q2: Does it work offline?
A: Yes! Vajra AI works completely offline. All processing happens locally on your computer.

Q3: How much system resources does it use?
A: Typically 5-10% CPU and 200-500MB RAM during normal operation.

Q4: Can it detect specific viruses?
A: It detects suspicious behavior patterns rather than specific viruses. For example, it can detect:

Programs mining cryptocurrency

Ransomware encrypting files

Spyware sending data

DDoS participation

Q5: Is my data safe?
A: Absolutely! All data stays on your local machine. No information is sent to external servers.

Q6: How often should I check the dashboard?
A: For active monitoring, keep it running in background. Check alerts when they appear. For passive use, check once daily.

Q7: Can I customize detection thresholds?
A: Yes! Go to Settings tab to adjust:

CPU/Memory thresholds

Alert levels

Refresh intervals

Notification preferences

Q8: What should I do when I get an alert?
A: Recommended steps:

Note the threat details

Check which process is causing it

Research the process online

If malicious, terminate the process

Run a full antivirus scan

Q9: Does it work on servers?
A: Yes! Vajra AI works on:

Windows Server

Linux servers (Ubuntu, CentOS)

macOS Server

Cloud instances

Q10: How to update the software?
A:

bash
# If using git:
git pull origin main
pip install -r requirements.txt --upgrade

# If downloaded ZIP:
1. Download new version
2. Replace files (keep your data)
3. Run: pip install -r requirements.txt --upgrade
📞 Support & Contact
Getting Help
GitHub Issues: Create an issue

Email: purushottamthakur2007@gmail.com / kumarsainipjk@gmail.com

Documentation: Check docs/ folder in project


Examples: Sample detection scenarios

Reporting Bugs
When reporting issues, include:

Operating System and version

Python version

Error message screenshot

Steps to reproduce

Expected vs actual behavior

Feature Requests
We welcome feature suggestions! Please include:

Use case description

Expected benefits

Priority level

Any relevant references

📜 License
Vajra AI is released under the MIT License. See LICENSE file for details.

🙏 Acknowledgments
Contributors: All developers who contributed to the project

Libraries: Streamlit, Scikit-learn, Psutil communities

Testers: Early adopters who provided valuable feedback

🔄 Update History
Version	Date	Changes
v1.0	Jan 2025	Initial release with core features
v1.1	Feb 2025	Added module integration, improved UI
v1.2	Mar 2025	Enhanced threat detection, bug fixes
🎉 Getting Started Checklist
Download and extract ZIP file

Install Python 3.8+

Install dependencies using pip install -r requirements.txt

Verify installation with test script

Run streamlit run main_app.py

Open http://localhost:8501 in browser

Configure settings as needed

Monitor system for a day to establish baseline

Set up regular monitoring routine

Happy Monitoring! 🛡️
Your system is now protected by intelligent AI-powered security monitoring.
