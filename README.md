# tk1_playbooks
Ansible playbooks for my Jetson TK1

**Bootstrapping:**

1. From the [L4T](https://developer.nvidia.com/linux-tegra) site download the latest Driver Packages and Sample File System, and follow the Quick Start Guide to flash a clean image. Use this flash command to maximize eMMC space: `sudo ./flash.sh -S 14580MiB jetson-tk1 mmcblk0p1`
2. Login ubuntu/ubuntu, open a root terminal, `apt-add-repository -y universe && apt-get update && apt-get install -y aptitude git ansible`
3. `ansible-pull -d /etc/tk1_playbooks -U https://github.com/mlin/tk1_playbooks.git -i 'localhost,' -v`

