# Sudo Privilege Vulnerability

## 1. Sudo Privilege
It is a program that allows users to run programs with the security privileges of another user, by default the superuser. The user can have the privilege of root to execute the program within its own password (or no password, it depends on the configuration).

**Local Privilege Escalation (本地提权):** Exploiting a bug, design flaw or configuration oversight in an operating system or software application to gain elevated access to resources that are normally protected from an application or user.

## 2. Related Files
**/etc/sudoers:** It is the configuration file. The user can use sudo only if he has the configuration in this file.
Examples:
1)    `root    ALL=(ALL)    ALL`
(root doesn’t need password to use sudo)
2)    `%ossuser    ALL=(root)    NOPASSWD: /test/sudo/modifytimezone.sh`
(ossuser can sudo /test/sudo/modifytimezone.sh this file without password)
3)    `%ossuer    ALL=(root)    NOPASSWD: /bin/chown,/bin/chmod`
(ossuer can use chown and chmod commands under the file /bin/chown and /bin/chmod without password)

Inappropriate Sudo configuration will cause users have high level privileges, then users could abuse this privilege to control the system. For example, if user1 wants do something that admin1 could do that, user1 should be authorized to have some previlege of admin1, insteads of escalating the privilege of root.

## 3. Attack Scenario
