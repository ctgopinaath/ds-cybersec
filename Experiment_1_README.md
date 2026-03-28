
# Experiment 1: Malware Analysis (Detailed)

## Aim
To perform experiment 1 as part of malware analysis using Ubuntu tools in a controlled environment.

## Objective
- Understand the concept behind experiment 1
- Perform analysis using appropriate tools
- Interpret results and behavior

## Theory
Malware analysis involves studying malicious programs to understand their behavior, origin, and impact.
This experiment focuses on concept 1 including static/dynamic/reverse/network analysis depending on the case.

## Tools Used and Purpose

### sha256sum
Used to generate a cryptographic hash of a file. Helps in identifying malware uniquely and comparing with threat databases.

### file
Determines the file type. Important because malware often disguises itself with fake extensions.

### strings
Extracts readable ASCII strings from binaries. Helps identify hidden URLs, commands, or suspicious patterns.

### clamscan (ClamAV)
Scans files using antivirus signatures. Helps detect known malware.

### strace
Monitors system calls made by a program. Helps understand runtime behavior.

### ltrace
Tracks library calls used by a program.

### tcpdump
Captures network packets to analyze communication.

### objdump
Displays binary structure and headers.

### exiftool
Extracts metadata from files.

### upx
Packs/unpacks executables. Malware often uses packing to evade detection.

### chkrootkit / rkhunter
Detect rootkits and hidden threats.

### apktool / jadx
Reverse engineer Android applications.

## Installation
```bash
sudo apt update
sudo apt install clamav strace ltrace tcpdump wireshark exiftool upx chkrootkit rkhunter apktool jadx python3-pip -y
pip3 install pefile oletools pdfid
sudo freshclam
```

## Steps
1. Prepare sample file (EICAR or test binary)
2. Perform static analysis (hash, file type, strings)
3. Perform dynamic analysis if applicable
4. Observe behavior and logs

## Commands
```bash
sha256sum sample
file sample
strings sample
clamscan sample
strace ./sample
ltrace ./sample
tcpdump -i any
objdump -x sample
exiftool sample
upx -t sample
chkrootkit
rkhunter --check
```

## Sample Output
Example:
```
sample: Eicar-Test-Signature FOUND
open("/etc/passwd", O_RDONLY) = 3
```

## Result
Experiment 1 completed successfully. Malware behavior and characteristics were analyzed.

## Usage
- Cybersecurity analysis
- Incident response
- Threat detection
- Reverse engineering

## Precautions
- Always use Virtual Machine
- Do not execute real malware on host
- Use safe samples
