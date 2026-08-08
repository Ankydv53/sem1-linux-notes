# OverTheWire Bandit — Linux Practice

> Personal notes and progress while learning Linux through the OverTheWire Bandit wargame.

--------------------------------------------------------------------------------


## Bandit Progress

| Level   | Main Concept                     | Done |
|:-------:|:--------------------------------:|:----:|
|  0 → 1  | SSH / Remote Login               |  1   |
|  1 → 2  | Special Filenames                |  1   |
|  2 → 3  | Spaces in Filenames              |  1   |
|  3 → 4  | Hidden Files                     |  1   |
|  4 → 5  | File Identification              |  1   |
|  5 → 6  | Finding Files                    |  1   |
|  6 → 7  | File Properties & Search         |  0   |
|  7 → 8  | grep / Text Searching            |  0   |
|  8 → 9  | sort / uniq                      |  0   |
|  9 → 10 | strings / Encoded Data           |  0   |
| 10 → 11 | Base64 Encoding                  |  0   |
| 11 → 12 | ROT13 / Character Transformation |  0   |
| 12 → 13 | Compression / File Formats       |  0   |
| 13 → 14 | SSH Keys                         |  0   |
| 14 → 15 | Network Services / Ports         |  0   |
| 15 → 16 | SSL / TLS                        |  0   |
| 16 → 17 | Port Scanning                    |  0   |
| 17 → 18 | Git / Version Control            |  0   |
| 18 → 19 | Restricted Commands              |  0   |
| 19 → 20 | Setuid / Permissions             |  0   |
| 20 → 21 | Network Daemon / Connections     |  0   |
| 21 → 22 | Cron Jobs                        |  0   |
| 22 → 23 | Cron / Shell Scripts             |  0   |
| 23 → 24 | Automated Scripts                |  0   |
| 24 → 25 | Shell Scripting                  |  0   |
| 25 → 26 | SSH / Shell Environment          |  0   |
| 26 → 27 | Restricted Shell                 |  0   |
| 27 → 28 | Git Repository                   |  0   |
| 28 → 29 | Git Objects / History            |  0   |
| 29 → 30 | Git Branches / Data              |  0   |
| 30 → 31 | Git Tags / History               |  0   |
| 31 → 32 | Git Push / Repository            |  0   |
| 32 → 33 | Shell Variables / Commands       |  0   |
| 33 → 34 | Final Challenge / Review         |  0   |

> **Progress:** `0 = Pending` · `1 = Completed`



--------------------------------------------------------------------------------


# Level 0 → 1

**Objective:** Login to the Bandit Level 0 server using SSH.

**Commands:**

`ssh bandit0@bandit.labs.overthewire.org -p 2220`

`ls`

`cat readme`

**What I learned:** How to connect and log in to a remote Linux server using SSH through the terminal.

**Key takeaway:** SSH allows secure remote access to a Linux machine from the command line.

---

--------------------------------------------------------------------------------

# Level 1 → 2

**Objective:** Find the password stored in a file named `-`.

**Commands:**

`ls`

`cat ./-`

**What I learned:** A filename beginning with - can be interpreted as a command-line option, so ./ can be used to clearly specify that it is a filename.

**Key takeaway:** Use ./ when working with filenames that begin with - to prevent them from being interpreted as command options.

---

--------------------------------------------------------------------------------

# Level 2 → 3

**Objective:** Find the password stored in a file whose name contains spaces.

**Commands:**

`ls`

