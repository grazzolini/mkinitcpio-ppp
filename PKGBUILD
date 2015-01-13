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
            '7f348d4bf74d19795b1c6e96fcb1ea1d30206434417a7b38b35354287c0d6dae'
            '8db2ae7bc35bba941883f323d3b285433c8035ffa7473547f1fe5b7b4e523b5b'
            '6a2d1234f411dd0393b42207c2447d53eaa19fd7887991870a04648ec2e49f6b')

package() {
  install -Dm644 "$srcdir/ppp_hook"      "$pkgdir/usr/lib/initcpio/hooks/ppp"
  install -Dm644 "$srcdir/ppp_install"   "$pkgdir/usr/lib/initcpio/install/ppp"
}
