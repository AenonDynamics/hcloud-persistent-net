hcloud-persistent-net
=============================

**persistent network interface names for hetzner cloud**

With the release of the new AMD EPYC based cloud servers (CPX), Hetzner has applied some changes to their virtualization platform (QEMU). The network interface names have changed due to the modern virtio_net network adapter 0x1041 including different pcie bus addresses.

The recent released ARM64 platfrom uses the same bus addresses as the AMD platform.

Initially created as [blog post on andidittrich.com](https://andidittrich.com/2020/05/hetzner-cloud-predictable-network-interface-names.html)

## Features ##

* persistent network interface names for AMD Epyc, ARM64 and Intel Xeon CPUs
* simple interface names: `wan`, `net0`, `net1`, `net2`
* completely based on systemd-networkd

## Usage ##

### Enable Services ###

```bash
# enable systemd service
systemctl enable systemd-networkd.service
```

## Contribution ##

The **.deb** package is automatically generated via a **Continuous Delivery Pipeline** - please do not build packages manually!

## License ##
hcloud-persistent-net is OpenSource and licensed under the Terms of [Mozilla Public License 2.0](https://opensource.org/licenses/MPL-2.0). You're welcome to [contribute](docs/CONTRIBUTING.md)
