# Maintainer: Eric Vidal <eric@obarun.org>

pkgname=gpm-s6serv
pkgver=0.1
pkgrel=1
pkgdesc="gpm service for s6"
arch=(x86_64)
license=('beerware')
depends=('gpm' 's6' 's6-rc' 's6-boot')
conflicts=()
install=gpm-s6serv.install
source=('gpm.daemon.run.s6'	
		'gpm.log.run.s6'
		'LICENSE')
md5sums=('a54fdaac00cd79383e8d4574618b7d08'
         'fb7c71e44133e5a264bf1c01ec86318b'
         '191a37ae657aa17e37e75d0242865dba')

package() {
	
	# daemon
	install -Dm 0755 "$srcdir/gpm.daemon.run.s6" "$pkgdir/etc/s6-serv/available/classic/gpm/run"
	
	# log
	install -Dm 0755 "$srcdir/gpm.log.run.s6" "$pkgdir/etc/s6-serv/available/classic/gpm/log/run"
	
	install -Dm 0755 "$srcdir/LICENSE" "$pkgdir/usr/share/licenses/gpm-s6serv/LICENSE"
}
