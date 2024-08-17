# Linux-Server-Forensics

1. You need ``IP``.
2. then connect with ``SSH`` with target machine password.
3. like that : ``<user>@<Target-IP>`` now hit Enter button.
4. Enter Password and then hit the Enter Button and you are connected with Target.
5. After all Enjoy...


# **Victim [Machine] 1:**

> 1. Go to ``cd /var/log/apache2 ``
> 2. ``ls``
> 3. You found two file or more files.
> 4. Enter this command for nmap path or more path's ``cat access.log | grep nmap | cut -d ‘“‘ -f 2 | sort | uniq``
> 5. what page allow users to upload files ? Command : ``cd /var/www/`` or ``cd /var/www/html`` totally find the upload Files/Folders.
> 6. What IP uploaded files to the server Command : ``grep “POST” access.log`` on the `var/log/apache2/` directory.
> 7. Who left an exposed security notice on the server ? Command : ``cat access.log | grep -i dirbus | grep -v 404 | cut -d ‘“‘ -f 2 | sort | uniq``
> 8. What command and option did the attacker use to establish a backdoor ? Command : ``cat /etc/crontab``
> 9. What is the Password of the second root account ? Commad : ``cd /etc/`` ``cat passwd``

# **Victim [Machine] 2:** 

> 1. Name one of the non-standard HTTP Resquests. ? Command : ``cat access.log | cut -d ‘“‘ -f 2 | sort | uniq`` on the var/log/apache2/ directory.
> 2. At what time was the Nmap scan performed? (Format: HH:MM:SS)? Command : ``cat access.log | grep -a <name of found from access.log>
> 3. What username and hostname combination can be found in one of the autorized_keys file ? (Format : username@hostname)? Command : ``cat /root/.ssh/authorized_keys`` on the /var/log/apache2/ directory.
> 4. What is the first command present in root's bash_history file ? Command : ``sudo head /root/.bash_history``

# **Victim [Machine] 3:**
> 1. Figure out what's going on and find the flag ? Commad : ``systemctl status IpManager.service`` and ``cat /etc/network/ZGtsam5hZG1ua2Fu.sh`` and you will found answes..[gh0st_1n_the_machine]
