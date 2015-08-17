# Contributor: Andrea Scarpino <andrea@archlinux.org>

pkgname=qtsvg-git
pkgver=v5.1.0.beta1.4.ged11da0
pkgrel=1
pkgdesc="A cross-platform application and UI framework (QtSvg)"
arch=('i686' 'x86_64')
url="http://qt-project.org/"
license=('GPL3' 'LGPL')
depends=('qtbase-git')
makedepends=('git')
options=('!libtool')
source=(git://gitorious.org/qt/qtsvg.git#branch=dev)
md5sums=('SKIP')

pkgver() {
  cd qtsvg
  git describe --always | sed 's|-|.|g'
}

build() {
  cd qtsvg
  /opt/qt-git/bin/qmake
  make
}

package() {
  cd qtsvg
  make INSTALL_ROOT="${pkgdir}" install
}
