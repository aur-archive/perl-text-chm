# Maintainer: trizen .= x@gmail.com

pkgname=perl-text-chm
pkgver=0.01
pkgrel=1
pkgdesc="Text::CHM - Perl extension for handling MS Compiled HtmlHelp Files"
arch=('any')
url="https://metacpan.org/module/Text::CHM"
license=('GPL' 'PerlArtistic')
depends=('perl' 'chmlib')
options=('!emptydirs')
source=("http://cpan.metacpan.org/authors/id/D/DD/DDS/Text-CHM-${pkgver}.tar.gz")
md5sums=('33dd0a2d9a22025bf39727e7c589faaa')

build() {
  cd ${srcdir}/Text-CHM-${pkgver}
  PERL_MM_USE_DEFAULT=1 perl Makefile.PL INSTALLDIRS=vendor
  make
}

package() {
  cd ${srcdir}/Text-CHM-${pkgver}
  make install DESTDIR=${pkgdir}
  find ${pkgdir} -name '.packlist' -delete
  find ${pkgdir} -name '*.pod' -delete
}
