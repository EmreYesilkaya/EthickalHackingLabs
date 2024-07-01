# Ethical Hacking Technologies
## Lab Work 3: Malware Activity Analysis

**Student: Emre Yesilkaya**

### Resources and Tools
- Memory (RAM) dump image; raw file.
- Volatility - working memory (RAM) analysis software ([Volatility Foundation](https://www.volatilityfoundation.org/releases)).
- Any other software or tools can be used.

### Evaluation of Results

| Assessment                           | Possible Maximum Evaluation | Subject                            | Comments                               |
|--------------------------------------|-----------------------------|------------------------------------|----------------------------------------|
| 8                                    | Gathered information about the main activities of malware | PID, IP, session, ports | |
| 2                                    | Malicious code was analyzed  | Malicious code process analysis was performed | |
| 10                                   |                             |                                    |                                        |

### Using Cybercrime Investigation Tools

1. **Can you identify the exact date and time (time must be in your time zone) when the memory dump was made?**

   | Title (image) | Data         | Time                  |
   |---------------|--------------|-----------------------|
   | SystemTime    | 2020-10-19   | 12:30:45              |

2. **Can you identify the operating system from the working memory image?**

   | Title (image)                  | Operating System or Family |
   |--------------------------------|-----------------------------|
   | "NTBuildLab" and "NtSystemRoot"| Windows 7 SP1               |

3. **Can you provide information about the number of processors or cores (CPU Core)?**

   | Title (image)      | CPU Core |
   |--------------------|----------|
   | KeNumberProcessors | 2        |

4. **Can you identify the date and time of launch of applications linked to cloud services (data caches) on the memory image (the time must be in your time zone)?**

   | Title (programmes)                | Date of Launch | Start-up Time         |
   |-----------------------------------|----------------|-----------------------|
   | C:\Program Files\Nextcloud\nextcloud.exe pstree | 2020-10-18 | 2020-10-18 11:30:46 |

5. **Can you identify the date and time of the start of the application that was used for email on the memory image (the time must be based on your time zone)?**

   | Title (program’s) | Date of Launch         | Start-up Time                        |
   |-------------------|------------------------|--------------------------------------|
   | firefox.exe       | 2020-10-18 11:30:52    | İlk Oturum: 2020-10-18 11:30:52 (Çıkış Zamanı: 2020-10-18 11:31:09) |
   |                   |                        | İkinci Oturum: 2020-10-19 09:32:17 (Çıkış Zamanı: 2020-10-19 09:57:56) |

6. **Can you identify on the memory image where or which (possible) e-mail is read by the user?**

   | Title (program’s) | IP Address Port   | Note                                  |
   |-------------------|-------------------|---------------------------------------|
   | tor               | 127.0.0.1 9050    | Not sure                              |

7. **Can you determine what the partitions are and/or what encrypted partitions ("partitions") have been mounted?**

   | Title (section)                  | Connected from... | Connected to                       | Note (if necessary to clarify the title of the section)  |
   |----------------------------------|-------------------|------------------------------------|---------------------------------------------------------|
   | @WanaDecryptor@.exe              | MACHINE\SOFTWARE\MICROSOFT\WINDOWS NT\CURRENTVERSION\IMAGE FILE EXECUTION OPTIONS | \Device\HarddiskVolume2\Users\Administrator\Nextcloud\Documents (2) | |

8. **Can you list the software (at least 5) that the computer user may have used in the process of outputting the files?**

   | Eil. No. | Name (software)       | Evidence                                                                                                        | Note (if necessary to explain the choice)                |
   |----------|-----------------------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------|
   | 1        | Explorer.exe          | Running as explorer.exe with PIDs such as 2752 and 3320.                                                        | Explorer is directly involved in file manipulation—creating, deleting, and moving files within the operating system essential for any file output operations. |
   | 2        | Nextcloud.exe         | Running as nextcloud.exe with PID 3612.                                                                         | This is a cloud synchronization tool which often involves downloading and uploading files, thus handling file outputs especially in sync operations. |
   | 3        | Qemu-ga.exe           | Running as "C:\Program Files\Qemu-ga\qemu-ga.exe" with PID 1288.                                                | Facilitates integration between host and guest systems in a virtual environment, which may include file transfer operations. |
   | 4        | Spoolsv.exe           | Running as C:\Windows\System32\spoolsv.exe with PID 264.                                                        | This is the print spooler service that manages printing jobs directly involved in outputting documents to printers. |
   | 5        | Wmpnetwk.exe          | Running as "C:\Program Files\Windows Media Player\wmpnetwk.exe" with PID 2612.                                   | Handles media streaming and sharing; involved in outputting media files across network locations. |

9. **Can you determine the IP address assigned to the computer (please make a note where this assumption is made)?**

   | IP address  | Note           |
   |-------------|----------------|
   | 10.10.15.8  |                |

10. **Can you identify the information of the libraries (1-3) in the image?**

   | Name (file)   | Name (Companies that created the library) | File version  | Product version |
   |---------------|--------------------------------------------|---------------|-----------------|
   | Qt5Gui.dll    | The Qt Company Ltd.                        | n/a           | n/a             |
   | CRYPT32.dll   | Microsoft Corporation                      |               |                 |
   | IPHLPAPI.DLL  | IPHLPAPI.DLL                               |               |                 |

11. **Can you determine what software took the image of the memory and when (the time must be in your time zone)?**

   | Title (program) | Data   | Time   |
   |-----------------|--------|--------|
   | Win32.exe       | Not sure | Not sure |

### Conclusion

This lab focused on analyzing malware activity using memory dump images and Volatility software. The primary tasks included identifying the operating system, determining process details, and understanding the impact of malicious software on the system. The findings provide a detailed view of how malware operates and interacts with system resources, aiding in the development of effective countermeasures.

---

