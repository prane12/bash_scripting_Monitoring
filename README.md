# bash_scripting_Monitoring

## Real-Time System Monitoring Dashboard Script

### **Overview**
This script provides a real-time monitoring dashboard for various system metrics, including CPU usage, memory usage, network activity, disk space, system load averages, active processes, and service status. It can be run continuously with a configurable refresh interval or specific parts can be called individually using command-line options.

 ### **Features**

-  **CPU Usage**: Displays the top 10 applications consuming the most CPU.

-  **Memory Usage**: Displays the top 10 applications consuming the most memory.
  
-  **Network Monitoring**: Shows the number of concurrent connections, packet drops, and data transfer statistics.

-  **Disk Space Usage**: Lists disk usage by mounted partitions and partitions using more than 80% of the space.

-  **System Load Averages**: Displays the system's load averages.

-  **CPU Usage Breakdown**: Shows detailed CPU usage statistics.

-  **Memory Usage Details**: Displays detailed memory usage statistics.

-  **Swap Memory Usage**: Shows total, used, and free swap memory.

-  **Active Processes**: Lists the number of active processes and the top 5 by CPU and memory usage.

-  **Service Monitoring**: Checks the status of essential services like SSH, web server, and firewall services.

### **Prerequisites**
The script is designed to run on Unix-like systems (Linux or macOS).
Ensure you have the necessary permissions to execute system commands like **ps**, **ss**, **netstat**, **df**, **uptime**, **free**, and **systemctl**.

### Installation
Clone the repository or download the script file.
Make the script executable:

`chmod +x dashboard.sh`

### Usage
You can run the script in various modes depending on the monitoring data you wish to see. Below are the options available:


### Options

- `-c`: **Show top 10 applications by CPU usage.**
- `-m`: **Show top 10 applications by memory usage.**
- `-n`: **Show network monitoring information.**
- `-d`: **Show disk space usage by mounted partitions.**
- `-l`: **Show system load averages.**
- `-u`: **Show CPU usage breakdown and memory usage.**
- `-s`: **Monitor essential services** (e.g., SSH, web server, firewall).
- `-a`: **Show the number of active processes** and the top 5 processes by CPU and memory usage.


### Examples
Run the script with a full dashboard:

`./dashboard.sh`

This will run all the monitoring functions in a loop with the default refresh interval.

### Run the script to display CPU usage only:

`./dashboard.sh -c`

### Display memory usage and network monitoring information:

`./dashboard.sh -m -n`

### Monitor essential services like SSH and web servers:

`./dashboard.sh -s`

### Show CPU and memory usage details:

`./dashboard.sh -u`

### Configuring the Refresh Interval
To change the refresh interval, modify the REFRESH_INTERVAL variable at the top of the script:

`REFRESH_INTERVAL=10`
