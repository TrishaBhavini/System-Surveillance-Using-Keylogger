# Keylogger for macOS

## Overview
This project focuses on safeguarding data and ensuring its recovery in the contemporary business landscape. It leverages the Core Graphics framework to interact with the macOS system and monitor keyboard events efficiently. The implementation is built using C to provide a robust and efficient keylogging mechanism.

**Note:** This keylogger does **not** work in secure areas such as password inputs. A workaround has not yet been found.

## Features
- Monitors and logs keyboard events on macOS.
- Uses Core Graphics framework for seamless interaction with macOS.
- Efficient and lightweight implementation in C.
- Supports logging to a user-defined file location.
- Can be configured to start automatically on system boot.

## Installation

### Step 1: Clone the Repository
```sh
$ git clone https://github.com/TrishaBhavini/System-Surveillance-Using-Keylogger && cd System-Surveillance-Using-Keylogger/Main
```

### Step 2: Build and Install
```sh
$ make && make install
```
This will install the keylogger to `/usr/local/bin/keylogger`.

### Step 3: Running the Keylogger
By default, logs will be stored in `/var/log/keystroke.log`. Running the keylogger may require root access, but you can configure it to log elsewhere:
```sh
$ keylogger ~/logfile.txt
```
Example output:
```sh
Logging to: /var/log/keystroke.log
```

### Step 4: Enable Startup Execution
To make the keylogger start on system boot:
```sh
$ sudo make startup
```
This will ensure the keylogger runs automatically when the system starts.

## Uninstallation
To remove the keylogger but retain log files:
```sh
$ sudo make uninstall
```

## Disclaimer
This tool is intended for educational and security research purposes only. Unauthorized use of keyloggers is illegal and unethical. Please use it responsibly and in compliance with all applicable laws.
