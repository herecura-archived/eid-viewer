# vim:set ts=2 sw=2 et:
# Maintainer: Emil Vanherp <emil DOT vanherp AT hot mail DOT com>
# Contributor: Alad Wenter <https://wiki.archlinux.org/index.php/Special:EmailUser/Alad>
# Contributor: Vianney le Clément <vleclement AT gmail·com>
# Contributor: Valère Monseur <valere DOT monseur AT ymail·com>
pkgname=eid-viewer
pkgver=4.1.20
pkgrel=1

pkgdesc="Viewer for Belgian Electronic Identity Card"
arch=('i686' 'x86_64')
url="http://eid.belgium.be/"
license=('LGPL3')
depends=('java-runtime' 'gsettings-desktop-schemas' 'eid-mw' 'desktop-file-utils' 'hicolor-icon-theme')
source=("https://dist.eid.belgium.be/continuous/sources/$pkgname-$pkgver-v$pkgver.src.tar.gz")
sha256sums=('1e141c8617a91f82fe64ce35edd0eb334c34579e534f0f8e2a716d60aae52da8')

build() {
  cd "$pkgname-$pkgver"
  ./configure --prefix=/usr
}

package() {
  cd "$pkgname-$pkgver"
  make install DESTDIR="$pkgdir"
}

