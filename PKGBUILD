pkgname=simavr
pkgver=1.5.pty
pkgrel=1
pkgdesc='AVR simulator with serial to PTY interface'
url='https://github.com/andi8086/simavr'
arch=('x86_64')
license=('GPLv3')
makedepends=('avr-gcc' 'avr-libc')
source=()

prepare() {
	ln -snf "$startdir" "$srcdir/$pkgname"
}

build() {
	cd "$pkgname"
	make
}

package() {
	cd "$pkgname"
	make DESTDIR="$pkgdir/usr" install
}

