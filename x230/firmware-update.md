# Firmware Update

This guide describes how to update the Heads firmware of the NitroPad.

These instructions are relevant in the following cases:

- You want to update the Heads firmware.
- You have already performed an OEM factory reset, but the TPM  counter has not been reset.


### Preparation

1. Connect your NitroPad to a power plug and load its battery to over 70%
2. Download the [latest firmware](https://github.com/Nitrokey/heads/releases) and store it on a USB drive. The files are in the "Assets" dropdown box at the end of the release information.
3. For hash sum verification, store `SHA256SUM.txt` file at the USB drive. 

E.g. for `v1.1-rc3` version:
1. Firmware should be downloaded from  [here](https://github.com/Nitrokey/heads/releases/tag/v1.1-rc3)
2. Firmware and hashsum files should be located on the USB drive in the main directory:
```
/nitropad_x230_v1.1-rc3.rom
/SHA256SUM.txt
```

#### Firmware file verification

It is mandatory to run a firmware file consistency check before writing it to the device. 
After copying the firmware file to the USB drive make sure the latter is properly unmounted/ejected to avoid write issues. The consistency check should be run on NitroPad, so the data verified will be exact same as the later read by the update application.


1. Start Nitropad and open recovery console from `Options -> Exit to recovery shell`
2. Execute the following to verify the firmware:
```
$ mount-usb              # select USB device
$ cd /media
$ sha256sum -c SHA256SUM.txt
```
For `v1.1-rc3` version this should result in:
```
$ sha256sum -c SHA256SUM.txt
nitropad_x230_v1.1-rc3.rom: OK
```
This confirms the content of the file is as expected.

### Procedure

This is the actual update procedure. Usually the first two screens will not be shown - in that case please start from step 3.


1. (Optional screen) Select "Ignore error and continue to default boot menu".

![img1](./images/firmware-update/1.jpg)

2. (Optional screen) Select "Ignore error and continue to default boot menu".

![img2](./images/firmware-update/2.jpg)

3. Go to "Options".

![img3](./images/firmware-update/3.jpg)

4. Select "Flash/Update the BIOS".

![img4](./images/firmware-update/4.jpg)

5. Please confirm the first option.

![img5](./images/firmware-update/5.jpg)

6. Confirm the process with Enter.

![img6](./images/firmware-update/6.jpg)

7. Select the desired .rom file.

![img7](./images/firmware-update/7.jpg)

8. Confirm the process with Enter.

![img8](./images/firmware-update/8.jpg)

9. Confirm the restart with Enter.

![img9](./images/firmware-update/9.jpg)

Now you have updated your firmware.

### Further steps
In case `ERROR: TOTP Generation Failed!` screen will show up, please follow the instructions for Factory Reset (on the left side menu), starting from step 11.
