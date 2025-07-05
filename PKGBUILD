# Maintainer: Marc Vidal <mvidaldp@gmail.com>
# Unofficial Maintainer: you-oops-dev <The profile (AUR) has all the contacts for communication or write to GitHub>

pkgname=adguardhome-bin
_pkgname=AdGuardHome
pkgver=0.107.63
_pkgver="v${pkgver}"
pkgrel=1
pkgdesc='Network-wide ads and trackers blocking DNS server (binary version).'
arch=('i686' 'x86_64' 'aarch64' 'armv5h' 'armv6h' 'armv7h')
url='https://github.com/AdguardTeam/AdGuardHome'
license=('GPL')
provides=("${pkgname}")
conflicts=('adguardhome')
install=adguardhome-bin.install
_releaseurl="${url}/releases/download/${_pkgver}"
source=(sysusers.conf tmpfiles.conf AdGuardHome.service adguard-cert.sh)
options=('!strip' '!debug')

source_i686=("${_pkgname}-${pkgver}.tar.gz::${_releaseurl}/${_pkgname}_linux_386.tar.gz")
source_x86_64=("${_pkgname}-${pkgver}.tar.gz::${_releaseurl}/${_pkgname}_linux_amd64.tar.gz")
source_aarch64=("${_pkgname}-${pkgver}.tar.gz::${_releaseurl}/${_pkgname}_linux_arm64.tar.gz")
source_armv5h=("${_pkgname}-${pkgver}.tar.gz::${_releaseurl}/${_pkgname}_linux_armv5.tar.gz")
source_armv6h=("${_pkgname}-${pkgver}.tar.gz::${_releaseurl}/${_pkgname}_linux_armv6.tar.gz")
source_armv7h=("${_pkgname}-${pkgver}.tar.gz::${_releaseurl}/${_pkgname}_linux_armv7.tar.gz")

sha256sums=('SKIP'
            'SKIP'
            'SKIP'
            'SKIP')
sha256sums_i686=('d1f370e6e0ef7150bbe8762125d04fb8fff55164916f033a04b0be420ad510e1')
sha256sums_x86_64=('d1f370e6e0ef7150bbe8762125d04fb8fff55164916f033a04b0be420ad510e1')
sha256sums_aarch64=('d1f370e6e0ef7150bbe8762125d04fb8fff55164916f033a04b0be420ad510e1')
sha256sums_armv5h=('d1f370e6e0ef7150bbe8762125d04fb8fff55164916f033a04b0be420ad510e1')
sha256sums_armv6h=('d1f370e6e0ef7150bbe8762125d04fb8fff55164916f033a04b0be420ad510e1')
sha256sums_armv7h=('d1f370e6e0ef7150bbe8762125d04fb8fff55164916f033a04b0be420ad510e1')

package() {
    install -Dm755 "${_pkgname}/${_pkgname}" "${pkgdir}/var/lib/adguardhome/${_pkgname}"
    install -Dm644 "${_pkgname}.service" "${pkgdir}/usr/lib/systemd/system/${_pkgname}.service"
    install -Dm644 "${srcdir}/sysusers.conf" "${pkgdir}/usr/lib/sysusers.d/${_pkgname}.conf"
    install -Dm644 "${srcdir}/tmpfiles.conf" "${pkgdir}/usr/lib/tmpfiles.d/${_pkgname}.conf"
    install -Dm755 "${srcdir}/adguard-cert.sh" "${pkgdir}/usr/bin/adguard-cert.sh"
}
