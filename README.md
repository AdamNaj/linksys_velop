# linksys_velop
The linksys_velop platform allows for presence detection by listing devices connected to your Linksys Velop router.

It was tested with a Linksys Velop WHW03v1 Firmware version 1.1.11.197735

The component is a modified version of https://github.com/home-assistant/home-assistant/tree/dev/homeassistant/components/linksys_smart
The change was required due to a Velop firmware update that started requiring credentials.

## Installation

1. Using the tool of choice open the directory (folder) for your HA configuration (where you find `configuration.yaml`).
2. If you do not have a `custom_components` directory (folder) there, you need to create it.
3. In the `custom_components` directory (folder) create a new folder called `linksys_velop`.
4. Download _all_ the files from the `custom_components/linksys_velop/` directory (folder) in this repository.
5. Place the files you downloaded in the new directory (folder) you created.
6. Restart Home Assistant.
7. Move on to the configuration.

Using your HA configuration directory (folder) as a starting point you should now also have this:

```text
custom_components/linksys_velop/__init__.py
custom_components/linksys_velop/device_tracker.py
custom_components/linksys_velop/manifest.json
```

## Example configuration.yaml

```yaml
device_tracker:
  - platform: linksys_velop
    host: 192.168.1.1
    username: admin
    password: YOUR_PASSWORD
```

### Configuration options

Key | Type | Required | Description
-- | -- | -- | --
`host` | `string` | `True` | The hostname or IP address of your access point, e.g., 192.168.1.1.
`username` | `string` | `False` | Defaults to `admin`. You should not have to customize it as Velops deveult to `admin` on login and only allow you to specify password.
`password` | `string` | `True` | The password for your given local admin account.

## Contributions are welcome!

If you want to contribute to this please read the [Contribution guidelines](CONTRIBUTING.md)
