# vim:set ts=2 sw=2 et:
# Maintainer: Alad Wenter <alad@linuxbbq.org>
# Contributor: Vianney le Clément <vleclement AT gmail·com>
# Contributor: Valère Monseur <valere DOT monseur AT ymail·com>
pkgname=eid-viewer
pkgver=4.1.10
pkgrel=2
pkgdesc="Viewer for Belgian Electronic Identity Card"
arch=('i686' 'x86_64')
url="http://eid.belgium.be/"
license=('LGPL3')
depends=('java-runtime' 'gsettings-desktop-schemas' 'eid-mw' 'desktop-file-utils' 'hicolor-icon-theme')
source=("https://dist.eid.belgium.be/continuous/sources/$pkgname-$pkgver-v$pkgver.src.tar.gz")
sha256sums=('3eae66dc57c6270157a7b93510b7f178a4fc4e94c2956c7c6583b096dd43e7a5')

build() {
  cd "$pkgname-$pkgver"
  ./configure --prefix=/usr
}

package() {
  cd "$pkgname-$pkgver"
  make install DESTDIR="$pkgdir"
}

