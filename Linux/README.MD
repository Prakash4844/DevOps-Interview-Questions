#### Here are Some Resources: 
---
##### Resources
[Let's Learn Linux](https://letslearnlinux.tech)

---
##### Links to interview questions

1. [Simplilearn - Top 30 Linux Command Interview Questions and Answers](https://www.simplilearn.com/linux-commands-interview-questions-article)
2. [InterviewBit - Linux Interview Questions](https://www.interviewbit.com/linux-interview-questions/)
3. [intellipaat - Top 50 Linux Interview Questions and Answers](https://intellipaat.com/blog/interview-question/linux-interview-questions/)
4. [Edureka - Top 50 Linux Interview Questions For Beginners](https://www.edureka.co/blog/interview-questions/linux-interview-questions-for-beginners/)
5. [JavaTpoint - Top 62 Linux Interview Questions](https://www.javatpoint.com/linux-interview-questions)
6. [Mindmajix - Linux Interview Questions](https://mindmajix.com/linux-interview-questions)
7. [Guru99 - Top 60 Linux Interview Questions and Answers](https://www.guru99.com/linux-interview-questions-answers.html)
8. [Tecmint - Most Commonly Asked Questions in Linux Interviews](https://www.tecmint.com/linux-interview-questions/)
9. [Hkrtrainings - Linux Interview Questions](https://hkrtrainings.com/linux-interview-questions)
10. [GeekforGeeks - Top Linux Interview Questions With Answer](https://www.geeksforgeeks.org/linux-interview-questions/)

**NOTE** - Above resources are not mine and belong to their owners, questions may overlap.

## Table of Contents

1. [General Questions](#questions)
2. [Scenario-based Questions](#some-scenario-based-devops-question)

# Questions

## Essentials

1. **What is Linux, and how does it differ from other operating systems?**

   Linux is an open-source Unix-like operating system kernel that serves as the core of many different Linux distributions (distros). Linux differs from other operating systems primarily in its open-source nature. It is freely available for anyone to use, modify, and distribute. This open-source model fosters a large and active community of developers and users.

2. **Can you explain the Linux file system hierarchy? What are the key directories and their purposes?**

   The Linux file system hierarchy is structured as a tree with the root directory ("/") at the top. Some key directories and their purposes include:
   
   - `/bin`: Contains essential system binaries.
   - `/etc`: Configuration files and scripts.
   - `/home`: Home directories for users.
   - `/lib` and `/lib64`: Shared libraries.
   - `/tmp`: Temporary files.
   - `/var`: Variable data like logs and databases.
   - `/usr`: User-related programs and data.
   - `/sbin`: System binaries (usually for system administration).
   - `/dev`: Device files.
   - `/proc`: Virtual file system providing process information.

3. **What is the shell in Linux, and why is it important?**

   The shell is a command-line interface that allows users to interact with the Linux operating system. It interprets user commands and performs the necessary operations. Common Linux shells include Bash, Zsh, and Fish. The shell is important because it provides a powerful and flexible way to control and manage the system, automate tasks, and perform various administrative tasks.

4. **How do you find out which shell you are using, and how can you change your default shell?**

   To find out the current shell, use the `echo $SHELL` command. To change the default shell for a user, you can use the `chsh` command followed by the desired shell's path.

5. **What is a Linux distribution (distro)? Can you name a few popular Linux distributions?**

   A Linux distribution is a complete operating system package that includes the Linux kernel, software applications, libraries, and package management tools. Popular Linux distributions include Ubuntu, Debian, CentOS, Fedora, and Arch Linux, among others.

6. **Explain the concept of runlevels in Linux and how they are used.**

- **Runlevels** in Linux represent different operating states of a system. Runlevel 0 is for system shutdown, while runlevel 6 is for system reboot. Runlevels are managed by the `init` process or its modern alternatives like `systemd`.

Runlevels are different operating modes of a Linux system, each with a specific purpose. 1 (single-user mode), 3 (multi-user mode with networking), and 5 (graphical multi-user mode). They are used to control the system's behavior during startup and shutdown, allowing administrators to specify which services and processes should run in each runlevel.
   

7. **What is the purpose of the `/etc/passwd` and `/etc/shadow` files in Linux?**

   - `/etc/passwd`: Contains user account information, including usernames, user IDs (UIDs), home directories, and default shells.
   - `/etc/shadow`: Stores encrypted user passwords and password-related information, ensuring password security.

8. **How do you change file permissions in Linux, and what are the different permission levels?**

   File permissions can be changed using the `chmod` command. The permission levels are read (`r`), write (`w`), and execute (`x`), and they apply to three entities: owner, group, and others. For example, `chmod 644 file.txt` grants read (4) permission to the owner and read (4) permission to the group and others but denies write and execute permissions.

9. **What is the difference between a soft link and a hard link in Linux?**

   - Soft link (symbolic link): It is a reference to another file by its path. If the original file is deleted, the soft link becomes broken.
   - Hard link: It is a duplicate reference to the same inode (data structure). If the original file is deleted, the hard link still points to the same data.

10. **How can you search for files and directories in Linux using the command line?**

    You can use the `find` command to search for files and directories based on various criteria, such as name, size, and modification time. For example, `find /path/to/search -name "file.txt"` searches for files named "file.txt" under the specified path.

11. **What is the purpose of the `sudo` command in Linux, and how does it work?**

    `sudo` stands for "superuser do" and is used to execute commands with superuser (root) privileges. It allows authorized users to perform administrative tasks while keeping a record of their actions. Users need to be in the sudoers file to use `sudo`.

12. **How do you check the system's resource utilization, such as CPU and memory usage?**

    You can use various commands like `top`, `htop`, `free`, and `vmstat` to monitor system resource utilization. These commands display information about CPU usage, memory usage, and other system statistics in real-time.

13. **Explain the difference between a process and a thread in Linux.**

    - Process: A process is an independent program with its own memory space, resources, and execution environment.
    - Thread: A thread is a smaller unit of a process that shares the same memory space and resources with other threads in the same process. Threads can execute concurrently within the process.

14. **What is a package manager in Linux, and how does it simplify software installation and management?**

    A package manager is a tool that automates the installation, removal, and updating of software packages on a Linux system. It resolves dependencies, ensuring that required libraries and components are installed. Common package managers include APT (Debian/Ubuntu), YUM (Red Hat/CentOS), and Pacman (Arch Linux).

15. **How do you update the package repository and upgrade installed packages on a Debian-based system like Ubuntu?**

    You can update the package repository with `sudo apt update` and upgrade installed packages with `sudo apt upgrade`.

16. **Describe the boot process of a Linux system.**

    The Linux boot process typically involves several stages, including BIOS/UEFI, bootloader (e.g., GRUB), kernel initialization, and initialization of user-space processes and services. The kernel is loaded into memory, mounts the root filesystem, and starts the init or systemd process, which then initializes the system services.

17. **How can you add a new user to a Linux system, and what are the important user-related files and commands?**

    You can add a new user using the `useradd` command and set their password with `passwd`. Important user-related files include `/etc/passwd`, `/etc/shadow`, and `/etc/group`. Commands like `userdel` and `usermod` are used for user management.

18. **Explain the purpose of the `/etc/fstab` file in Linux and its relevance to disk management.**

    `/etc/fstab` is a configuration file that defines how and where filesystems should be mounted during system boot. It specifies devices, mount points, filesystem types, and options. Properly configuring this file is crucial for automounting devices and managing disk storage.

19. **What is the purpose of the `cron` and `at` commands in Linux, and how do you schedule tasks with them?**

-   **cron:** Used for scheduling recurring tasks. Users can edit their cron jobs using the crontab command.
-   **at:** Allows one-time scheduling of tasks. Use at followed by the desired time and command to schedule a job.

20. **How do you troubleshoot network connectivity issues on a Linux system?**

    Troubleshooting network issues involves using various tools like ping, traceroute, netstat, and ifconfig to check connectivity, routing, and network configuration. Reviewing log files in /var/log can also provide valuable information.

21. **Explain the concept of piping in Linux, and provide an example.**

   - **Piping** in Linux allows you to take the output of one command and use it as the input for another. The pipe symbol (`|`) is used to connect commands. For example:
   
     ```bash
     cat file.txt | grep "keyword"
     ```
   
     This command reads the contents of `file.txt`, pipes it to `grep`, and searches for the "keyword."

22. **How do you find and kill a process in Linux?**

   - To find a process, you can use the `ps` command or its variants like `ps aux`. To kill a process, you can use the `kill` command followed by the process ID (PID). For example:
   
     ```bash
     ps aux | grep "process_name"
     kill PID
     ```

23. **Explain the purpose of the `df` and `du` commands in Linux, and how they differ.**

   - The `df` command displays disk space usage on file systems, including available and used space.
   - The `du` command is used to estimate file and directory space usage. It calculates the size of individual files or directories.

24. **What is the `grep` command in Linux, and how is it used for text searching?**

    - The `grep` command is used to search for text patterns within files or text streams. It can be used with regular expressions to perform complex searches. For example:
    
      ```bash
      grep "pattern" file.txt
      ```

25. **Explain the purpose of the `tar` command in Linux and how to create and extract tar archives.**

    - The `tar` command is used to create, manipulate, and extract archive files. To create a tar archive:
    
      - To create: `tar -czvf archive.tar.gz directory/`
      - To extract: `tar -xzvf archive.tar.gz`

26. **What is SSH, and how is it used for remote access in Linux?**

    - **SSH** (Secure Shell) is a network protocol used for secure remote access to Linux systems. It allows users to log in to a remote machine over an encrypted connection and execute commands. To connect via SSH, use the `ssh` command, e.g. `ssh user@hostname`.

27. **How do you schedule recurring tasks in Linux using cron jobs? Provide an example.**

    - To schedule tasks using **cron jobs**, you can edit the crontab file with the `crontab -e` command. For example, to run a script every day at midnight:
    
      ```
      0 0 * * * /path/to/script.sh
      ```

---
---


## Some scenario-based DevOps question.


1. **Scenario:** You receive an alert that the root partition is running out of disk space on a critical server. How would you identify and free up space on the root partition?

   - **Answer:** To address this issue, you can follow these steps:

     - First, log in to the server as a user with root or sudo privileges.
     - Check the disk space usage using the `df` command to identify which filesystems are low on space.
     - Use the `du` command to identify large directories or files within the root partition that can be cleaned up.
     - Look for log files or temporary files that can be safely deleted to free up space.
     - Consider moving non-essential data to a different filesystem if available.
     - Ensure you don't remove critical system files or directories.

2. **Scenario:** A user complains about being unable to connect to an SSH server. What steps would you take to diagnose and resolve this issue?

   - **Answer:** To troubleshoot SSH connectivity issues:

     - Check if the SSH server is running on the target system using `systemctl status sshd` (for systemd) or `service ssh status` (for SysV).
     - Verify if the SSH port (default is 22) is open and accessible through a firewall.
     - Review the SSH server logs in `/var/log/auth.log` or `/var/log/secure` for error messages.
     - Ensure the user's account exists and has SSH access in `/etc/passwd` and `/etc/ssh/sshd_config`.
     - Confirm that the user's public key or password is correctly configured for authentication.
     - Check if the server has sufficient resources (CPU, memory, etc.) to handle SSH connections.

3. **Scenario:** You suspect that a process is consuming too much CPU and causing performance problems on a Linux server. How would you identify the culprit process and take corrective action?

   - **Answer:** To identify and manage the CPU-intensive process:

     - Use the `top` or `htop` command to monitor CPU usage in real-time. Identify the process with the highest CPU utilization.
     - Note the process ID (PID) of the culprit process.
     - Investigate further using tools like `ps`, `pidstat`, or `strace` to understand what the process is doing.
     - If the process is unnecessary or misbehaving, you can terminate it using the `kill` command with the PID.
     - Implement long-term solutions, such as optimizing the process or configuring resource limits with `ulimit` or `cgroups`.

4. **Scenario:** Your web server is experiencing a sudden increase in traffic, and the server's load average is spiking. What strategies would you employ to mitigate the load and keep the server responsive?

   - **Answer:** To handle increased web traffic and reduce server load:

     - Identify the source of the traffic (e.g., legitimate users, a botnet, a DDoS attack).
     - Consider implementing a Content Delivery Network (CDN) to offload static content.
     - Optimize web server configurations (e.g., Apache, Nginx) to handle concurrent connections efficiently.
     - Increase server resources, such as CPU, memory, or network bandwidth.
     - Implement caching mechanisms (e.g., Varnish, Redis) to reduce dynamic content generation.
     - Configure rate limiting or firewall rules to block malicious traffic.
     - Monitor server performance and traffic patterns to fine-tune the setup.

5. **Scenario:** A colleague accidentally deleted a critical file on a Linux system. How would you attempt to recover the deleted file?

   - **Answer:** To attempt file recovery:

     - Act quickly to minimize the chances of overwriting the deleted file's data.
     - Check if the file is in the system's trash/recycle bin.
     - Use the `undelete` command if available (not standard on all Linux systems).
     - Use file recovery tools like `extundelete` (for ext file systems) or `testdisk` to scan for and recover deleted files.
     - Restore from backups if regular backups are available.

6. **Scenario:** You need to automate a daily backup of a directory and its subdirectories. What tools and strategies would you use to create an automated backup solution?

   - **Answer:** To automate daily backups:

     - Use the `rsync` command or a backup tool like `rsnapshot` or `Bacula` to perform incremental backups.
     - Create a shell script that runs the backup command daily using `cron`.
     - Store the backups on a separate storage device or remote server.
     - Implement retention policies to manage backup versions and save disk space.
     - Schedule regular tests and monitoring to ensure backups are successful and restorable.

7. **Scenario:** A Linux server is not syncing its time with the network time server, causing time discrepancies in log files. How would you diagnose and correct the time synchronization issue?

   - **Answer:** To diagnose and correct time synchronization issues:

     - Check if the NTP (Network Time Protocol) service is running using `systemctl status ntp` (for systemd) or `service ntp status` (for SysV).
     - Verify that the server's firewall allows outbound NTP traffic.
     - Review NTP configuration in `/etc/ntp.conf` or `/etc/chrony/chrony.conf` to ensure it's configured correctly.
     - If necessary, restart the NTP service and force synchronization using `ntpd -g` or `chronyc makestep`.
     - Monitor time synchronization status with commands like `ntpq -p` or `chronyc tracking`.

8. **Scenario:** You're tasked with securing a Linux server by disabling unnecessary services and implementing a firewall. How would you go about this process?

   - **Answer:** To secure a Linux server:

     - Identify unnecessary services with the `netstat` or `ss` command and disable them using `systemctl` or `service`.
     - Configure a firewall (e.g., `iptables`, `firewalld`, `ufw`) to restrict incoming and outgoing traffic, allowing only necessary ports and services.
     - Keep the system and software up-to-date with regular security patches (`yum`, `apt`, `dnf`, etc.).
     - Implement strong user authentication, such as SSH key-based authentication.
     - Monitor logs (`/var/log`) for security events and set up intrusion detection systems (IDS) if needed.
     - Regularly perform security audits and vulnerability assessments.

9. **Scenario:** A user reports that they are unable to print from a Linux workstation to a network printer. How would you troubleshoot and resolve this printing issue?

   - **Answer:** To troubleshoot and resolve printing issues:

     - Check if the printer is powered on, connected to the network, and online.
     - Verify that the printer driver is installed on the Linux workstation.
     - Review the CUPS (Common Unix Printing System) logs in `/var/log/cups` for error messages.
     - Ensure that the user has the necessary permissions to print (in CUPS and system settings).
     - Test the printer by sending a print job from the command line (`lp` command) or a graphical application.
     - Restart the CUPS service using `systemctl restart cups` (for systemd) or `service cups restart` (for SysV).
    

 - Consider reconfiguring the printer in CUPS if needed.

10. **Scenario:** You suspect that a server is under a Distributed Denial of Service (DDoS) attack. What steps would you take to mitigate the attack and protect the server?

    - **Answer:** To mitigate a DDoS attack and protect the server:

      - Contact the hosting or network provider to inform them of the attack and request assistance.
      - Implement rate limiting or traffic filtering using tools like `iptables` or dedicated DDoS mitigation appliances.
      - Divert traffic through a DDoS scrubbing service or Content Delivery Network (CDN).
      - Consider deploying intrusion detection and prevention systems (IDS/IPS) to block malicious traffic.
      - Monitor server performance and network traffic to detect and mitigate attacks in real-time.
      - Review log files for signs of the attack and gather evidence for legal action if necessary.

11. **Scenario:** You're responsible for managing user accounts on a Linux server, and you need to create a new user with specific permissions. How would you create the user and grant the necessary permissions?

    - **Answer:** To create a new user and grant permissions:

      - Use the `useradd` command to create a new user account: `sudo useradd -m username`
      - Set the user's password with the `passwd` command: `sudo passwd username`
      - Assign the user to the appropriate user group(s) using the `usermod` command: `sudo usermod -aG groupname username`
      - Modify file and directory permissions to grant or restrict access as needed using the `chmod` and `chown` commands.
      - Configure access control using tools like `sudo` to allow or restrict specific commands or tasks.

12. **Scenario:** Your Linux server is experiencing slow response times, and you suspect that disk I/O is the bottleneck. How would you identify the source of the I/O performance issue and optimize it?

    - **Answer:** To identify and optimize disk I/O performance:

      - Use tools like `iostat`, `iotop`, or `sar` to monitor disk I/O metrics and identify the busiest disks or processes.
      - Investigate which processes are generating excessive I/O activity and optimize them (e.g., reduce disk writes).
      - Implement read and write caching mechanisms (e.g., using `systemd` service units, `bcache`, `dm-cache`) if appropriate.
      - Consider adding additional disks or upgrading to faster storage devices.
      - Tune filesystem options (e.g., `noatime`, `discard`) to reduce unnecessary disk activity.
      - Monitor and adjust disk I/O-related kernel parameters if needed.

13. **Scenario:** You've been tasked with setting up a secure remote access solution for a team of developers. How would you configure SSH for secure remote access to the server?

    - **Answer:** To set up secure remote access with SSH:

      - Ensure the SSH server (`sshd`) is installed and running on the server.
      - Configure SSH server settings in `/etc/ssh/sshd_config` to enhance security, including disabling password authentication, using SSH keys, and limiting user access.
      - Generate SSH key pairs for each developer and distribute their public keys to the server's `~/.ssh/authorized_keys` file.
      - Set appropriate permissions on SSH configuration files and user home directories (`chmod 700 ~/.ssh`, `chmod 600 ~/.ssh/authorized_keys`).
      - Optionally, implement two-factor authentication (2FA) for an extra layer of security.
      - Use a firewall to restrict SSH access to specific IP addresses or networks.
      - Regularly update SSH and the server's operating system to patch security vulnerabilities.

14. **Scenario:** A critical software application running on a Linux server crashes repeatedly. What debugging tools and techniques would you use to diagnose the issue and find a solution?

    - **Answer:** To debug a crashing application:

      - Review log files, particularly those in `/var/log`, for error messages or stack traces related to the application.
      - Use debugging tools like `gdb` to attach to the running process and collect information about the crash.
      - Check for available updates or patches for the application.
      - Inspect system resources (CPU, memory) to ensure the server has adequate resources to run the application.
      - Analyze application-specific logs or output to identify patterns or causes of crashes.
      - Reproduce the issue in a controlled environment to isolate the problem and test potential solutions.

15. **Scenario:** You need to schedule a script to run automatically every night at 2 AM. How would you set up a cron job to achieve this?

    - **Answer:** To schedule a cron job for nightly execution:

      - Edit the user's crontab file using the `crontab -e` command.
      - Add the following line to run the script at 2 AM every night:
        ```
        0 2 * * * /path/to/your/script.sh
        ```
      - Save and exit the crontab editor.
      - The script will now execute at 2 AM daily. You can customize the schedule by modifying the cron expression as needed.
