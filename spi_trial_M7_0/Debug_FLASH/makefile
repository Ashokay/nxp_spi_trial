################################################################################
# Automatically-generated file. Do not edit!
################################################################################

-include ../makefile.init

RM := rm -rf

# All of the sources participating in the build are defined here
-include sources.mk
-include src/subdir.mk
-include generate/src/subdir.mk
-include board/subdir.mk
-include RTD/src/subdir.mk
-include Project_Settings/Startup_Code/subdir.mk
-include subdir.mk
-include objects.mk

ifneq ($(MAKECMDGOALS),clean)
ifneq ($(strip $(C_DEPS)),)
-include $(C_DEPS)
endif
endif

-include ../makefile.defs

# Add inputs and outputs from these tool invocations to the build variables 
SECONDARY_SIZE += \
spi_trial_M7_0.siz \

# Define the name for the hex file
HEX_FILE := spi_trial_M7_0.hex

# All Target
all: spi_trial_M7_0.elf $(HEX_FILE) secondary-outputs

dependents:
	-cd /home/ubuntu/nxp_spi_trial/spi_trial_M7_1/Debug_FLASH && $(MAKE) all

# Tool invocations
spi_trial_M7_0.elf: $(OBJS) /home/ubuntu/nxp_spi_trial/spi_trial_M7_0/Project_Settings/Linker_Files/linker_flash_c0_s32k322.ld $(USER_OBJS) /home/ubuntu/nxp_spi_trial/spi_trial_M7_1/Debug_FLASH/spi_trial_M7_1.elf
	@echo 'Building target: $@'
	@echo 'Invoking: Standard S32DS C Linker'
	arm-none-eabi-gcc -o "spi_trial_M7_0.elf" "@spi_trial_M7_0.args"  $(USER_OBJS)
	@echo 'Finished building target: $@'
	@echo ' '

spi_trial_M7_0.siz: spi_trial_M7_0.elf
	@echo 'Invoking: Standard S32DS Print Size'
	arm-none-eabi-size --format=berkeley spi_trial_M7_0.elf
	@echo 'Finished building: $@'
	@echo ' '

# Rule to generate the hex file from the elf file
$(HEX_FILE): spi_trial_M7_0.elf
	@echo 'Invoking: Standard S32DS Create Flash Image'
	arm-none-eabi-objcopy -O ihex spi_trial_M7_0.elf $(HEX_FILE)
	@echo 'Finished building: $@'
	@echo ' '

# Other Targets
clean:
	-$(RM) ./*
	-@echo ' '

secondary-outputs: $(SECONDARY_SIZE)

.PHONY: all clean dependents
/home/ubuntu/nxp_spi_trial/spi_trial_M7_1/Debug_FLASH/spi_trial_M7_1.elf:

-include ../makefile.targets
