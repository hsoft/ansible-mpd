# ansible-mpd

Installs and configures a [mpd][mpd] service.

## Features

* Ensures that the MPD service is installed and running
* Configures using a "sed" approach rather than templating, allowing you to use your distro's
  default config rather than this role's.

## Requirements

* Ansible 2.3+
* Debian jessie target

## Example

```
- hosts: all
  vars:
    mpd_music_directory: /path/to/music
    # Listen to external clients
    mpd_bind_to_address: "0.0.0.0"
  roles:
    - mpd
```


See [defaults](defaults/main.yml) for more details.

[mpd]: https://www.musicpd.org/
