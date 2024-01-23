# Answers & Test Notes

1. Manual installation process for GRUB2 on a BIOS System?
	1. Create the GRUB2 configuration file `grub2-mkconfig /boot/grub2/grub.cfg`
	2. List block devices.
	3. Find the primary hard drive.
	4. Install GRUB2 in the MBR.
	5. Reboot the system.
2. You have set up your Linux system so that logging information is stored at `/run/log/journal`. Users accessing this folder report that journals are lost each time the system reboots. Which command will you need to make log data available permanently?
	**Answer:** `systemd-tmpfiles --create --prefix /var/log/journal`
3. ``hwclock`` or `timedatectl` is the command you should use to modify the time on the system's clock.
4. About `telinit`: Telinits set runlevels for a Linux system.
	1. Runlevel 0: Shuts down the system
	2. Runlevel 1: Runs the system in **single user mode**, which is useful for administrative tasks.
	3. Runlevel 2: Runs the system in multiuser mode but without networking services.
	4. Runlevel 3: Runs the system in multiuser mode with networking but without a GUI. This is the normal or **default runlevel**.
	5. Runlevel 4: Runs the machine in a state as specified by the user.
	6. Runlevel 5: Runs the machine in a multiuser mode with networking and a GUI started.
	7. Runlevel 6: Reboots the system.
5. **Cloud-init** is a service that allows you to customize a Linux-based OS for the cloud. It does the setup for a cloud instance using a configuration file.
6. PAM flags in descending order of priority:
	1. required: flagged module will immediately return control if it fails
	2. requisite: flagged module needs to successfully complete for libpam to succesfully allow the application
	3. sufficient - if earlier modules are successful, the flagged module will bring control back to the application successfully
	4. optional - success or failure of the flagged module is not noteworthy for PAM
	5. reset - clears status and restarts the next module in the stack
	6. ignore - module return status has no impact
7. Which command is used to install an SSH key on a Linux server as an authorized key for passwordless logins?
	**Answer:** `ssh-copy-id`
8. Some terms
	1. **Kickstart**: method of installing a Linux operating system without human supervision or involvement.
	2. **Linux containers**: processes that are kept separated from the rest of the Linux system.
	3. **Anaconda**: program used to install Linux distributions like Red Hat Linux and Fedora. When run, it analyzes the target computer system's hardware and configures it appropriately, creating a matching filesystem for it.
9. `lpr` prints stuff, `lpq` displays printer status.
10.  You need to view all the valid security credentials stored on a cache on you Linux machine. Which of these commands will you use to view them?
	**Answer**: `klist`: used to display a list of cached Kerberos tickets.
11. You need to start the mysql service on a Linux machine. However, you want to start the service at a specific runlevel. Which command should you use?
	**Answer**: `chkconfig`
12. More terms, I guess:
	1. `brctl`: allows connecting KVM(kernel-based virtual machine) guests and hosts. `#brctl addbr <bridge-over-tomm>`
	2. `libvrt`: The libvrt daemon has a list of defined networks on the KVM system using the following command: `#virsh net-list`
	3. KVM: open-source virtual machine implementation that is a part of the Linux system.
13. `/etc/profile` contains environment variables that apply for all users on a Linux machine.
14. Which command specifies network filtering rules for entire sets of IP addresses?
	**Answer**: `ipset` or `sudo ipset`. `ipset` is a complimentary tool to be used with `iptables` that allows you to specify rules that apply to entire *sets* of IP addresses.
15. `echo $#` returns the number of positional arguments / **command line parameters** passed.
16.  You need an **interface to boot** a Linux system that supports remote diagnostics and troubleshooting in case there is an issue. Which of these should you choose?
	**Answer**: UEFI
17. `pam_tally2 --user=$USER --reset` unlocks user accounts
18. `PATH=$PATH=/usr/bin/bash` sets the command search path for the shell

# Previous: [Securing Linux](Securing%20Linux.md)
# Next: [09 Jan 24 Practice Test](09%20Jan%2024%20Practice%20Test.md)