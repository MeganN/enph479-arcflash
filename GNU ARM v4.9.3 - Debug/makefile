################################################################################
# Automatically-generated file. Do not edit!
################################################################################

-include ../makefile.init

RM := rm -rf

# All of the sources participating in the build are defined here
-include sources.mk
-include src/subdir.mk
-include emlib/subdir.mk
-include CMSIS/EFM32TG/subdir.mk
-include BSP/subdir.mk
-include subdir.mk
-include objects.mk

ifneq ($(MAKECMDGOALS),clean)
ifneq ($(strip $(C_DEPS)),)
-include $(C_DEPS)
endif
endif

-include ../makefile.defs

# Add inputs and outputs from these tool invocations to the build variables 

# All Target
all: Flash_Trigger.axf

# Tool invocations
Flash_Trigger.axf: $(OBJS) $(USER_OBJS)
	@echo 'Building target: $@'
	@echo 'Invoking: GNU ARM C Linker'
	arm-none-eabi-gcc -g -gdwarf-2 -mcpu=cortex-m3 -mthumb -T "Flash_Trigger.ld" -Xlinker --gc-sections -Xlinker -Map="Flash_Trigger.map" --specs=nano.specs -o Flash_Trigger.axf "./BSP/bsp_bcc.o" "./BSP/bsp_stk.o" "./BSP/bsp_stk_leds.o" "./BSP/bsp_trace.o" "./CMSIS/EFM32TG/startup_efm32tg.o" "./CMSIS/EFM32TG/system_efm32tg.o" "./emlib/em_assert.o" "./emlib/em_cmu.o" "./emlib/em_emu.o" "./emlib/em_gpio.o" "./emlib/em_system.o" "./emlib/em_usart.o" "./src/flash_trigger.o" -Wl,--start-group -lgcc -lc -lnosys -Wl,--end-group
	@echo 'Finished building target: $@'
	@echo ' '

	@echo 'Building hex file: Flash_Trigger.hex'
	arm-none-eabi-objcopy -O ihex "Flash_Trigger.axf" "Flash_Trigger.hex"
	@echo ' '

	@echo 'Building bin file: Flash_Trigger.bin'
	arm-none-eabi-objcopy -O binary "Flash_Trigger.axf" "Flash_Trigger.bin"
	@echo ' '

	@echo 'Building s37 file: Flash_Trigger.s37'
	arm-none-eabi-objcopy -O srec "Flash_Trigger.axf" "Flash_Trigger.s37"
	@echo ' '

	@echo 'Running size tool'
	arm-none-eabi-size "Flash_Trigger.axf"
	@echo ' '

# Other Targets
clean:
	-$(RM) $(EXECUTABLES)$(OBJS)$(C_DEPS) Flash_Trigger.axf
	-@echo ' '

.PHONY: all clean dependents
.SECONDARY:

-include ../makefile.targets
