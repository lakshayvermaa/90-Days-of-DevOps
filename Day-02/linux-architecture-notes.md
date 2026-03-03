# Day 02 - Linux Architecture, Processes & Foundation

## 1. Linux Architecture

Linux follows a layered architecture:

- Hardware
- Kernel (Core of OS)
- Shell
- Applications (User Space)

System calls act as a bridge between user space and kernel space.

---

## 2. Kernel Responsibilities

- CPU scheduling
- Memory management
- Process management
- Device management
- System calls

The kernel directly interacts with hardware.

---

## 3. What is a Process?

- A program is a static file.
- When executed, it becomes a process.
- Every process has a unique PID.
- OS manages processes using a Process Control Block (PCB).

---

## 4. Process Creation (Basic Concept)

- fork() → creates a new process (child process)
- exec() → loads a new program into that process
- Parent can wait using wait()

---

## 5. Useful Commands Practiced

- ps -ef → List running processes
- top → Monitor CPU & memory usage
- kill → Terminate a process
- systemctl → Manage services
- uptime → Check system load

---

Day 02 focused on building strong Linux fundamentals before moving deeper into systemd and process states.
