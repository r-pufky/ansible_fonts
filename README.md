# Fonts
Manage custom system fonts.

## Requirements
No additional requirements.

## Role Variables
Settings have been throughly documented for usage.

[defaults/main.yml](https://github.com/r-pufky/ansible_fonts/blob/main/defaults/main.yml).

## Dependencies
N/A

## Example Playbook
Places fonts in a vars location for the host/group and update `fonts_source` to
refer to this location.

host_vars/computer.example.com/vars/fonts.yml
``` yaml
fonts_source: 'group_vars/data/fonts'
```

site.yml
``` yaml
- name:   'linux box'
  hosts:  'computer.example.com'
  become: true
  roles:
     - 'r_pufky.fonts'
```

## Issues
Create a bug and provide as much information as possible.

Associate pull requests with a submitted bug.

## License
[AGPL-3.0 License](https://github.com/r-pufky/ansible_fonts/blob/main/LICENSE)

## Author Information
https://keybase.io/rpufky
