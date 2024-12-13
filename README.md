
# sysopctl

`sysopctl` is a custom Linux command-line utility designed to manage and monitor various system resources and tasks. It provides an intuitive interface for operations such as managing services, checking system health, analyzing logs, and creating backups.

---

## Flowchart

Below is the flowchart representation of the functionality of `sysopctl`:

![Sysopctl Flowchart](https://github.com/user-attachments/assets/1fbed2a7-8fc4-4d3e-9c5a-3d32ece61608)

```plaintext
                             +-----------------------+
                             |       sysopctl       |
                             +-----------------------+
                                       |
          ---------------------------------------------------------
          |                 |                 |                   |
  +---------------+  +----------------+  +---------------+  +-------------------+
  | Service Mgmt  |  | System Monitor |  | Disk & Logs   |  |    Backup Ops     |
  +---------------+  +----------------+  +---------------+  +-------------------+
          |                 |                 |                   |
+----------------+  +----------------+  +---------------+  +---------------------+
| List/Start/Stop|  | View Load/Proc |  | Disk Usage/Log|  | Backup Directory/File|
+----------------+  +----------------+  +---------------+  +---------------------+
```
---


## Features

- **Service Management**
  - List active services.
  - Start or stop specific services.

- **System Monitoring**
  - View current system load averages.
  - Monitor running processes in real-time.

- **Disk and Log Analysis**
  - Display disk usage by partition.
  - Analyze critical log entries.

- **Backup Operations**
  - Create backups of directories or files using `rsync`.

- **General Commands**
  - `--help`: Displays detailed usage instructions.
  - `--version`: Shows the current version of `sysopctl`.

---

## Installation

### Prerequisites

Ensure the following tools are installed on your Linux system:
- `bash` (version 4.0 or higher)
- `systemctl`
- `rsync`
- `journalctl`
- `df`, `uptime`, `htop` (optional for advanced features)

### Steps

1. Clone the repository:
   ```bash
   git clone <repository-url>
   cd sysopctl
   ```

2. Make the script executable:
   ```bash
   chmod +x sysopctl.sh
   ```

3. (Optional) Install the manual page:
   ```bash
   sudo cp sysopctl.1 /usr/share/man/man1/
   man sysopctl
   ```

---

## Usage

Run `sysopctl` followed by the desired command:

### General Commands

- **Help**: Display help information
  ```bash
  ./sysopctl.sh --help
  ```
- **Version**: Show the version of the utility
  ```bash
  ./sysopctl.sh --version
  ```

### Service Management

- **List Services**: List all active services
  ```bash
  ./sysopctl.sh service list
  ```
- **Start Service**: Start a specific service
  ```bash
  ./sysopctl.sh service start <service-name>
  ```
- **Stop Service**: Stop a specific service
  ```bash
  ./sysopctl.sh service stop <service-name>
  ```

### System Monitoring

- **System Load**: Display current load averages

  ```bash
  ./sysopctl.sh system load
  ```

- **Process Monitor**: Monitor processes in real-time

  ```bash
  ./sysopctl.sh process monitor
  ```

### Disk and Log Operations

- **Disk Usage**: Show disk usage by partition
  ```bash
  ./sysopctl.sh disk usage
  ```
- **Log Analysis**: Analyze critical log entries
  ```bash
  ./sysopctl.sh logs analyze
  ```

### Backup

- **Create Backup**: Backup a specified directory or file
  ```bash
  ./sysopctl.sh backup <path>
  ```

---

## Example

Backup a user’s documents folder:

```bash
./sysopctl.sh backup /home/user/documents
```

Start the `sshd` service:

```bash
./sysopctl.sh service start sshd
```

Analyze recent critical log entries:

```bash
./sysopctl.sh logs analyze
```

---


