pkgname=maven2
pkgver=2.2.1
pkgrel=3
pkgdesc="A Java project management and project comprehension tool"
arch=('any')
url="http://maven.apache.org"
license=('APACHE')
depends=('java-environment')
backup=(opt/maven/conf/settings.xml)
source=(http://archive.apache.org/dist/maven/binaries/apache-maven-$pkgver-bin.tar.bz2 \
	maven.sh)
md5sums=('c581a15cb0001d9b771ad6df7c8156f8'
         'cac30b2331aeb63e40297bbea7fffcc9')

provides=('maven')
conflicts=('maven')

package() {
    mkdir -p "$pkgdir"/opt
    mv apache-maven-$pkgver "$pkgdir"/opt/maven
    install -D -m 755 "$srcdir"/maven.sh "$pkgdir"/etc/profile.d/maven.sh
    rm "$pkgdir"/opt/maven/*.txt
}
