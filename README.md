# openGL-error
Having an OpenGL: ~~ERROR~~ RuntimeException: No OpenGL context found in the current thread
---- Minecraft Crash Report ----
// My bad.

Time: 9/25/18 6:41 AM
Description: Initializing game

org.lwjgl.LWJGLException: Pixel format not accelerated
	at org.lwjgl.opengl.WindowsPeerInfo.nChoosePixelFormat(Native Method)
	at org.lwjgl.opengl.WindowsPeerInfo.choosePixelFormat(WindowsPeerInfo.java:52)
	at org.lwjgl.opengl.WindowsDisplay.createWindow(WindowsDisplay.java:247)
	at org.lwjgl.opengl.Display.createWindow(Display.java:306)
	at org.lwjgl.opengl.Display.create(Display.java:848)
	at org.lwjgl.opengl.Display.create(Display.java:757)
	at org.lwjgl.opengl.Display.create(Display.java:739)
	at bcx.ap(SourceFile:598)
	at bcx.an(SourceFile:434)
	at bcx.a(SourceFile:381)
	at net.minecraft.client.main.Main.main(SourceFile:124)


A detailed walkthrough of the error, its code path and all known details is as follows:
---------------------------------------------------------------------------------------

-- Head --
Thread: Client thread
Stacktrace:
	at org.lwjgl.opengl.WindowsPeerInfo.nChoosePixelFormat(Native Method)
	at org.lwjgl.opengl.WindowsPeerInfo.choosePixelFormat(WindowsPeerInfo.java:52)
	at org.lwjgl.opengl.WindowsDisplay.createWindow(WindowsDisplay.java:247)
	at org.lwjgl.opengl.Display.createWindow(Display.java:306)
	at org.lwjgl.opengl.Display.create(Display.java:848)
	at org.lwjgl.opengl.Display.create(Display.java:757)
	at org.lwjgl.opengl.Display.create(Display.java:739)
	at bcx.ap(SourceFile:598)
	at bcx.an(SourceFile:434)

-- Initialization --
Details:
Stacktrace:
	at bcx.a(SourceFile:381)
	at net.minecraft.client.main.Main.main(SourceFile:124)

-- System Details --
Details:
	Minecraft Version: 1.10.2
	Operating System: Windows 7 (amd64) version 6.1
	Java Version: 1.8.0_181, Oracle Corporation
	Java VM Version: Java HotSpot(TM) 64-Bit Server VM (mixed mode), Oracle Corporation
	Memory: 157958688 bytes (150 MB) / 255066112 bytes (243 MB) up to 8576565248 bytes (8179 MB)
	JVM Flags: 6 total; -XX:HeapDumpPath=MojangTricksIntelDriversForPerformance_javaw.exe_minecraft.exe.heapdump -Xmx8G -XX:+UseConcMarkSweepGC -XX:+CMSIncrementalMode -XX:-UseAdaptiveSizePolicy -Xmn128M
	IntCache: cache: 0, tcache: 0, allocated: 0, tallocated: 0
	Launched Version: 1.10.2
	LWJGL: 2.9.4
	OpenGL: ~~ERROR~~ RuntimeException: No OpenGL context found in the current thread.
	GL Caps: 
	Using VBOs: Yes
	Is Modded: Probably not. Jar signature remains and client brand is untouched.
	Type: Client (map_client.txt)
	Resource Packs: 
	Current Language: ~~ERROR~~ NullPointerException: null
	Profiler Position: N/A (disabled)
	CPU: <unknown>
  
  Below is also my dxdiag log. All my Drivers are up to date, Newest version of Java...I'm at a loss
  
  ------------------
System Information
------------------
Time of this report: 9/25/2018, 06:44:18
       Machine name: OWNER7-PC
   Operating System: Windows 7 Home Premium 64-bit (6.1, Build 7601) Service Pack 1 (7601.win7sp1_ldr_escrow.180815-1700)
           Language: English (Regional Setting: English)
System Manufacturer: Hewlett-Packard
       System Model: p6837c
               BIOS: BIOS Date: 12/28/11 19:32:03 Ver: 6.11
          Processor: AMD Athlon(tm) II X4 645 Processor (4 CPUs), ~3.1GHz
             Memory: 18432MB RAM
Available OS Memory: 16384MB RAM
          Page File: 3541MB used, 29225MB available
        Windows Dir: C:\Windows
    DirectX Version: DirectX 11
DX Setup Parameters: Not found
   User DPI Setting: Using System DPI
 System DPI Setting: 96 DPI (100 percent)
    DWM DPI Scaling: Disabled
     DxDiag Version: 6.01.7601.17514 64bit Unicode

------------
DxDiag Notes
------------
      Display Tab 1: No problems found.
        Sound Tab 1: No problems found.
        Sound Tab 2: No problems found.
          Input Tab: No problems found.

--------------------
DirectX Debug Levels
--------------------
Direct3D:    0/4 (retail)
DirectDraw:  0/4 (retail)
DirectInput: 0/5 (retail)
DirectMusic: 0/5 (retail)
DirectPlay:  0/9 (retail)
DirectSound: 0/5 (retail)
DirectShow:  0/6 (retail)

---------------
Display Devices
---------------
          Card name: 
       Manufacturer: 
          Chip type: 
           DAC type: 
         Device Key: Enum\
     Display Memory: n/a
   Dedicated Memory: n/a
      Shared Memory: n/a
       Current Mode: 1600 x 1200 (32 bit) (1Hz)
        Driver Name: 
