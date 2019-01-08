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
[FPGAdeveloper Creating a custom AXI-Streaming IP in Vivado](http://www.fpgadeveloper.com/2017/11/creating-a-custom-axi-streaming-ip-in-vivado.html)\
[Serial emulation over USB](http://www.wiki.xilinx.com/Zynq-7000+AP+SoC+USB+CDC+Device+Class+Design+Example+Techtip)

Petalinux\
[Petalinux Reference Guide](https://www.xilinx.com/support/documentation/sw_manuals/xilinx2018_1/ug1144-petalinux-tools-reference-guide.pdf)\
[PetaLinux Tools Documentation](https://www.xilinx.com/support/documentation/sw_manuals/xilinx2018_1/ug1157-petalinux-tools-command-line-guide.pdf)

AXI\
[Introduction to AXI Protocol](https://www.aldec.com/en/company/blog/122--introduction-to-axi-protocol) \
[AMBA® AXI Protocol Specification](http://mazsola.iit.uni-miskolc.hu/~drdani/docs_arm/AMBAaxi.pdf) \
[Vivado Design Suite AXI Reference Guide](https://www.xilinx.com/support/documentation/ip_documentation/axi_ref_guide/latest/ug1037-vivado-axi-reference-guide.pdf) \
[AXI4-Stream Infrastructure IP Suite v2.2 LogiCORE IP Product Guide](https://www.xilinx.com/support/documentation/ip_documentation/axis_infrastructure_ip_suite/v1_1/pg085-axi4stream-infrastructure.pdf)

Source\
[AXI Fifo Driver](https://github.com/torvalds/linux/blob/master/drivers/staging/axis-fifo/axis-fifo.c)

Current probe\
test_board project
````
/xilinx/bgw_current_probe_design
````
IP repo (adc reading and adc emulation)
````
~/xilinx/bgw_current_probe_design/ip_repo
````
TE FSBL (for USB device)
````
~/xilinx/test_board_stream/test_board/os/petalinux/zynq_fsbl_te.elf
````

Pinned\
[Zynq-7000 SoC XADC](https://www.xilinx.com/support/documentation/user_guides/ug480_7Series_XADC.pdf)\
[https://kb.ettus.com/X300/X310](https://kb.ettus.com/X300/X310)\
ethernet: [1G/2.5G Ethernet PCS/PMA or SGMII v16.1 LogiCORE IP Product Guide](https://www.xilinx.com/support/documentation/ip_documentation/gig_ethernet_pcs_pma/v16_1/pg047-gig-eth-pcs-pma.pdf)\
emmmc: [Trenz guide](https://wiki.trenz-electronic.de/display/TE0720/eMMC)\
[fpga common mistakes](http://class.ece.iastate.edu/cpre488/resources/ISU_488_common_mistakes.pdf)\
[FTN IP jezgro za enkripciju podataka sa AXI interfejsom](http://www.ftn.uns.ac.rs/n144778477/ip-jezgro-za-enkripciju-podataka-sa-axi-interfejsom)\
https://opsero.com/products/ 
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

udp\
https://gist.github.com/cslarsen/11339448 \
https://docs.python.org/2/howto/sockets.html \
https://wiki.python.org/moin/UdpCommunication \
https://www.cs.cmu.edu/afs/cs/academic/class/15213-f99/www/class26/udpclient.c \

usb device \
[TE7020 Schematic](https://www.trenz-electronic.de/fileadmin/docs/Trenz_Electronic/Modules_and_Module_Carriers/4x5/TE0720/REV03/Documents/SCH-TE0720-03-1CF.PDF)\
[TE0703 Schematic](https://www.trenz-electronic.de/fileadmin/docs/Trenz_Electronic/Modules_and_Module_Carriers/4x5/4x5_Carriers/TE0703/REV05/Documents/SCH-TE0703-05.PDF)\
[https://elinux.org/images/8/83/USB3320-datasheet.pdf](https://elinux.org/images/8/83/USB3320-datasheet.pdf)\
[Zynq-7000 AP SoC USB CDC Device Class Design Example Techtip](http://www.wiki.xilinx.com/Zynq-7000+AP+SoC+USB+CDC+Device+Class+Design+Example+Techtip)

usb device sardware modifications:
1) Remove USB type A J6
2) Solder µUSB type B J12
3) Remove CM choke L87 and solder it on L4
4) Replace resistor R5 (size 0402) by 1K +/-5%  resistor
5) Replace capacitor C27 (size 0805) with 1-6.5µF (>10V).
6) Remove capacitor C5

usb device software modifications (or skip steps 1-3 and flash precompiled binary zynq_fsbl_te.elf)
1) Create first stage bootloader project from template in EDS
2) Modify according to Trenz FSBL
3) Complie and flash
4) For linux drivers see [Zynq-7000 AP SoC USB CDC Device Class Design Example Techtip](http://www.wiki.xilinx.com/Zynq-7000+AP+SoC+USB+CDC+Device+Class+Design+Example+Techtip)
5) Additional Peralinux device tree modification:
/* USB PHY */
```
/{
    usb_phy0: usb_phy@0 {
        //compatible = "ulpi-phy";
        compatible = "usb-nop-xceiv";
        #phy-cells = <0>;
        reg = <0xe0002000 0x1000>;
        view-port = <0x0170>;
        drv-vbus;
    };
};

&usb0 {
    //dr_mode = "host";
    dr_mode = "peripheral";
    //dr_mode = "otg";
    usb-phy = <&usb_phy0>;
};
```
# Pinout - Clock capable pins
[Pin labels](https://www.xilinx.com/support/packagefiles/z7packages/xc7z020clg484pkg.txt) - P pins\
[XC7Z020 device pinout (pg. 41)](https://www.xilinx.com/support/documentation/user_guides/ug865-Zynq-7000-Pkg-Pinout.pdf#page=41) - MRCC, SRCC pins \
[Trenz TE720 pinout table](https://github.com/dekisa/xilinx/blob/master/doc/pin%20mapping/te0720_te0703_fpga_pinout_table.pdf)
