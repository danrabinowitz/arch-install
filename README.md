# Usage:

1. Create the custom ISO by running:
```
./create_iso
```

2. Burn the ISO to a USB flash drive by following the output of the previous step.

3. Boot from the custom ISO

4. Start the install with:
```
/run/archiso/bootmnt/custom_files/install/usr/local/sbin/custom-init1
```

5. As per the output of the previous command:
```
ssh-keygen -R 192.168.5.120 && ssh inspiron3000
/usr/local/sbin/custom-run-remote-setup-script
```

6. After reboot, login as root


# TODO:

* Use `rankmirrors` to find best mirrors automatically
