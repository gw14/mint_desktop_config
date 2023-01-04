
<H3>Check System Compatibility With KVM:</H3>

egrep -c '(vmx|svm)' /proc/cpuinfo

*If you get an output above 0, that means KVM is compatible with your system*

<H3>Install KVM:</H3>

sudo apt-get install qemu-kvm libvirt-daemon-system libvirt-clients bridge-utils virt-manager

<H3>Add Your User to the KVM and Libvirt Group:</H3>
It is now time to add your user to KVM and libvirt group to set up KVM so that you don’t run into any permissions-related errors.

sudo usermod -aG kvm $USER
sudo usermod -aG libvirt $USER

**[reboot]**

https://linuxhint.com/install_kvm_virtualization_ubuntu/