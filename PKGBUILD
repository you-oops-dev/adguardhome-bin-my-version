# Maintainer: Marc Vidal <mvidaldp@gmail.com>
# Unofficial Maintainer: you-oops-dev <The profile (AUR) has all the contacts for communication or write to GitHub>

pkgname=adguardhome-bin
_pkgname=AdGuardHome
pkgver=0.107.5
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
source=(sysusers.conf tmpfiles.conf AdGuardHome.service)
options=('!strip' '!debug')

source_i686=("${_pkgname}-${pkgver}.tar.gz::${_releaseurl}/${_pkgname}_linux_386.tar.gz")
source_x86_64=("${_pkgname}-${pkgver}.tar.gz::${_releaseurl}/${_pkgname}_linux_amd64.tar.gz")
source_aarch64=("${_pkgname}-${pkgver}.tar.gz::${_releaseurl}/${_pkgname}_linux_arm64.tar.gz")
source_armv5h=("${_pkgname}-${pkgver}.tar.gz::${_releaseurl}/${_pkgname}_linux_armv5.tar.gz")
source_armv6h=("${_pkgname}-${pkgver}.tar.gz::${_releaseurl}/${_pkgname}_linux_armv6.tar.gz")
source_armv7h=("${_pkgname}-${pkgver}.tar.gz::${_releaseurl}/${_pkgname}_linux_armv7.tar.gz")

sha256sums=('SKIP'
            'SKIP'
            'SKIP')
sha256sums_i686=('b1941ef2b3580f48014a935e5d2fb885baa84f99d415b910488ddce95b90382f')
sha256sums_x86_64=('b1941ef2b3580f48014a935e5d2fb885baa84f99d415b910488ddce95b90382f')
sha256sums_aarch64=('b1941ef2b3580f48014a935e5d2fb885baa84f99d415b910488ddce95b90382f')
sha256sums_armv5h=('b1941ef2b3580f48014a935e5d2fb885baa84f99d415b910488ddce95b90382f')
sha256sums_armv6h=('b1941ef2b3580f48014a935e5d2fb885baa84f99d415b910488ddce95b90382f')
sha256sums_armv7h=('b1941ef2b3580f48014a935e5d2fb885baa84f99d415b910488ddce95b90382f')

package() {
    install -Dm755 "${_pkgname}/${_pkgname}" "${pkgdir}/var/lib/adguardhome/${_pkgname}"
    install -Dm644 "${_pkgname}.service" "${pkgdir}/usr/lib/systemd/system/${_pkgname}.service"
    install -Dm644 "${srcdir}/sysusers.conf" "${pkgdir}/usr/lib/sysusers.d/${_pkgname}.conf"
    install -Dm644 "${srcdir}/tmpfiles.conf" "${pkgdir}/usr/lib/tmpfiles.d/${_pkgname}.conf"
}
