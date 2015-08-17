# Maintainer: Alexej Magura <agm2819*gmail*>
# 
# 
pkgname=savex
pkgver=0.1b.rev5
pkgrel=2
pkgdesc="A better way to start window managers that you just want to try out without having to worry about them crashing and killing the X Server."
arch=('i686' 'x86_64')
url="https://sourceforge.net/p/savex/"
license=('GPL3')
depends=(gcc-libs)
source=("http://sourceforge.net/projects/savex/files/0.1b.rev5/${pkgname}-${pkgver}.tar.gz/download" "Makefile")
md5sums=(bbd52245290239b5f4af4bfa8a33e606 7b3665560a17748c5a97be585411d3a3)

prepare() {
    cd $srcdir/$pkgname-$pkgver
    diff -u Makefile $srcdir/Makefile > Makefile.diff || echo "Okay"
    patch Makefile Makefile.diff
}

build() {
    cd $srcdir/$pkgname-$pkgver

    make

}

package() {
    cd $srcdir/$pkgname-$pkgver

    make DESTDIR=$pkgdir install


}
