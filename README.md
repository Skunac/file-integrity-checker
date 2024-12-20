# File Integrity Checker

## 📋 **Overview**
The **File Integrity Checker** is a simple tool to verify if log files have been tampered with. It helps ensure log files remain unchanged, which is important for system security and auditing.

This project is part of my learning journey following the [DevOps Roadmap](https://roadmap.sh/devops). It introduces key concepts like hashing, file integrity checks, and basic scripting.

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

## ⚙️ **Usage**
### **1. Initialize File Hashes**
```bash
./integrity-check init /var/log
```
**Output:**
```
Hashes stored successfully.
```
This stores initial hashes for log files in `/var/log`.

### **2. Check File Integrity**
```bash
./integrity-check check /var/log/syslog
```
**Output (If tampered):**
```
Status: Modified (Hash mismatch)
```
**Output (If unchanged):**
```
Status: Unmodified
```

### **3. Update File Hash**
```bash
./integrity-check update /var/log/syslog
```
**Output:**
```
Hash updated successfully.
```

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

## 🛠️ **Setup**
1. **Clone the Repo**
   ```bash
   git clone https://github.com/your-username/file-integrity-checker.git
   cd file-integrity-checker
   ```
2. **Make Script Executable**
   ```bash
   chmod +x integrity-check
   ```
3. **Run Initial Setup**
   ```bash
   ./integrity-check init /path/to/your/log/files
   ```

---

**Simple, effective log file security!** 🚀

