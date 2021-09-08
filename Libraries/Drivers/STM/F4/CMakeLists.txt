# Here is for STM32F4XX Driver module

# Need add stm32f4xx_hal.h
include_directories(${CMAKE_CURRENT_SOURCE_DIR})

include_directories(${CMAKE_CURRENT_SOURCE_DIR}/stm32f4xx_hal_driver/Inc)
include_directories(${CMAKE_CURRENT_SOURCE_DIR}/stm32f4xx_hal_driver/Inc/Legacy)

aux_source_directory( "${CMAKE_CURRENT_SOURCE_DIR}/stm32f4xx_hal_driver/Src" ST_HAL_DRV_SRCS)

set(ST_HAL_DRV_SRCS
    ${ST_HAL_DRV_SRCS}
    ${CMAKE_CURRENT_SOURCE_DIR}/stm32f4xx_hal_driver/Src/Legacy/stm32f4xx_hal_can.c
)
#[[ set(ST_HAL_DRV_SRCS
    ${CMAKE_CURRENT_SOURCE_DIR}/stm32f4xx_hal_driver/Src/stm32f4xx_hal_adc_ex.c
    ${CMAKE_CURRENT_SOURCE_DIR}/stm32f4xx_hal_driver/Src/stm32f4xx_hal_adc.c
    ${CMAKE_CURRENT_SOURCE_DIR}/stm32f4xx_hal_driver/Src/stm32f4xx_hal_can.c
    ${CMAKE_CURRENT_SOURCE_DIR}/stm32f4xx_hal_driver/Src/stm32f4xx_hal_cec.c
    ${CMAKE_CURRENT_SOURCE_DIR}/stm32f4xx_hal_driver/Src/stm32f4xx_hal_cortex.c
    ${CMAKE_CURRENT_SOURCE_DIR}/stm32f4xx_hal_driver/Src/stm32f4xx_hal_crc.c
    ${CMAKE_CURRENT_SOURCE_DIR}/stm32f4xx_hal_driver/Src/stm32f4xx_hal_cryp_ex.c
    ${CMAKE_CURRENT_SOURCE_DIR}/stm32f4xx_hal_driver/Src/stm32f4xx_hal_cryp.c
    ${CMAKE_CURRENT_SOURCE_DIR}/stm32f4xx_hal_driver/Src/stm32f4xx_hal_dac_ex.c
    ${CMAKE_CURRENT_SOURCE_DIR}/stm32f4xx_hal_driver/Src/stm32f4xx_hal_dac.c
    ${CMAKE_CURRENT_SOURCE_DIR}/stm32f4xx_hal_driver/Src/stm32f4xx_hal_dcmi_ex.c
    ${CMAKE_CURRENT_SOURCE_DIR}/stm32f4xx_hal_driver/Src/stm32f4xx_hal_dcmi.c
    ${CMAKE_CURRENT_SOURCE_DIR}/stm32f4xx_hal_driver/Src/stm32f4xx_hal_dfsdm.c
    ${CMAKE_CURRENT_SOURCE_DIR}/stm32f4xx_hal_driver/Src/stm32f4xx_hal_dma_ex.c
    ${CMAKE_CURRENT_SOURCE_DIR}/stm32f4xx_hal_driver/Src/stm32f4xx_hal_dma.c
    ${CMAKE_CURRENT_SOURCE_DIR}/stm32f4xx_hal_driver/Src/stm32f4xx_hal_dma2d.c
    ${CMAKE_CURRENT_SOURCE_DIR}/stm32f4xx_hal_driver/Src/stm32f4xx_hal_dsi.c
    ${CMAKE_CURRENT_SOURCE_DIR}/stm32f4xx_hal_driver/Src/stm32f4xx_hal_eth.c
    ${CMAKE_CURRENT_SOURCE_DIR}/stm32f4xx_hal_driver/Src/stm32f4xx_hal_exti.c
    ${CMAKE_CURRENT_SOURCE_DIR}/stm32f4xx_hal_driver/Src/stm32f4xx_hal_flash_ex.c
    ${CMAKE_CURRENT_SOURCE_DIR}/stm32f4xx_hal_driver/Src/stm32f4xx_hal_flash_ramfunc.c
    ${CMAKE_CURRENT_SOURCE_DIR}/stm32f4xx_hal_driver/Src/stm32f4xx_hal_flash.c
    ${CMAKE_CURRENT_SOURCE_DIR}/stm32f4xx_hal_driver/Src/stm32f4xx_hal_fmpi2c_ex.c
    ${CMAKE_CURRENT_SOURCE_DIR}/stm32f4xx_hal_driver/Src/stm32f4xx_hal_fmpi2c.c
    ${CMAKE_CURRENT_SOURCE_DIR}/stm32f4xx_hal_driver/Src/stm32f4xx_hal_fmpsmbus.c
    ${CMAKE_CURRENT_SOURCE_DIR}/stm32f4xx_hal_driver/Src/stm32f4xx_hal_fmpsmbus_ex.c
    ${CMAKE_CURRENT_SOURCE_DIR}/stm32f4xx_hal_driver/Src/stm32f4xx_hal_gpio.c
    ${CMAKE_CURRENT_SOURCE_DIR}/stm32f4xx_hal_driver/Src/stm32f4xx_hal_hash.c
    ${CMAKE_CURRENT_SOURCE_DIR}/stm32f4xx_hal_driver/Src/stm32f4xx_hal_hash_ex.c
    ${CMAKE_CURRENT_SOURCE_DIR}/stm32f4xx_hal_driver/Src/stm32f4xx_hal_hcd.c
    ${CMAKE_CURRENT_SOURCE_DIR}/stm32f4xx_hal_driver/Src/stm32f4xx_hal_i2c.c
    ${CMAKE_CURRENT_SOURCE_DIR}/stm32f4xx_hal_driver/Src/stm32f4xx_hal_i2c_ex.c
    ${CMAKE_CURRENT_SOURCE_DIR}/stm32f4xx_hal_driver/Src/stm32f4xx_hal_i2s.c
    ${CMAKE_CURRENT_SOURCE_DIR}/stm32f4xx_hal_driver/Src/stm32f4xx_hal_i2s_ex.c
    ${CMAKE_CURRENT_SOURCE_DIR}/stm32f4xx_hal_driver/Src/stm32f4xx_hal_irda.c
    ${CMAKE_CURRENT_SOURCE_DIR}/stm32f4xx_hal_driver/Src/stm32f4xx_hal_iwdg.c
    ${CMAKE_CURRENT_SOURCE_DIR}/stm32f4xx_hal_driver/Src/stm32f4xx_hal_lptim.c
    ${CMAKE_CURRENT_SOURCE_DIR}/stm32f4xx_hal_driver/Src/stm32f4xx_hal_ltdc.c
    ${CMAKE_CURRENT_SOURCE_DIR}/stm32f4xx_hal_driver/Src/stm32f4xx_hal_ltdc_ex.c
    ${CMAKE_CURRENT_SOURCE_DIR}/stm32f4xx_hal_driver/Src/stm32f4xx_hal_mmc.c
    ${CMAKE_CURRENT_SOURCE_DIR}/stm32f4xx_hal_driver/Src/stm32f4xx_hal_msp_template.c
    ${CMAKE_CURRENT_SOURCE_DIR}/stm32f4xx_hal_driver/Src/stm32f4xx_hal_nand.c
    ${CMAKE_CURRENT_SOURCE_DIR}/stm32f4xx_hal_driver/Src/stm32f4xx_hal_nor.c
    ${CMAKE_CURRENT_SOURCE_DIR}/stm32f4xx_hal_driver/Src/stm32f4xx_hal_pccard.c
    ${CMAKE_CURRENT_SOURCE_DIR}/stm32f4xx_hal_driver/Src/stm32f4xx_hal_pcd.c
    ${CMAKE_CURRENT_SOURCE_DIR}/stm32f4xx_hal_driver/Src/stm32f4xx_hal_pcd_ex.c
    ${CMAKE_CURRENT_SOURCE_DIR}/stm32f4xx_hal_driver/Src/stm32f4xx_hal_pwr.c
    ${CMAKE_CURRENT_SOURCE_DIR}/stm32f4xx_hal_driver/Src/stm32f4xx_hal_pwr_ex.c
    ${CMAKE_CURRENT_SOURCE_DIR}/stm32f4xx_hal_driver/Src/stm32f4xx_hal_qspi.c
    ${CMAKE_CURRENT_SOURCE_DIR}/stm32f4xx_hal_driver/Src/stm32f4xx_hal_rcc.c
    ${CMAKE_CURRENT_SOURCE_DIR}/stm32f4xx_hal_driver/Src/stm32f4xx_hal_rcc_ex.c
    ${CMAKE_CURRENT_SOURCE_DIR}/stm32f4xx_hal_driver/Src/stm32f4xx_hal_rng.c
    ${CMAKE_CURRENT_SOURCE_DIR}/stm32f4xx_hal_driver/Src/stm32f4xx_hal_rtc.c
    ${CMAKE_CURRENT_SOURCE_DIR}/stm32f4xx_hal_driver/Src/stm32f4xx_hal_rtc_ex.c
    ${CMAKE_CURRENT_SOURCE_DIR}/stm32f4xx_hal_driver/Src/stm32f4xx_hal_sai.c
    ${CMAKE_CURRENT_SOURCE_DIR}/stm32f4xx_hal_driver/Src/stm32f4xx_hal_sai_ex.c
    ${CMAKE_CURRENT_SOURCE_DIR}/stm32f4xx_hal_driver/Src/stm32f4xx_hal_sd.c
    ${CMAKE_CURRENT_SOURCE_DIR}/stm32f4xx_hal_driver/Src/stm32f4xx_hal_sdram.c
    ${CMAKE_CURRENT_SOURCE_DIR}/stm32f4xx_hal_driver/Src/stm32f4xx_hal_smartcard.c
    ${CMAKE_CURRENT_SOURCE_DIR}/stm32f4xx_hal_driver/Src/stm32f4xx_hal_smbus.c
    ${CMAKE_CURRENT_SOURCE_DIR}/stm32f4xx_hal_driver/Src/stm32f4xx_hal_spdifrx.c
    ${CMAKE_CURRENT_SOURCE_DIR}/stm32f4xx_hal_driver/Src/stm32f4xx_hal_spi.c
    ${CMAKE_CURRENT_SOURCE_DIR}/stm32f4xx_hal_driver/Src/stm32f4xx_hal_sram.c
    ${CMAKE_CURRENT_SOURCE_DIR}/stm32f4xx_hal_driver/Src/stm32f4xx_hal_tim.c
    ${CMAKE_CURRENT_SOURCE_DIR}/stm32f4xx_hal_driver/Src/stm32f4xx_hal_tim_ex.c
    ${CMAKE_CURRENT_SOURCE_DIR}/stm32f4xx_hal_driver/Src/stm32f4xx_hal_timebase_rtc_alarm_template.c
    ${CMAKE_CURRENT_SOURCE_DIR}/stm32f4xx_hal_driver/Src/stm32f4xx_hal_timebase_rtc_wakeup_template.c
    ${CMAKE_CURRENT_SOURCE_DIR}/stm32f4xx_hal_driver/Src/stm32f4xx_hal_timebase_tim_template.c
    ${CMAKE_CURRENT_SOURCE_DIR}/stm32f4xx_hal_driver/Src/stm32f4xx_hal_uart.c
    ${CMAKE_CURRENT_SOURCE_DIR}/stm32f4xx_hal_driver/Src/stm32f4xx_hal_usart.c
    ${CMAKE_CURRENT_SOURCE_DIR}/stm32f4xx_hal_driver/Src/stm32f4xx_hal_wwdg.c
)
]]

add_library(stdrivers STATIC ST_HAL_DRV_SRCS)
install(TARGETS stdrivers DESTINATION lib${LIB_SUFFIX})