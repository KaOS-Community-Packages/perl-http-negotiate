pkgname=perl-http-negotiate
pkgver=6.01
pkgrel=1
pkgdesc="Choose a variant to serve"
arch=('x86_64')
url="http://search.cpan.org/dist/HTTP-Negotiate"
license=('PerlArtistic' 'GPL')
depends=('perl' 'perl-http-message')
options=('!emptydirs')
source=(http://search.cpan.org/CPAN/authors/id/G/GA/GAAS/HTTP-Negotiate-$pkgver.tar.gz)
sha1sums=('4a4974639d9b64f7132cb075f551f7293f788c62')

build() {
  cd HTTP-Negotiate-$pkgver
  perl Makefile.PL INSTALLDIRS=vendor
  make
}

check() {
  cd HTTP-Negotiate-$pkgver
  make test
}

package() {
  cd HTTP-Negotiate-$pkgver
  make DESTDIR="$pkgdir" install
}
