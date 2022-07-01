# Maintainer: DN-debug <dev95nandi@gmail.com>

pkgname=sdorfehs
_pkgname="sdorfehs"
pkgver=1.4
pkgrel=1
pkgdesc="Enhanced successor of Ratpoison window manager"
conflicts=('sdorfehs')
arch=('x86_64')
license=('GPLv2')
depends=('libxinerama' 'readline' 'bash' 'perl' 'libxtst' 'libxft' 'texinfo')
url="git@github.com:jcs/sdorfehs.git"
source=("${_pkgname}"::"git+https://github.com/jcs/sdorfehs.git#branch=master"
        "${_pkgname}.desktop")
md5sums=('SKIP'
         'ba8b496db766ef5b2ad69ad9f7b32d71')

build() {
  cd "${srcdir}/${_pkgname}"
  make
}

package() {
  cd "${srcdir}/${_pkgname}"
  make DESTDIR="${pkgdir}" install

  install -Dm644 "${srcdir}/${_pkgname}.desktop" \
    "${pkgdir}/usr/share/xsessions/${_pkgname}.desktop"
}
