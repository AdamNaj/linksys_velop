# linksys_velop
The linksys_velop platform allows for presence detection by listing devices connected to your Linksys Velop router.

It was tested with a Linksys Velop WHW03v1 Firmware version 1.1.11.197735

## Example configuration.yaml

```yaml
device_tracker:
  - platform: linksys_velop
    host: 192.168.1.1
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
