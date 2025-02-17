---
created: 2025-02-10T09:49
updated: 2025-02-10T10:30
---
comment de réparation Windows

**cmd admin:**
___
*sfc /scannow && DISM /Online /Cleanup-Image /CheckHealth && DISM /Online /Cleanup-Image /ScanHealth && DISM /Online /Cleanup-Image /RestoreHealth && DISM /Online /Cleanup-Image /StartComponentCleanup && sfc /scannow && shutdown /r /t 0*
___


