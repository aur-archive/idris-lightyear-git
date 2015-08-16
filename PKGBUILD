# Maintainer: Leif Warner <abimelech@gmail.com>
_gitname=lightyear
_authorName=ziman
pkgname=idris-$_gitname-git
pkgver=54.6ee4495
pkgrel=1
pkgdesc="Parser combinators for Idris"
url="https://github.com/$_authorName/$_gitname"
license=('custom:BSD3')
arch=('i686' 'x86_64')
depends=('idris')
source=("git://github.com/$_authorName/$_gitname.git")
md5sums=('SKIP')

pkgver() {
  cd $_gitname
  echo "$(git rev-list --count HEAD).$(git rev-parse --short HEAD)"
}
build() {
  cd $_gitname
  idris --build $_gitname.ipkg
}
package() {
  cd $_gitname
  TARGET=$pkgdir`idris --libdir` idris --install $_gitname.ipkg
}
