##🔍 Python Port Scanner

A simple and beginner‑friendly TCP port scanner built using Python's socket library.
This tool scans a target IP address and detects open ports within a specified range.

🚀 Features

Scans common ports (20–1024)

Lightweight and easy to understand

Uses Python’s built‑in networking functions

Great for learning ethical hacking, network fundamentals, and socket programming

Fast and minimal codebase

📦 Requirements

Python 3.x

Works on Windows, Linux, and macOS

No external libraries are required.

🧠 How It Works

The script attempts to establish a connection to each port using socket.connect_ex().
If the connection succeeds (result == 0), the port is marked as open.

📌 Usage

Run the script:

python3 port_scanner.py


Enter the target IP address when prompted:

Enter IP address to scan: 192.168.1.10

🧾 Code
import socket

target = input("Enter IP address to scan: ")
ports = range(20, 1025)  # common ports

print(f"Scanning {target}...")

for port in ports:
    sock = socket.socket(socket.AF_INET, socket.SOCK_STREAM)
    sock.settimeout(0.5)
    result = sock.connect_ex((target, port))
    if result == 0:
        print(f"Port {port} is open")
    sock.close()

⚠️ Ethical Disclaimer

This tool is for educational and ethical penetration testing purposes only.
Do NOT scan IPs or networks that you do not own or lack explicit permission to test.
Unauthorized scanning is illegal and against ethical hacking principles.

📄 License

This project is licensed under the MIT License.
Feel free to modify and use it responsibly.
