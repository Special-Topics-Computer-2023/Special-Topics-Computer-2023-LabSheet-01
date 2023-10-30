# 64030161 Rachata Supanurak

เมืออัพโหลดโปรแกรมไฟกระพริบลงบอร์ดและเชื่อมต่อ pin 22 เข้ากับ LED แล้วที่บอร์ดจะมีไฟกระพริบ ติด - ดับ สลับกันและ terminal จะแสดงผลดังนี้
```css

entry 0x40080698
I (27) boot: ESP-IDF v4.4.5-dirty 2nd stage bootloader
I (27) boot: compile time 19:07:32
I (27) boot: chip revision: v3.0
I (31) boot.esp32: SPI Speed      : 40MHz
I (36) boot.esp32: SPI Mode       : DIO
I (40) boot.esp32: SPI Flash Size : 4MB
I (45) boot: Enabling RNG early entropy source...
I (50) boot: Partition Table:
I (54) boot: ## Label            Usage          Type ST Offset   Length
I (61) boot:  0 nvs              WiFi data        01 02 00009000 00006000
I (68) boot:  1 phy_init         RF data          01 01 0000f000 00001000
I (76) boot:  2 factory          factory app      00 00 00010000 00100000
I (83) boot: End of partition table
I (88) esp_image: segment 0: paddr=00010020 vaddr=3f400020 size=091ach ( 37292) map
I (110) esp_image: segment 1: paddr=000191d4 vaddr=3ffb0000 size=01bc8h (  7112) load
I (113) esp_image: segment 2: paddr=0001ada4 vaddr=40080000 size=05274h ( 21108) load
I (124) esp_image: segment 3: paddr=00020020 vaddr=400d0020 size=1629ch ( 90780) map
I (157) esp_image: segment 4: paddr=000362c4 vaddr=40085274 size=06278h ( 25208) load
I (173) boot: Loaded app from partition at offset 0x10000
I (173) boot: Disabling RNG early entropy source...
I (185) cpu_start: Pro cpu up.
I (185) cpu_start: Starting app cpu, entry point is 0x40080fe8
0x40080fe8: call_start_cpu1 at /Users/rachatasupanurak/esp/esp-idf/components/esp_system/port/cpu_start.c:147

I (0) cpu_start: App cpu up.
I (199) cpu_start: Pro cpu start user code
I (199) cpu_start: cpu freq: 160000000
I (199) cpu_start: Application information:
I (204) cpu_start: Project name:     IOT_Lab_1
I (209) cpu_start: App version:      927b033-dirty
I (214) cpu_start: Compile time:     Oct 30 2023 19:07:23
I (220) cpu_start: ELF file SHA256:  17e2b86a01d7f616...
I (226) cpu_start: ESP-IDF:          v4.4.5-dirty
I (232) cpu_start: Min chip rev:     v0.0
I (237) cpu_start: Max chip rev:     v3.99 
I (241) cpu_start: Chip rev:         v3.0
I (246) heap_init: Initializing. RAM available for dynamic allocation:
I (253) heap_init: At 3FFAE6E0 len 00001920 (6 KiB): DRAM
I (259) heap_init: At 3FFB24B0 len 0002DB50 (182 KiB): DRAM
I (266) heap_init: At 3FFE0440 len 00003AE0 (14 KiB): D/IRAM
I (272) heap_init: At 3FFE4350 len 0001BCB0 (111 KiB): D/IRAM
I (278) heap_init: At 4008B4EC len 00014B14 (82 KiB): IRAM
I (286) spi_flash: detected chip: generic
I (289) spi_flash: flash io: dio
I (294) cpu_start: Starting scheduler on PRO CPU.
I (0) cpu_start: Starting scheduler on APP CPU.
I (304) gpio: GPIO[22]| InputEn: 0| OutputEn: 0| OpenDrain: 0| Pullup: 1| Pulldown: 0| Intr:0
```
บอร์ดจะมีไฟกระพริบติด - ดับ ดังนี้
![297BD034-AE0A-44E0-8942-BFE5E0E87164_1_102_o](https://github.com/RachataS/Special-Topics-Computer-2023-LabSheet-01/assets/115066261/3ab61af4-52b7-4660-8a96-e3baae556ef6)

![IMG_7250](https://github.com/RachataS/Special-Topics-Computer-2023-LabSheet-01/assets/115066261/63f87ea2-d5ca-4c9b-8bb0-ce52b4da475d)
