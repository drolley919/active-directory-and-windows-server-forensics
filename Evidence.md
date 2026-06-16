# Evidence

## Memory Image System Identification

Volatility 3 was used to examine the acquired memory image and identify system characteristics. Analysis revealed operating system information, kernel details, architecture, processor count, and system metadata necessary to establish forensic context.

⸻

## Active Process Enumeration

Process enumeration was performed to identify applications and services running at the time the memory image was acquired. Analysis revealed active forensic tools, browser processes, and network-related utilities.

Notable processes included FTK Imager and Netcat (ncat.exe), providing insight into system activity and user interactions.

⸻

## Command-Line Activity Analysis

Command-line artifacts associated with running processes were analyzed to determine how applications were executed. Examination of command-line arguments identified execution details for browser processes, FTK Imager, and Netcat.

Analysis revealed an active Netcat process configured to launch a command shell, demonstrating command execution activity present within memory.

⸻

## Process Relationship Analysis

Parent-child process relationships were examined using Volatility process tree analysis. This review provided visibility into process execution chains and helped reconstruct application activity occurring on the system.

⸻

## File Artifact Recovery

Volatility file scanning techniques were used to identify recoverable artifacts within memory. Analysis located user-created files and other artifacts that remained resident in memory structures at the time of acquisition.

⸻

## BitLocker Recovery Key Extraction

Memory-resident file artifacts were extracted using Volatility’s dumpfiles capability. Analysis successfully recovered a BitLocker recovery key document from memory.

This artifact demonstrates the forensic value of memory analysis and highlights how sensitive information can remain accessible within volatile memory.

⸻

## Registry System Identification

Registry analysis of the SYSTEM hive was performed to identify host-specific configuration information. Examination revealed the computer name and system identification artifacts associated with the investigated machine.

⸻

## Registry Time Zone Analysis

The SYSTEM hive was analyzed to determine configured time zone settings. Time zone information is critical when normalizing timestamps and reconstructing forensic timelines.

⸻

## Registry Time Zone Context Analysis

Additional registry analysis was performed against the TimeZoneInformation key to identify associated bias values and daylight-saving settings.

These artifacts support accurate event correlation and timeline reconstruction.

⸻

## Registry Autorun Discovery

The SOFTWARE hive was examined for autorun entries commonly associated with startup programs and persistence mechanisms. Analysis identified configured startup entries within Windows CurrentVersion registry paths.

⸻

## Registry Autorun Registry Review

Further review of autorun registry locations was conducted to identify executable paths associated with startup applications. Analysis revealed SecurityHealthSystray.exe configured within an autorun location.

⸻

## Operating System Version Analysis

The SOFTWARE hive was analyzed to identify operating system version and build information.

Analysis identified:

* Windows 10 Enterprise
* Version 23H2
* Build 22631

⸻

## SAM User Account Analysis

The Security Account Manager (SAM) hive was examined to identify configured user accounts. Analysis revealed account information including usernames, Security Identifiers (SIDs), login activity, password settings, and account status.

⸻

## Administrative Group Membership Analysis

Administrative group memberships were reviewed within the SAM hive to identify accounts possessing elevated privileges. Examination of associated SIDs provided visibility into privileged access assignments.

⸻

## Evidence Summary

The collected evidence demonstrates successful acquisition and analysis of memory-resident artifacts, registry data, operating system information, user accounts, administrative privileges, startup entries, and sensitive recovery-key artifacts.

Together, these artifacts provide investigators with a comprehensive view of system activity, configuration, user access, and potential persistence mechanisms present within the examined environment.
