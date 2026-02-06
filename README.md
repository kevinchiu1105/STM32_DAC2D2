# STM32_DAC2D2
Cache Coherency: Because the H7 has D-Cache, you must invalidate the cache for the destination buffer (SCB_InvalidateDCache_by_Addr) after a DMA transfer, or use non-cacheable memory (e.g., AXI SRAM or D3 SRAM).
Alignment: Data buffers should ideally be 32-byte aligned.
Alternative: For more complex operations, HAL_DMA2D_Start_IT can be used to initiate non-blocking transfers with interrupts. 

Ref
L8圖像格式
https://support.touchgfx.com/zh-TW/docs/development/ui-development/scenarios/using-the-l8-image-format-to-reduce-memory-consumption
https://www.st.com/content/ccc/resource/training/technical/product_training/group0/a1/73/3f/fd/cb/1c/4b/23/STM32H7-System-ChromART_DMA2D/files/STM32H7-System-ChromART_DMA2D.pdf/_jcr_content/translations/en.STM32H7-System-ChromART_DMA2D.pdf
