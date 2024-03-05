# How can I write my own driver file

1. You need to call FatFs_clock() with 100Hz frequency - the best way is to call it from timer interrupt
2. You need to provide all functions marked as **external** in `ff.h`:
- ```void FatFs_CS_HIGH(void)``` - this function should put Chip Select pin into HIGH state - 3,3V
- ```void FatFs_CS_LOW(void)``` - this function should put Chip Select pin into LOW state - 3,3V
- ```void FatFs_power_on(void)``` - here if you havent done it yet, you can provide initialization of SPI and GPIO
- ```void FatFs_power_off(void)``` - here you can disable SPI and GPIO
- ```uint8_t FatFs_SPI_SendRcv(uint8_t data)``` - here you get 8 bits to send and returns 8 bits recieved