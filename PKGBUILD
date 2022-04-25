#!/bin/bash

# Disable various shellcheck rules that produce false positives in this file.
# Repository rules should be added to the .shellcheckrc file located in the
# repository root directory, see https://github.com/koalaman/shellcheck/wiki
# and https://archiv8.github.io for further information.
# shellcheck disable=SC2034,SC2154
# ToDo: Add files: User documentation
# ToDo: Add files: Tooling
# FixMe: Namcap warnings and errors

# Maintainer: Ross Clark <archiv8@artisteducator.com>
# Contributor: Ross Clark <archiv8@artisteducator.com>
pkgname=sdupes
pkgver=1.0
pkgrel=1
pkgdesc="fast file duplicate detection"
arch=(x86_64)
license=(gpl3+)
makedepends=(git)
provides=(sdupes)
source=("https://github.com/sph-mn/sdupes/archive/v1.0.tar.gz")
url="https://github.com/sph-mn/sdupes"
md5sums=(70e1f6f35f93611a8f54bebaadb19782)

package() {
  cd "${srcdir}/sdupes-$pkgver"
  ./exe/compile-c
  install -Dt "${pkgdir}/usr/bin" temp/sdupes
}
