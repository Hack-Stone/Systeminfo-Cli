System Info Fetcher 🖥️

A simple Python script to retrieve detailed system information from a Windows machine using systeminfo and psutil.

📋 Features

Retrieves full system information via the systeminfo command.

Displays virtual memory stats using the psutil library.

Pauses the console at the end so the user can review the data.


🛠️ Requirements

Python 3.x

psutil package


Install dependencies with:

pip install psutil

📄 Usage

python system_info.py

Output Example

OS Name:                   Microsoft Windows 10 Pro
OS Version:                10.0.19045 N/A Build 19045
System Manufacturer:       Dell Inc.
...
Memory : svmem(total=17179869184, available=9486848000, percent=44.8, used=7863840000, free=730000000)
Press any key to continue . . .

📁 How It Works

1. Uses subprocess to run the systeminfo command (only works on Windows).


2. Parses and formats each line of output.


3. Fetches memory statistics with psutil.virtual_memory().


4. Uses os.system("pause") to keep the console open.



⚠️ Notes

This script is built for Windows only.

To run on Linux/Mac, systeminfo must be replaced with platform-specific commands (uname, lscpu, etc.).


📜 License

This project is licensed under the MIT License.