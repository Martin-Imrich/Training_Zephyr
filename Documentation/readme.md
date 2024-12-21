.venv

C:\Users\urimrm\.mcuxpressotools\

Directory: C:\NXP
Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
d-----        25.11.2024      9:58                LinkServer_24.9.75
d-----        25.11.2024      9:58                LPCScrypt_2.1.3_83
d-----        25.11.2024      9:58                MCU-LINK_installer_3.148

Directory: C:\Users\urimrm\AppData\Local\Programs\MCUXpressoInstaller\.cache
Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
d-----        25.11.2024     19:15                dtc-1.6.1-3-x86_64.pkg
d-----        25.11.2024     19:16                gcc-libs-13.2.0-2-x86_64.pkg
d-----        25.11.2024     19:17                libyaml-0.2.5-2-x86_64.pkg
d-----        25.11.2024     19:13                msys2-runtime-3.4.9-3-x86_64
...

Directory: C:\Users\urimrm\.mcuxpressotools
Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
d-----        25.11.2024     19:26                .venv
d-----        25.11.2024      9:53                debug_common
d-----        25.11.2024      9:52                dtc-msys2
d-----        25.11.2024      9:52                gperf
d-----        25.11.2024      9:52                ninja
d-----        25.11.2024      9:52                wget

## Cloning Repositories

git clone https://github.com/nxp-mcuxpresso/mcux-sdk.git
git clone https://github.com/zephyrproject-rtos/zephyr.git
git branch oooor git status
- should be main

``` C:\Users\urimrm\.mcuxpressotools\.venv\Scripts\activate.bat ```
``` python -m west init -m https://github.com/NXP-mcuxpresso/mcux-sdk --mr main c:\Users\urimrm\Projekty\Training\ZephyrRTOS\mcux-sdk ```

``` python -m west init -m https://github.com/zephyrproject-rtos/zephyr --mr main c:\Users\urimrm\Projekty\Training\ZephyrRTOS\zephyr ```

python -m west init: This runs the west tool using Python's -m option, which allows you to run a module as a script.
-m https://github.com/NXP-mcuxpresso/mcux-sdk: This specifies the URL of the manifest repository to initialize.
--mr main: This specifies the manifest revision to use, in this case, the main branch.
c:\Users\urimrm\Projekty\Training\ZephyrRTOS\mcux-sdk: This is the directory where the west tool will initialize the project.

Access is denied: 'c:\\Users\\urimrm\\Projekty\\Training\\ZephyrRTOS\\mcux-sdk\\.west\\manifest-tmp\\.git\\objects\\pack\\pack-554f1ef9443cd0f11b09597e5af4c0f3b41d5301.idx'

!!!!!!!!!!!!!!!!!!!!!!!!!!!
The git repository at "c:\Users\urimrm\Projekty\Training\ZephyrRTOS\mcux-sdk\.west\manifest-tmp"
 has too many active changes, only a subset of Git features will be enabled.

 The git repositories in the current folder are potentially unsafe as the
  folders are owned by someone other than the current user.
  - mark as safe and open
!!!!!!!!!!!!!!!!!!!!!!!!!!!

// activate virtual environment
``` C:\Users\urimrm\.mcuxpressotools\.venv\Scripts\activate.ps1 ```

- Warning

cd C:\Users\urimrm\Projekty\Training\ZephyrRTOS

Open Powershell as admin:
``` git clone https://github.com/zephyrproject-rtos/zephyr.git ```
Cloning:
``` git clone https://github.com/nxp-mcuxpresso/mcux-sdk.git ```
``` git branch ``` oooor ``` git status ``` -> main

``` git checkout [branch name] ```

// Mark the Repository as Safe: You can explicitly mark the folder as safe for Git:
``` git config --global --add safe.directory "c:/Users/urimrm/Projekty/Training/ZephyrRTOS/mcux-sdk" ```

// Change Ownership to the Current User: Run the following from an elevated command prompt:
``` takeown /F c:\Users\urimrm\Projekty\Training\ZephyrRTOS\mcux-sdk /R /D Y ```

``` python -m west init ``` // ok
``` python -m west update ``` // ok

// if previously run west init
``` rmdir /s /q c:\Users\urimrm\Projekty\Training\ZephyrRTOS\mcux-sdk\.west ```

# Warnings
## more than 260 chars
- I stored git repositories "zephyr" and "mcux-sdk" into  shorter c:\GIT\Zephyr\

# During Lecture

Useful paths:
- ```C:\Users\urimrm\Projekty\Training\ZephyrRTOS\zephyr\zephyr\boards\nxp\frdm_mcxn947\frdm_mcxn947_mcxn947_cpu0.dts```
- ```cd c:/Users/urimrm/Projekty/Training/ZephyrRTOS/zephyr/Examples/frdm_mcxn947_mcxn947_cpu0_hello_world/build```

west tool creates a build directory for several targets
- just link server running (preinstalled by default)?
-

3.7.99 - untagged state of version (99)

West build
- ls =
- prj.conf = for merging multiple configuration files
-
- west config -l # configuration options
- west build -b frdm_ # (double tab should autocomplete if west is installed correctly)
- west build -b frdm_mcxn947/mcxn947/cpu0

WEST flash
- ``` west flash -d build/frdm_mcxn947/mcxn947/cpu0 ```
- another option: west flash -d build/frdm_mcxn947/mcxn947/cpu0 -r openocd

``` $ usb console.py -c #will run $ kermit -l /dev/ttyACM0 -b 115299 -c ```
* *** Booting Zephyr OS build v4.0.0-898-gb7b4de8afeb9 ***
* git describe <-> from git

Zephyr kernel configuration:
* ```$ west build -t menuconfig -d build/frdm_mcxn947/../cpu0```
* ```$ west build -t guiconfig -d build/frdm_mcxn947/../cpu0```

* *** $ west build -t report ***
