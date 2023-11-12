# LabSheet-01 (การ upload firmware)

1. จากตัวอย่างโปรแกรม จะเห็นว่าเราใช้ GPIO หมายเลข 22  ดังนั้น ที่บนบอร์ด ให้ต่อสาย  jump จากขาที่เขียน GPIO22 ไปยัง LED ดวงหนึ่งที่อยู่บนบอร์ด (สมมติเป็น LED หมายเลข 8)


 <p align="center">
<img  src="Images/GPIOJumperToLED.png" alt="GPIOJumperToLED" style="width:640px;" >
</p>


2. ให้ต่อบอร์ดทดลองเข้ากับ USB ของคอมพิวเตอร์


3. ให้เข้าไปที่ device manager เพื่อดูว่าหมายเลขของ communication port ที่คอมพิวเตอร์จัดให้บอร์ดทดลองของเราเป็นเลขอะไร ซึ่งบอร์ด ESP32 ที่ใช้ในการทดลองนี้ใช้ชิป USB to Serial รุ่น `Silicon Labs CP210x USB to UART Bridge` ให้จำชื่อ Communication port ไว้ ซึ่งในตัวอย่างนี้คือ __COM5__  
 

 <p align="center">
<img  src="Images/CommPort.png" alt="CommPort" style="width:640px;" >
</p>

4. กลับมาที่โปรแกรม ESP32 IDE  ให้เลือก Comm port โดยคลิกที่รูปเฟืองใน combobox `on:` 

(1) คลิกที่รูปเฟืองใน combobox `on:`

(2) เลือก Communication port ที่ต่อกับบอร์ดทดลอง แล้วกด `Finish`

 <p align="center">
<img  src="Images/SelectCommPort.png" alt="SelectCommPort" style="width:640px;" >
</p>

5. Upload firmware เข้าสู่บอร์ดทดลอง 

(1) คลิกปุ่ม `Launch in 'RUN' mode`

(2) สังเกตุการรายงานผลจาก IDE


 <p align="center">
<img  src="Images/LaunchInRUNMode.png" alt="LaunchInRUNMode" style="width:640px;" >
</p>

ถ้าโปรแกรมได้สำเร็จ จะมีข้อความดังตัวอย่างต่อไปนี้

``` 
Connecting.....
Chip is ESP32-D0WD-V3 (revision 3)
Features: WiFi, BT, Dual Core, 240MHz, VRef calibration in efuse, Coding Scheme None
Crystal is 40MHz
MAC: 94:b5:55:f3:98:00
Uploading stub...
Running stub...
Stub running...
Changing baud rate to 460800
Changed.
Configuring flash size...
Flash will be erased from 0x00001000 to 0x00007fff...
Flash will be erased from 0x00010000 to 0x0003bfff...
Flash will be erased from 0x00008000 to 0x00008fff...
Compressed 25392 bytes to 15888...
Writing at 0x00001000... (100 %)
Wrote 25392 bytes (15888 compressed) at 0x00001000 in 0.8 seconds (effective 264.9 kbit/s)...
Hash of data verified.
Compressed 179024 bytes to 93086...
Writing at 0x00010000... (16 %)
Writing at 0x0001bc95... (33 %)
Writing at 0x000214bd... (50 %)
Writing at 0x0002717c... (66 %)
Writing at 0x0002f7b2... (83 %)
Writing at 0x0003794b... (100 %)
Wrote 179024 bytes (93086 compressed) at 0x00010000 in 2.6 seconds (effective 558.1 kbit/s)...
Hash of data verified.
Compressed 3072 bytes to 103...
Writing at 0x00008000... (100 %)
Wrote 3072 bytes (103 compressed) at 0x00008000 in 0.1 seconds (effective 366.8 kbit/s)...
Hash of data verified.

Leaving...
Hard resetting via RTS pin...
Executing action: flash
Running ninja in directory d:\githubrepos\__engedu\lab\lab-01-led-blinky\build
Executing "ninja flash"...
Done
```

6. สังเกตบนบอร์ด จะมีไฟกระพริบเป็นจังหวะติด-ดับสลับกันทุก 1 วินาที

- ถ้ามีสิ่งผิดปกติ เช่นไม่สามารถ  upload ได้ให้ตรวจสอบการเชื่อมต่อและหลายเลข Communication port ให้ถูกต้อง 
- ถ้ามีข้อความ Connecting............................. และรายงานว่าไม่สามารถเชื่อมต่อได้ ให้ทำการกดปุ่ม BOOT ที่บนบอร์ดไว้จนกว่าโปรแกรมได้  
- สามารถสังเกตว่าบอร์ดสามารถโปรแกรมได้ จากบรรทัดต่อไปนี้

