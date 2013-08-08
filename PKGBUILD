pkgname=slim-theme-redhex
pkgver=1.0
pkgrel=1
pkgdesc="Red Hex SLiM theme"
url="http://lp.wildwestscifi.net"
arch=('i686' 'x86_64')
license=('GPL')
groups=()
depends=()
makedepends=()
provides=('slim-theme-redhex')
conflicts=()
replaces=()
backup=()
options=()
source=()
noextract=()
md5sums=()

_gitroot="https://github.com/whoracle/slimtheme"
_gitname=slimtheme

build() {
  cd "$srcdir"

  if [ -d $srcdir/$_gitname ] ; then
    cd $srcdir/$_gitname && git pull origin
    msg "The local files are updated."
  else
    git clone $_gitroot $_gitname
  fi

  msg "GIT checkout done or server timeout"
}

package() {
  cd "$srcdir/$_gitname"

  install -v -d "$pkgdir/usr/share/slim/themes/redhex"
  cp slim.theme panel.png background.png $pkgdir/usr/share/slim/themes/redhex/

  msg "Finished packaging"
}
