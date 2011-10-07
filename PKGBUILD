# Author: Tobias Quinn <tobias@tobiasquinn.com>
# Maintainer: Tobias Quinn <tobias@tobiasquinn.com>
pkgname=gnome-shell-mousewheel-zoom
pkgver=0.5.3
pkgrel=2
pkgdesc="Enable mousewheel zoom using left-alt key using gnome-shell"
arch=('i686' 'x86_64')
url="https://github.com/tobiasquinn/gnome-shell-mousewheel-zoom"
license=('GPL3')
depends=('python2' 'dbus-python' 'python-xlib' 'gnome-shell')
conflicts=('gnome-shell-mousewheel-zoom-git')
provides=('gnome-shell-mousewheel-zoom')
source=("gnome-shell-mousewheel-zoom_$pkgver.tar.gz::https://github.com/tobiasquinn/gnome-shell-mousewheel-zoom/tarball/upstream/$pkgver")
md5sums=('a88c5dbc922d23d81d293ea2cb5129bf')
_sourcename=('tobiasquinn-gnome-shell-mousewheel-zoom-1f1e4cb')
build() {
  # Change to use python2
  sed -i "s/usr\/bin\/env python$/usr\/bin\/env python2/" ${srcdir}/${_sourcename}/mousewheelzoom.py
}

package() {
  install -D -m755 ${srcdir}/${_sourcename}/mousewheelzoom.py "${pkgdir}/usr/bin/mousewheelzoom.py" || return 1
  install -D -m644 ${srcdir}/${_sourcename}/mousewheelzoom.py.desktop "${pkgdir}/etc/xdg/autostart/mousewheelzoom.py.desktop" || return 1
}

# vim:set ts=2 sw=2 et:
