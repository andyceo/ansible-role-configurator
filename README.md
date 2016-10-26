# Ansible Role: configurator

This role creates directories and files, render templates, copies files on host, etc. It is useful to preconfigure docker-packaged software.

## Requirements

Ubuntu 16.04

## Features

- Full directory copying (`configurator.fulldirs`). Already existing files in `dest` will not be touched, if not changed or not exists in `src`. Be careful with trailing slashes (behavior is similar to rsync, see [docpage for copy Ansible module](http://docs.ansible.com/ansible/copy_module.html))
- Directory creation and update its mode, owner, group (`configurator.directories`)
- Files copying (`configurator.files`)
- Symlinks creation (`configurator.symlinks`)
- Can notify on change
- Default values for mode, owner, group, notify can be provided
