# Maintainer: Rolinh <robinDOThahlingATgw-computingDOTnet>
pkgname=yuvcutter
pkgver=0.3.2
pkgrel=1
pkgdesc="Tool to cut the first N frames from a RAW YUV file"
arch=('x86_64' 'i686')
url="http://projects.gw-computing.net/projects/yuvcutter"
license=('BSD')
depends=('glibc')
makedepends=()
provides=('yuvcutter')
conflicts=('yuvcutter-git')
source=(http://projects.gw-computing.net/attachments/download/80/${pkgname}-${pkgver}.tar.gz)
md5sums=('b287acb2c14633781e6ec6e5f11699c3')

build() {
  cd ${pkgname}-${pkgver}

  make
}

package() {
  cd ${pkgname}-${pkgver}

  make PREFIX=/usr MANDIR=/usr/share/man DESTDIR=${pkgdir} install

  install -Dm644 LICENSE "${pkgdir}/usr/share/licenses/${pkgname}/LICENSE"
}

# vim:set ts=2 sw=2 et:
