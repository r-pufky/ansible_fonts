# Fonts
Manage custom system fonts.

## Requirements
[supported platforms](https://github.com/r-pufky/ansible_fonts/blob/main/meta/main.yml)

## Role Variables
[defaults](https://github.com/r-pufky/ansible_fonts/blob/main/defaults/main.yml)

## Dependencies
**galaxy-ng** roles cannot be used independently. Part of
[r_pufky.deb](https://github.com/r-pufky/ansible_collection_deb) collection.

## Example Playbook
Places fonts in a vars location for the host/group and update `fonts_source` to
refer to this location.

group_vars/data/fonts:
```
custom_truetype_font.ttf
custom_opentype_font.otf
custom_web_font.woff
```

host_vars/computer.example.com/vars/fonts.yml
``` yaml
fonts_source: 'group_vars/data/fonts'
fonts_packages:
  - 'fonts-liberation'
```

site.yml
``` yaml
- name: 'linux box'
  hosts: 'computer.example.com'
  become: true
  roles:
     - 'r_pufky.deb.fonts'
```

## Development
Configure [environment](https://github.com/r-pufky/ansible_collection_docs/blob/main/dev/environment/README.md)

Run all unit tests:
``` bash
molecule test --all
```

### Issues
Create a bug and provide as much information as possible.

Associate pull requests with a submitted bug.

## License
[AGPL-3.0 License](https://www.tldrlegal.com/license/gnu-affero-general-public-license-v3-agpl-3-0)
 [(direct link)](https://github.com/r-pufky/ansible_fonts/blob/main/LICENSE)

## Author Information
PGP Fingerprint: [466EEC2B67516C7117C85CE3A0BC35D16698BAB9](https://keys.openpgp.org/vks/v1/by-fingerprint/466EEC2B67516C7117C85CE3A0BC35D16698BAB9)
| [github gist](https://gist.github.com/r-pufky/a8df36977c55b5bb20829267c4c49d22)
