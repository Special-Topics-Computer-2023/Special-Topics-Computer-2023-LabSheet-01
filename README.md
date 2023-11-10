## 64030059 Danupat Sangseekaew
เมืออัพโหลดโปรแกรมไฟกระพริบลงบอร์ดและเชื่อมต่อ pin 22 เข้ากับ LED แล้วที่บอร์ดจะมีไฟกระพริบ ติด - ดับ สลับกันและ terminal
```
ets Jul 29 2019 12:21:46

rst:0x1 (POWERON_RESET),boot:0x13 (SPI_FAST_FLASH_BOOT)
configsip: 0, SPIWP:0xee
clk_drv:0x00,q_drv:0x00,d_drv:0x00,cs0_drv:0x00,hd_drv:0x00,wp_drv:0x00
mode:DIO, clock div:2
load:0x3fff0030,len:6944
load:0x40078000,len:15500
load:0x40080400,len:3844
0x40080400: _init at ??:?

entry 0x4008064c
I (27) boot: ESP-IDF v5.0.2-dirty 2nd stage bootloader
I (27) boot: compile time 00:10:00
I (27) boot: chip revision: v3.0
I (31) boot.esp32: SPI Speed      : 40MHz
I (36) boot.esp32: SPI Mode       : DIO
I (40) boot.esp32: SPI Flash Size : 2MB
I (45) boot: Enabling RNG early entropy source...
I (50) boot: Partition Table:
I (54) boot: ## Label            Usage          Type ST Offset   Length
I (61) boot:  0 nvs              WiFi data        01 02 00009000 00006000
I (68) boot:  1 phy_init         RF data          01 01 0000f000 00001000
I (76) boot:  2 factory          factory app      00 00 00010000 00100000
I (83) boot: End of partition table
I (87) esp_image: segment 0: paddr=00010020 vaddr=3f400020 size=091ach ( 37292) map
I (109) esp_image: segment 1: paddr=000191d4 vaddr=3ffb0000 size=01ed4h (  7892) load
I (113) esp_image: segment 2: paddr=0001b0b0 vaddr=40080000 size=04f68h ( 20328) load
I (124) esp_image: segment 3: paddr=00020020 vaddr=400d0020 size=16d88h ( 93576) map
I (158) esp_image: segment 4: paddr=00036db0 vaddr=40084f68 size=068fch ( 26876) load
I (175) boot: Loaded app from partition at offset 0x10000
I (175) boot: Disabling RNG early entropy source...
I (186) cpu_start: Pro cpu up.
I (187) cpu_start: Starting app cpu, entry point is 0x40081044
0x40081044: call_start_cpu1 at C:/Espressif/frameworks/esp-idf-v5.0.2/components/esp_system/port/cpu_start.c:141

I (0) cpu_start: App cpu up.
I (201) cpu_start: Pro cpu start user code
I (201) cpu_start: cpu freq: 160000000 Hz
I (201) cpu_start: Application information:
I (206) cpu_start: Project name:     app-template
I (211) cpu_start: App version:      1
I (215) cpu_start: Compile time:     Nov  8 2023 00:01:42
I (222) cpu_start: ELF file SHA256:  185c73fe3669ffed...
I (227) cpu_start: ESP-IDF:          v5.0.2-dirty
I (233) cpu_start: Min chip rev:     v0.0
I (238) cpu_start: Max chip rev:     v3.99 
I (242) cpu_start: Chip rev:         v3.0
I (247) heap_init: Initializing. RAM available for dynamic allocation:
I (255) heap_init: At 3FFAE6E0 len 00001920 (6 KiB): DRAM
I (260) heap_init: At 3FFB27C8 len 0002D838 (182 KiB): DRAM
I (267) heap_init: At 3FFE0440 len 00003AE0 (14 KiB): D/IRAM
I (273) heap_init: At 3FFE4350 len 0001BCB0 (111 KiB): D/IRAM
I (279) heap_init: At 4008B864 len 0001479C (81 KiB): IRAM
I (287) spi_flash: detected chip: generic
I (290) spi_flash: flash io: dio
W (294) spi_flash: Detected size(4096k) larger than the size in the binary image header(2048k). Using the size in the binary image header.
I (308) cpu_start: Starting scheduler on PRO CPU.
I (0) cpu_start: Starting scheduler on APP CPU.
I (319) gpio: GPIO[22]| InputEn: 0| OutputEn: 0| OpenDrain: 0| Pullup: 1| Pulldown: 0| Intr:0

```

## Video การทำงาน
![721318617 049597](https://github.com/DanupatSangseekaew/Special-Topics-Computer-2023-LabSheet-01/assets/100436724/a4d85480-a889-482d-aaf4-d6ccc5298512)




