# File Integrity Checker

## 📋 **Overview**
The **File Integrity Checker** is a simple tool to verify if log files have been tampered with. It helps ensure log files remain unchanged, which is important for system security and auditing.

This project is part of my learning journey following the [DevOps Roadmap](https://roadmap.sh/devops). It directly follows the [File Integrity Checker Project](https://roadmap.sh/projects/file-integrity-checker) outlined in the roadmap. The project introduces key concepts like hashing, file integrity checks, and basic scripting.

---

## 🚀 **Features**
- **Check File Integrity**: Detects changes to log files by comparing file hashes.
- **Directory Support**: Works with single files or entire directories.
- **Cryptographic Hashing**: Uses SHA-256 to generate unique fingerprints for files.
- **Reinitialize Hashes**: Allows manual re-initialization of stored hashes.
- **Status Reporting**: Shows if files are modified, unmodified, or updated.

---

## 🎯 **Objectives**
- **Enhance Security**: Detect unauthorized changes in log files.
- **Learn Hashing**: Get hands-on experience with SHA-256.
- **Practice Scripting**: Improve Bash and command-line skills.

---

## 📚 **How It Works**
1. **Initialization**: Store hashes of log files for future comparisons.
2. **Check Integrity**: Compare current file hashes to stored ones.
3. **Update Hashes**: Recalculate and store updated hashes if changes are expected.

---

## ⚙️ **Setup and Usage**

1. **Clone the Repo**  
   Clone the repository and navigate to the project directory:
   ```bash
   git clone https://github.com/your-username/file-integrity-checker.git
   cd file-integrity-checker
   ```

2. **Make Script Executable**  
   Make the main script executable:
   ```bash
   chmod +x integrity-check
   ```

3. **Initialize File Hashes**  
   Generate and store hashes for either a single file or an entire directory:
   ```bash
   ./integrity-check init /path/to/your/log/files
   ```
   Examples:
   - Single file:
     ```bash
     ./integrity-check init /var/log/syslog
     ```
   - Directory:
     ```bash
     ./integrity-check init /var/log
     ```

4. **Check File Integrity**  
   Compare current hashes with stored ones to detect changes:
   ```bash
   ./integrity-check check /path/to/your/log/files
   ```

5. **Update File Hashes**  
   Recalculate and store updated hashes when changes are expected:
   ```bash
   ./integrity-check update /path/to/your/log/files
   ```

---

## 🚀 **Commands Summary**
| **Command**                               | **Description**                                      |
|-------------------------------------------|------------------------------------------------------|
| `./integrity-check init /path`            | Store initial hashes for the specified file or path. |
| `./integrity-check check /path`           | Check file integrity by comparing hashes.            |
| `./integrity-check update /path`          | Update hashes for modified files.                   |

---

## 📦 **Project Structure**
```
file-integrity-checker/
├── integrity-check         # Main script file
├── hash_store/             # Directory to store file hashes
├── README.md               # Project documentation
└── examples/               # Example log files for testing
```

---

**Simple, effective log file security!** 🚀