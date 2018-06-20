# Maintainer: Edmunt Pienkowsky <roed@onet.eu>

pkgname='rpi-cirrus'
pkgdesc='Scripts and config files for the Cirrus Logic Audio Card'
url='http://github.com/RoEdAl/rpi-cirrus-config'
pkgver='1.0'
pkgrel='1'
arch=('any')
license=('GPL')
depends=('alsa-utils')

source=(
    "${pkgname}-config-${pkgver}.tar.gz::http://github.com/RoEdAl/rpi-cirrus-config/archive/v${pkgver}.tar.gz"
)

md5sums=('805935019865f0564654cca140ed1b96')

package(){

    cd ${srcdir}/${pkgname}-config-${pkgver}

    install -d -m 0755 ${pkgdir}/usr/share/alsa/cards
    install -p -m 0644 alsa/RPiCirrus.conf ${pkgdir}/usr/share/alsa/cards

    install -d -m 0755 ${pkgdir}/usr/share/${pkgname}
    install -p -m 0644 mixer-scripts/rpi-cirrus-functions.sh ${pkgdir}/usr/share/${pkgname}
    install -p -m 0644 README.md ${pkgdir}/usr/share/${pkgname}

    install -d -m 0755 ${pkgdir}/usr/bin
    install -p -m 0755 mixer-scripts/rpicirrusctl.sh ${pkgdir}/usr/bin/rpicirrusctl
}
