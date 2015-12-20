pkgname=supertux2
_pkgname=supertux
pkgver=0.4.0
pkgrel=1
pkgdesc="SuperTux is a jump'n'run game with strong inspiration from the Super Mario Bros. games for the various Nintendo platforms."
url="https://github.com/SuperTux/supertux"
arch=('x86_64')
license=('GPL3')
depends=('sdl2' 'sdl2_image' 'physfs' 'openal' 'glew' 'boost' 'boost-libs' 'curl' 'libogg' 'libvorbis')
source=("https://github.com/SuperTux/supertux/releases/download/v${pkgver}/${_pkgname}-${pkgver}.tar.bz2")
md5sums=('8acc3aa1077f0da95c99fdd5f4925088')

build() {
    cd ${srcdir}/${_pkgname}-${pkgver}
    cmake -D CMAKE_INSTALL_PREFIX=/usr -D INSTALL_SUBDIR_BIN=bin .
    make
}

package() {
  cd ${srcdir}/${_pkgname}-${pkgver}
  make DESTDIR=${pkgdir} install
}
