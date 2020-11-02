# Android Flash Rom Instructions

## What's Needed

- Rom.zip
- platform-tools (adb, fastboot)
- twrp.iso

## Steps

1. Connect device with PC and make sure developer option is enabled, navigate to `/platform-tools`, run

```
adb reboot bootloader
```

2. Copy `twrp.iso` into `/platform-tools`, run

```
fastboot flash recovery twrp.img
fastboot reboot
```

3. This will install `twrp` onto the device, run this to go to recovery everytime

```
adb reboot recovery
```

4. Do a clean `Wipe`, and click on `Mount` to format just the `Data` folder.

5. Push the zipped rom file onto device, make sure to move that zipped rom to the same directory as `adb`,

```
adb push PixExp-10-PORT-clover-20200515.zip /sdcard
```

6. Wait for that to finish (~ 40s), and click `Install` on TWRP to find the zipped file

7. Done
