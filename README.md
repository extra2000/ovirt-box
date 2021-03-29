# ovirt-box

| License | Versioning | Build |
| ------- | ---------- | ----- |
| [![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT) | [![semantic-release](https://img.shields.io/badge/%20%20%F0%9F%93%A6%F0%9F%9A%80-semantic--release-e10079.svg)](https://github.com/semantic-release/semantic-release) | [![Build status](https://ci.appveyor.com/api/projects/status/2vd8f1uj6ycw74ke/branch/master?svg=true)](https://ci.appveyor.com/project/nikAizuddin/ovirt-box/branch/master) |

Developer box for [oVirt](https://github.com/oVirt).


## Creating Vagrant Box

Copy vagrant file from `vagrant/examples/` and then create the vagrant box (you can change to `--provider=libvirt` if you want to use Libvirt provider):
```
$ cp -v vagrant/examples/Vagrantfile.ovirt-box.centos-7.x86_64.example vagrant/Vagrantfile.ovirt-box
$ vagrant up --provider=virtualbox
```

Provision the vagrant box:
```
$ vagrant ssh ovirt-box -- sudo salt-call state.highstate
$ vagrant ssh ovirt-box -- sudo salt-call state.sls ovirt
```
