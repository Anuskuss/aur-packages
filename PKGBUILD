# Maintainer: Hyacinthe Cartiaux <hyacinthe.cartiaux@free.fr>
# Contributor: zhuqin <zhuqin83@gmail.com>
pkgname=lensfun-git
_gitname=lensfun
pkgver=0.3.2.r2032.gad957f64
pkgrel=1
pkgdesc="Database of photographic lenses and a library that allows advanced access to the database"
arch=(i686 x86_64)
url="https://lensfun.github.io/"
license=('LGPL3')
depends=('glibc' 'glib2')
makedepends=('git' 'python' 'libpng' 'cmake')
optdepends=('python: for lensfun-update-data and lensfun-add-adapter')
provides=('lensfun=0.3.0')
conflicts=('lensfun')
source=("lensfun::git+https://github.com/lensfun/lensfun.git")
sha256sums=('SKIP')

pkgver() {
  cd $_gitname
  git describe --long | sed -r 's/^v//;s/([^-]*-g)/r\1/;s/-/./g'
}

build() {
  cd $_gitname
  cmake -DCMAKE_INSTALL_PREFIX=/usr \
        -DCMAKE_INSTALL_LIBDIR=lib \
        -DCMAKE_BUILD_TYPE=Release \
        .
  make
}

package() {
  cd $_gitname
  make DESTDIR="$pkgdir/" install
}
