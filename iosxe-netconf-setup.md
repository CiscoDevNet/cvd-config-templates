#Enabling NETCONF on IOSXE

1. Setup AAA and SSH to be ready for NETCONF over SSH. You may not need these steps if your device is already setup for SSH access.

   ````
   Device>enable
   Device#configure terminal

   Device(config)#hostname AD3-9300
   AD3-9300(config)#ip domain-name cisco.com

   AD3-9300(config)#aaa new-model
   AD3-9300(config)#aaa authentication login default local
   AD3-9300(config)#aaa authorization exec default local
   AD3-9300(config)#username user priviledge 15 password pass

   AD3-9300(config)#crypto key generate rsa
   AD3-9300(config)#ip ssh version 2

   ````


2. Enable NETCONF on the device.

   ```
   AD3-9300>enable
   AD3-9300#configure terminal

   AD3-9300(config)#netconf-yang
   ```