Driver File Version:  ()
     Driver Version: 
        DDI Version: unknown
       Driver Model: unknown
  Driver Attributes: Final Retail
   Driver Date/Size: , 0 bytes
        WHQL Logo'd: n/a
    WHQL Date Stamp: n/a
  Device Identifier: {D7B70EE0-4340-11CF-B123-B03DAEC2CB35}
          Vendor ID: 0x0000
          Device ID: 0x0000
          SubSys ID: 0x00000000
        Revision ID: 0x0000
 Driver Strong Name: Unknown
     Rank Of Driver: Unknown
        Video Accel: 
      Deinterlace Caps: n/a
       D3D9 Overlay: n/a
            DXVA-HD: n/a
       DDraw Status: Not Available
         D3D Status: Not Available
         AGP Status: Not Available

-------------
Sound Devices
-------------
            Description: Headphones (2- Razer Kraken USB)
 Default Sound Playback: Yes
 Default Voice Playback: Yes
            Hardware ID: USB\VID_1532&PID_0502&REV_0100&MI_00
        Manufacturer ID: 65535
             Product ID: 65535
                   Type: WDM
            Driver Name: USBAUDIO.sys
         Driver Version: 6.01.7601.18208 (English)
      Driver Attributes: Final Retail
            WHQL Logo'd: Yes
          Date and Size: 7/12/2013 05:40:58, 109824 bytes
            Other Files: 
        Driver Provider: Microsoft
         HW Accel Level: Basic
              Cap Flags: 0xF1F
    Min/Max Sample Rate: 100, 200000
Static/Strm HW Mix Bufs: 1, 0
 Static/Strm HW 3D Bufs: 0, 0
              HW Memory: 0
       Voice Management: No
 EAX(tm) 2.0 Listen/Src: No, No
   I3DL2(tm) Listen/Src: No, No
Sensaura(tm) ZoomFX(tm): No

            Description: Realtek Digital Output (Realtek High Definition Audio)
 Default Sound Playback: No
 Default Voice Playback: No
            Hardware ID: HDAUDIO\FUNC_01&VEN_10EC&DEV_0888&SUBSYS_103C2AB1&REV_1003
        Manufacturer ID: 1
             Product ID: 100
                   Type: WDM
            Driver Name: RTKVHD64.sys
         Driver Version: 6.00.0001.6196 (English)
      Driver Attributes: Final Retail
            WHQL Logo'd: Yes
          Date and Size: 9/7/2010 11:27:34, 2484072 bytes
            Other Files: 
        Driver Provider: Realtek Semiconductor Corp.
         HW Accel Level: Basic
              Cap Flags: 0xF1F
    Min/Max Sample Rate: 100, 200000
Static/Strm HW Mix Bufs: 1, 0
 Static/Strm HW 3D Bufs: 0, 0
              HW Memory: 0
       Voice Management: No
 EAX(tm) 2.0 Listen/Src: No, No
   I3DL2(tm) Listen/Src: No, No
Sensaura(tm) ZoomFX(tm): No

---------------------
Sound Capture Devices
---------------------
            Description: Microphone (2- Razer Kraken USB)
  Default Sound Capture: Yes
  Default Voice Capture: Yes
            Driver Name: USBAUDIO.sys
         Driver Version: 6.01.7601.18208 (English)
      Driver Attributes: Final Retail
          Date and Size: 7/12/2013 05:40:58, 109824 bytes
              Cap Flags: 0x1
           Format Flags: 0xFFFFF

-------------------
DirectInput Devices
-------------------
      Device Name: Mouse
         Attached: 1
    Controller ID: n/a
Vendor/Product ID: n/a
        FF Driver: n/a

      Device Name: Keyboard
         Attached: 1
    Controller ID: n/a
Vendor/Product ID: n/a
        FF Driver: n/a

      Device Name: Razer Kraken USB
         Attached: 1
    Controller ID: 0x0
Vendor/Product ID: 0x1532, 0x0502
        FF Driver: n/a

      Device Name: USB KEYBOARD
         Attached: 1
    Controller ID: 0x0
Vendor/Product ID: 0x258A, 0x0001
        FF Driver: n/a

      Device Name: USB KEYBOARD
         Attached: 1
    Controller ID: 0x0
Vendor/Product ID: 0x258A, 0x0001
        FF Driver: n/a

Poll w/ Interrupt: No

-----------
USB Devices
-----------
+ USB Root Hub
| Vendor/Product ID: 0x1002, 0x4397
| Matching Device ID: usb\root_hub
| Service: usbhub
| Driver: usbhub.sys, 5/2/2018 10:32:58, 344064 bytes
| Driver: usbd.sys, 7/13/2009 19:06:23, 7936 bytes

----------------
Gameport Devices
----------------

------------
PS/2 Devices
------------
+ HID Keyboard Device
| Vendor/Product ID: 0x258A, 0x0001
| Matching Device ID: hid_device_system_keyboard
| Service: kbdhid
| Driver: kbdhid.sys, 11/20/2010 22:23:47, 33280 bytes
| Driver: kbdclass.sys, 7/13/2009 20:48:04, 50768 bytes
| 
+ Terminal Server Keyboard Driver
| Matching Device ID: root\rdp_kbd
| Upper Filters: kbdclass
| Service: TermDD
| Driver: i8042prt.sys, 7/13/2009 18:19:57, 105472 bytes
| Driver: kbdclass.sys, 7/13/2009 20:48:04, 50768 bytes
| 
+ HID-compliant mouse
| Vendor/Product ID: 0x0461, 0x4E23
| Matching Device ID: hid_device_system_mouse
| Service: mouhid
| Driver: mouhid.sys, 7/13/2009 19:00:20, 31232 bytes
| Driver: mouclass.sys, 7/13/2009 20:48:27, 49216 bytes
| 
+ Terminal Server Mouse Driver
| Matching Device ID: root\rdp_mou
| Upper Filters: mouclass
| Service: TermDD
| Driver: termdd.sys, 2/10/2018 13:35:42, 63168 bytes
| Driver: sermouse.sys, 7/13/2009 19:00:20, 26624 bytes
| Driver: mouclass.sys, 7/13/2009 20:48:27, 49216 bytes

