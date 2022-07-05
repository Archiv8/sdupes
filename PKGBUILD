#!/bin/bash

# Disable various shellcheck rules that produce false positives in this file.
# Repository rules should be added to the .shellcheckrc file located in the
# repository root directory, see https://github.com/koalaman/shellcheck/wiki
# and https://archiv8.github.io for further information.
# shellcheck disable=SC2034,SC2154
# ToDo: Add files: User documentation
# ToDo: Add files: Tooling
# FixMe: Namcap warnings and errors

# Maintainer: Ross Clark <https://github.com/Archiv8/sdupes/discussions>
# Contributor: Ross Clark <https://github.com/Archiv8/sdupes/discussions>

pkgname="sdupes"
pkgver=1.0
pkgrel=2
pkgdesc="Fast file duplicate detection"
arch=(
  "x86_64"
)
license=(
  "gpl3+"
)
makedepends=(
  "git"
)
depends=(
  "glibc"
)
provides=(
  "sdupes"
)
source=(
  "${pkgname}-${pkgver}.tar.gz"::"https://github.com/sph-mn/sdupes/archive/v1.0.tar.gz"
)
url="https://github.com/sph-mn/sdupes"
sha512sums=(
  "1c52dd5226e726da8568eb1961a99440bbb7e17def5f5ae6a6ecd08262eb7ea7f80df52fb4354c01f345a9abd9acf787a1a1c73db258c73e9e44a76a58e13c28"
)

package() {

  cd "${srcdir}/${pkgname}-$pkgver"

  ./exe/compile-c

  install -Dt "${pkgdir}/usr/bin" temp/sdupes
}
