# Maintainer: Matthew Krafczyk <krafczyk.matthew@gmail.com>
# Contributor: Matthew Krafczyk <krafczyk.matthew@gmail.com>

pkgname=suspend-prevent
pkgver=0.0.0
pkgrel=1
pkgdesc="A Script and set of systemd services to prevent suspend on lid close while on AC"
url="https://github.com/krafczyk/suspend-prevent"
arch=('any')
license=('GPL')
makedepends=('git' 'cmake')
conflicts=('suspend-prevent')
provides=('suspend-prevent')
source=('git://github.com/krafczyk/suspend-prevent.git#branch=master')
md5sums=('SKIP')

pkgver() {
  cd "$srcdir"/"$pkgname"
  git describe --long --tags | sed 's|^v||;s|-|.|g'
}

build() {
  cd "$srcdir"/"$pkgname"
  cmake -DCMAKE_INSTALL_PREFIX=${pkgdir}
  make

}

package() {
  cd "$srcdir"/"$pkgname"
  make install
}
