# vm
1. Boot the Ubuntu VM in VirtualBox
2. In the VM window menu bar, click:
      `Devices → Insert Guest Additions CD image`
    - If it prompts to download, say Yes and let it download
4. Inside Ubuntu (guest)
    - Install required packages so Guest Additions can build
    ```bash
    sudo apt update
    sudo apt install build-essential dkms linux-headers-$(uname -r)
    ```
    - Mount and run the Guest Additions installer:
    ```bash
    cd /media/$USER/VBox_GAs_*
    sudo ./VBoxLinuxAdditions.run
    ```
5. `sudo reboot`
6. Settings → General → Advanced → Shared Clipboard is Bidirectional
