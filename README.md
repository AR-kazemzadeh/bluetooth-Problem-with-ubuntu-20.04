# bluetooth-Problem-with-ubuntu-20.04
bluetooth Problem with ubuntu 20.04, and fixed by this way

    sudo apt install blueman
    sudo add-apt-repository ppa:blaze/rtbth-dkms
    sudo apt-get update
    sudo apt-get install rtbth-dkms
then 

    sudo vim /etc/modules
Comment all and add this line

    rtbth
for save this add:

    :W
    
for close the Vim:

    :Q
Reboot and open

    sudo blueman-manager
Now all Problome is fixed But If still not work, try this

    sudo rmmod btusb
    sleep 1
    sudo modprobe btusb
    
If still not work, try this

update /etc/default/grub with this value

    GRUB_CMDLINE_LINUX_DEFAULT="quiet splash pci=nommconf pcie_aspm=off"
    
update grub

    sudo update-grub
    
then reboot and enjoy your music



