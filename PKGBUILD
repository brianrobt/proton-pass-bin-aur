# Maintainer: Mysti

pkgname=proton-pass-bin
pkgver=1.23.0
pkgrel=1
pkgdesc="Open-source password manager for effortless protection. Securely store, share and auto-login your accounts with Proton Pass, using end-to-end encryption trusted by millions."
arch=("x86_64")
url="https://proton.me/pass"
groups=("ProtonPass")
source=("https://proton.me/download/PassDesktop/linux/x64/proton-pass_${pkgver}_amd64.deb")
sha256sums=('7b0acf937bf58e017ceee63eecff2841d58045cb8529d7e2335073ba530f0698')
conflicts=('proton-pass' 'protonpass')
replaces=('proton-pass' 'protonpass')

package() {
	tar -xvf data.tar.xz -C "$pkgdir/"

	install -d "$pkgdir/opt/"
	mv "$pkgdir/usr/lib/proton-pass" "$pkgdir/opt/"

	ln -sf "/opt/proton-pass/Proton Pass" "$pkgdir/usr/bin/proton-pass"

	rm -rf "$pkgdir"/usr/share/{doc,lintian}
}
