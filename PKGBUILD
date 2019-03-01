# Maintainer: Knut Ahlers <knut@ahlers.me>
# Collaborator: Julien Coloos <julien.coloos [at] gmail [dot] com>

pkgname=initrd-ssh-cryptsetup
pkgver=0.7
pkgrel=1
pkgdesc="Allows for LUKS-encrypted devices to be unlocked remotely over SSH"
arch=('any')
url="https://github.com/suiryc/archlinux-$pkgname"
license=('GPL3')
depends=(
	'dropbear'
	'cryptsetup'
	'mkinitcpio-nfs-utils'
	'iproute2'
)
install=$pkgname.install
changelog=ChangeLog
source=(
	"ssh-cryptsetup.hook"
	"ssh-cryptsetup.install"
	"$pkgname.install"
)
sha512sums=('4875054e8c49002895129b892429eac9c8eec285bde5d64e512135abc81ae9bb70247e8bfc5eb874ba6bd401a017657cf53a849235cbfd5c1cfb0abbf66d01d8'
            'aa5582830776d018ad59e12dcc22d3cfa27bd434827987fab0a85e4f92cc3a6ec2ed16256ea3b5557eac5ffafbe5d979ce0f9d86c3cea9440c5ecddb4c0e2adc'
            'e5f5adb46cfda8e87ff0f4641310c6dc8e39f9ed58e6b4fd8e9b8389f66f88274b3513813a2e2e61a0cf9a32e16a52f69213752b12acdf324429230b632afe4c')

package() {
	install -Dm644 "$srcdir/ssh-cryptsetup.install" "$pkgdir/usr/lib/initcpio/install/ssh-cryptsetup"
	install -Dm644 "$srcdir/ssh-cryptsetup.hook" "$pkgdir/usr/lib/initcpio/hooks/ssh-cryptsetup"
}
