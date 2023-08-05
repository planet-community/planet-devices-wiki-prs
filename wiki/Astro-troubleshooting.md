# Astro: Troubleshooting

## Booting stuck after enabling Zygisk in Magisk

To disable Zygisk, connect the device to your computer, and while it's stuck booting:

```
$ adb shell
Astro:/ $ su
Astro:/ # magisk --sqlite 'select * from settings'
key=su_biometric|value=0
key=zygisk|value=1
key=denylist|value=0
Astro:/ # magisk --sqlite "update settings set value=0 WHERE key='zygisk'"
Astro:/ # exit
Astro:/ $ exit
$ adb reboot
```
