# Nginx deb package CIs

[![Automatic package build](https://github.com/LexVar/nginx_debian_ci/actions/workflows/build.yml/badge.svg)](https://github.com/LexVar/nginx_debian_ci/actions/workflows/build.yml)

Github CI to build deb packages of nginx with specific modules.

Two GITHUB CI's are available:
- Automatic package build
- Manual package build

Automatic debs are built and available as artefacts in the `Automatic package build` CI for every new commit in master.
Packages can be manually built with different nginx versions and modules using the `Manual package build` CI, by changing the listed fields in "Run Workflow".

## Environment Variables

Several environment variables can be changed:
- Nginx version, Default: 1.18.0-2
- Nginx distribution codename, Default: buster
- Codename for new package, Default: vts10
- New package name, Default: nginx-with-vts
- Nginx modules name, Default: nginx-module-vts
- Nginx modules download URL, Default: https://github.com/vozlt/nginx-module-vts/archive/v0.1.18.tar.gz

Multiple modules URL's can be set separated by spaces. Only tar.gz files are supported.
The module names are only set for changelog purposes.

Nginx versions are identified in the NGINX_VERSION and NGINX_CODENAME variables.
Codename for the built package is set in the CODENAME variable.
New package name is set in PKG_NAME.
The name of the included modules are set in MODULES_NAME.
The corresponding modules archive URL's are set in the MODULES_URL variable.

## Tested Nginx Modules
* nginx-module-vts v0.1.18

## Software
* Nginx version 1.18.0-2~buster
* Debian 10 buster
* Docker
