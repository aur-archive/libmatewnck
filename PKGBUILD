# Maintainer : Martin Wimpress <code@flexion.org>
# Contributor: Giovanni "Talorno" Ricciardi <kar98k.sniper@gmail.com>
# Contributor: Xpander <xpander0@gmail.com>

pkgname=libmatewnck
pkgver=1.6.1
pkgrel=5
pkgdesc="Description: MATE Window Navigator Construction Kit. A library to use for writing pagers and task lists."
url="http://mate-desktop.org"
arch=('i686' 'x86_64' 'armv6h' 'armv7h')
license=('LGPL')
depends=('gtk2' 'libxres' 'startup-notification')
makedepends=('gobject-introspection' 'mate-common' 'perl-xml-parser')
options=('!emptydirs')
source=("http://pub.mate-desktop.org/releases/1.6/${pkgname}-${pkgver}.tar.xz")
sha1sums=('10e2def928dd74529c49a624803187098ea2b0f6')

build() {
    cd "${srcdir}/${pkgname}-${pkgver}"
    ./configure \
        --prefix=/usr \
        --disable-static \
        --enable-gtk-doc \
        --enable-startup-notification \
        --enable-introspection
    make
}

package() {
    cd "${srcdir}/${pkgname}-${pkgver}"
    make DESTDIR="${pkgdir}" install
}
