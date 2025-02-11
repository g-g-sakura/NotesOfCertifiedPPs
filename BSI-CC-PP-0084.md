# Introduction
[BSI-CC-PP-0084 Security IC Platform Protection Profile with Augmentation Packages](https://commoncriteriaportal.org/nfs/ccpfiles/files/ppfiles/pp0084b_pdf.pdf) was developed by Eurosmart, evaluated by Brightsight, and certified by BSI, the Certification Body in Germany.
The PP was developed based on [BSI-CC-PP-0035 Security IC Platform Protection Profile](https://commoncriteriaportal.org/nfs/ccpfiles/files/ppfiles/pp0035b.pdf).

# Security Objectives Rationale
In paragraph 127, it is stated that "*the corresponding threat is* **_removed_**" for threats T.Phys-Probing and T.Phys-Manipulation.
If we read examples for "**remove**" in [7.2.7 of CC:2022 Part 1](https://commoncriteriaportal.org/files/ccfiles/CC2022PART1R1.pdf#page=48), there are three examples shown.
The authors may have intended that a logic similar to second example is applicable for countering threats T.Phys-Probing and T.Phys-Manipulation.

However, it should be noted that the physical protection is NOT removing attackers possessing the high attack potential.
As security ICs can be under full control of attackers, practically it is just a matter of time whether assets can be accessed.

Threfore, it should be better to use "**diminish**" instead of "**remove**", as per [7.2.7 of CC:2022 Part 1](https://commoncriteriaportal.org/files/ccfiles/CC2022PART1R1.pdf#page=48).
