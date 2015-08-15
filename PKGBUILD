# Contributor: Andreas Schrafl <aschrafl@gmail.com>
# Based on work form : Alucryd <alucryd@gmail.com>
pkgname=gnome-shell-extension-autohide-topbar
pkgver=2.0
pkgrel=6
pkgdesc="A gnome-shell extension to hide the top bar automatically"
url=("https://github.com/Shanto/GNOME-3.2-Shell-extensions")
source=("https://github.com/Shanto/GNOME-3.2-Shell-extensions/tarball/master")
md5sums=('c582a7e6bdafed7885fb4bde632ff968')

_folder=('Shanto-GNOME-3.2-Shell-extensions-cbf7940')
_extname=('autohidetopbar@fpmurphy.com')

arch=('any')
license=('GPL2')
depends=('gnome-shell')

build() {
   # cd "$srcdir/$_extname"
   # msg "Increase double-clicking threshold."
   # sed -i 's/TIME_DELTA = 1500/TIME_DELTA = 2000/g' extension.js
	cd $srcdir/$_folder/$_extname
	sed -i 's/3\.2/3\.8/g' metadata.json
}

package() {
	cd "$srcdir/$_folder"
	mkdir -p "$pkgdir/usr/share/gnome-shell/extensions/"
	cp -R "$_extname" "$pkgdir/usr/share/gnome-shell/extensions"
}
