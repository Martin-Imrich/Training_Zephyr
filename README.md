# Zephyr RTOS Training
* ``` C:\Git\ZephyrProject ```
    * The Zephyr Project is a scalable real-time operating system (RTOS) supporting multiple hardware architectures, optimized for resource constrained devices, and built with security in mind.

# Enironment setup
* Zephyr repos stored at location
* ``` C:\Git\ZephyrProject\zephyr ```
    * ?
* ``` C:\Git\ZephyrProject\mcux-sdk ```
    * ?
* ``` C:\Git\ZephyrProject\zynq ```
    * [Board-Filter](https://docs.zephyrproject.org/latest/boards/index.html#)
    * Family: xilinx_zynq7000, Series: xc7zxxxs, SOC: xc7z007s "machine emulator"

* Creating .venv
    * ``` python3 -m venv ~/zephyrproject/.venv ```
    * ``` source ~/zephyrproject/.venv/bin/activate ```
    * ``` deactivate ```
    * ``` west init ~/zephyrproject ```

* Build the project
   * ``` cd zephyr ```
   * ``` west build -p always -b frdm_mcxn947/mcxn947/cpu0 samples/hello_world ```
   * ``` west build -t clean ``` 
   * ``` west flash ```
   * ``` west flash -r jlink ```

* Rebuild the project
   * [Procedure](!https://docs.zephyrproject.org/latest/develop/application/index.html#rebuilding-an-application)
 
