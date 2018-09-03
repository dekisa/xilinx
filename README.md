# xilinx

Documentation \
[Trenz Starter Kit 720](https://wiki.trenz-electronic.de/display/PD/Starter+Kit+720) \
[Zynq-7000 SoC Technical Reference Manual](https://www.xilinx.com/support/documentation/user_guides/ug585-Zynq-7000-TRM.pdf#nameddest=xPSPLMIOEMIOSignalsAndInterfaces)\
[UltraFast Embedded Design Methodology Guide](https://www.xilinx.com/support/documentation/sw_manuals/ug1046-ultrafast-design-methodology-guide.pdf):
[Chapter 3: Hardware Design Considerations - Dataflow](https://www.xilinx.com/support/documentation/sw_manuals/ug1046-ultrafast-design-methodology-guide.pdf#G5.385115)\
[AXI Stream FIFO](https://www.xilinx.com/support/documentation/ip_documentation/axi_fifo_mm_s/v4_1/pg080-axi-fifo-mm-s.pdf)

Guides \
[Xilinx Wiki](http://www.wiki.xilinx.com/Technical%20Articles)\
[Vivado Design Suite Tutorial Embedded Processor Hardware Design](https://www.xilinx.com/support/documentation/sw_manuals/xilinx2018_1/ug940-vivado-tutorial-embedded-design.pdf)\
[Zynq-7000 All Programmable SoC: Embedded Design Tutorial](https://www.xilinx.com/support/documentation/sw_manuals/xilinx2018_1/ug1165-zynq-embedded-design-tutorial.pdf)\
[FPGAdeveloper Creating a custom AXI-Streaming IP in Vivado](http://www.fpgadeveloper.com/2017/11/creating-a-custom-axi-streaming-ip-in-vivado.html)

Petalinux\
[Petalinux Reference Guide](https://www.xilinx.com/support/documentation/sw_manuals/xilinx2018_1/ug1144-petalinux-tools-reference-guide.pdf)\
[PetaLinux Tools Documentation](https://www.xilinx.com/support/documentation/sw_manuals/xilinx2018_1/ug1157-petalinux-tools-command-line-guide.pdf)

AXI\
[Introduction to AXI Protocol](https://www.aldec.com/en/company/blog/122--introduction-to-axi-protocol) \
[AMBA® AXI Protocol Specification](http://mazsola.iit.uni-miskolc.hu/~drdani/docs_arm/AMBAaxi.pdf) \
[Vivado Design Suite AXI Reference Guide](https://www.xilinx.com/support/documentation/ip_documentation/axi_ref_guide/latest/ug1037-vivado-axi-reference-guide.pdf) \
[AXI4-Stream Infrastructure IP Suite v2.2 LogiCORE IP Product Guide](https://www.xilinx.com/support/documentation/ip_documentation/axis_infrastructure_ip_suite/v1_1/pg085-axi4stream-infrastructure.pdf)

Pinned\
[Zynq-7000 SoC XADC](https://www.xilinx.com/support/documentation/user_guides/ug480_7Series_XADC.pdf)\
[https://kb.ettus.com/X300/X310](https://kb.ettus.com/X300/X310)\
ethernet: [1G/2.5G Ethernet PCS/PMA or SGMII v16.1 LogiCORE IP Product Guide](https://www.xilinx.com/support/documentation/ip_documentation/gig_ethernet_pcs_pma/v16_1/pg047-gig-eth-pcs-pma.pdf)\
emmmc: [Trenz guide](https://wiki.trenz-electronic.de/display/TE0720/eMMC)\
[fpga common mistakes](http://class.ece.iastate.edu/cpre488/resources/ISU_488_common_mistakes.pdf)\
[FTN IP jezgro za enkripciju podataka sa AXI interfejsom](http://www.ftn.uns.ac.rs/n144778477/ip-jezgro-za-enkripciju-podataka-sa-axi-interfejsom)

notes:\
Create a BOOT.BIN file for a Zynq family device that includes FIT image.
```
petalinux-package --boot --format BIN --u-boot --kernel -o ./BOOT.bin
```

Create a BOOT.BIN file for a Zynq family device that includes BIT file.
```
petalinux-package --boot --format BIN --fsbl $FSBL --fpga --u-boot -o $BOOTBIN 
```

Industrial IO\
https://01.org/linuxgraphics/gfx-docs/drm/driver-api/iio/index.html \
https://wiki.analog.com/resources/tools-software/linux-drivers/iio-adc/ad7887 \
https://wiki.analog.com/resources/tools-software/linux-software/iio_oscilloscope \
https://events.static.linuxfound.org/sites/events/files/slides/iio_high_speed.pdf \
https://github.com/analogdevicesinc/iio-oscilloscope \
https://git.kernel.org/pub/scm/linux/kernel/git/torvalds/linux.git/tree/drivers/iio/adc/ad7887.c?id=HEAD \
https://wiki.analog.com/software/linux/docs/iio/iio-trig-bfin-timer

axidma driver\
https://github.com/bperez77/xilinx_axidma/issues/24
https://github.com/bperez77/xilinx_axidma

