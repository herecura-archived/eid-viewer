# vim:set ts=2 sw=2 et:
# Maintainer: Alad Wenter <alad@linuxbbq.org>
# Contributor: Vianney le Clément <vleclement AT gmail·com>
# Contributor: Valère Monseur <valere DOT monseur AT ymail·com>
pkgname=eid-viewer
pkgver=4.0.7
pkgrel=1
pkgdesc="Viewer for Belgian Electronic Identity Card"
arch=('i686' 'x86_64')
url="http://eid.belgium.be/"
license=('LGPL3')
depends=('bash' 'pcsclite' 'java-runtime' 'gsettings-desktop-schemas')
source=("http://eid.belgium.be/nl/binaries/eid-viewer-$pkgver-184.src.tar_tcm227-250014.gz")
sha256sums=('923962eecd907ac8e123fecbedd6c5988352e557ec0c4b95df4eac11433cd7be')
install=eid-viewer.install

build() {
  cd "$srcdir/$pkgname-$pkgver"
  ./configure --prefix=/usr
}

package() {
  cd "$srcdir/$pkgname-$pkgver"
  make install DESTDIR="$pkgdir"
}

sha256sums=('923962eecd907ac8e123fecbedd6c5988352e557ec0c4b95df4eac11433cd7be')