------------------------
Disk & DVD/CD-ROM Drives
------------------------
      Drive: C:
 Free Space: 595.5 GB
Total Space: 953.8 GB
File System: NTFS
      Model: ST1000DM 003-1CH162 SATA Disk Device

      Drive: Q:
      Model: n/a

      Drive: D:
      Model: hp DVD A  DH16ABLH SATA CdRom Device
     Driver: c:\windows\system32\drivers\cdrom.sys, 6.01.7601.17514 (English), 11/20/2010 22:23:47, 147456 bytes

--------------
System Devices
--------------
     Name: PCI standard PCI-to-PCI bridge
Device ID: PCI\VEN_1022&DEV_9609&SUBSYS_2AB1103C&REV_00\3&267A616A&0&50
   Driver: C:\Windows\system32\DRIVERS\pci.sys, 6.01.7601.24056 (English), 2/10/2018 13:35:41, 185024 bytes

     Name: PCI standard host CPU bridge
Device ID: PCI\VEN_1022&DEV_1200&SUBSYS_00000000&REV_00\3&267A616A&0&C0
   Driver: n/a

     Name: Standard Enhanced PCI to USB Host Controller
Device ID: PCI\VEN_1002&DEV_4396&SUBSYS_2AB1103C&REV_00\3&267A616A&0&92
   Driver: C:\Windows\system32\drivers\usbehci.sys, 6.01.7601.17514 (English), 11/20/2010 22:23:47, 52224 bytes
   Driver: C:\Windows\system32\drivers\usbport.sys, 6.01.7601.17514 (English), 11/20/2010 22:23:47, 325120 bytes
   Driver: C:\Windows\system32\drivers\usbhub.sys, 6.01.7601.24138 (English), 5/2/2018 10:32:58, 344064 bytes

     Name: PCI standard PCI-to-PCI bridge
Device ID: PCI\VEN_1022&DEV_9603&SUBSYS_2AB1103C&REV_00\3&267A616A&0&10
   Driver: C:\Windows\system32\DRIVERS\pci.sys, 6.01.7601.24056 (English), 2/10/2018 13:35:41, 185024 bytes

     Name: AMD SATA Controller
Device ID: PCI\VEN_1002&DEV_4391&SUBSYS_2AB1103C&REV_00\3&267A616A&0&88
   Driver: C:\Windows\system32\DRIVERS\amd_sata.sys, 1.02.0001.0337 (English), 3/31/2013 18:32:04, 82600 bytes
   Driver: C:\Windows\system32\DRIVERS\amd_xata.sys, 1.02.0001.0337 (English), 3/31/2013 18:32:04, 42664 bytes

     Name: PCI standard ISA bridge
Device ID: PCI\VEN_1002&DEV_439D&SUBSYS_2AB1103C&REV_00\3&267A616A&0&A3
   Driver: C:\Windows\system32\DRIVERS\msisadrv.sys, 6.01.7601.24056 (English), 2/10/2018 13:35:40, 15040 bytes

     Name: AMD SMBus
Device ID: PCI\VEN_1002&DEV_4385&SUBSYS_2AB1103C&REV_3C\3&267A616A&0&A0
   Driver: n/a

     Name: PCI standard host CPU bridge
Device ID: PCI\VEN_1022&DEV_9601&SUBSYS_2AB1103C&REV_00\3&267A616A&0&00
   Driver: n/a

     Name: Standard OpenHCD USB Host Controller
Device ID: PCI\VEN_1002&DEV_4398&SUBSYS_2AB1103C&REV_00\3&267A616A&0&99
   Driver: C:\Windows\system32\drivers\usbohci.sys, 6.01.7600.16385 (English), 7/13/2009 19:06:30, 25600 bytes
   Driver: C:\Windows\system32\drivers\usbport.sys, 6.01.7601.17514 (English), 11/20/2010 22:23:47, 325120 bytes
   Driver: C:\Windows\system32\drivers\usbhub.sys, 6.01.7601.24138 (English), 5/2/2018 10:32:58, 344064 bytes

     Name: ATI I/O Communications Processor PCI Bus Controller
Device ID: PCI\VEN_1002&DEV_4384&SUBSYS_00000000&REV_00\3&267A616A&0&A4
   Driver: C:\Windows\system32\DRIVERS\pci.sys, 6.01.7601.24056 (English), 2/10/2018 13:35:41, 185024 bytes

     Name: PCI standard host CPU bridge
Device ID: PCI\VEN_1022&DEV_1204&SUBSYS_00000000&REV_00\3&267A616A&0&C4
   Driver: n/a

     Name: Standard OpenHCD USB Host Controller
Device ID: PCI\VEN_1002&DEV_4398&SUBSYS_2AB1103C&REV_00\3&267A616A&0&91
   Driver: C:\Windows\system32\drivers\usbohci.sys, 6.01.7600.16385 (English), 7/13/2009 19:06:30, 25600 bytes
   Driver: C:\Windows\system32\drivers\usbport.sys, 6.01.7601.17514 (English), 11/20/2010 22:23:47, 325120 bytes
   Driver: C:\Windows\system32\drivers\usbhub.sys, 6.01.7601.24138 (English), 5/2/2018 10:32:58, 344064 bytes

     Name: High Definition Audio Controller
Device ID: PCI\VEN_1002&DEV_4383&SUBSYS_2AB1103C&REV_00\3&267A616A&0&A2
   Driver: C:\Windows\system32\DRIVERS\hdaudbus.sys, 6.01.7601.17514 (English), 11/20/2010 22:23:47, 122368 bytes

     Name: Realtek PCIe FE Family Controller
Device ID: PCI\VEN_10EC&DEV_8136&SUBSYS_2AB1103C&REV_05\4&C011167&0&0050
   Driver: n/a

     Name: PCI standard host CPU bridge
