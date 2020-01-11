export FLASH_SIZE=8
export HOMEKIT_SPI_FLASH_BASE_ADDR=0x7a000
export FLASH_MODE=dout
docker run --env FLASH_SIZE=8 --env HOMEKIT_SPI_FLASH_BASE_ADDR=0x7a000 -it --rm -v `pwd`:/project -w /project esp-rtos make -C examples/garage all
make -C examples/garage flash monitor

# To erase flash
make -C examples/garage erase_flash
