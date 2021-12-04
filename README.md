![Windows 11 Syscall table](https://i.ibb.co/JKLw1QY/Title.jpg "Windows 11 Syscall table")

# 11Syscalls
Windows 11 Syscall numbers. Ready to use in direct syscall. Actively maintained.

This repository contains system call tables collected from windows 11. As of now only 10.0.22000 is included, But I have planned to continue updating this table over time.
I can use any help with this table and even provide more data over time.

# Windows versions included
| OS | CodeName | Edition | Build Number | Architecture | DLL | Syscall Table |
|:---:|:---:|:---:|:---:|:---:|:---:|:---:|
| Windows | 21H2* | Pro | 10.0.22000 | x64 | ntdll.dll | [link](https://github.com/ikermit/11Syscalls/blob/main/MD/10.0.22000.md) |

*Note: For some reason Windows 11 10.0.22000 and Windows 10 10.0.19044 are both named 21H2.

# Older Versions of windows
For Windows versions such as 10.0.19044 (21H2) and below that check this repo: [j00ru/windows-syscalls](https://github.com/j00ru/windows-syscalls "j00ru/windows-syscalls")

# How i gather these data?
The concept is very simple First, We look up the `NtDll` file for a certain `OpCode` which for `Nt` functions usually is `4C 8B D1 B8`, Then the next `8 byte` is the `syscall number`, Then we extract all those numbers in order.

# Usage
You can use data from this table to do a direct system call, And skipping the call from ntdll and bypass Edr and hooking accordingly.


# Credits
[@j00ru](https://github.com/j00ru "@j00ru")
