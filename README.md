labtech_agent_reinstall
========================

**Original Author:** MartynKeigher in ##labtech on Freenode

**Description:**
This can be used by a Labtech monitor / Windows scheduled task / Windows GPO to re-install the Labtech Agent if it is removed.

Usage:
----------
* Edit the line in script.bat that contains \\domain-name.local\Netlogon\LabTechAgent.exe to point to the location and name of the LTAgent on the network. 
* Run script.bat from a Labtech agent, scheduled task, or GPO and the script will check if Ltsvc.exe is found in the proper location. If it is not then it will attempt to reinstall.

Scheduling as a task
----------
To schedule a task at 1pm every day use the following command in the command line. First, edit this command to point to script.bat.
`at 13:00 /every:M,T,W,Th,F,S,Su C:\path\to\script.bat`
