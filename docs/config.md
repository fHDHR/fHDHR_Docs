# Config

The example config file contains all of the things that the typical user may need to fill out.
The 3 basic items in the `fhdhr` section are the only ones that you should be concerned with setting. The WebUI has a settings page with access to the same settings.

Please see the [Advanced Configuration](../adv_config) page for more settings.

## fHDHR

Under `fhdhr`, you'll find 2 addresses listed. `0.0.0.0` works great for a listen address, however, it seems that SSDP works best if the discovery address is set to the IP to say that there is a service at.

```ini
[fhdhr]
# address = 0.0.0.0
# port = 5004
# discovery_address = 0.0.0.0
```
