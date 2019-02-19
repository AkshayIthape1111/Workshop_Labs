# Process Management

## Job Control in Linux
---
### What are jobs ?
1. In Linux or Unix, a job is defined as a task or command that has started running but not yet finished what it is doing.
2. As Linux and Unix are multitasking operating systems, they allow you to run multiple commands simultaneously.
3. Each running command is called a job, and is assigned a unique id called the job number.
4. It is very easy to manage jobs in Linux.
5. The main commands you use for job control in Linux are as follows.
   * jobs - List all the jobs that are running or suspended.
   * fg - Bring the job to the foreground.
   * bg - Send the job to the background.
   * stop or Ctrl + z - Suspend the job.
   * kill or Ctrl + c - Terminate the job.
### Managing jobs in Linux
How to manage jobs in Linux can be easily understood via an example.
<br/>
Lets simultaneously run a few commands that takes some time to complete.
```
sleep 150 &
sleep 250 &
sleep 300 &
sleep 200 &
```
Here we have executed 4 sleep commands and all are started in the background as denoted by &.
#### List the running jobs
```
jobs
```
#### Bring a job to the foreground
```
fg %job-number
fg %2
```
#### Send a job to the background
```
bg %job-number
bg %2
```
#### Suspend the job
```
stop %job-number
```
#### List process IDs of the jobs
```
jobs -l
```
#### Terminate a job
```
kill %job-number
kill %3
```
---
## Process Management
