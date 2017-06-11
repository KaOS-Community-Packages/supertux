pkgname=supertux2
_pkgname=supertux
pkgver=0.5.1
pkgrel=2
pkgdesc="SuperTux is a jump'n'run game with strong inspiration from the Super Mario Bros. games for the various Nintendo platforms."
url="https://github.com/SuperTux/supertux"
arch=('x86_64')
license=('GPL3')
depends=('sdl2' 'sdl2_image' 'openal' 'glew' 'boost' 'boost-libs' 'curl' 'libogg' 'libvorbis')
source=("https://github.com/SuperTux/supertux/releases/download/v${pkgver}/SuperTux-v${pkgver}-Source.tar.gz")
md5sums=('b8b678362e3c5c9e366fb1fb3550a2e0')

build() {
    cd "SuperTux-v${pkgver}-Source"
    cmake -DCMAKE_BUILD_TYPE=Release -DINSTALL_SUBDIR_BIN=bin -DCMAKE_INSTALL_PREFIX=/usr
    make
}

package() {
  cd "SuperTux-v${pkgver}-Source"
  make DESTDIR=${pkgdir} install
}
