################################################################################
# Automatically-generated file. Do not edit!
# Toolchain: GNU Tools for STM32 (10.3-2021.10)
################################################################################

-include ../makefile.init

RM := rm -rf

# All of the sources participating in the build are defined here
-include sources.mk
-include Startup/subdir.mk
-include Src/subdir.mk
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

OPTIONAL_TOOL_DEPS := \
$(wildcard ../makefile.defs) \
$(wildcard ../makefile.init) \
$(wildcard ../makefile.targets) \


BUILD_ARTIFACT_NAME := Bare-Metal-STM32L051K8T6-LED-ON-OFF
BUILD_ARTIFACT_EXTENSION := elf
BUILD_ARTIFACT_PREFIX :=
BUILD_ARTIFACT := $(BUILD_ARTIFACT_PREFIX)$(BUILD_ARTIFACT_NAME)$(if $(BUILD_ARTIFACT_EXTENSION),.$(BUILD_ARTIFACT_EXTENSION),)

# Add inputs and outputs from these tool invocations to the build variables 
EXECUTABLES += \
Bare-Metal-STM32L051K8T6-LED-ON-OFF.elf \

MAP_FILES += \
Bare-Metal-STM32L051K8T6-LED-ON-OFF.map \

SIZE_OUTPUT += \
default.size.stdout \

OBJDUMP_LIST += \
Bare-Metal-STM32L051K8T6-LED-ON-OFF.list \


# All Target
all: main-build

# Main-build Target
main-build: Bare-Metal-STM32L051K8T6-LED-ON-OFF.elf secondary-outputs

# Tool invocations
Bare-Metal-STM32L051K8T6-LED-ON-OFF.elf Bare-Metal-STM32L051K8T6-LED-ON-OFF.map: $(OBJS) $(USER_OBJS) C:\Users\Lenovo\STM32CubeIDE\workspace_1.10.1\Bare-Metal-STM32L051K8T6-LED-ON-OFF\STM32L051K8TX_FLASH.ld makefile objects.list $(OPTIONAL_TOOL_DEPS)
	arm-none-eabi-gcc -o "Bare-Metal-STM32L051K8T6-LED-ON-OFF.elf" @"objects.list" $(USER_OBJS) $(LIBS) -mcpu=cortex-m0plus -T"C:\Users\Lenovo\STM32CubeIDE\workspace_1.10.1\Bare-Metal-STM32L051K8T6-LED-ON-OFF\STM32L051K8TX_FLASH.ld" --specs=nosys.specs -Wl,-Map="Bare-Metal-STM32L051K8T6-LED-ON-OFF.map" -Wl,--gc-sections -static --specs=nano.specs -mfloat-abi=soft -mthumb -Wl,--start-group -lc -lm -Wl,--end-group
	@echo 'Finished building target: $@'
	@echo ' '

default.size.stdout: $(EXECUTABLES) makefile objects.list $(OPTIONAL_TOOL_DEPS)
	arm-none-eabi-size  $(EXECUTABLES)
	@echo 'Finished building: $@'
	@echo ' '

Bare-Metal-STM32L051K8T6-LED-ON-OFF.list: $(EXECUTABLES) makefile objects.list $(OPTIONAL_TOOL_DEPS)
	arm-none-eabi-objdump -h -S $(EXECUTABLES) > "Bare-Metal-STM32L051K8T6-LED-ON-OFF.list"
	@echo 'Finished building: $@'
	@echo ' '

# Other Targets
clean:
	-$(RM) Bare-Metal-STM32L051K8T6-LED-ON-OFF.elf Bare-Metal-STM32L051K8T6-LED-ON-OFF.list Bare-Metal-STM32L051K8T6-LED-ON-OFF.map default.size.stdout
	-@echo ' '

secondary-outputs: $(SIZE_OUTPUT) $(OBJDUMP_LIST)

fail-specified-linker-script-missing:
	@echo 'Error: Cannot find the specified linker script. Check the linker settings in the build configuration.'
	@exit 2

warn-no-linker-script-specified:
	@echo 'Warning: No linker script specified. Check the linker settings in the build configuration.'

.PHONY: all clean dependents main-build fail-specified-linker-script-missing warn-no-linker-script-specified

-include ../makefile.targets
