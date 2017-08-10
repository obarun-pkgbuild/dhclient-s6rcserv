# Maintainer: Eric Vidal <eric@obarun.org>

pkgname=dhclient-s6rcserv
pkgver=0.1
pkgrel=2
pkgdesc="dhclient service for s6"
arch=(x86_64)
license=('beerware')
depends=('dhclient' 's6' 's6-rc' 's6-boot')
conflicts=()
install=dhclient-s6rcserv.install
source=('dhclient.daemon.dependencies.s6'
		'dhclient.daemon.pipeline-name.s6'
		'dhclient.daemon.producer-for.s6'
		'dhclient.daemon.run.s6'	
		'dhclient.daemon.type.s6'
		
		'dhclient.log.consumer-for.s6'
		'dhclient.log.dependencies.s6'
		'dhclient.log.run.s6'
		'dhclient.log.type.s6'
		
		'bundle.dhclient.contents.s6'
		'bundle.dhclient.type.s6'
		'LICENSE')
md5sums=('68b329da9893e34099c7d8ad5cb9c940'
         '04b57a0142c627e01df0cf9544e3ac40'
         '8176ff14bed4334863f4b413f8e34be3'
         'ba5c196bef0a79776a164cbe5829d1f0'
         '42c13bdd7f61c06ac59c1aaca9c0f07a'
         '56e5664d563ae433d33940193bed8384'
         '68b329da9893e34099c7d8ad5cb9c940'
         'a155da4aa5e4668924e44ce568e79c68'
         '42c13bdd7f61c06ac59c1aaca9c0f07a'
         'd01250573c8f41c987a60a1df0104f97'
         '71abe97e2554d37f1d12c5bf4945297f'
         '191a37ae657aa17e37e75d0242865dba')

package() {
	
	# bundle , trouble here user-dhclient need a maj at dhclient e.g user-Base
	install -Dm 0644 "$srcdir/bundle.dhclient.contents.s6" "$pkgdir/etc/s6-serv/available/rc/bundle-Dhclient/contents"
	install -Dm 0644 "$srcdir/bundle.dhclient.type.s6" "$pkgdir/etc/s6-serv/available/rc/bundle-Dhclient/type"
	
	# daemon
	install -Dm 0644 "$srcdir/dhclient.daemon.dependencies.s6" "$pkgdir/etc/s6-serv/available/rc/dhclient-daemon/dependencies"
	install -Dm 0644 "$srcdir/dhclient.daemon.pipeline-name.s6" "$pkgdir/etc/s6-serv/available/rc/dhclient-daemon/pipeline-name"
	install -Dm 0644 "$srcdir/dhclient.daemon.producer-for.s6" "$pkgdir/etc/s6-serv/available/rc/dhclient-daemon/producer-for"
	install -Dm 0644 "$srcdir/dhclient.daemon.run.s6" "$pkgdir/etc/s6-serv/available/rc/dhclient-daemon/run"
	install -Dm 0644 "$srcdir/dhclient.daemon.type.s6" "$pkgdir/etc/s6-serv/available/rc/dhclient-daemon/type"
	
	# log
	install -Dm 0644 "$srcdir/dhclient.log.consumer-for.s6" "$pkgdir/etc/s6-serv/available/rc/dhclient-log/consumer-for"
	install -Dm 0644 "$srcdir/dhclient.log.dependencies.s6" "$pkgdir/etc/s6-serv/available/rc/dhclient-log/dependencies"
	install -Dm 0644 "$srcdir/dhclient.log.run.s6" "$pkgdir/etc/s6-serv/available/rc/dhclient-log/run"
	install -Dm 0644 "$srcdir/dhclient.log.type.s6" "$pkgdir/etc/s6-serv/available/rc/dhclient-log/type"
	
	install -Dm 0644 "$srcdir/LICENSE" "$pkgdir/usr/share/licenses/dhclient-s6rcserv/LICENSE"
}