`cat ./'--spaces in this filename--'

**What I learned:** Linux treats spaces as separators between arguments, so spaces inside filenames must be escaped or the filename must be quoted.

**Key takeaway:** Use \ to escape spaces or quotes around filenames containing spaces.

---

--------------------------------------------------------------------------------

# Level 3 → 4

**Objective:** Find the password stored in a hidden file inside the `inhere` directory.

**Commands:**

`ls`

`cd inhere`

`ls -la`

`cat ...Hiding-From-You`

**What I learned:** Linux hidden files usually begin with a dot, and normal ls does not display them.

**Key takeaway:** Use ls -la to display hidden files along with detailed file information.

---

--------------------------------------------------------------------------------

# Level 4 → 5

**Objective:** Find the human-readable file among several files in the `inhere` directory.

**Commands:**
`cd inhere`
`file ./*`
`cd ./-file07`
`ls`

**What I learned:** I learn `file` cmd and proper use of it.

**Key takeaway:** use file ./* to display all file types then cd file and then ls to get password.

---

--------------------------------------------------------------------------------

# Level 5 → 6

**Objective:** Find a file with specific properties such as size, permissions, and file type.

**Commands:**
`cd inhere`
`find ! -executable -size 1033c -type f`
`cat ./maybehere07/.file2`

**What I learned:** I learned use of find command 

**Key takeaway:**use find command to find the needed file then use cat to get password.

---

--------------------------------------------------------------------------------

# Level 6 → 7

**Objective:** Find a file somewhere on the server with specific owner, group, and size properties.

**Commands:**

**What I learned:**

**Key takeaway:**

---

--------------------------------------------------------------------------------

# Level 7 → 8

**Objective:** Find the password in a file by searching for a specific word.

**Commands:**

**What I learned:**

**Key takeaway:**

---

--------------------------------------------------------------------------------

# Level 8 → 9

**Objective:** Find the password that occurs only once in a file containing repeated lines.

**Commands:**

**What I learned:**

**Key takeaway:**

---

--------------------------------------------------------------------------------

# Level 9 → 10

**Objective:** Find the password hidden among human-readable strings in a binary file.

**Commands:**

**What I learned:**

**Key takeaway:**

---

--------------------------------------------------------------------------------

# Level 10 → 11

**Objective:** Decode Base64-encoded data to obtain the password.

**Commands:**

**What I learned:**

**Key takeaway:**

---

--------------------------------------------------------------------------------

# Level 11 → 12

**Objective:** Decode text that has been transformed using ROT13.

**Commands:**

**What I learned:**

**Key takeaway:**

---

--------------------------------------------------------------------------------

# Level 12 → 13

**Objective:** Extract and repeatedly decompress compressed data to find the password.

**Commands:**

**What I learned:**

**Key takeaway:**

---

--------------------------------------------------------------------------------

# Level 13 → 14

**Objective:** Use an SSH private key to log in to the next Bandit level.

**Commands:**

**What I learned:**

**Key takeaway:**

---

--------------------------------------------------------------------------------

# Level 14 → 15

**Objective:** Submit the current password to a service running on localhost through a network connection.

**Commands:**

**What I learned:**

**Key takeaway:**

---

--------------------------------------------------------------------------------

# Level 15 → 16

**Objective:** Use SSL/TLS to securely connect to a local service and retrieve the next password.

**Commands:**

**What I learned:**

**Key takeaway:**

---

--------------------------------------------------------------------------------

# Level 16 → 17

**Objective:** Identify the correct port among a range of ports and use SSL/TLS to obtain the password.

**Commands:**

**What I learned:**

**Key takeaway:**

---

--------------------------------------------------------------------------------

# Level 17 → 18

**Objective:** Compare two files and identify the changed line containing the next password.

**Commands:**

**What I learned:**

**Key takeaway:**

---

--------------------------------------------------------------------------------

# Level 18 → 19

**Objective:** Log in and retrieve the password despite a restricted login shell.

**Commands:**

**What I learned:**

**Key takeaway:**

---

--------------------------------------------------------------------------------

# Level 19 → 20

**Objective:** Use a Setuid program to access the password for the next level.

**Commands:**

**What I learned:**

**Key takeaway:**

---

--------------------------------------------------------------------------------

# Level 20 → 21

**Objective:** Use a network service and communicate with it to obtain the next password.

**Commands:**

**What I learned:**

**Key takeaway:**

---

--------------------------------------------------------------------------------

# Level 21 → 22

**Objective:** Inspect scheduled cron jobs and determine how they provide the next password.

**Commands:**

**What I learned:**

**Key takeaway:**

---

--------------------------------------------------------------------------------

# Level 22 → 23

**Objective:** Analyze a cron job script and determine how it handles the password.

**Commands:**

**What I learned:**

**Key takeaway:**

---

--------------------------------------------------------------------------------

# Level 23 → 24

**Objective:** Understand and use a scheduled shell script to obtain the next password.

**Commands:**

**What I learned:**

**Key takeaway:**

---

--------------------------------------------------------------------------------

# Level 24 → 25

**Objective:** Use a network service and scripting to find the required PIN and obtain the next password.

**Commands:**

**What I learned:**

**Key takeaway:**

---

--------------------------------------------------------------------------------

# Level 25 → 26

**Objective:** Use SSH and understand the unusual shell environment to reach the next level.

**Commands:**

**What I learned:**

**Key takeaway:**

---

--------------------------------------------------------------------------------

# Level 26 → 27

**Objective:** Escape the restricted shell environment and obtain access to the next level.

**Commands:**

**What I learned:**

**Key takeaway:**

---

--------------------------------------------------------------------------------

# Level 27 → 28

**Objective:** Clone a Git repository and find the password stored in the repository.

**Commands:**

**What I learned:**

**Key takeaway:**

---

--------------------------------------------------------------------------------

# Level 28 → 29

**Objective:** Inspect Git history and repository data to find a removed or changed password.

**Commands:**

**What I learned:**

**Key takeaway:**

---

--------------------------------------------------------------------------------

# Level 29 → 30

**Objective:** Inspect Git branches and repository data to find the password.

**Commands:**

**What I learned:**

**Key takeaway:**

---

--------------------------------------------------------------------------------

# Level 30 → 31

**Objective:** Inspect Git tags and repository history to locate the password.

**Commands:**

**What I learned:**

**Key takeaway:**

---

--------------------------------------------------------------------------------

# Level 31 → 32

**Objective:** Use Git to push the required data to the remote repository and obtain the next password.

**Commands:**

**What I learned:**

**Key takeaway:**

---

--------------------------------------------------------------------------------

# Level 32 → 33

**Objective:** Escape the uppercase-only shell environment and execute commands to obtain the next password.

**Commands:**

**What I learned:**

**Key takeaway:**

---

--------------------------------------------------------------------------------

# Level 33 → 34

**Objective:** Complete the final Bandit challenge and review the Linux and security concepts learned throughout the wargame.

**Commands:**

**What I learned:**

**Key takeaway:**

---

--------------------------------------------------------------------------------

## Overall Progress

**Levels completed:** `0 / 34`

**Commands learned:** `0`

**Current focus:** Linux CLI & problem solving

---
