| Ordered | Objective Title                                               | EST Total Min | Mode of Delivery          |
| ------- | ------------------------------------------------------------- | ------------- | ------------------------- |
| 0       | Course Start                                                  | 45            | Instruction (Resident)    |
| 1       | MacOS (Familiarization and Hardening)                         | 30            | Instruction (Resident)    |
| 2       | Identity and Signature Management (1SFC IDM)                  | 130           | Guest Instructor          |
| 2b      | Alternate Stuff, Account Hardening and Ad Tech                | 45            | Instruction (Resident)    |
| 2       | Stuff                                                         | 45            | Instruction (Resident)    |
| 3       | Email Aliases                                                 | 15            | Instruction (Resident)    |
| 3       | DFP Terms                                                     | 15            | Distributed (Asynchronos) |
| 3       | Account Authentication (Password, Password Managers, and MFA) | 60            | Instruction (Resident)    |
| 5       | VPN                                                           | 30            | Instruction (Resident)    |
| 6       | Cryptography (Concepts, Application)                          | 70            | Instruction (Resident)    |
| 6       | Secure Communication                                          | 45            | Instruction (Resident)    |
| 7       | Virtual Machines                                              | 60            | Instruction (Resident)    |
| 4       | Browser Hardening (configuration, plugins, activity)          | 30            | Instruction (Resident)    |
| 8       | Windows Hardening                                             | 20            | Instruction (Resident)    |
| 9       | Network Hardening                                             | 60            | Instruction (Resident)    |
| 10      | Mobile Hardening                                              | 30            | Instruction (Resident)    |
| END     | CAPSTONE                                                      | 70            | Assessment                |
| END     | Closing                                                       | 30            | -                         |
| END     | TOTAL TIME                                                    | 830           | 16.6                      |
<!-- TBLFM: @>$3=sum(@I..@-1) -->
<!-- TBLFM: @>$4=(@>$3/50) -->
### NOTE: 
The formulas require an additional plugin: [Advanced Tables](source https://github.com/tgrosinger/md-advanced-tables/blob/main/docs/formulas.md)
Below are the formulas with comments
```md
// Formula to get total minutes in the third column
<!-- TBLFM: @>$3=sum(@I..@-1) -->
// Formula to get total academic hours (50 minutes) based on the total minutes 
<!-- TBLFM: @>$4=(@>$3/50) -->
```

## Referenced Terms
Modes of Delivery:
-  Instruction (Resident)
-  Instruction (Non-Resident)
-  Distributed (Synchronos)
-  Distributed (Asynchronos)
-  Blended
