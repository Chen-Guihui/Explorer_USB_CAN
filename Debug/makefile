################################################################################
# Automatically-generated file. Do not edit!
################################################################################

-include ../makefile.init

RM := rm -rf

# All of the sources participating in the build are defined here
-include sources.mk
-include startup/subdir.mk
-include Src/subdir.mk
-include Middlewares/Third_Party/FreeRTOS/Source/portable/MemMang/subdir.mk
-include Middlewares/Third_Party/FreeRTOS/Source/portable/GCC/ARM_CM4F/subdir.mk
-include Middlewares/Third_Party/FreeRTOS/Source/CMSIS_RTOS/subdir.mk
-include Middlewares/Third_Party/FreeRTOS/Source/subdir.mk
-include Middlewares/ST/STM32_USB_Device_Library/Core/Src/subdir.mk
-include Middlewares/ST/STM32_USB_Device_Library/Class/CDC/Src/subdir.mk
-include Drivers/STM32F4xx_HAL_Driver/Src/subdir.mk
-include subdir.mk
-include objects.mk

ifneq ($(MAKECMDGOALS),clean)
ifneq ($(strip $(C_DEPS)),)
-include $(C_DEPS)
endif
endif

-include ../makefile.defs

# Add inputs and outputs from these tool invocations to the build variables 
SECOUTPUTBUILDVAR += \
EXECUTABLES \


# All Target
all: Explorer_USB_CAN.elf secondary-outputs

# Tool invocations
Explorer_USB_CAN.elf: $(OBJS) $(USER_OBJS)
	arm-atollic-eabi-gcc -o "Explorer_USB_CAN.elf" $(OBJS) $(USER_OBJS) $(LIBS) -mthumb -mcpu=cortex-m4 -mfloat-abi=hard -mfpu=fpv4-sp-d16 -T"../STM32F407ZG_FLASH.ld" -specs=nosys.specs -static "-Wl,-Map=Explorer_USB_CAN.map" -Wl,--gc-sections -Wl,--defsym=malloc_getpagesize_P=0x80 -Wl,--start-group -lc -lm -Wl,--end-group -specs=nano.specs
	$(MAKE) --no-print-directory post-build

EXECUTABLES: Explorer_USB_CAN.elf $(EXECUTABLES)
	"D:\Program Files\TrueSTUDIO for STM32 9.2.0\ide\jre\bin\java" -jar "D:\Program Files\TrueSTUDIO for STM32 9.2.0\Tools\arm-atollic-reports.jar" sizeinfo list Explorer_USB_CAN.elf

# Other Targets
clean:
	-$(RM) $(EXECUTABLES)$(SECOUTPUTBUILDVAR)$(OBJS)$(C_DEPS) Explorer_USB_CAN.elf
	-@echo ' '

post-build:
	-arm-atollic-eabi-objcopy.exe -O ihex "Explorer_USB_CAN.elf" "Explorer_USB_CAN.hex"
	-@echo ' '

secondary-outputs: $(SECOUTPUTBUILDVAR)

.PHONY: all clean dependents
.SECONDARY: post-build

-include ../makefile.targets
