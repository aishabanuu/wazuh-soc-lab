## File Integrity Monitoring (FIM)

### Objective

Validate Wazuh's ability to detect unauthorized changes to monitored files and directories.

### Activities

- Created a monitored file.
- Modified file contents.
- Renamed the file.
- Deleted the file.

### Commands Executed

```bash
mkdir ~/important

cd ~/important

touch test.txt

echo "Hello Wazuh" >> test.txt

mv test.txt test_backup.txt

rm test_backup.txt
```

### Security Events Expected

- File Created
- File Modified
- File Renamed
- File Deleted

### Outcome

File Integrity Monitoring successfully demonstrated Wazuh's ability to detect changes to monitored files and generate corresponding security events.
