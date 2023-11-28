# Jamu Youtube 🗿

A Zygisk module which fix "ctsProfileMatch" (SafetyNet) and "MEETS_DEVICE_INTEGRITY" (Play
Integrity).

To use this module you must have one of this:

- Magisk with Zygisk enabled.
- KernelSU with [ZygiskNext](https://github.com/Dr-TSNG/ZygiskNext) module installed.

[**Download the latest here**](https://github.com/febjnck/jamuyoutube/releases/latest).

## Donations

- [Saweria](https://saweria.com/febjnck)

## About module

Jamu buat nge-Fix YouTube Premium 4 Bulan 🗿

## Failing BASIC verdict

If you are failing basicIntegrity (SafetyNet) or MEETS_BASIC_INTEGRITY (Play Integrity) something is
wrong in your setup. My recommended steps in order to find the problem:

- Disable all modules except mine.
- Check your SELinux (must be enforced).

Some modules which modify system can trigger DroidGuard detection, never hook GMS processes.

## Certify Play Store and fix Google Wallet

Follow this steps:

- Flash my module in Magisk/KernelSU (if you already have my module, just ignore this step).
- Clear Google Wallet cache (if you have it).
- Clear Google Play Store cache and data.
- Clear Google Play Services (com.google.android.gms) cache and data (Optionally skip clearing data and wait some time, ~24h, for it to resolve on its own).
- Reboot

## Troubleshooting

### Fails to meet device integrity (KernelSU)

- Disable ZygiskNext
- Reboot
- Enable ZygiskNext

### Passes device integrity, but fails in Wallet (even after clearing cache)

- Remove all data from Google Play Services

<details>
<summary>Guide</summary>

![Google services cache](./wallet-troubleshoot-1.jpg)
![Clear Storage](./wallet-troubleshoot-2.jpg)
![Clear All Data](./wallet-troubleshoot-3.jpg)

</details>

## Read module logs

You can read module logs using this command:

```
adb shell "logcat | grep 'PIF'"
```

## Can this module pass MEETS_STRONG_INTEGRITY?

No.
