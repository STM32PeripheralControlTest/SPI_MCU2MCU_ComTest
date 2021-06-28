# SPI_MCU2MCU_ComTest
Communication test between 3 STM32L476RGNucleo boards.

## System architecture
STM32L476RGNucleo-1 : 
  SPI1 full-duplex master
  SPI2 receive only slave
  SPI3 receive only slave.
  Software CS.

STM32L476RGNucleo-2
  SPI2 transmit only slave.

STM32L476RGNucleo-3
  SPI2 transmit only slave.

SCLK of the SPI1 in the board-1 is connected to all slave SCLK.
Software CS of the board-1 is connected to all slave CS.
MISO of the SPI1 in the board-1 is connected to SPI2 MISO in the board-2.
MOSI of the SPI2 in the board-1 is connected to SPI2 MISO in the board-2 
MOSI of the SPI3 in the board-1 is connected to SPI2 MISO in the board-3

## Pin layout
See STM32CubeMX file.

