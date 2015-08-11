## synchronize

[![Travis CI](http://img.shields.io/travis/ypid/ansible-synchronize.svg?style=flat)](http://travis-ci.org/ypid/ansible-synchronize)
[![Ansible Galaxy](http://img.shields.io/badge/galaxy-ypid.synchronize-660198.svg?style=flat)](https://galaxy.ansible.com/list#/roles/4749)
[![Platforms](http://img.shields.io/badge/platforms-debian%20/%20ubuntu-lightgrey.svg?style=flat)](#)
[![GitHub Tags](https://img.shields.io/github/tag/ypid/ansible-synchronize.svg)](https://github.com/ypid/ansible-synchronize)
[![GitHub Stars](https://img.shields.io/github/stars/ypid/ansible-synchronize.svg)](https://github.com/ypid/ansible-synchronize)


Simple role to synchronize files/directories from the Ansible controller to target systems.

This role was written to be able to specify directories to synchronize via inventory variables. It is based on the Ansible’s [synchronize module]. If the [copy module] seems more suitable checkout the role [ypid.copy].

[synchronize module]: https://docs.ansible.com/ansible/synchronize_module.html
[copy module]: https://docs.ansible.com/ansible/copy_module.html
[ypid.copy]: https://galaxy.ansible.com/list#/roles/4558

### Installation

This role requires at least Ansible `v1.8.4`. To install it, run:

    ansible-galaxy install ypid.synchronize

To install via git, run either:

    git clone https://github.com/ypid/ansible-synchronize.git ypid.synchronize
    git submodule add https://github.com/ypid/ansible-synchronize.git ypid.synchronize




### Role variables

List of default variables available in the inventory:

    ---
    
    ## Checkout the documentation for the synchronize module.
    
    # synchronize_list:
    #   - src: '/etc/issue'
    #     dest: '/var/backups/'
    #     delete: yes
    #   - src: '/etc/cron.d'
    #     dest: '/var/backups/'
    #     recursive: yes
    #     delete: yes
    
    ## "Global" files/directories to synchronize
    synchronize_list: []
    # synchronize_list:
    #   - src: '/path/to/source/file'
    #     dest: '/path/to/target/file'
    #     create_parent_dirs: no
    #     # state: 'absent'
    
    ## "Host group" files/directories to synchronize
    synchronize_group_list: []
    
    ## "Host" files/directories to synchronize
    synchronize_host_list: []




### Authors and license

`synchronize` role was written by:

- [Robin Schneider](https://github.com/ypid) | [e-mail](mailto:ypid@riseup.net)

License: [AGPLv3](https://tldrlegal.com/license/gnu-affero-general-public-license-v3-%28agpl-3.0%29)

***

README generated by [Ansigenome](https://github.com/nickjj/ansigenome/).
