# docker

Ansible role for setting up a Docker host. Follows official Docker installation documentation for [Debian](https://docs.docker.com/installation/debian/#debian-jessie-8-64-bit) and [Ubuntu](https://docs.docker.com/installation/ubuntulinux/#ubuntu-trusty-1404-lts-64-bit), expects relatively up-to-date Linux kernel (3.8+). Although it is possible to install on older releases, for simplicity this role focuses on "out of the box" supported "Debian-family" distros.

## Requirements

Ubuntu 14.04 'trusty' or Debian 8.0 'jessie'.

## Dependencies

[apt](https://github.com/cspicer/ansible-apt)

## Platforms

### Debian

* jessie

### Ubuntu

* trusty

## Variables

See [`defaults/main.yml`](defaults/main.yml) for default values.

## Tasks

### debian

### ubuntu

## Examples

## Development

* Source hosted at [GitHub][repo]
* Report issues/questions/feature requests on [GitHub Issues][issues]

Pull requests are very welcome! Make sure your patches are well tested.
Ideally create a topic branch for every separate change you make. For
example:

1. Fork the repo
2. Create your feature branch (`git checkout -b my-new-feature`)
3. Commit your changes (`git commit -am 'Added some feature'`)
4. Push to the branch (`git push origin my-new-feature`)
5. Create new Pull Request

## Author Information

Created and maintained by [Chris Spicer][cspicer] (<github@cspicer.ca>).

## License

MIT License (see [LICENSE][license])

[cspicer]: https://github.com/cspicer
[repo]: https://github.com/cspicer/ansible-docker
[issues]: https://github.com/cspicer/ansible-docker/issues
[license]: https://github.com/cspicer/ansible-docker/blob/master/LICENSE
