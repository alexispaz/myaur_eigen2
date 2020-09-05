# $Id: PKGBUILD 204732 2014-01-26 09:43:39Z ronald $
# Maintainer: Tom Gundersen <teg@jklm.no>
# Contributor: Andrea Scarpino <andrea@archlinux.org>
# Contributor: Tobias Powalowski <tpowa@archlinux.org>

pkgname=eigen2
pkgver=2.0.17
pkgrel=3
pkgdesc="A lightweight C++ template library for vector and matrix math, a.k.a. linear algebra"
arch=('any')
url='http://eigen.tuxfamily.org/index.php?title=Main_Page'
license=('GPL' 'LGPL3')
makedepends=('cmake' 'pkg-config')
source=("git+https://gitlab.com/libeigen/eigen.git#tag=2.0.17")
sha1sums=('SKIP')

build() {
  cd "${srcdir}"
  mkdir -p build
  cd build
  cmake ../eigen \
    -DCMAKE_BUILD_TYPE=Release \
    -DCMAKE_INSTALL_PREFIX=/usr
  make
}

package() {
  cd "${srcdir}/build"
  make DESTDIR="${pkgdir}" install
}
