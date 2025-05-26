# Maintainer: Luna Team

pkgname=blackarch-gui-installer
pkgver=1.0.0
pkgrel=1
pkgdesc="GUI installer for BlackArch Linux tools"
arch=('any')
url="https://github.com/bunnyhop-dev/blackarch-gui-installer"
license=('GPL3')
depends=('python' 'python-pyqt5' 'pacman' 'sudo')
makedepends=('python-setuptools')
source=("https://github.com/bunnyhop-dev/blackarch-gui-installer/releases/download/Release-0526/$pkgname-$pkgver.tar.gz")
sha512sums=('SKIP')

package() {
  cd "$srcdir/$pkgname-$pkgver"

  install -Dm755 blackarch-gui-installer.py "$pkgdir/usr/bin/$pkgname"

  if [ -f LICENSE ]; then
    install -Dm644 LICENSE "$pkgdir/usr/share/licenses/$pkgname/LICENSE"
  else
    echo "WARNING: LICENSE file not found in source directory."
  fi
}