Device ID: PCI\VEN_1022&DEV_1203&SUBSYS_00000000&REV_00\3&267A616A&0&C3
   Driver: n/a

     Name: Standard OpenHCD USB Host Controller
Device ID: PCI\VEN_1002&DEV_4397&SUBSYS_2AB1103C&REV_00\3&267A616A&0&98
   Driver: C:\Windows\system32\drivers\usbohci.sys, 6.01.7600.16385 (English), 7/13/2009 19:06:30, 25600 bytes
   Driver: C:\Windows\system32\drivers\usbport.sys, 6.01.7601.17514 (English), 11/20/2010 22:23:47, 325120 bytes
   Driver: C:\Windows\system32\drivers\usbhub.sys, 6.01.7601.24138 (English), 5/2/2018 10:32:58, 344064 bytes

     Name: NVIDIA GeForce GTX 1050 Ti
Device ID: PCI\VEN_10DE&DEV_1C82&SUBSYS_219010DE&REV_A1\4&3527B13C&0&0010
   Driver: C:\Windows\system32\DRIVERS\NVIDIA Corporation\Drs\dbInstaller.exe, 24.21.0014.1163 (English), 9/19/2018 08:29:48, 723912 bytes
   Driver: C:\Windows\system32\DRIVERS\NVIDIA Corporation\Drs\nvdrsdb.bin, 9/18/2018 16:15:58, 1532700 bytes
   Driver: C:\Windows\System32\DriverStore\FileRepository\nv_dispi.inf_amd64_neutral_091e78abaaa811b5\NvContainerSetup.exe, 1.00.0007.0000 (English), 9/19/2018 08:30:24, 4438960 bytes
   Driver: C:\Windows\System32\DriverStore\FileRepository\nv_dispi.inf_amd64_neutral_091e78abaaa811b5\NvCplSetupInt.exe, 1.00.0007.0000 (English), 9/19/2018 08:30:26, 101349560 bytes
   Driver: C:\Program Files (x86)\NVIDIA Corporation\coprocmanager\detoured.dll, 2.01.0000.0224 (English), 9/19/2018 08:30:30, 29232 bytes
   Driver: C:\Program Files (x86)\NVIDIA Corporation\coprocmanager\nvd3d9wrap.dll, 24.21.0014.1163 (English), 9/19/2018 08:29:18, 191224 bytes
   Driver: C:\Program Files (x86)\NVIDIA Corporation\coprocmanager\nvdxgiwrap.dll, 24.21.0014.1163 (English), 9/19/2018 08:29:30, 125048 bytes
   Driver: C:\Program Files\NVIDIA Corporation\coprocmanager\detoured.dll, 2.01.0000.0224 (English), 9/19/2018 08:30:30, 29232 bytes
   Driver: C:\Program Files\NVIDIA Corporation\coprocmanager\nvd3d9wrapx.dll, 24.21.0014.1163 (English), 9/19/2018 08:29:18, 221528 bytes
   Driver: C:\Program Files\NVIDIA Corporation\coprocmanager\nvdxgiwrapx.dll, 24.21.0014.1163 (English), 9/19/2018 08:29:32, 145584 bytes
   Driver: C:\Windows\system32\unknown\DisplayDriverRAS.dll, 1.10.0000.0000 (English), 9/19/2018 08:29:48, 868296 bytes
   Driver: C:\Program Files\NVIDIA Corporation\license.txt, 9/18/2018 16:15:58, 27203 bytes
   Driver: C:\Program Files\NVIDIA Corporation\nvgsync\detoured.dll, 2.01.0000.0224 (English), 9/19/2018 08:30:30, 29232 bytes
   Driver: C:\Program Files\NVIDIA Corporation\nvgsync\nvgsyncdetours.dll, 9/19/2018 08:30:36, 163000 bytes
   Driver: C:\Program Files\NVIDIA Corporation\NVSMI\MCU.exe, 1.01.5204.20580 (English), 9/19/2018 08:29:58, 858568 bytes
   Driver: C:\Program Files\NVIDIA Corporation\NVSMI\nvdebugdump.exe, 6.14.0014.1163 (English), 9/19/2018 08:30:30, 429152 bytes
   Driver: C:\Program Files\NVIDIA Corporation\NVSMI\nvidia-smi.1.pdf, 9/18/2018 16:15:58, 104239 bytes
   Driver: C:\Program Files\NVIDIA Corporation\NVSMI\nvidia-smi.exe, 8.17.0014.1163 (English), 9/19/2018 08:30:40, 538032 bytes
   Driver: C:\Program Files\NVIDIA Corporation\NVSMI\nvml.dll, 8.17.0014.1163 (English), 9/19/2018 08:30:56, 949296 bytes
   Driver: C:\Windows\system32\unknown\OpenCL32.dll, 2.02.0001.0000 (English), 9/19/2018 08:31:54, 456816 bytes
   Driver: C:\Windows\system32\unknown\OpenCL64.dll, 2.02.0001.0000 (English), 9/19/2018 08:31:54, 551912 bytes
   Driver: C:\Windows\system32\DRIVERS\nvlddmkm.sys, 24.21.0014.1163 (English), 9/19/2018 08:30:52, 19918432 bytes
   Driver: C:\Windows\system32\NvFBC64.dll, 6.14.0014.1163 (English), 9/19/2018 08:30:34, 1941424 bytes
   Driver: C:\Windows\system32\NvIFR64.dll, 6.14.0014.1163 (English), 9/19/2018 08:30:48, 1444904 bytes
   Driver: C:\Windows\system32\NvIFROpenGL.dll, 24.21.0014.1163 (English), 9/19/2018 08:30:48, 628840 bytes
   Driver: C:\Windows\system32\nv-vk64.json, 9/18/2018 16:15:58, 669 bytes
   Driver: C:\Windows\system32\nvEncodeAPI64.dll, 24.21.0014.1163 (English), 9/19/2018 08:29:32, 547304 bytes
   Driver: C:\Windows\system32\nvapi64.dll, 24.21.0014.1163 (English), 9/19/2018 08:29:06, 4688208 bytes
   Driver: C:\Windows\system32\nvcbl64.dll, 24.21.0014.1163 (English), 9/19/2018 08:30:10, 489528 bytes
   Driver: C:\Windows\system32\nvcompiler.dll, 24.21.0014.1163 (English), 9/19/2018 08:30:18, 40439856 bytes
   Driver: C:\Windows\system32\nvcuda.dll, 24.21.0014.1163 (English), 9/19/2018 08:29:14, 19705336 bytes
   Driver: C:\Windows\system32\nvcuvid.dll, 7.17.0014.1163 (English), 9/19/2018 08:30:28, 4393408 bytes
   Driver: C:\Windows\system32\nvd3dumx.dll, 24.21.0014.1163 (English), 9/19/2018 08:29:24, 20893440 bytes
   Driver: C:\Windows\system32\nvfatbinaryLoader.dll, 24.21.0014.1163 (English), 9/19/2018 08:29:34, 1159896 bytes
   Driver: C:\Windows\system32\nvinfo.pb, 9/18/2018 16:15:58, 44159 bytes
   Driver: C:\Windows\system32\nvinitx.dll, 24.21.0014.1163 (English), 9/19/2018 08:29:36, 182720 bytes
   Driver: C:\Windows\system32\nvoglshim64.dll, 24.21.0014.1163 (English), 9/19/2018 08:29:40, 164888 bytes
   Driver: C:\Windows\system32\nvoglv64.dll, 24.21.0014.1163 (English), 9/19/2018 08:31:08, 39414344 bytes
   Driver: C:\Windows\system32\nvopencl.dll, 24.21.0014.1163 (English), 9/19/2018 08:29:50, 35296800 bytes
   Driver: C:\Windows\system32\nvoptix.dll, 5.02.0000.0000 (English), 9/19/2018 08:31:16, 48343240 bytes
   Driver: C:\Windows\system32\nvptxJitCompiler.dll, 24.21.0014.1163 (English), 9/19/2018 08:30:00, 15561552 bytes
   Driver: C:\Windows\system32\nvrtum64.dll, 24.21.0014.1163 (English), 9/19/2018 08:31:26, 20020752 bytes
   Driver: C:\Windows\system32\nvumdshimx.dll, 24.21.0014.1163 (English), 9/19/2018 08:30:06, 505864 bytes
   Driver: C:\Windows\system32\nvwgf2umx.dll, 24.21.0014.1163 (English), 9/19/2018 08:30:14, 28973600 bytes
   Driver: C:\Windows\system32\vulkan-1-999-0-0-0.dll, 1.01.0082.0000 (English), 9/19/2018 08:31:56, 978312 bytes
   Driver: C:\Windows\system32\vulkan-1.dll, 1.01.0082.0000 (English), 9/19/2018 08:31:56, 978312 bytes
   Driver: C:\Windows\system32\vulkaninfo-1-999-0-0-0.exe, 1.01.0082.0000 (English), 9/19/2018 08:31:56, 268168 bytes
   Driver: C:\Windows\system32\vulkaninfo.exe, 1.01.0082.0000 (English), 9/19/2018 08:31:56, 268168 bytes
   Driver: C:\Windows\SysWow64\NvFBC.dll, 6.14.0014.1163 (English), 9/19/2018 08:30:34, 1457712 bytes
   Driver: C:\Windows\SysWow64\NvIFR.dll, 6.14.0014.1163 (English), 9/19/2018 08:30:46, 1114896 bytes
   Driver: C:\Windows\SysWow64\NvIFROpenGL.dll, 24.21.0014.1163 (English), 9/19/2018 08:30:48, 519024 bytes
   Driver: C:\Windows\SysWow64\nv-vk32.json, 9/18/2018 16:15:58, 669 bytes
   Driver: C:\Windows\SysWow64\nvEncodeAPI.dll, 24.21.0014.1163 (English), 9/19/2018 08:29:32, 465328 bytes
   Driver: C:\Windows\SysWow64\nvapi.dll, 24.21.0014.1163 (English), 9/19/2018 08:29:04, 4146024 bytes
   Driver: C:\Windows\SysWow64\nvcompiler.dll, 24.21.0014.1163 (English), 9/19/2018 08:30:12, 35312736 bytes
   Driver: C:\Windows\SysWow64\nvcuda.dll, 24.21.0014.1163 (English), 9/19/2018 08:29:10, 16984120 bytes
   Driver: C:\Windows\SysWow64\nvcuvid.dll, 7.17.0014.1163 (English), 9/19/2018 08:30:26, 3926472 bytes
   Driver: C:\Windows\SysWow64\nvd3dum.dll, 24.21.0014.1163 (English), 9/19/2018 08:29:20, 17399208 bytes
   Driver: C:\Windows\SysWow64\nvfatbinaryLoader.dll, 24.21.0014.1163 (English), 9/19/2018 08:29:34, 907272 bytes
   Driver: C:\Windows\SysWow64\nvinit.dll, 24.21.0014.1163 (English), 9/19/2018 08:29:36, 160160 bytes
   Driver: C:\Windows\SysWow64\nvoglshim32.dll, 24.21.0014.1163 (English), 9/19/2018 08:29:38, 142760 bytes
   Driver: C:\Windows\SysWow64\nvoglv32.dll, 24.21.0014.1163 (English), 9/19/2018 08:31:02, 29360896 bytes
   Driver: C:\Windows\SysWow64\nvopencl.dll, 24.21.0014.1163 (English), 9/19/2018 08:29:42, 29972896 bytes
   Driver: C:\Windows\SysWow64\nvptxJitCompiler.dll, 24.21.0014.1163 (English), 9/19/2018 08:29:56, 12934264 bytes
   Driver: C:\Windows\SysWow64\nvumdshim.dll, 24.21.0014.1163 (English), 9/19/2018 08:30:04, 420120 bytes
   Driver: C:\Windows\SysWow64\nvwgf2um.dll, 24.21.0014.1163 (English), 9/19/2018 08:30:08, 25855120 bytes
   Driver: C:\Windows\SysWow64\vulkan-1-999-0-0-0.dll, 1.01.0082.0000 (English), 9/19/2018 08:31:56, 845192 bytes
   Driver: C:\Windows\SysWow64\vulkan-1.dll, 1.01.0082.0000 (English), 9/19/2018 08:31:56, 845192 bytes
   Driver: C:\Windows\SysWow64\vulkaninfo-1-999-0-0-0.exe, 1.01.0082.0000 (English), 9/19/2018 08:31:58, 243584 bytes
   Driver: C:\Windows\SysWow64\vulkaninfo.exe, 1.01.0082.0000 (English), 9/19/2018 08:31:58, 243584 bytes
   Driver: C:\Windows\system32\nvdispco6441163.dll, 2.00.0053.0004 (English), 9/19/2018 08:30:32, 2017712 bytes
   Driver: C:\Windows\system32\nvdispgenco6441163.dll, 2.00.0026.0002 (English), 9/19/2018 08:30:32, 1468352 bytes

     Name: PCI standard host CPU bridge
