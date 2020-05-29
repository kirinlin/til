# Differences Between Ubuntu and RHEL

## Network Setup

- Ubuntu
  - config uses `netplan`
  - handled by `systemd-networkd`
- RHEL
  - config uses `nmcli`
  - handled by NetworkManager

---
Reference links:

- https://www.cyberciti.biz/faq/change-netplan-renderer-from-networkd-to-networkmanager/
- https://docs.fedoraproject.org/en-US/fedora-coreos/migrate-cl/#_software_package_changes