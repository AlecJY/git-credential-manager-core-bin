_realname='git-credential-manager'
pkgname="${_realname}-bin"
pkgver=2.6.0
pkgrel=1
pkgdesc="Secure, cross-platform Git credential storage with authentication to GitHub, Azure Repos, and other popular Git hosting services."
arch=('any')
url='https://github.com/git-ecosystem/git-credential-manager'
license=('MIT')
source=("https://github.com/git-ecosystem/git-credential-manager/releases/download/v${pkgver}/gcm-win-x86-${pkgver}.zip")
depends=('git')
replaces=('git-credential-manager-core-bin')
conflicts=('git-credential-manager-core-bin')
install="${pkgname}.install"
sha256sums=('3bfba8e61483ddaad66811a4ec32689026619d4b2e6511e740e5227bc4965a41')

build() {
    cd "${srcdir}"
    rm gcm-win-x86-${pkgver}.zip
}

package() {
    cd "${srcdir}"
    install -Dm644 NOTICE "${pkgdir}/usr/share/licenses/${_realname}/LICENSE"
    rm NOTICE
    mkdir -p ${pkgdir}/usr/lib/git-core
    cp * "${pkgdir}/usr/lib/git-core"
}
