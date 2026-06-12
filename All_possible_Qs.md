If you're preparing for a DevOps interview, Python questions are usually focused less on algorithms and more on automation, scripting, infrastructure management, APIs, file handling, and troubleshooting.

Here are common Python interview questions that DevOps engineers are asked:

## Python Fundamentals

1. What are the differences between a list, tuple, set, and dictionary?
2. What is the difference between `==` and `is`?
3. Explain mutable vs immutable objects.
4. What are Python decorators?
5. What are generators and why would you use them?
6. What is the difference between `append()` and `extend()`?
7. How does exception handling work in Python?
8. What is the purpose of `__init__()`?
9. Explain Python's garbage collection mechanism.
10. What are lambda functions?

---

## Scripting and Automation

1. Write a script to monitor disk usage and send an alert when usage exceeds 80%.
2. How would you automate log cleanup for files older than 30 days?
3. Write a script to check whether a service is running.
4. How would you restart a process automatically if it crashes?
5. Write a script to read a configuration file and update specific values.
6. How would you schedule Python scripts in Linux?
7. How can Python be used to automate server provisioning?

Example:

```python
import shutil

total, used, free = shutil.disk_usage("/")
usage = (used / total) * 100

if usage > 80:
    print("Alert: Disk usage exceeded 80%")
```

---

## File Handling

1. How do you read large log files efficiently?
2. What is the difference between `read()`, `readline()`, and `readlines()`?
3. How would you search for a specific pattern in multiple log files?
4. How do you handle CSV and JSON files in Python?
5. How would you parse application logs for errors?

Example:

```python
with open("app.log") as f:
    for line in f:
        if "ERROR" in line:
            print(line)
```

---

## Linux and System Administration

1. How do you execute Linux commands from Python?
2. What is the difference between `os.system()` and `subprocess`?
3. How would you retrieve CPU and memory utilization using Python?
4. How do you get environment variables in Python?
5. How would you find all running processes?

Example:

```python
import subprocess

result = subprocess.run(
    ["df", "-h"],
    capture_output=True,
    text=True
)

print(result.stdout)
```

---

## API and Networking

1. How do you make REST API calls using Python?
2. What libraries are commonly used for API interactions?
3. How would you authenticate using API tokens?
4. How do you handle API rate limits?
5. Write a script to query a monitoring system API.

Example:

```python
import requests

response = requests.get(
    "https://api.example.com/health",
    headers={"Authorization": "Bearer TOKEN"}
)

print(response.json())
```

---

## DevOps Tool Integration

1. How would you interact with Jenkins from Python?
2. How can Python automate Docker operations?
3. How would you trigger an Ansible playbook using Python?
4. How can Python interact with Kubernetes?
5. What Python libraries are used for cloud automation?

Common libraries:

* `boto3` (AWS)
* `kubernetes`
* `docker`
* `paramiko`
* `requests`

---

## Cloud and Infrastructure

1. How would you create an EC2 instance using Python?
2. Explain how `boto3` works.
3. How would you list all S3 buckets in an AWS account?
4. How would you automate infrastructure provisioning?
5. How do you manage secrets securely in Python scripts?

Example:

```python
import boto3

s3 = boto3.client("s3")

for bucket in s3.list_buckets()["Buckets"]:
    print(bucket["Name"])
```

---

## Multithreading and Performance

1. What is the Global Interpreter Lock (GIL)?
2. Difference between multithreading and multiprocessing?
3. When would you use `asyncio`?
4. How would you process thousands of servers concurrently?
5. How can you improve the performance of a Python automation script?

---

## Troubleshooting Questions

1. A Python script works manually but fails in a cron job. How would you debug it?
2. Your automation script suddenly becomes slow. How would you investigate?
3. A script consumes excessive memory. How would you find the root cause?
4. How would you add logging to production scripts?
5. How do you handle retries for transient failures?

---

## Frequently Asked Coding Questions for DevOps

1. Reverse a string without using slicing.
2. Find duplicate elements in a list.
3. Count occurrences of words in a log file.
4. Find the largest file in a directory.
5. Merge two dictionaries.
6. Check whether a file exists.
7. Read a large file line by line.
8. Find the top 10 most frequent IP addresses in a log.
9. Validate whether a host is reachable.
10. Parse JSON and extract specific fields.

These are the types of Python questions most commonly asked for DevOps, SRE, Platform Engineer, Cloud Engineer, and Automation Engineer interviews. The strongest preparation areas are:

* File handling
* `subprocess`
* APIs (`requests`)
* AWS (`boto3`)
* Log parsing
* Linux automation
* Error handling and logging
* Basic data structures and Python internals.
