# Maintainer: Leonid Shagabutdinov <leonid@shagabutdinov.com>
# Upstream URL: https://github.com/seletskiy/runki
#
# Dont forget to star the repo if you liked the package

pkgname=runki
pkgver=20140608
pkgrel=1
pkgdesc="Pacman database extraction utility"
arch=('any')
url="https://github.com/Shagabutdinov/runki"
license=('MIT')
depends=('pacman')
makedepends=('git')
conflicts=('runki')
provides=('runki')
source=("$pkgname"::'git://github.com/Shagabutdinov/runki.git')
md5sums=('SKIP')

pkgver() {
  cd "$srcdir/$pkgname"
  git log -1 --format="%cd" --date=short | sed 's|-||g'
}

build() {
  cd "$srcdir/$pkgname"
  go build
}

package() {
  cd "$srcdir/$pkgname"
  mkdir -p $pkgdir/usr/bin
  mv runki $pkgdir/usr/bin
}