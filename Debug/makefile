################################################################################
# Automatically-generated file. Do not edit!
################################################################################

-include ../makefile.init

RM := rm -rf

# All of the sources participating in the build are defined here
-include sources.mk
-include Drivers/STM32F7xx_HAL_Driver/Src/subdir.mk
-include Core/Startup/subdir.mk
-include Core/Src/subdir.mk
-include subdir.mk
-include objects.mk

ifneq ($(MAKECMDGOALS),clean)
ifneq ($(strip $(S_DEPS)),)
-include $(S_DEPS)
endif
ifneq ($(strip $(S_UPPER_DEPS)),)
-include $(S_UPPER_DEPS)
endif
ifneq ($(strip $(C_DEPS)),)
-include $(C_DEPS)
endif
endif

-include ../makefile.defs

# Add inputs and outputs from these tool invocations to the build variables 
EXECUTABLES += \
IAP_STM32F7-master.elf \

SIZE_OUTPUT += \
default.size.stdout \

OBJDUMP_LIST += \
IAP_STM32F7-master.list \

OBJCOPY_BIN += \
IAP_STM32F7-master.bin \


# All Target
all: IAP_STM32F7-master.elf secondary-outputs

# Tool invocations
IAP_STM32F7-master.elf: $(OBJS) $(USER_OBJS) D:\mcu\IAP_STM32F7-master\STM32F767ZITX_FLASH.ld
	arm-none-eabi-gcc -o "IAP_STM32F7-master.elf" @"objects.list" $(USER_OBJS) $(LIBS) -mcpu=cortex-m7 -T"D:\mcu\IAP_STM32F7-master\STM32F767ZITX_FLASH.ld" --specs=nosys.specs -Wl,-Map="IAP_STM32F7-master.map" -Wl,--gc-sections -static --specs=nano.specs -mfpu=fpv5-d16 -mfloat-abi=hard -mthumb -u _printf_float -Wl,--start-group -lc -lm -Wl,--end-group
	@echo 'Finished building target: $@'
	@echo ' '

default.size.stdout: $(EXECUTABLES)
	arm-none-eabi-size  $(EXECUTABLES)
	@echo 'Finished building: $@'
	@echo ' '

IAP_STM32F7-master.list: $(EXECUTABLES)
	arm-none-eabi-objdump -h -S $(EXECUTABLES) > "IAP_STM32F7-master.list"
	@echo 'Finished building: $@'
	@echo ' '

IAP_STM32F7-master.bin: $(EXECUTABLES)
	arm-none-eabi-objcopy  -O binary $(EXECUTABLES) "IAP_STM32F7-master.bin"
	@echo 'Finished building: $@'
	@echo ' '

# Other Targets
clean:
	-$(RM) *
	-@echo ' '

secondary-outputs: $(SIZE_OUTPUT) $(OBJDUMP_LIST) $(OBJCOPY_BIN)

.PHONY: all clean dependents
.SECONDARY:

-include ../makefile.targets
