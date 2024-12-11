pkgname=astian-wallpapers
arch=("x86_64")
depends=()
makedepends=("extra-cmake-modules")
pkgdesc="Built-in wallpapers for Astian_OS."
pkgrel=1
pkgver=1.0.0
url="https://astian.org"
license=("GPL")
source=("https://github.com/Ponchale/${pkgname}/archive/refs/tags/${pkgver}.tar.gz")
sha256sums=('89b690fcca14e3cd271ddcadebf9465d1f1d9a28e12f80cdb8e3da29dae40a41')

prepare() {
    cd "${srcdir}/${pkgname}-${pkgver}"
    mkdir -p build
}

build() {
    cd "${srcdir}/${pkgname}-${pkgver}/build"
    cmake -DCMAKE_INSTALL_PREFIX=/usr ..
    make
}
package() {
    cd ${pkgname}-${pkgver}/build
    make DESTDIR="${pkgdir}" install
}