Device ID: PCI\VEN_1022&DEV_1202&SUBSYS_00000000&REV_00\3&267A616A&0&C2
   Driver: n/a

     Name: Standard OpenHCD USB Host Controller
Device ID: PCI\VEN_1002&DEV_4397&SUBSYS_2AB1103C&REV_00\3&267A616A&0&90
   Driver: C:\Windows\system32\drivers\usbohci.sys, 6.01.7600.16385 (English), 7/13/2009 19:06:30, 25600 bytes
   Driver: C:\Windows\system32\drivers\usbport.sys, 6.01.7601.17514 (English), 11/20/2010 22:23:47, 325120 bytes
   Driver: C:\Windows\system32\drivers\usbhub.sys, 6.01.7601.24138 (English), 5/2/2018 10:32:58, 344064 bytes

     Name: High Definition Audio Controller
Device ID: PCI\VEN_10DE&DEV_0BEE&SUBSYS_219010DE&REV_A1\4&3527B13C&0&0110
   Driver: C:\Windows\system32\DRIVERS\hdaudbus.sys, 6.01.7601.17514 (English), 11/20/2010 22:23:47, 122368 bytes

     Name: PCI standard host CPU bridge
Device ID: PCI\VEN_1022&DEV_1201&SUBSYS_00000000&REV_00\3&267A616A&0&C1
   Driver: n/a

     Name: Standard Enhanced PCI to USB Host Controller
