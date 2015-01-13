# Maintainer: Giancarlo Razzolini <grazzolini@gmail.com>
pkgname=mkinitcpio-ppp
pkgver=0.0.1
pkgrel=1
pkgdesc="PPP hook for dialing to a ppp connection inside the initrd. In combination with dropbear_initrd_encrypt, it allows remote unlocking over the internet"
arch=('any')
url="https://github.com/grazzolini/mkinitcpio-ppp"
license=('BSD')
depends=('ppp')
install=$pkgname.install
source=('ChangeLog' "$pkgname.install" 'ppp_hook' 'ppp_install')
changelog='ChangeLog'
sha256sums=('e3ff4bf495ff342c591f8036d15eb613b4f216bd9498ad83791aaf6341b786a3'
            '75d1de5480b1fbdbd81dd16c6b2b65f8167e50105e4be4f0f52ce517ead9cf8e'
            '257bee86a3f6c1b3d99ed77fbeb96389a24ee5859ac3978efa796c9a763b68b3'
            '43843daa8ec2c9a65dec35bc91885de7ea03f49738b3a9a47ecbb1c95d5da2ca')

package() {
  install -Dm644 "$srcdir/ppp_hook"      "$pkgdir/usr/lib/initcpio/hooks/ppp"
  install -Dm644 "$srcdir/ppp_install"   "$pkgdir/usr/lib/initcpio/install/ppp"
}
