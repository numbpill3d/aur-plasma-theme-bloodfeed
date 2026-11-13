# Maintainer: numbpill3d <void@nothing>
# Contributor: numbpill3d <void@nothing>
pkgname=plasma-theme-bloodfeed
pkgname+=(sddm-theme-bloodfeed)
pkgname+=(plymouth-theme-bloodfeed)
pkgver=1.0
pkgrel=1
pkgdesc='Crimson VHS KDE Plasma 6 theme suite by splicer scorn (voidrane)'
arch=('any')
url='https://github.com/numbpill3d/bloodfeed'
license=('GPL-3.0-or-later')
depends=('plasma-workspace' 'kwin' 'kvantum' 'kde-icon-theme')
optdepends=(
  'konsole: Konsole terminal colour scheme'
  'kitty: kitty terminal colour scheme'
  'sddm: SDDM login theme'
  'plymouth: Plymouth boot splash'
)
source=("${pkgname}-1.0.tar.gz::https://github.com/numbpill3d/bloodfeed/archive/refs/tags/v1.0.tar.gz")
sha256sums=('SKIP')


package_plasma-theme-bloodfeed() {
  cd "$srcdir/bloodfeed-1.0"

  install -d "$pkgdir/usr/share/plasma/desktoptheme"
  cp -r plasma/desktoptheme/Bloodfeed "$pkgdir/usr/share/plasma/desktoptheme/"
  install -d "$pkgdir/usr/share/plasma/look-and-feel"
  cp -r plasma/look-and-feel/scorn.bloodfeed "$pkgdir/usr/share/plasma/look-and-feel/"
  install -d "$pkgdir/usr/share/aurorae/themes"
  cp -r aurorae/Bloodfeed "$pkgdir/usr/share/aurorae/themes/"
  install -Dm644 colors/Bloodfeed.colors "$pkgdir/usr/share/color-schemes/Bloodfeed.colors"
  install -d "$pkgdir/usr/share/icons"
  cp -r icons/Bloodfeed "$pkgdir/usr/share/icons/"
  install -d "$pkgdir/usr/share/Kvantum"
  cp -r kvantum/Bloodfeed "$pkgdir/usr/share/Kvantum/"
  install -Dm644 terminal/Bloodfeed.colorscheme "$pkgdir/usr/share/konsole/Bloodfeed.colorscheme"
  install -Dm644 terminal/Bloodfeed.profile "$pkgdir/usr/share/konsole/Bloodfeed.profile"
  install -Dm644 terminal/bloodfeed-kitty.conf "$pkgdir/usr/share/kitty/themes/bloodfeed-kitty.conf"

  install -Dm644 LICENSE "$pkgdir/usr/share/licenses/$pkgname/LICENSE"
}

package_sddm-theme-bloodfeed() {
  depends=('sddm')
  optdepends=('plasma-theme-bloodfeed: the Plasma 6 half of the suite')
  pkgdesc='SDDM login theme — Crimson VHS KDE Plasma 6 theme suite by splicer scorn (voidrane)'
  cd "$srcdir/bloodfeed-1.0"
  install -d "$pkgdir/usr/share/sddm/themes"
  cp -r sddm/bloodfeed "$pkgdir/usr/share/sddm/themes/"
  install -Dm644 LICENSE "$pkgdir/usr/share/licenses/$pkgname/LICENSE"
}

package_plymouth-theme-bloodfeed() {
  depends=('plymouth')
  optdepends=('plasma-theme-bloodfeed: the Plasma 6 half of the suite')
  pkgdesc='Plymouth boot splash — Crimson VHS KDE Plasma 6 theme suite by splicer scorn (voidrane)'
  cd "$srcdir/bloodfeed-1.0"
  install -d "$pkgdir/usr/share/plymouth/themes"
  cp -r plymouth/bloodfeed "$pkgdir/usr/share/plymouth/themes/"
  install -Dm644 LICENSE "$pkgdir/usr/share/licenses/$pkgname/LICENSE"
}
