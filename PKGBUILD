# Maintainer: Florian Zeitz <florob at babelmonkeys dot de>

pkgname=numactl
pkgver=2.0.7
pkgrel=1
pkgdesc="Simple NUMA policy support"
arch=('i686' 'x86_64')
url="http://oss.sgi.com/projects/libnuma/"
license=('LGPL2.1' 'GPL2')
depends=('perl')
source=(ftp://oss.sgi.com/www/projects/libnuma/download/$pkgname-${pkgver/_/-}.tar.gz)
sha1sums=('dfdf539da65d1e880f04202071c139c4d2ba2da9')

build() {
  cd "$srcdir/$pkgname-${pkgver/_/-}"
  make || return 1
  make prefix="$pkgdir/usr" libdir="$pkgdir/usr/lib" install || return 1
  rm -r $pkgdir/usr/share/man/man2
}
