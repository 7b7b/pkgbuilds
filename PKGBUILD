pkgname=eggwm
pkgver=1.0
pkgrel=1
pkgdesc="A simple and light Qt5 WM.  100% compatible with the EWMH and ICCCM standards."
arch=('i686' 'x86_64')
license=('GPL3')
depends=('qt5-base' 'qt5-x11extras' 'libx11' 'libxcb')
makedepends=('git' 'qt5-tools')
source=("git+https://github.com/7b7b/$pkgname")
sha256sums=("SKIP")

build() {
  cd "$pkgname"
  qmake QMAKE_CFLAGS_ISYSTEM= PREFIX=/usr DATADIR=share
  make
}

package() {
  cd "$pkgname"
  make INSTALL_ROOT="$pkgdir" install
}
