#Contributor: CSSlayer <wengxt@gmail.com>

pkgname=kimtoy
pkgver=1.9
pkgdesc="Standalone input method panel"
pkgrel=1
arch=(i686 x86_64)
url="http://kde-apps.org/content/show.php/KIMToy?content=140967"
license=(GPL)
makedepends=(cmake automoc4)
depends=(kdebase-workspace)
options=()
source=(http://kde-apps.org/CONTENT/content-files/140967-kimtoy-${pkgver}.tar.bz2)

build() {
  cd ${srcdir}/${pkgname}-${pkgver}

  cmake -DCMAKE_INSTALL_PREFIX=`kde4-config --prefix` . || return 1
  make || return 1
}

package ()
{
  cd ${srcdir}/${pkgname}-${pkgver}
  make DESTDIR=${pkgdir} install || return 1
}
md5sums=('1109018a2b314fdec32f7465e8630efe')
