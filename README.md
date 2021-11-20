# xibo-linux

This role installs and configures the Xibo Linux player.
Additionally it installs Xorg and a systemd service that automatically starts the player.

## Requirements

This role was developed on Debian Bullseye without desktop environment.

## Role Variables

This role uses the following Variables:

| Name                          |     Required/Default     | Description                                                                                     |
| ----------------------------- | :----------------------: | ----------------------------------------------------------------------------------------------- |
| `xibo_linux_cms_address`      |    :heavy_check_mark:    | The URL of your CMS installation, e.g `https://cms.example.org`.                                |
| `xibo_linux_cms_key`          |    :heavy_check_mark:    | The CMS Key found under Settings in your CMS installation.                                      |
| `xibo_linux_display_id`       | `{{ ansible_hostname }}` | The displayId is used as unique identifier of the display. Usually the hostname should be fine. |
| `xibo_linux_user`             |          `xibo`          | The name of the user which is created for autologin at startup.                                 |
| `xibo_linux_virtual_terminal` |           `2`            | The virtual terminal where Xorg gets launched.                                                  |

## Example

The following example playbook assumes that you cloned this role to `roles/xibo_linux` (i.e. the name of the role is `xibo_linux` instead of `ansible_xibo_linux`).

```yml
- hosts: info01
  roles:
    - role: xibo_linux
        xibo_linux_cms_address: https://cms.example.org
        xibo_linux_cms_key: cmsPrivateKey
        xibo_linux_display_id: cad25a9c24003050186ebbdc07e6dabf
```

## License

This work is licensed under the [MIT License](./LICENSE).

## Author Information

- [Sven Feyerabend (SF2311)](https://github.com/SF2311) _Sven.Feyerabend at stuvus.uni-stuttgart.de_