```
Writing at 0x00010000... (16 %)
Writing at 0x0001bc95... (33 %)
Writing ...   
```
## ผลลัพธ์ ##
```
[1/5] cmd.exe /C "cd /D D:\Espressif\frameworks\esp-idf-v4.4.3\workspace\Lab-01-LED-Blinkky\build\esp-idf\esptool_py && python D:/Espressif/frameworks/esp-idf-v4.4.3/components/partition_table/check_sizes.py --offset 0x8000 partition --type app D:/Espressif/frameworks/esp-idf-v4.4.3/workspace/Lab-01-LED-Blinkky/build/partition_table/partition-table.bin D:/Espressif/frameworks/esp-idf-v4.4.3/workspace/Lab-01-LED-Blinkky/build/Lab-01-LED-Blinkky.bin"
Lab-01-LED-Blinkky.bin binary size 0x2bde0 bytes. Smallest app partition is 0x100000 bytes. 0xd4220 bytes (83%) free.
[2/5] Performing build step for 'bootloader'
[1/1] cmd.exe /C "cd /D D:\Espressif\frameworks\esp-idf-v4.4.3\workspace\Lab-01-LED-Blinkky\build\bootloader\esp-idf\esptool_py && python D:/Espressif/frameworks/esp-idf-v4.4.3/components/partition_table/check_sizes.py --offset 0x8000 bootloader 0x1000 D:/Espressif/frameworks/esp-idf-v4.4.3/workspace/Lab-01-LED-Blinkky/build/bootloader/bootloader.bin"
Bootloader binary size 0x6330 bytes. 0xcd0 bytes (11%) free.
[2/3] cmd.exe /C "cd /D D:\Espressif\frameworks\esp-idf-v4.4.3\components\esptool_py && D:\Espressif\tools\cmake\3.23.1\bin\cmake.exe -D IDF_PATH="D:/Espressif/frameworks/esp-idf-v4.4.3" -D SERIAL_TOOL="python D:/Espressif/frameworks/esp-idf-v4.4.3/components/esptool_py/esptool/esptool.py --chip esp32" -D SERIAL_TOOL_ARGS="--before=default_reset --after=hard_reset write_flash @flash_args" -D WORKING_DIRECTORY="D:/Espressif/frameworks/esp-idf-v4.4.3/workspace/Lab-01-LED-Blinkky/build" -P D:/Espressif/frameworks/esp-idf-v4.4.3/components/esptool_py/run_serial_tool.cmake"
esptool.py esp32 -p COM3 -b 460800 --before=default_reset --after=hard_reset write_flash --flash_mode dio --flash_freq 40m --flash_size 2MB 0x1000 bootloader/bootloader.bin 0x10000 Lab-01-LED-Blinkky.bin 0x8000 partition_table/partition-table.bin
esptool.py v3.3.2
Serial port COM3
Connecting....
Chip is ESP32-D0WD-V3 (revision 3)
Features: WiFi, BT, Dual Core, 240MHz, VRef calibration in efuse, Coding Scheme None
Crystal is 40MHz
MAC: 94:b5:55:f3:54:48
Uploading stub...
Running stub...
Stub running...
Changing baud rate to 460800
Changed.
Configuring flash size...
Flash will be erased from 0x00001000 to 0x00007fff...
Flash will be erased from 0x00010000 to 0x0003bfff...
Flash will be erased from 0x00008000 to 0x00008fff...
Compressed 25392 bytes to 15891...
Writing at 0x00001000... (100 %)
Wrote 25392 bytes (15891 compressed) at 0x00001000 in 0.8 seconds (effective 265.2 kbit/s)...
Hash of data verified.
Compressed 179680 bytes to 93495...
Writing at 0x00010000... (16 %)
Writing at 0x0001bcd1... (33 %)
Writing at 0x00021502... (50 %)
Writing at 0x000271d8... (66 %)
Writing at 0x0002f818... (83 %)
Writing at 0x0003798c... (100 %)
Wrote 179680 bytes (93495 compressed) at 0x00010000 in 2.6 seconds (effective 555.6 kbit/s)...
Hash of data verified.
Compressed 3072 bytes to 103...
Writing at 0x00008000... (100 %)
Wrote 3072 bytes (103 compressed) at 0x00008000 in 0.1 seconds (effective 419.6 kbit/s)...
Hash of data verified.

Leaving...
Hard resetting via RTS pin...
Executing action: flash
Running ninja in directory d:\espressif\frameworks\esp-idf-v4.4.3\workspace\lab-01-led-blinkky\build
Executing "ninja flash"...
Done

```
## video การทดลอง ##

![401581458_6600151000082349_4126741717060201089_n](https://github.com/TanapatPluemchai/Special-Topics-Computer-2023-LabSheet-01/assets/115067806/718f9aeb-89b3-4821-9f34-62e2ad12d0e9)



