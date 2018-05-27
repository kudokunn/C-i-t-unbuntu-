#### 1. Thao tác cần làm: apt update, apt upgrade.
#### 2. Các phần mềm cần cài sau khi cài Ubuntu: Chrome, Telegram, VLC, Deepin Teminal, Fcit-unikey,Vmware
#### 3. Chỉnh boot để boot tự vào win 10 ưu tiên

* Vmware:

       sudo apt install gcc build-essential -y
       
       wget <link down vm linux từ trang chủ>
       
       chmod +x VMware-Workstation-Full-14.0.0-6661328.x86_64.bundle
       
       sudo ./VMware-Workstation-Full-14.0.0-6661328.x86_64.bundle
       
=> Xong cấu hình bình 

* Telegram:

        sudo add-apt-repository ppa:atareao/telegram

        sudo apt-get update

        sudo apt-get install telegram       
    

* Chrome 

        # Install
        
        wget https://dl.google.com/linux/direct/google-chrome-stable_current_amd64.deb
        
        sudo dpkg -i –force-depends google-chrome-stable_current_amd64.deb
        
        sudo apt-get install -f

        # Remove
        
        sudo apt-get purge google-chrome-stable
        
        sudo apt-get autoremove
        
 * VLC
 
        sudo add-apt-repository ppa:videolan/stable-daily
        
        sudo apt-get update
        
        sudo apt-get install vlc
        
 * Deepin Teminal
 
        # vi /etc/apt/sources.list
        [
        deb http://packages.linuxdeepin.com/deepin trusty main non-free universe
        deb-src http://packages.linuxdeepin.com/deepin trusty main non-free universe
        
        ]
        
        wget http://packages.linuxdeepin.com/deepin/project/deepin-keyring.gpg
        
        gpg --import deepin-keyring.gpg
        
        gpg --list-keys
        
        sudo gpg --export --armor 209088E7 | sudo apt-key add -
        
        sudo apt-get update

        sudo apt-get install deepin-terminal

* Fcit-unikey

        sudo apt-get install fcitx-unikey
        
        # Xong logout user và đăng nhập 
        
* Lỗi  E: Could not get lock /var/lib/apt/lists/lock - open (11: Resource temporarily unavailable)
       E: Unable to lock directory /var/lib/apt/lists/


        $ sudo rm /var/lib/apt/lists/lock
        
        $ sudo rm /var/cache/apt/archives/lock

        $ sudo apt update
        
### Thiết lập win 10 boot mặc định trong grub 

 * Cài đặt phần mềm Grub Customizer
 
         sudo add-apt-repository ppa:danielrichter2007/grub-customizer
         sudo apt-get update
         sudo apt-get install grub-customize

* Mở phần mềm grub Customizer và đẩy win 10 lên đầu là OK
