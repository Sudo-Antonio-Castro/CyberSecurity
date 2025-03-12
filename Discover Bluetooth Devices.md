# Discover Bluetooth Devices

In this video, we will use the Terminal to scan for active Bluetooth devices.



https://github.com/user-attachments/assets/673223e3-2a83-40e4-941c-58ba931a0f74



## Questions

1. *How many devices were found?*
2. *How many of the scanned devices were alive and in range?*
3. *What Bluetooth services are available on the Laptop?*
4. *What is the class ID number for the Speaker?*

### Walkthrough

1. Open Terminal.
2. Use **hciconfig** to view onboard Bluetooth adapter.
3. Use **hciconfig hci0 up** to initialize the adapter.
4. Use **hciconfig** to verify operation.
5. Use **hcitool scan** to scan for Bluetooth devices.
6. Use **l2ping X:X:X:X:X:X** to check device is in range.
7. Use **sdptool browse X:X** to view services on Laptop.
8. Use **hcitool inq** to view class and clock offset.

**Commands**

[**hciconfig**](https://linux.die.net/man/8/hciconfig#:~:text=hciconfig%20is%20used%20to%20configure,devices%20installed%20in%20the%20system.) 
: is used to configure Bluetooth devices. hciX is the name of a Bluetooth device installed in the system.

[**hcitool**](https://linux.die.net/man/1/hcitool)
: is used to configure Bluetooth connections and send some special command to Bluetooth devices.

[**l2ping**](https://linux.die.net/man/1/l2ping#:~:text=bd_addr-,Description,given%20in%20dotted%20hex%20notation.)
: sends a L2CAP echo request to the Bluetooth MAC address bd_addr given in dotted hex notation.

[**sdptool**](https://linux.die.net/man/1/sdptool)
: provides the interface for performing SDP queries on Bluetooth devices, and administering a local sdpd.
