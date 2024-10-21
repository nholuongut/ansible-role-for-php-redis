# Ansible Role: PhpRedis

![](https://i.imgur.com/waxVImv.png)
### [View all Roadmaps](https://github.com/nholuongut/all-roadmaps) &nbsp;&middot;&nbsp; [Best Practices](https://github.com/nholuongut/all-roadmaps/blob/main/public/best-practices/) &nbsp;&middot;&nbsp; [Questions](https://www.linkedin.com/in/nholuong/)
<br/>

Installs PhpRedis support on Linux.

## Requirements

This role doesn't *explicitly* require Redis to be installed, but if you don't have the daemon running somewhere (either on the same server, or somewhere else), this role won't be all that helpful. Check out `nholuong.redis` for a simple role to install and configure Redis (either on the same server, or separate servers).

## Role Variables

Available variables are listed below, along with default values (see `defaults/main.yml`):

    php_enablerepo: ""

(RedHat/CentOS only) If you have enabled any additional repositories (might I suggest nholuong.repo-epel or nholuong.repo-remi), those repositories can be listed under this variable (e.g. `remi,epel`). This can be handy, as an example, if you want to install the latest version of PHP from Remi's repository.

    php_redis_package: php-redis

(Default for Debian/Ubuntu shown). If installing from apt or yum, which package to install which provides the PhpRedis extension. (For PHP 5.x on Debian, this should be `php5-redis`).

### Install from source

If you want to install PhpRedis directly from source (if you're on an OS that doesn't have it available as a package, or if you want a newer version than is available through your package manager), you can use the variables below to configure the source installation:

    php_redis_install_from_source: false

Whether to install PhpRedis from source. If you'd like to install a specific version of PhpRedis not available via the system package manager, you can compile the extension from source.

    php_redis_source_repo: https://github.com/phpredis/phpredis.git

The git repository for the PhpRedis extension.

    php_redis_source_version: develop

The branch, tag, or commit hash to use when cloning the source repository. Can be a branch (e.g. `develop` or `php7`), a tag (e.g. `2.2.7`), or a commit hash (e.g. `5241a5c`).

    php_redis_source_clone_dir: ~/phpredis

The location where the PhpRedis source code will be cloned locally.

    php_redis_source_configure_command: "./configure"

The command to configure a PhpRedis source install. You can modify this command if you want to do something like add `--enable-redis-igbinary`.

## Dependencies

  - nholuong.php

## Example Playbook

    - hosts: webservers
      roles:
        - { role: nholuong.php-redis }

# 🚀 I'm are always open to your feedback.  Please contact as bellow information:
### [Contact ]
* [Name: nho Luong]
* [Skype](luongutnho_skype)
* [Github](https://github.com/nholuongut/)
* [Linkedin](https://www.linkedin.com/in/nholuong/)
* [Email Address](luongutnho@hotmail.com)

![](https://i.imgur.com/waxVImv.png)
![](Donate.png)
[![ko-fi](https://ko-fi.com/img/githubbutton_sm.svg)](https://ko-fi.com/nholuong)

# License
* Nho Luong (c). All Rights Reserved.🌟