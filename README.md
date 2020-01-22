# Blinky application using the Mbed2 source code

This is a simple example app to demonstrate how to build Mbed 2 applications from the source code.

## Requirements

Ensure Mbed CLI is installed and working:

```
mbed --version
```

## Steps

1. Download and install the application.
  ```
  mbed import https://github.com/MarceloSalazar/mbed2-blinky
  ```

2. Compile using the `release` profile
  ```
  cd mbed2-blinky
  mbed compile -t ARM -m NUCLEO_F031K6 --profile=release -v
  ```
  After 5 seconds, you should get the application compiled:

  ```
  | Module          |       .text |     .data |      .bss |
  |-----------------|-------------|-----------|-----------|
  | [lib]\cpprt_p.l |     68(+68) |     0(+0) |     0(+0) |
  | [lib]\mc_p.l    |   694(+694) |     4(+4) |   40(+40) |
  | [lib]\mf_p.l    |   172(+172) |     0(+0) |     0(+0) |
  | anon$$obj.o     |     32(+32) |     0(+0) |     0(+0) |
  | main.o          |     88(+88) |     0(+0) |   28(+28) |
  | mbed\drivers    |   228(+228) |     0(+0) | 100(+100) |
  | mbed\hal        | 1270(+1270) |     6(+6) |   64(+64) |
  | mbed\platform   | 1520(+1520) | 124(+124) | 393(+393) |
  | mbed\targets    | 4820(+4820) |   12(+12) | 212(+212) |
  | Subtotals       | 8892(+8892) | 146(+146) | 837(+837) |
  Total Static RAM memory (data + bss): 983(+983) bytes
  Total Flash memory (text + data): 9038(+9038) bytes

  Image: .\BUILD\NUCLEO_F031K6\ARM-RELEASE\mbed2-blinky.bin
  ```

3. Program the platform by copying the binary file to the Mbed drive