Device ID: PCI\VEN_1002&DEV_4396&SUBSYS_2AB1103C&REV_00\3&267A616A&0&9A
   Driver: C:\Windows\system32\drivers\usbehci.sys, 6.01.7601.17514 (English), 11/20/2010 22:23:47, 52224 bytes
   Driver: C:\Windows\system32\drivers\usbport.sys, 6.01.7601.17514 (English), 11/20/2010 22:23:47, 325120 bytes
   Driver: C:\Windows\system32\drivers\usbhub.sys, 6.01.7601.24138 (English), 5/2/2018 10:32:58, 344064 bytes

------------------
DirectShow Filters
------------------

DirectShow Filters:
WMAudio Decoder DMO,0x00800800,1,1,WMADMOD.DLL,6.01.7601.19091
WMAPro over S/PDIF DMO,0x00600800,1,1,WMADMOD.DLL,6.01.7601.19091
WMSpeech Decoder DMO,0x00600800,1,1,WMSPDMOD.DLL,6.01.7601.19091
MP3 Decoder DMO,0x00600800,1,1,mp3dmod.dll,6.01.7601.19091
Mpeg4s Decoder DMO,0x00800001,1,1,mp4sdecd.dll,6.01.7601.19091
WMV Screen decoder DMO,0x00600800,1,1,wmvsdecd.dll,6.01.7601.19091
WMVideo Decoder DMO,0x00800001,1,1,wmvdecod.dll,6.01.7601.19091
Mpeg43 Decoder DMO,0x00800001,1,1,mp43decd.dll,6.01.7601.19091
Mpeg4 Decoder DMO,0x00800001,1,1,mpg4decd.dll,6.01.7601.19091
DV Muxer,0x00400000,0,0,qdv.dll,6.06.7601.17514
Color Space Converter,0x00400001,1,1,quartz.dll,6.06.7601.23709
WM ASF Reader,0x00400000,0,0,qasf.dll,12.00.7601.19091
Screen Capture filter,0x00200000,0,1,wmpsrcwp.dll,12.00.7601.17514
AVI Splitter,0x00600000,1,1,quartz.dll,6.06.7601.23709
VGA 16 Color Ditherer,0x00400000,1,1,quartz.dll,6.06.7601.23709
SBE2MediaTypeProfile,0x00200000,0,0,sbe.dll,6.06.7601.17528
Microsoft DTV-DVD Video Decoder,0x005fffff,2,4,msmpeg2vdec.dll,12.00.9200.17037
AC3 Parser Filter,0x00600000,1,1,mpg2splt.ax,6.06.7601.17528
StreamBufferSink,0x00200000,0,0,sbe.dll,6.06.7601.17528
Microsoft TV Captions Decoder,0x00200001,1,0,MSTVCapn.dll,6.01.7601.17715
MJPEG Decompressor,0x00600000,1,1,quartz.dll,6.06.7601.23709
CBVA DMO wrapper filter,0x00200000,1,1,cbva.dll,6.01.7601.17514
MPEG-I Stream Splitter,0x00600000,1,2,quartz.dll,6.06.7601.23709
SAMI (CC) Parser,0x00400000,1,1,quartz.dll,6.06.7601.23709
VBI Codec,0x00600000,1,4,VBICodec.ax,6.06.7601.17514
MPEG-2 Splitter,0x005fffff,1,0,mpg2splt.ax,6.06.7601.17528
Closed Captions Analysis Filter,0x00200000,2,5,cca.dll,6.06.7601.17514
SBE2FileScan,0x00200000,0,0,sbe.dll,6.06.7601.17528
Microsoft MPEG-2 Video Encoder,0x00200000,1,1,msmpeg2enc.dll,6.01.7601.19091
Internal Script Command Renderer,0x00800001,1,0,quartz.dll,6.06.7601.23709
MPEG Audio Decoder,0x03680001,1,1,quartz.dll,6.06.7601.23709
DV Splitter,0x00600000,1,2,qdv.dll,6.06.7601.17514
Video Mixing Renderer 9,0x00200000,1,0,quartz.dll,6.06.7601.23709
Microsoft MPEG-2 Encoder,0x00200000,2,1,msmpeg2enc.dll,6.01.7601.19091
ACM Wrapper,0x00600000,1,1,quartz.dll,6.06.7601.23709
Video Renderer,0x00800001,1,0,quartz.dll,6.06.7601.23709
MPEG-2 Video Stream Analyzer,0x00200000,0,0,sbe.dll,6.06.7601.17528
Line 21 Decoder,0x00600000,1,1,,
Video Port Manager,0x00600000,2,1,quartz.dll,6.06.7601.23709
Video Renderer,0x00400000,1,0,quartz.dll,6.06.7601.23709
VPS Decoder,0x00200000,0,0,WSTPager.ax,6.06.7601.17514
WM ASF Writer,0x00400000,0,0,qasf.dll,12.00.7601.19091
VBI Surface Allocator,0x00600000,1,1,vbisurf.ax,6.01.7601.17514
File writer,0x00200000,1,0,qcap.dll,6.06.7601.17514
iTV Data Sink,0x00600000,1,0,itvdata.dll,6.06.7601.17514
iTV Data Capture filter,0x00600000,1,1,itvdata.dll,6.06.7601.17514
DVD Navigator,0x00200000,0,3,qdvd.dll,6.06.7601.23471
Microsoft TV Subtitles Decoder,0x00200001,1,0,MSTVCapn.dll,6.01.7601.17715
Overlay Mixer2,0x00200000,1,1,,
RDP DShow Redirection Filter,0xffffffff,1,0,DShowRdpFilter.dll,
Microsoft MPEG-2 Audio Encoder,0x00200000,1,1,msmpeg2enc.dll,6.01.7601.19091
WST Pager,0x00200000,1,1,WSTPager.ax,6.06.7601.17514
MPEG-2 Demultiplexer,0x00600000,1,1,mpg2splt.ax,6.06.7601.17528
DV Video Decoder,0x00800000,1,1,qdv.dll,6.06.7601.17514
SampleGrabber,0x00200000,1,1,qedit.dll,6.06.7601.19091
Null Renderer,0x00200000,1,0,qedit.dll,6.06.7601.19091
MPEG-2 Sections and Tables,0x005fffff,1,0,Mpeg2Data.ax,6.06.7601.17514
Microsoft AC3 Encoder,0x00200000,1,1,msac3enc.dll,6.01.7601.17514
StreamBufferSource,0x00200000,0,0,sbe.dll,6.06.7601.17528
Smart Tee,0x00200000,1,2,qcap.dll,6.06.7601.17514
Overlay Mixer,0x00200000,0,0,,
AVI Decompressor,0x00600000,1,1,quartz.dll,6.06.7601.23709
NetBridge,0x00200000,2,0,netbridge.dll,6.01.7601.17514
AVI/WAV File Source,0x00400000,0,2,quartz.dll,6.06.7601.23709
Wave Parser,0x00400000,1,1,quartz.dll,6.06.7601.23709
MIDI Parser,0x00400000,1,1,quartz.dll,6.06.7601.23709
Multi-file Parser,0x00400000,1,1,quartz.dll,6.06.7601.23709
File stream renderer,0x00400000,1,1,quartz.dll,6.06.7601.23709
Microsoft DTV-DVD Audio Decoder,0x005fffff,1,1,msmpeg2adec.dll,6.01.7601.23285
StreamBufferSink2,0x00200000,0,0,sbe.dll,6.06.7601.17528
AVI Mux,0x00200000,1,0,qcap.dll,6.06.7601.17514
Line 21 Decoder 2,0x00600002,1,1,quartz.dll,6.06.7601.23709
File Source (Async.),0x00400000,0,1,quartz.dll,6.06.7601.23709
File Source (URL),0x00400000,0,1,quartz.dll,6.06.7601.23709
Media Center Extender Encryption Filter,0x00200000,2,2,Mcx2Filter.dll,6.01.7601.17514
AudioRecorder WAV Dest,0x00200000,0,0,WavDest.dll,
AudioRecorder Wave Form,0x00200000,0,0,WavDest.dll,
SoundRecorder Null Renderer,0x00200000,0,0,WavDest.dll,
Infinite Pin Tee Filter,0x00200000,1,1,qcap.dll,6.06.7601.17514
Enhanced Video Renderer,0x00200000,1,0,evr.dll,6.01.7601.23471
BDA MPEG2 Transport Information Filter,0x00200000,2,0,psisrndr.ax,6.06.7601.17669
MPEG Video Decoder,0x40000001,1,1,quartz.dll,6.06.7601.23709

