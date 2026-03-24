# ATU-100 as Remote Outdoor Antenna Tuner

Remote outdoor build of the ATU-100 automatic antenna tuner (based on N7DDC design).
Installed at antenna feedpoint to reduce feedline losses and improve matching efficiency.

## Hardware
- Design: ATU-100 N7DDC
- MCU: PIC16F1938

## Enclosure
- Model: ZP150.100.45UJPH TM ABSPC KRADEX
- Product link: https://www.tme.eu/pl/details/zp15010045ujphabsp/obudowy-uniwersalne/kradex/zp150-100-45ujph-tm-abspc/

## Firmware / Configuration
```
> ./pk2cmd -PPIC16F1938 -A5.0 -GE0-FF
Read successfully.

EEData Memory
0000 78  05  01  15  13  01  00  00  
0008 00  00  07  00  07  00  01  00  
0010 00  50  01  10  02  20  04  50  
0018 10  00  22  00  45  00  FF  FF  
0020 00  10  00  22  00  47  01  00  
0028 02  20  04  70  10  00  FF  FF  
0030 00  10  00  01  00  00  FF  FF  
0038 FF  FF  FF  FF  FF  FF  FF  FF  
0040 FF  FF  FF  FF  FF  FF  FF  FF  
0048 FF  FF  FF  FF  FF  FF  FF  FF  
0050 FF  FF  FF  FF  FF  FF  FF  FF  
0058 FF  FF  FF  FF  FF  FF  FF  FF  
0060 FF  FF  FF  FF  FF  FF  FF  FF  
0068 FF  FF  FF  FF  FF  FF  FF  FF  
0070 FF  FF  FF  FF  FF  FF  FF  FF  
0078 FF  FF  FF  FF  FF  FF  FF  FF  
0080 FF  FF  FF  FF  FF  FF  FF  FF  
0088 FF  FF  FF  FF  FF  FF  FF  FF  
0090 FF  FF  FF  FF  FF  FF  FF  FF  
0098 FF  FF  FF  FF  FF  FF  FF  FF  
00A0 FF  FF  FF  FF  FF  FF  FF  FF  
00A8 FF  FF  FF  FF  FF  FF  FF  FF  
00B0 FF  FF  FF  FF  FF  FF  FF  FF  
00B8 FF  FF  FF  FF  FF  FF  FF  FF  
00C0 FF  FF  FF  FF  FF  FF  FF  FF  
00C8 FF  FF  FF  FF  FF  FF  FF  FF  
00D0 FF  FF  FF  FF  FF  FF  FF  FF  
00D8 FF  FF  FF  FF  FF  FF  FF  FF  
00E0 FF  FF  FF  FF  FF  FF  FF  FF  
00E8 FF  FF  FF  FF  FF  FF  FF  FF  
00F0 FF  FF  FF  FF  FF  FF  FF  FF  
00F8 FF  FF  FF  7B  01  01  2C  38  

Operation Succeeded
```

---

## Assembly

![PCB 1](resources/pcb_1.jpeg)

---

## Case Build & Weatherproofing

A 3 mm plexiglass (PMMA) plate was laser-cut and used as an internal mounting frame for the PCB and display.  

![Case 1](resources/case_1.jpeg)
![Case 2](resources/case_2.jpeg)
![Case 3](resources/case_3.jpeg)
![Case 4](resources/case_4.jpeg)
![Case 5](resources/case_5.jpeg)
![Case 6](resources/case_6.jpeg)
![Case 7](resources/case_7.jpeg)
![Case 8](resources/case_8.jpeg)
![Case 9](resources/case_9.jpeg)
![Case 10](resources/case_10.jpeg)
![Case 11](resources/case_11.jpeg)
![Case 12](resources/case_12.jpeg)

---

## Mounting on Balcony Railing

For installation on a balcony railing, a dedicated mounting bracket was designed and 3D-printed using ABS material.
The bracket was required to securely attach the unit and provide stable support against the railing.

![Mount 1](resources/mount_1.jpeg)
![Mount 2](resources/mount_2.jpeg)
![Mount 3](resources/mount_3.jpeg)
![Mount 4](resources/mount_4.jpeg)
![Mount 5](resources/mount_5.jpeg)
![Mount 6](resources/mount_6.jpeg)
![Mount 7](resources/mount_7.jpeg)
![Mount 8](resources/mount_8.jpeg)
![Mount 9](resources/mount_9.jpeg)
![Mount 10](resources/mount_10.jpeg)

## Summary

The ATU-100 is a limited, low-performance tuner, but its constraints are well understood and predictable.
Considering these limitations upfront, the overall build should be regarded as successful. While not fully autonomous and requiring occasional user intervention, the tuner is capable of effectively matching the antenna in this specific use case.

## ATU-100 drawbacks

The ATU-100 is a low-cost solution with a simplified measurement system based on a tandem match, providing only forward and reflected power readings.
This approach is insufficient for fast and optimal tuning. The algorithm lacks key parameters such as impedance and phase information, which are available in higher-end tuners like the AH-4 and CG3000.
Additionally, the ATU-100 does not measure frequency, so it cannot recall previous tuning states. It also lacks a built-in attenuator, exposing the transmitter to high SWR during the tuning process.