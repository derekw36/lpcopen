# LPCOpen library
zephyr_library()

# Map CPU definitions
zephyr_compile_definitions_ifdef(CONFIG_CPU_CORTEX_M3 -DCORE_M3)

# Map SoC definitions
zephyr_compile_definitions_ifdef(CONFIG_SOC_LPC1768 -DCHIP_LPC175X_6X)

# SoC series subdirectories
add_subdirectory_ifdef(CONFIG_SOC_SERIES_LPC17XX 17xx_40xx)
