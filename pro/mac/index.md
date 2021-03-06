# Nitrokey Pro, Mac

1. Once you plug in the Nitrokey, your computer will start the Keyboard Setup Assistant. **Don't run through this assistant but exit it right away.**
2. Download and start the [Nitrokey App](https://www.nitrokey.com/download). Follow the [instructions](https://www.nitrokey.com/documentation/change-user-and-admin-pin) to change the default User PIN (default: 123456) and Admin PIN (default: 12345678) to your own choices.

![img](./images/App-change-pin.png)

Your Nitrokey is now ready to use. [Checkout](https://www.nitrokey.com/documentation/applications) the various use cases and supported applications.

::: tip  Note 
- For some Versions of MacOS it is necessary to install custom [ccid driver](https://github.com/martinpaljak/osx-ccid-installer) (for information see [here](https://ludovicrousseau.blogspot.com/2016/04/os-x-el-capitan-and-ccid-driver-upgrades.html)), but in general MacOS should have the driver onboard. 
- For many use cases described, it is necessary to have either OpenPGP or S/MIME keys installed on the device (see below).
:::
## Key Creation with OpenPGP or S/MIME
There are two widely used standards for email encryption. While OpenPGP/GnuPG is popular among individuals, S/MIME/x.509 is mostly used by enterprises. If you are in doubt which one to choose, you should use OpenPGP.

- [instructions](https://www.nitrokey.com/documentation/openpgp-email-encryption) for using the OpenPGP standard with the Nitrokey
- [instructions](https://www.nitrokey.com/documentation/smime-email-encryption) for using S/MIME with the Nitrokey
