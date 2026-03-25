################################################################################
# Automatically-generated file. Do not edit!
# Toolchain: GNU Tools for STM32 (13.3.rel1)
################################################################################

-include ../makefile.init

RM := rm -rf

# All of the sources participating in the build are defined here
-include sources.mk
-include Startup/subdir.mk
-include Src/subdir.mk
-include SDK_1.0.3_NUCLEO-F401RE/shared/Utilities/subdir.mk
-include SDK_1.0.3_NUCLEO-F401RE/shared/Drivers/STM32F401RE_StdPeriph_Driver/src/subdir.mk
-include SDK_1.0.3_NUCLEO-F401RE/shared/Drivers/CMSIS/Source/subdir.mk
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


BUILD_ARTIFACT_NAME := ProjectDautien_nhom_3
BUILD_ARTIFACT_EXTENSION := elf
BUILD_ARTIFACT_PREFIX :=
BUILD_ARTIFACT := $(BUILD_ARTIFACT_PREFIX)$(BUILD_ARTIFACT_NAME)$(if $(BUILD_ARTIFACT_EXTENSION),.$(BUILD_ARTIFACT_EXTENSION),)

# Add inputs and outputs from these tool invocations to the build variables 
EXECUTABLES += \
ProjectDautien_nhom_3.elf \

MAP_FILES += \
ProjectDautien_nhom_3.map \

SIZE_OUTPUT += \
default.size.stdout \

OBJDUMP_LIST += \
ProjectDautien_nhom_3.list \


# All Target
all: main-build

# Main-build Target
main-build: ProjectDautien_nhom_3.elf secondary-outputs

# Tool invocations
ProjectDautien_nhom_3.elf ProjectDautien_nhom_3.map: $(OBJS) $(USER_OBJS) /Users/macos/Buoi1_Nhom3/ProjectDautien_Nhom_3/STM32F401RETX_FLASH.ld makefile objects.list $(OPTIONAL_TOOL_DEPS)
	arm-none-eabi-gcc -o "ProjectDautien_nhom_3.elf" @"objects.list" $(USER_OBJS) $(LIBS) -mcpu=cortex-m4 -T"/Users/macos/Buoi1_Nhom3/ProjectDautien_Nhom_3/STM32F401RETX_FLASH.ld" --specs=nosys.specs -Wl,-Map="ProjectDautien_nhom_3.map" -Wl,--gc-sections -static -L"/Users/macos/Downloads/SDK_1.0.3_NUCLEO-F401RE/lib_stm" --specs=nano.specs -mfpu=fpv4-sp-d16 -mfloat-abi=hard -mthumb -Wl,--start-group -lc -lm -Wl,--end-group
	@echo 'Finished building target: $@'
	@echo ' '

default.size.stdout: $(EXECUTABLES) makefile objects.list $(OPTIONAL_TOOL_DEPS)
	arm-none-eabi-size  $(EXECUTABLES)
	@echo 'Finished building: $@'
	@echo ' '

ProjectDautien_nhom_3.list: $(EXECUTABLES) makefile objects.list $(OPTIONAL_TOOL_DEPS)
	arm-none-eabi-objdump -h -S $(EXECUTABLES) > "ProjectDautien_nhom_3.list"
	@echo 'Finished building: $@'
	@echo ' '

# Other Targets
clean:
	-$(RM) ProjectDautien_nhom_3.elf ProjectDautien_nhom_3.list ProjectDautien_nhom_3.map default.size.stdout
	-@echo ' '

secondary-outputs: $(SIZE_OUTPUT) $(OBJDUMP_LIST)

fail-specified-linker-script-missing:
	@echo 'Error: Cannot find the specified linker script. Check the linker settings in the build configuration.'
	@exit 2

warn-no-linker-script-specified:
	@echo 'Warning: No linker script specified. Check the linker settings in the build configuration.'

.PHONY: all clean dependents main-build fail-specified-linker-script-missing warn-no-linker-script-specified

-include ../makefile.targets
