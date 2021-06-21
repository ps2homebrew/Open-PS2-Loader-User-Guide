.. _network_config:

**Network config**
==================

| ----
| *[Default are marked in bold / infos gathered from several posts /
  messages from SP193 – thanks to him]*

You can access the Network config settings screens by pressing |start|
from the games/apps pages then selecting Network config in the menu.
This screen allows you to set up your network config (captain obvious
:P) when you want to run your games using ethernet or if you want to
install your games on your HDD using HDL server.

These settings will be saved into conf_network.cfg file in mc#:/OPL
folder.

They are several important changes from OPL 0.9.2 :

| **1.** The control for the link speed and duplex options is now
  disabled by default, so that users will know that they are meant to be
  advanced options.
| **2.** DHCP support was added. If DHCP is used, then the user will not
  need to deal with IP addresses.
| **3.** NetBIOS address resolution was introduced, so that it is
  possible for the user to enter the computer’s name and to not
  know/worry about IP addresses.
| **4.** Network settings will now take effect immediately; it is no
  longer required to restart OPL.

.. image:: 1211205318-network-config.png
   :alt: title

**Network config screen :**

-  **Advanced options :** < **Off** / On > – when switched to ON, this
   option allows you to force a “custom” ethernet mode. See below.

-  **Ethernet link mode :** < **Auto** / 100Mbit (half/full)-duplex /
   10Mbit (half/full)-duplex > – this is an advanced option that should
   not be changed easily – as misconfiguring the link speed and duplex
   settings may likely give sub-standard performance and reliability and
   can cause communication break down. Default is auto
   (auto-negotiation) and it’s also the recommended setting. As far as
   possible, when auto-negociation fails, 100Mbit Full-Duplex mode
   should be used – unless not supported. When duplex option (full or
   half) is changed, it should be changed on both ends (PS2 and server).

**- PS2 –**

-  **IP adress type :** < **DHCP** / Static > – DHCP is the default and
   recommended setting. DHCP will assign a new available IP adress to
   your PS2 on your network at each OPL launch. To use it correctly, you
   need to enable DHCP in your router’s settings and reserve the PS2 IP
   address within it (so IP address that your PS2 is given will never be
   assigned to something else by the DHCP server). Use STATIC when you
   don’t use a router (when your PS2 is directly connected to your PC).

-  **IP adress :** **192.168.X.X** – only adjustable if your PS2 IP
   adress type is set to STATIC, grey-out if set to DHCP. IP address for
   your PS2.

-  **Mask :** **255.255.255.0** – only adjustable if your PS2 IP adress
   type is set to STATIC, grey-out if set to DHCP. The subnet mask for
   your network.

-  **Gateway :** **192.168.X.X** – only adjustable if your PS2 IP adress
   type is set to STATIC, grey-out if set to DHCP. It’s either the IP of
   your router if you use one (if you choose STATIC while using a
   router), or your PC IP adress if your PS2 is connected directly to
   your PC.

-  **DNS Server :** **192.168.X.X** – this setting is not required for
   SMB / HDL Server support. It’s required by the Network update
   feature. If you’re using a router/switch in your network, that is
   your DNS server.

----

**- SMB Server –**

-  **Adress Type :** < **NetBIOS** / IP > – NetBIOS allows you to enter
   the computer’s name instead of its IP address. It makes your PS2 able
   to locate the PC on the network, even if the IP address of the PC was
   changed (due to the PC being configured with DHCP for example). The
   computer’s name must be entered in capital letters (mandatory). Enter
   “hostname” in command prompt to get your computer’s name if you don’t
   know it (or right-click on Computer > Properties). When NetBIOS is
   used with DHCP, you no longer have to worry about IP adresses. IP of
   your PC if IP is choosen.

-  **Adress :** < **not set** > – enter here (in capital letters) your
   computer’s name if you choose NetBIOS as SMB adress type, or enter
   here your PC IP adress.

-  **Port :** **445** – default port used by SMB protocol. Not
   recommended to change it.

-  **Share :** < **not set** > – allows you to specify the name you use
   for your PS2 shared folder on your computer. “PS2SMB” is the common
   one default used by a lot of users – but you have to enter it in this
   field. As suggested by the hint text, you can leave this field empty
   (i.e. not set) to list your shares – just keep in mind you can not
   list shares on any Microsoft OS later than Windows 7 (maybe Vista is
   affected too, full explanation
   `here <http://psx-scene.com/forums/f150/open-ps2-loader-project-v0-9-3-a-62141/index766.html#post1209912>`__).

-  **User :** < **not set** > – allows you to specify a username if your
   computer requires a username for access. If you are using the Guest
   account on your computer, enter “GUEST” here (in capitals letters, no
   quotes) and give this account permissions to modify, read, write and
   to list your shared folder on your computer.

-  **Password :** – set here your password if your computer account
   requires one, otherwise leave blank. Leave blank if you are using the
   Guest account.

-  Press **OK** to validate the changes and exit this screen – or press
   |title| or |image1| (according to the select button you choose in the
   settings screen) – to go back to the previous screen without any
   changes made.

----

-  **Recommended settings when using a crossover cable (no router) :**

::

   Advanced options : Off
   Ethernet link mode : Auto
   - PS2 –
   IP adress type : *Static*
   IP adress : 192.168.X.X
   Mask : 255.255.255.X
   Gateway : 192.168.X.X
   DNS Server : 192.168.X.X
   - SMB Server –
   Adress Type : *NetBIOS*
   Adress : JOHNDOE-PC
   Port : 445
   Share : PS2SMB
   User : JohnDoe
   Password : (blank)

-  **Recommended settings when using a router :**

::

   Advanced options : Off
   Ethernet link mode : Auto
   - PS2 –
   IP adress type : *DHCP*
   IP adress : 192.168.X.X
   Mask : 255.255.255.X
   Gateway : 192.168.X.X
   DNS Server : 192.168.X.X
   - SMB Server –
   Adress Type : *NetBIOS*
   Adress : JOHNDOE-PC
   Port : 445
   Share : PS2SMB
   User : JohnDoe
   Password : (blank)

----

*Examples of working network configs :*
---------------------------------------

-  **(1)** contribution from
   @\ `algol <http://psx-scene.com/forums/f150/open-ps2-loader-0-9-3-user-guide-156387/#post1209205>`__
   : no router – crossover cable ; OS : Windows XP Pro (SP3).

::

   Advanced options : OFF
   Ethernet link mode : 100Mbit full-duplex
   - PS2 -
   IP adress type : Static
   IP adress : 169.254.238.101
   Mask : 255.255.255.0
   Gateway : 169.254.238.135
   DNS Server : 192.168.0.1
   - SMB Server -
   Address type : IP
   Address : 169.254.238.135
   Port : 445
   Share : PS2SMB
   User : Algol
   Password : (none)

.. |start| image:: 568074192-start.png
.. |title| image:: 74665754-cross.png
.. |image1| image:: 4184835271-circle.png
