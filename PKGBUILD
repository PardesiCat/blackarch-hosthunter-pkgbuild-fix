# This file is part of BlackArch Linux ( https://www.blackarch.org/ ).
# See COPYING for license details.

pkgname=hosthunter
pkgver=158.553f1c7
pkgrel=1
pkgdesc='A recon tool for discovering hostnames using OSINT techniques.'
groups=('blackarch' 'blackarch-recon')
arch=('any')
url='https://github.com/SpiderLabs/HostHunter'
license=('custom:unknown')
depends=('python' 'python-requests' 'python-selenium' 'python-urllib3'
         'python-pyopenssl' 'python-fake-useragent' 'python-validator-collection')
makedepends=('git')
source=("$pkgname::git+https://github.com/SpiderLabs/HostHunter.git")
sha512sums=('SKIP')

pkgver() {
  cd $pkgname

  echo $(git rev-list --count HEAD).$(git rev-parse --short HEAD)
}

package() {
  cd $pkgname

  install -Dm 755 "$pkgname.py" "$pkgdir/usr/bin/$pkgname"
  install -Dm 644 -t "$pkgdir/usr/share/doc/$pkgname/" README.md
}

