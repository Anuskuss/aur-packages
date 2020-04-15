# Maintainer: Sumner Evans <me [at] sumnerevans [dot] com>

pkgbase='navidrome-bin'
pkgname=(navidrome-bin)
pkgver='0.14.4'
pkgrel=1
pkgdesc='Music Server and Streamer compatible with Subsonic/Airsonic'
url='https://www.navidrome.org/'
license=('GPL3')
arch=(x86_64 armv6h armv7h aarch64)
provides=('navidrome')
conflicts=('navidrome')
depends=('glibc' 'ffmpeg')
source_x86_64=('https://github.com/deluan/navidrome/releases/download/v0.14.4/navidrome_0.14.4_Linux_x86_64.tar.gz')
source_armv6h=('https://github.com/deluan/navidrome/releases/download/v0.14.4/navidrome_0.14.4_Linux_armv6.tar.gz')
source_armv7h=('https://github.com/deluan/navidrome/releases/download/v0.14.4/navidrome_0.14.4_Linux_armv7.tar.gz')
source_aarch64=('https://github.com/deluan/navidrome/releases/download/v0.14.4/navidrome_0.14.4_Linux_arm64.tar.gz')
md5sums_x86_64=('cdad02bfab2a5e9f1b2da13b6620cd57')
md5sums_armv6h=('23725b36a2f05b5113900d0ae36bf6ac')
md5sums_armv7h=('fa63438ae5e0371d7f89ac4eadd2b170')
md5sums_aarch64=('11297142d36872fdcdd6df5627e9d1c0')

package() {
  install -Dm755 "$srcdir/navidrome" "$pkgdir/usr/bin/navidrome"
}

