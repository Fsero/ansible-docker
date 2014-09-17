# docker

Ansible role for setting up a Docker host. Installs Docker via the official Docker Ubuntu apt repository on both Ubuntu and Debian. For simplicity this role focuses on releases that have newer kernels and work out of the box with the official [Ubuntu install guide](https://docs.docker.com/installation/ubuntulinux/#ubuntu-trusty-1404-lts-64-bit) and repository.

## Requirements

* Ansible 1.8+
* Ubuntu 14.04 'trusty', Debian 8.0 'jessie' or newer

## Dependencies

###[apt](https://github.com/cspicer/ansible-apt)
Apt role is called as a dependency to add official Docker repo and signing key then update apt cache.

## Variables

See [`defaults/main.yml`](defaults/main.yml) for default values.

### docker

These variables should be set either as a dependency in `meta/main.yml` for your role, or as a part of your include statement. See below for examples.

Variable        | Type        | Description
--------        | ----        | -----------
apt_pkg         | List        | List of apt packages to be installed

## Tasks

### main

- Fail on unsupported releases of Debian and Ubuntu
- Install Docker from official apt repository

## Testing

This role can be tested via [Vagrant](https://github.com/mitchellh/vagrant) and includes a Vagrantfile and `ansible-galaxy` `requirements.yml` file to resolve any external dependencies.

External role dependencies are copied into `vagrant/roles` which is configured in [`ansible.cfg`](ansible.cfg) as a `roles_path`.

To bring up a test VM:
* Download dependencies with ansible-galaxy: `ansible-galaxy install -r requirements.yml`
* Launch the Vagrantfile: `vagrant up`

## Examples

Add to your playbook as a role include:

    ---
    - hosts: docker-hosts
      roles:
        - ansible-docker

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
