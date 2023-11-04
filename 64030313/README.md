# 64030313 นางสาวสุดารัตน์ ฆ้องอินตะ

# Code
```c
#include <stdio.h>
#include <stdbool.h>
#include <unistd.h>
#include "driver/gpio.h"

void app_main(void)
{
    gpio_reset_pin(22);
    gpio_set_direction(22, GPIO_MODE_OUTPUT);

    while (true)
    {
        gpio_set_level(22, 1);
        usleep(500000);
        gpio_set_level(22, 0);
        usleep(500000);
    }
}
```

# Video
![img](https://github.com/NamaoySudarat/Special-Topics-Computer-2023-LabSheet-01/assets/115037574/c9782408-ad2c-4ce6-a4ee-e243837892a5)
