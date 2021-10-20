# Role Name

This role installs and configures the xibo player for Linux. Additionally it sets up automatic login of the `xibo_user` and autostart oft the player at startup.


## Requirements

This role was developed on Debian Bullseye with XFCE as desktop environment. It configures lightdm for autologin.


## Role Variables

This role uses the following Variables:

| Name               |  Required/Default  | Description                                                                                      |
| ------------------ | :----------------: | ------------------------------------------------------------------------------------------------ |
| `xibo_cms_address` | :heavy_check_mark: | The URL of your CMS installation, e.g `https://cms.example.org`.                                 |
| `xibo_cms_key`     | :heavy_check_mark: | The CMS Key found under Settings in your CMS installation.                                       |
| `xibo_display_id`  | :heavy_check_mark: | The displayId is used as unique identifier of the display. Usually a random string is necessary. |
| `xibo_user`        |       `xibo`       | The name of the user which is created for autologin at startup.                                  |


## Example

The following example playbook assumes that you cloned this role to `roles/xibo_linux` (i.e. the name of the role is `xibo_linux` instead of `ansible_xibo_linux`).

```yml
- hosts: info01
  roles:
    - role: xibo_linux
        xibo_cms_address: https://cms.example.org
        xibo_cms_key: cmsPrivateKey
        xibo_display_id: cad25a9c24003050186ebbdc07e6dabf
```


## License

This work is licensed under the [MIT License](./LICENSE).


## Author corecore

- [Sven Feyerabend (SF2311)](https://github.com/SF2311) _Sven.Feyerabend at stuvus.uni-stuttgart.de_
