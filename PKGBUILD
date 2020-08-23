# Original PKGBUILD By: Furkan Kardame <furkan@fkardame.com>
# Contributor:Andreas Gerlach <andi@appelgriebsch.com>
# Maintainer: Andreas Gerlach <andi@appelgriebsch.com>

pkgname=chromium-widevine
pkgdesc='Systemd container based on Debian armhf, Chromium with widevine plugin'
pkgver=4.10.1610.6
pkgrel=3
arch=('aarch64')
url='https://www.widevine.com/'
license=('custom')
depends=('gcc-libs' 'glib2' 'glibc' 'xorg-xhost' 'git' 'curl')
makedepends=('debian-archive-keyring' 'debootstrap')
options=('!strip')
install=$pkgname.install
source=("chrome-eula_text.html::https://www.google.com/intl/en/chrome/privacy/eula_text.html"
        "launch_chromium_widevine.sh"
        "chromium.png"
        "chromium-widevine.desktop")
sha256sums=('SKIP'
            '5e11a5e8688e18bd261152a81127ffc65948ac8031c8b830c4127c47be041c08'
            '5c1d420c17b308987fda5fe731fc42b5bee3b9bd591aae571fd1cfc14eeb293b'
            'eb02fe3e5b80589e277864357ce8ac5e537c2cda8c37feb5b2c9130a8c9dfd12')

package() {
  mkdir -p "${pkgdir}"/usr/share/chromium-widevine/
  mkdir -p "${pkgdir}"/usr/share/applications/
  mkdir -p "${pkgdir}"/usr/local/bin/
  install -Dm644 ../chrome-eula_text.html "$pkgdir/usr/share/licenses/$pkgname/eula_text.html"
  install -Dm644 ../chrome-eula_text.html chromium.png "$pkgdir/usr/share/chromium-widevine/"
  install -Dm644 chromium-widevine.desktop "$pkgdir/usr/share/applications/"
  install -Dm755 launch_chromium_widevine.sh "$pkgdir/usr/local/bin/"
}
