# Maintainer: speps <speps at aur dot archlinux dot org>

pkgname=python2-backports
pkgver=1.0.1
pkgrel=1
pkgdesc="A collection of backported python features that run on python 2.5 or newer"
arch=('any')
url="http://www.icanblink.com"
license=('custom:PYTHON')
depends=('python2')
source=("http://download.ag-projects.com/SipClient/${pkgname/2}-$pkgver.tar.gz")
md5sums=('89005121e64171679aa25c5c25b56017')

build() {
  cd "$srcdir/${pkgname/2}-$pkgver"
  python2 setup.py build
}

package() {
  cd "$srcdir/${pkgname/2}-$pkgver"
  python2 setup.py install --root="$pkgdir/"

  # license
  install -Dm644 LICENSE \
    "$pkgdir/usr/share/licenses/$pkgname/LICENSE"
}
