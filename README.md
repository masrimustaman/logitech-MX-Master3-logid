## Installation

Installation instructions for different distributions are available from the developer, but here are the commands for an pop OS 20.04 workstation:

```bash
sudo apt install cmake libevdev-dev libudev-dev libconfig++-dev
git clone https://github.com/PixlOne/logiops
cd logiops
mkdir build
cd build
cmake ..
make
sudo make install
sudo touch /etc/logid.cfg
sudo systemctl enable --now logid
```
## My /etc/logid.cfg File
```
cd ~/Downloads
wget https://raw.githubusercontent.com/masrimustaman/logitech-MX-Master3-logid/main/logid.cfg
sudo cp ./logid.cfg /etc/logid.cfg 
sudo systemctl restart logid
```
### Programmable Mouse Buttons

Note that I chose to configure the scroll wheel button, but any of the following buttons are available for you to play with:

- 0x52 - scroll wheel button
- 0x53 - back button
- 0x56 - forward button
- 0xc3 - thumb button (default "Gesture" button with Logitech Options software)
- 0xc4 - mode shift button (by default toggles between ratchet and free-spin wheel modes)

