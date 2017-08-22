# Maintainer: Eric Vidal <eric@obarun.org>

pkgname=dhclient-s6rcserv
pkgver=0.1
pkgrel=3
pkgdesc="dhclient service for"
arch=(x86_64)
license=('beerware')
depends=('dhclient' 's6' 's6-rc' 's6-boot')
conflicts=()
source=('dhclient.longrun.dependencies'
		'dhclient.longrun.pipeline-name'
		'dhclient.longrun.producer-for'
		'dhclient.longrun.run'	
		'dhclient.longrun.type'
		
		'dhclient.log.consumer-for'
		'dhclient.log.dependencies'
		'dhclient.log.run'
		'dhclient.log.type'
		
		'bundle.dhclient.contents'
		'bundle.dhclient.type'
		'dhclient.logd'
		'LICENSE')
md5sums=('68b329da9893e34099c7d8ad5cb9c940'
         '04b57a0142c627e01df0cf9544e3ac40'
         '8176ff14bed4334863f4b413f8e34be3'
         'ba5c196bef0a79776a164cbe5829d1f0'
         '42c13bdd7f61c06ac59c1aaca9c0f07a'
         'f796b6866fdc854a94965030bcc61494'
         '68b329da9893e34099c7d8ad5cb9c940'
         'a155da4aa5e4668924e44ce568e79c68'
         '42c13bdd7f61c06ac59c1aaca9c0f07a'
         '07392328e714e1e339ff1a1506088036'
         '71abe97e2554d37f1d12c5bf4945297f'
         '5dc14a1ac09bf5e7f02156fb63d6d4ea'
         '191a37ae657aa17e37e75d0242865dba')

package() {
	
	# bundle , trouble here user-dhclient need a maj at dhclient e.g user-Base
	install -Dm 0644 "$srcdir/bundle.dhclient.contents" "$pkgdir/etc/s6-serv/available/rc/bundle-Dhclient/contents"
	install -Dm 0644 "$srcdir/bundle.dhclient.type" "$pkgdir/etc/s6-serv/available/rc/bundle-Dhclient/type"
	
	# longrun
	install -Dm 0644 "$srcdir/dhclient.longrun.dependencies" "$pkgdir/etc/s6-serv/available/rc/dhclient-longrun/dependencies"
	install -Dm 0644 "$srcdir/dhclient.longrun.pipeline-name" "$pkgdir/etc/s6-serv/available/rc/dhclient-longrun/pipeline-name"
	install -Dm 0644 "$srcdir/dhclient.longrun.producer-for" "$pkgdir/etc/s6-serv/available/rc/dhclient-longrun/producer-for"
	install -Dm 0644 "$srcdir/dhclient.longrun.run" "$pkgdir/etc/s6-serv/available/rc/dhclient-longrun/run"
	install -Dm 0644 "$srcdir/dhclient.longrun.type" "$pkgdir/etc/s6-serv/available/rc/dhclient-longrun/type"
	
	# log
	install -Dm 0644 "$srcdir/dhclient.log.consumer-for" "$pkgdir/etc/s6-serv/available/rc/dhclient-log/consumer-for"
	install -Dm 0644 "$srcdir/dhclient.log.dependencies" "$pkgdir/etc/s6-serv/available/rc/dhclient-log/dependencies"
	install -Dm 0644 "$srcdir/dhclient.log.run" "$pkgdir/etc/s6-serv/available/rc/dhclient-log/run"
	install -Dm 0644 "$srcdir/dhclient.log.type" "$pkgdir/etc/s6-serv/available/rc/dhclient-log/type"
	
	# hook
	install -Dm 0644 "$srcdir/dhclient.logd" "$pkgdir/etc/s6-serv/log.d/dhclient-rc"
	
	install -Dm 0644 "$srcdir/LICENSE" "$pkgdir/usr/share/licenses/dhclient-s6rcserv/LICENSE"
}
