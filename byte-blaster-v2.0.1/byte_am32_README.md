# byte_am32 V2 (2.0.0)

Use with Byte Blaster RP2040 firmware and configurator **2.0.0** on both ESCs.
Target: `F4A_4IN1_F421`. This hardware-specific build is not a universal
image for boards sharing that target name; confirm board revision and electrical
compatibility before flashing. Keep the configurator target check enabled.

Back up settings, install the controller UF2, then load the byte_am32 HEX through
the configurator ESC Firmware tab and update both compatible ESCs. Power-cycle,
review settings, verify directions and telemetry, then re-run FF/PID tuning.
The BIN is an application image, not a bootloader or complete MCU flash dump.

The matching modified source, build instructions, GPLv3 license and upstream
notices are included in **byte_am32_source_v2.0.0.zip** alongside these binaries. Extract it
and read BUILD_BYTE_AM32.md. The build wrapper selects the release configuration
and verifies the resulting HEX/BIN against the distributed hashes.

Stock AM32 does not provide full Byte V2 protocol compatibility. Firmware branding
does not add a device-side version handshake or certify sensor calibration.
