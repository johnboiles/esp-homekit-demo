PROGRAM = garage

EXTRA_COMPONENTS = \
	extras/http-parser \
	$(abspath ../../components/esp8266-open-rtos/cJSON) \
	$(abspath ../../components/common/wolfssl) \
	$(abspath ../../components/common/homekit)

FLASH_SIZE ?= 32
REED_PIN ?= 0
RELAY_PIN ?= 5

EXTRA_CFLAGS += -I../.. -DHOMEKIT_SHORT_APPLE_UUIDS -DREED_PIN=$(REED_PIN) -DRELAY_PIN=$(RELAY_PIN)


include $(SDK_PATH)/common.mk

monitor:
	$(FILTEROUTPUT) --port $(ESPPORT) --baud 9600 --elf $(PROGRAM_OUT)