WDM Streaming Tee/Splitter Devices:
Tee/Sink-to-Sink Converter,0x00200000,1,1,ksproxy.ax,6.01.7601.19091

Video Compressors:
WMVideo8 Encoder DMO,0x00600800,1,1,wmvxencd.dll,6.01.7601.19091
WMVideo9 Encoder DMO,0x00600800,1,1,wmvencod.dll,6.01.7601.19091
MSScreen 9 encoder DMO,0x00600800,1,1,wmvsencd.dll,6.01.7601.19091
DV Video Encoder,0x00200000,0,0,qdv.dll,6.06.7601.17514
MJPEG Compressor,0x00200000,0,0,quartz.dll,6.06.7601.23709

Audio Compressors:
WM Speech Encoder DMO,0x00600800,1,1,WMSPDMOE.DLL,6.01.7601.19091
WMAudio Encoder DMO,0x00600800,1,1,WMADMOE.DLL,6.01.7601.19091
IMA ADPCM,0x00200000,1,1,quartz.dll,6.06.7601.23709
PCM,0x00200000,1,1,quartz.dll,6.06.7601.23709
Microsoft ADPCM,0x00200000,1,1,quartz.dll,6.06.7601.23709
GSM 6.10,0x00200000,1,1,quartz.dll,6.06.7601.23709
CCITT A-Law,0x00200000,1,1,quartz.dll,6.06.7601.23709
CCITT u-Law,0x00200000,1,1,quartz.dll,6.06.7601.23709
MPEG Layer-3,0x00200000,1,1,quartz.dll,6.06.7601.23709

