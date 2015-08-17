# Contributer: giacomogiorgianni@gmail.com 

pkgname=texel
name=Texel
pkgver=0.3.1
pkgrel=1
pkgdesc="is a mass music meta data tagger"
arch=('i686' 'x86_64')
url="http://opendesktop.org/content/show.php/Texel?content=156784"
license=('GPL')
categories=()
depends=('kdebase-runtime' 'sox' 'libmusicbrainz3' 'taglib' 'libofa' 'automoc4')
makedepends=('gcc' 'cmake' )
source=("http://switch.dl.sourceforge.net/project/texel/source/0.3/$pkgname-$pkgver.tar.gz")
md5sums=('aff5b10577ae95f101f657d99ba0954c')

build() {
   cd $srcdir/$pkgname-$pkgver
    if [ -d build ] ; then
        rm build/* -rf
    else
        mkdir build
    fi
    cd build
   cmake -DCMAKE_INSTALL_PREFIX=/usr .. 
   make
}

package() {
  cd ${srcdir}/${pkgname}-${pkgver}/build
  make DESTDIR="$pkgdir/" install
}

