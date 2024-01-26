# Infinite-ISP
Infinite-ISP is a full-stack ISP development platform - from algorithm development to RTL design, FPGA/ASIC implementation, and associated firmware, tools, etc. It offers a unified platform that empowers ISP developers to accelerate ISP innovation. It includes a complete collection of camera pipeline modules written in Python, an FPGA bitstream & the associated Firmware for the implementation of the pipeline on the Kria KV260 development board, and lastly, a stand-alone Python-based Tuning Tool application for the pipeline.  The main components of the Infinite-ISP project are listed below:

| Repository name        | Description      | 
| -------------  | ------------- |
| **[Infinite-ISP_AlgorithmDesign](https://github.com/10x-Engineers/Infinite-ISP)**                        | Python based model of the Infinite-ISP pipeline for algorithm development |
| **[Infinite-ISP_ReferenceModel](https://github.com/10x-Engineers/Infinite-ISP_ReferenceModel)**                       | Python-based fixed-point model of the Infinite-ISP pipeline for hardware implementation |
| **[Infinite-ISP_FPGABinaries](https://github.com/10x-Engineers/Infinite-ISP_FPGABinaries)** :anchor:                 | FPGA binaries (bitstream + firmware executable) for the Xilinx® Kria KV260’s XCK26 Zynq UltraScale+ MPSoC |
| **[Infinite-ISP_Firmware](https://github.com/10x-Engineers/Infinite-ISP_Firmware)**                                   | Firmware for the Kria KV260’s embedded Arm® Cortex®A53 processor|
| **[Infinite-ISP_TuningTool](https://github.com/10x-Engineers/Infinite-ISP_TuningTool)**                               | Collection of calibration and analysis tools for the Infinite-ISP |


# Infinite-ISP FPGA Binaries
Infinite-ISP Image Signal Processing Pipeline FPGA binaries for XCK26 Zynq® UltraScale+™ MPSoC present on Xilinx® Kria™ KV260 Vision AI Starter Kit. Each binary file includes an FPGA bitstream paired with its firmware executable.

# How to use the FPGA Binary Files

## v1.2
### For AR1335 IAS module:
1. Connect AR1335 IAS image sensor module to the IAS1 port on Kria KV260 AI Starter Kit.
2. Insert SD Card (2GB or above) into the Kria KV260 board.
3. Connect the Kria KV260 board with a monitor screen using an HDMI cable.
4. Power up the Kria KV260 board and follow the [steps](https://docs.xilinx.com/r/en-US/ug1089-kv260-starter-kit/Ethernet-Recovery-Tool) for loading the on-board Xilinx Image Recovery Tool.
5. Upload the desired binary file (e.g. Infinite-ISP_v1.2-AR1335.bin) provided in the release on the Kria KV260 AI Starter Kit.
6. Reset the Kria KV260 board and visualize the Infinite-ISP output on your monitor screen.
7. Connect the USB cable with the JTAG/USB port on Kria to read the messages over the serial interface (baud rate 115200).
8. Select the required configuration by exploring the provided user menu:

<kbd>![status before dumping](/doc/v1.1/ar1335_1.png)</kbd> 

9. Once SD Card dumps are complete, you can remove the SD card from the Kria board.

<kbd>![status after dumping](/doc/v1.1/ar1335_2.png)</kbd> 

10. Extract the dumped single RAW-ISPout pair and Burst Capture frames from the SD card and visualize them using provided [scripts](/scripts).

## v1.1
### For AR1335 IAS module:
1. Connect AR1335 IAS image sensor module to the IAS1 port on Kria KV260 AI Starter Kit.
2. Insert SD Card (2GB or above) into the Kria KV260 board.
3. Connect the Kria KV260 board with a monitor screen using HDMI cable.
4. Power up the Kria KV260 board and follow the [steps](https://docs.xilinx.com/r/en-US/ug1089-kv260-starter-kit/Ethernet-Recovery-Tool) for loading the on-board Xilinx Image Recovery Tool.
5. Upload the desired binary file (e.g. Infinite-ISP_v1.1-AR1335-1080p.bin) provided in the release on the Kria KV260 AI Starter Kit.
6. Reset the Kria KV260 board and visualize the Infinite-ISP output on your monitor screen.
7. Connect the USB cable with the JTAG/USB port on Kria to read the messages over serial interface (baud rate 115200).
8. RAW-ISPout image pair and Burst Capture frames dump in SD Card status will be displayed over serial interface:

<kbd>![status before dumping](/doc/v1.1/ar1335_1.png)</kbd> 

9. Once SD Card dumps are complete, you can remove the SD card from the Kria board.

<kbd>![status after dumping](/doc/v1.1/ar1335_2.png)</kbd> 

10. Extract the dumped single RAW-ISPout pair and Burst Capture frames from the SD card and visualize them using provided [scripts](/scripts).

### For OV5647 image sensor module:
1. Connect OV5647 image sensor module to the RPi port on Kria KV260 AI Starter Kit.
2. Insert SD Card (2GB or above) into the Kria KV260 board.
3. Connect the Kria KV260 board with a monitor screen using HDMI cable.
4. Power up the Kria KV260 board and follow the [steps](https://docs.xilinx.com/r/en-US/ug1089-kv260-starter-kit/Ethernet-Recovery-Tool) for loading the on-board Xilinx Image Recovery Tool.
5. Upload the desired binary file (e.g. Infinite-ISP_v1.1-OV5647-1080p.bin) provided in the release on the Kria KV260 AI Starter Kit.
6. Reset the Kria KV260 board and visualize the Infinite-ISP output on your monitor screen.
7. Connect the USB cable with the JTAG/USB port on Kria to read the messages over serial interface (baud rate 115200).
8. RAW-ISPout image pair and Burst Capture frames dump in SD Card status will be displayed over serial interface:

<kbd>![status before dumping](/doc/v1.1/ov5647_1.png)</kbd>

9. Once SD Card dumps are complete, you can remove the SD card from the Kria board.

<kbd>![status before dumping](/doc/v1.1/ov5647_2.png)</kbd>

10. Extract the dumped single RAW-ISPout pair and Burst Capture frames from the SD card and visualize them using provided [scripts](/scripts).

## v1.0
1. Connect the AR1335 IAS image sensor module (included in Xilinx Kria KV260 Accessory Pack) to the IAS1 port on the Kria KV260 AI Starter Kit.
2. Insert an SD Card (2GB or above) into the Kria KV260 board.
3. Connect the Kria KV260 board with a monitor screen using an HDMI cable.
4. Power up the Kria KV260 board and follow the [steps](https://docs.xilinx.com/r/en-US/ug1089-kv260-starter-kit/Ethernet-Recovery-Tool) for loading the on-board Xilinx Image Recovery Tool.
5. Upload the desired binary file (e.g. 'Infinite-ISP_v1.0-1080p.bin') on the Kria KV260 AI Starter Kit.
6. Reset the Kria KV260 board and visualize the Infinite-ISP output on your monitor screen.
7. Connect the USB cable with the JTAG/USB port on Kria to read the messages over serial interface (baud rate 115200).
8. You can remove the SD card from the Kria board, extract the dumped single RGB-RAW pair and 300 RGB frames (if applicable), and visualize them using the provided scripts.

## Scripts for visualization of FPGA outputs in SD Card
| Name | Description |
| -----| ----- |
| sensor_bin_to_sensor_raw.py | converts the image sensor memory dump (.bin) data from the FPGA Platform to Bayer RAW frame (.raw) containing valid pixel data. |
| isp_output_bin_to_isp_output_png.py | converts the ISP output memory dump (.bin) data from the FPGA Platform to output image frame (.png) as well as output pixel data frame (.bin) for verification. |
| sensor_bin_to_sensor_raw_burst_capture.py | converts the image sensor memory dumps (.bin) of RAW Burst Capture from the FPGA Platform to Bayer RAW frames (.raw) containing valid pixel data. It also converts the Bayer RAW frames to equivalent grayscale .png for visualization. |
| video_creation.py | converts multiple ISP output memory dumps (.bin) from the FPGA Platform to corresponding output image frames (.png) and stitches them together into a .mp4 video. |

## Contact
For any inquiries or feedback, feel free to reach out.

Email: isp@10xengineers.ai

Website: http://www.10xengineers.ai

LinkedIn: https://www.linkedin.com/company/10x-engineers/
