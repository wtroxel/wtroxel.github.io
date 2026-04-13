---
layout: post
title: "Lab 1 | Packet Tracer - Navigate the IOS"
date: 2026-04-12 12:00:00 -0800
categories:
   - networkengineer
---
Objective: The goal of this following lab is to establish basic connections, access the command line, explore the help (?) option, explore EXEC Modes, and set the clock. This activity will showcase navigating Cisco IOS, configuration modes, accessing common commands, and changing the computer clock with the clock command.

Procedure:
Part 1: Establish Basic Connections, Access the CLI, and Explore Help
1. Click connection lightning bolt icon in lower left of packet tracer window
2. Select blue Console cable, connect ends to PC1 RS-232 port and S1 switch connection port
3. Select console port to complete connection
4. Click PC1 > select Desktop tab > click Terminal application icon
5. Confirm the setting for bits per seconds is 9600 bits per second > Press OK
![Terminal Configuration](/assets/networkengineer/01_Navigate_Cisco_IOS/00_TerminalConfig.png)
*Figure 1. Configuration for bits per second, data bits, parity, stop bits, and flow control settings.*
6. Click Press RETURN to get started! Click Enter or Return. See S1 prompt
7. Type “?” to display commands. Type “t?” and “te?” to show those starting with “t” and “te”
![Terminal Configuration](/assets/networkengineer/01_Navigate_Cisco_IOS/02_Priv_Exec_Commands.png)

Part 2: Explore EXEC Modes
1. Type “?” to display the command list. Note “enable” command and the information displayed
2. Type “en” and press Tab key for tab completion to complete partial command
3. Type “enable” and press Return or Enter. Should see # symbol such that prompt is S1#
4. Type “?” for new commands for privileged EXEC. Type “c?” for five that start with c
![Terminal Configuration](/assets/networkengineer/01_Navigate_Cisco_IOS/02_Priv_Exec_Commands.png)
5. Type “configure”  > press Return or Enter. See configure from terminal, memory, or network.
6. Press Enter to accept default parameter [terminal] and see prompt change to S1(config)#
7. Type “exit” to exit global configuration mode and return to privileged EXEC mode
![Terminal Configuration](/assets/networkengineer/01_Navigate_Cisco_IOS/03_Clock_Configure.png)

Part 3: Set the Clock
1. In privileged EXEC mode, type “show clock” to display the time and date
![Terminal Configuration](/assets/networkengineer/01_Navigate_Cisco_IOS/04_Clock_Confirm.png)
2. Type “clock” > press Enter > see “% Incomplete command” due to missing parameters
3. Type “clock set ?” to show additional parameters for setting the clock
4. Type “clock set” > press Enter > see “% Incomplete command” for missing parameters 
5. Type “clock set 15:00:00 ?” > check the output for additional information requests
6. Type "clock set 15:00:00 31 JAN 2035” > press Enter or Return
7. Type “show clock” > press Enter or Return > Visualize date and time of the clock
![Terminal Configuration](/assets/networkengineer/01_Navigate_Cisco_IOS/05_Clock_Change.png)

