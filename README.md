# setup-mac
Steps to setup personal mac. 
## Alfred
1. brew install php # after MAC Monterey, php is not installed by defaut
2. Install python2.7, click [here](https://www.python.org/downloads/release/python-2718/) 
3. pip2.7 install pytz # timezone workflow used.
4. [youdao workflow](https://github.com/wensonsmith/YoudaoTranslator/releases/tag/3.1.0) AK/SK, please access, [here](https://ai.youdao.com/console/#/service-singleton/text-translation)
## VirutalBox
### How to open my ubuntu vm with headless model during start mac
Refer [here](https://ma.ttias.be/auto-start-virtualbox-vms-headless-after-reboot-on-mac-osx/)

```shell
cat /Users/haofan/Library/LaunchAgents/org.virtualbox.launch.fanhao-ubuntu.plist
<?xml version="1.0" encoding="UTF-8"?>
<!DOCTYPE plist PUBLIC "-//Apple//DTD PLIST 1.0//EN" "http://www.apple.com/DTDs/PropertyList-1.0.dtd">
<plist version="1.0">
<dict>
  <key>Label</key>
  <string>org.virtualbox.launch.fanhao-ubuntu</string>
  <key>ProgramArguments</key>
  <array>
    <string>/Applications/VirtualBox.app/Contents/MacOS/VBoxManage</string>
    <string>startvm</string>
    <string>fanhao-ubuntu</string>
    <string>--type</string>
    <string>headless</string>
  </array>
  <key>RunAtLoad</key>
  <true/>
</dict>
</plist>
```
fanhao-ubuntu is my ubuntu server name, 
```code
VBoxManage list vms
"fanhao-ubuntu" {6b3c93f8-58a4-4d93-a922-ddaed383107e}
"fanhao-centos" {53b577f0-f119-4220-9ea2-3d1192ae3297}
"kubespray_k8s-1_1573872031790_95280" {e907267a-8899-475d-9dd0-15039f150e58}
```
