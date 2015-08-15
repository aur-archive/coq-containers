# Contributor: Paolo Herms

pkgname=coq-containers
pkgver=8.4
pkgrel=7
pkgdesc="A Coq library for containers"
arch=(i686 x86_64)
url="http://www.lix.polytechnique.fr/coq/pylons/coq/pylons/contribs/view/Containers/v8.4"
license=('LGPL')
depends=('coq')
makedepends=('ocaml' 'camlp5-transitional')
source=("http://www.lix.polytechnique.fr/coq/pylons/contribs/files/Containers/v8.4/Containers.tar.gz")

build() {
  cd "$srcdir"/Containers
  make -j
}

package() {
  cd "$srcdir"/Containers
  make COQLIB="$pkgdir/`coqtop -where`/"  install
}

md5sums=('ef92cdff1758f3c7b5b0028cdfd1a30e')
