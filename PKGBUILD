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
            '4d9d72518208496e1a6868962753d8f99812232f5f45b098c12279888f32c96f'
            '86ad9ae03f575c34309d0e1cce8adf9d82586fd816ecb26be2f91738006bb5bb')

package() {
  install -Dm644 "$srcdir/ppp_hook"      "$pkgdir/usr/lib/initcpio/hooks/ppp"
  install -Dm644 "$srcdir/ppp_install"   "$pkgdir/usr/lib/initcpio/install/ppp"
}
