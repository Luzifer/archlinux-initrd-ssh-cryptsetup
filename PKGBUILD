# Maintainer: Knut Ahlers <knut@ahlers.me>
# Collaborator: Julien Coloos <julien.coloos [at] gmail [dot] com>

pkgname=initrd-ssh-cryptsetup
pkgver=0.8
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
	'049ad69f78663e1c3202b089fb17ea4e07a524418ab6049f3890e1dc4871132c50d35ed0e73fb18230e3ec9c71c8b0cecba3e042f3e900a9633c8d734e5c30b7'
	'e5f5adb46cfda8e87ff0f4641310c6dc8e39f9ed58e6b4fd8e9b8389f66f88274b3513813a2e2e61a0cf9a32e16a52f69213752b12acdf324429230b632afe4c')

package() {
	install -Dm644 "$srcdir/ssh-cryptsetup.install" "$pkgdir/usr/lib/initcpio/install/ssh-cryptsetup"
	install -Dm644 "$srcdir/ssh-cryptsetup.hook" "$pkgdir/usr/lib/initcpio/hooks/ssh-cryptsetup"
}
