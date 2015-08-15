# Maintainer: Ilya Medvedev <medved55rus [at] gmail [dot] com>

pkgname=batti-faenza
pkgver=0.3.8
pkgrel=1
pkgdesc="batti with Faenza icon theme support"
arch=('any')
url="http://code.google.com/p/batti-gtk/"
license=('GPL')
depends=('dbus-python' 'pygtk' 'gtk2' 'upower' 'hicolor-icon-theme' 'faenza-icon-theme')
optdepends=('notification-daemon: for power status notifications' 'xfce4-notifyd: alternative to notification-daemon')
provides=('batti')
conflicts=('batti')
install="batti.install"
source=("http://batti-gtk.googlecode.com/files/batti-$pkgver.tar.gz"
	"Battery_Faenza_icon.patch"
	"BatteryMonitor_Faenza_icon.patch")
md5sums=('4b239ead1643c95a6d89c380bc167781'
         '12c0a0390347a83246f730e94f84b3ea'
         '6a85f88aa5b90a184567f1cc6d92d4d3')

build() {
    cd "$srcdir/batti-$pkgver"
    
    patch -p1 -i "${srcdir}/Battery_Faenza_icon.patch"
    patch -p1 -i "${srcdir}/BatteryMonitor_Faenza_icon.patch"
    
    python2 setup.py install --root="$pkgdir/" --optimize=1
}
