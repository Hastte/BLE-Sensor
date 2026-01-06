# Project Variables
PROJECT_NAME = ble-sensor
TARGET = $(PROJECT_NAME)

# Build directory
BUILD_DIR = build

# Compiler and tools
CC = arm-none-eabi-gcc
OBJCOPY = arm-none-eabi-objcopy
SIZE = arm-none-eabi-size

# MCU settings
MCU = -mcpu=cortex-m4 -mthumb -mfpu=fpv4-sp-d16 -mfloat-abi=hard

# C defines
C_DEFS = \
-DSTM32WB10xx \
-DUSE_HAL_DRIVER

# Include paths
C_INCLUDES = \
-Iinc

# C flags
CFLAGS = $(MCU) $(C_DEFS) $(C_INCLUDES) -O2 -Wall -fdata-sections -ffunction-sections

# Linker flags
LDFLAGS = $(MCU) -specs=nano.specs -Wl,--gc-sections -Wl,-Map=$(BUILD_DIR)/$(TARGET).map

# Source files
C_SOURCES = \
src/main.c

# Object files
OBJECTS = $(addprefix $(BUILD_DIR)/,$(notdir $(C_SOURCES:.c=.o)))

# Default target
all: $(BUILD_DIR)/$(TARGET).elf $(BUILD_DIR)/$(TARGET).hex $(BUILD_DIR)/$(TARGET).bin

# Build directory
$(BUILD_DIR):
	mkdir -p $@

# Compile C sources
$(BUILD_DIR)/%.o: src/%.c | $(BUILD_DIR)
	$(CC) -c $(CFLAGS) $< -o $@

# Link
$(BUILD_DIR)/$(TARGET).elf: $(OBJECTS)
	$(CC) $(OBJECTS) $(LDFLAGS) -o $@
	$(SIZE) $@

# Generate hex file
$(BUILD_DIR)/$(TARGET).hex: $(BUILD_DIR)/$(TARGET).elf
	$(OBJCOPY) -O ihex $< $@

# Generate binary file
$(BUILD_DIR)/$(TARGET).bin: $(BUILD_DIR)/$(TARGET).elf
	$(OBJCOPY) -O binary -S $< $@

# Clean
clean:
	rm -rf $(BUILD_DIR)

# Flash (requires st-flash utility)
flash: $(BUILD_DIR)/$(TARGET).bin
	st-flash write $(BUILD_DIR)/$(TARGET).bin 0x8000000

# Phony targets
.PHONY: all clean flash