Audio Capture Sources:
Microphone (2- Razer Kraken USB,0x00200000,0,0,qcap.dll,6.06.7601.17514

PBDA CP Filters:
PBDA DTFilter,0x00600000,1,1,CPFilters.dll,6.06.7601.19135
PBDA ETFilter,0x00200000,0,0,CPFilters.dll,6.06.7601.19135
PBDA PTFilter,0x00200000,0,0,CPFilters.dll,6.06.7601.19135

Midi Renderers:
Default MidiOut Device,0x00800000,1,0,quartz.dll,6.06.7601.23709
Microsoft GS Wavetable Synth,0x00200000,1,0,quartz.dll,6.06.7601.23709

WDM Streaming Capture Devices:
Realtek HD Audio Line input,0x00200000,1,1,ksproxy.ax,6.01.7601.19091
Realtek HD Audio Mic input,0x00200000,1,1,ksproxy.ax,6.01.7601.19091
Realtek HD Audio Stereo input,0x00200000,1,1,ksproxy.ax,6.01.7601.19091
Razer Kraken USB,0x00200000,2,2,ksproxy.ax,6.01.7601.19091

WDM Streaming Rendering Devices:
Realtek HD Audio front output,0x00200000,1,1,ksproxy.ax,6.01.7601.19091
Realtek HD Audio rear output,0x00200000,1,1,ksproxy.ax,6.01.7601.19091
Realtek HDA SPDIF Out,0x00200000,1,1,ksproxy.ax,6.01.7601.19091
Razer Kraken USB,0x00200000,2,2,ksproxy.ax,6.01.7601.19091

BDA Network Providers:
Microsoft ATSC Network Provider,0x00200000,0,1,MSDvbNP.ax,6.06.7601.17514
Microsoft DVBC Network Provider,0x00200000,0,1,MSDvbNP.ax,6.06.7601.17514
Microsoft DVBS Network Provider,0x00200000,0,1,MSDvbNP.ax,6.06.7601.17514
Microsoft DVBT Network Provider,0x00200000,0,1,MSDvbNP.ax,6.06.7601.17514
Microsoft Network Provider,0x00200000,0,1,MSNP.ax,6.06.7601.17514

Multi-Instance Capable VBI Codecs:
VBI Codec,0x00600000,1,4,VBICodec.ax,6.06.7601.17514

BDA Transport Information Renderers:
BDA MPEG2 Transport Information Filter,0x00600000,2,0,psisrndr.ax,6.06.7601.17669
MPEG-2 Sections and Tables,0x00600000,1,0,Mpeg2Data.ax,6.06.7601.17514

BDA CP/CA Filters:
Decrypt/Tag,0x00600000,1,1,EncDec.dll,6.06.7601.19135
Encrypt/Tag,0x00200000,0,0,EncDec.dll,6.06.7601.19135
PTFilter,0x00200000,0,0,EncDec.dll,6.06.7601.19135
XDS Codec,0x00200000,0,0,EncDec.dll,6.06.7601.19135

WDM Streaming Communication Transforms:
Tee/Sink-to-Sink Converter,0x00200000,1,1,ksproxy.ax,6.01.7601.19091

Audio Renderers:
Headphones (2- Razer Kraken USB,0x00200000,1,0,quartz.dll,6.06.7601.23709
Default DirectSound Device,0x00800000,1,0,quartz.dll,6.06.7601.23709
Default WaveOut Device,0x00200000,1,0,quartz.dll,6.06.7601.23709
DirectSound: Headphones (2- Razer Kraken USB),0x00200000,1,0,quartz.dll,6.06.7601.23709
DirectSound: Realtek Digital Output (Realtek High Definition Audio),0x00200000,1,0,quartz.dll,6.06.7601.23709
Realtek Digital Output (Realtek,0x00200000,1,0,quartz.dll,6.06.7601.23709

---------------
EVR Power Information
---------------
Current Setting: {5C67A112-A4C9-483F-B4A7-1D473BECAFDC} (Quality) 
  Quality Flags: 2576
    Enabled:
    Force throttling
    Allow half deinterlace
    Allow scaling
    Decode Power Usage: 100
  Balanced Flags: 1424
    Enabled:
    Force throttling
    Allow batching
    Force half deinterlace
    Force scaling
    Decode Power Usage: 50
  PowerFlags: 1424
    Enabled:
    Force throttling
    Allow batching
    Force half deinterlace
    Force scaling
    Decode Power Usage: 0
