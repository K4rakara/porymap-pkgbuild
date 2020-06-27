
# Maintainer: Jack Johannesen

pkgname=porymap
pkgver=4.2.0
pkgrel=1
pkgdesc="Map editor for pokeemerald, pokefirered, and pokeruby."
arch=('i686' 'x86_64' 'x64')
url="https://github.com/huderlem/porymap"
license=('MIT')
depends=('qt5-base')
makedepends=('make' 'git' 'qt5-base')
provides=('porymap')
source=("git://github.com/huderlem/porymap.git")
md5sums=('SKIP')

build() {
	cd $srcdir/porymap
	qmake
	make
}

package() {
	# Cd into $pkgdir.
	cd $pkgdir

	# Create the required directories in $pkgdir.
	mkdir -p $pkgdir/usr/bin/
	mkdir -p $pkgdir/usr/share/applications/
	mkdir -p $pkgdir/usr/share/pixmaps/

	# Copy files to the created directories in $pkgdir.
	cp $srcdir/porymap/porymap $pkgdir/usr/bin/
	cp $srcdir/../porymap.png $pkgdir/usr/share/pixmaps/
	cp $srcdir/../porymap.desktop $pkgdir/usr/share/applications/

	# All done!
}
