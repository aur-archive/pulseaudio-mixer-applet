# $Id: PKGBUILD 99926 2010-11-19 14:16:58Z heftig $
# Maintainer: Jan "heftig" Steffens <jan.steffens@gmail.com>
# Contributor: Samed Beyribey <ras0ir AT eventualis DOT org>

pkgname=pulseaudio-mixer-applet
pkgver=0.2.2
pkgrel=6
pkgdesc="GNOME panel applet to control PulseAudio devices and streams"
arch=(i686 x86_64)
url="https://launchpad.net/pama"
license=(GPL3)
depends=(gnome-media gnome-panel-bonobo libpulse glib2)
makedepends=(intltool)
source=(http://launchpad.net/pama/${pkgver%.*}/$pkgver/+download/pulseaudio-mixer-applet-$pkgver.tar.gz)
md5sums=('b7df43c999ad8583f779e678cfe768ae')

build() {
  cd "$srcdir/$pkgname-$pkgver"

  ./configure --prefix=/usr
  make
}

package() {
  cd "$srcdir/$pkgname-$pkgver"
  make DESTDIR="$pkgdir/" install
}
