#Maintainer: max-k <max-k AT post DOT com>

pkgname=pear-mail-mimedecode
_pkgname=Mail_mimeDecode
pkgver=1.5.5
pkgrel=3
pkgdesc='Provides a class to decode mime messages.'
arch=('any')
url="http://pear.php.net/package/${_pkgname}"
license=('BSD')
depends=('pear-mail-mime>=1.4.0')
makedepends=('php-pear>=1.6.0')
options=('!strip')
noextract=(${_pkgname}-${pkgver}.tgz)
source=(http://download.pear.php.net/package/${_pkgname}-${pkgver}.tgz)
md5sums=('915bf1c68a5518afc14700d5b1132200')

package() {
  cd ${srcdir}
  local _PEARDIR="${pkgdir}/usr/share/pear"
  local _PEAROPTS="-D php_dir=${_PEARDIR} -D doc_dir=${_PEARDIR}/doc"
  local _PEAROPTS="${_PEAROPTS} -D test_dir=${_PEARDIR}/test"
  local _PEAROPTS="${_PEAROPTS} -D data_dir=${_PEARDIR}/data"
  pear ${_PEAROPTS} install -O -n ${_pkgname}-${pkgver}.tgz
  rm -r ${_PEARDIR}/{.channels,.depdb*,.filemap,.lock,.registry/.chan*}
}

