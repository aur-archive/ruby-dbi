# Generated by gem2arch (https://github.com/anatol/gem2arch)
# Maintainer: Rhys Davies <rhys@johnguant.com>

_gemname=dbi
pkgname=ruby-$_gemname
pkgver=0.4.5
pkgrel=1
pkgdesc='A vendor independent interface for accessing databases, similar to Perl'\''s DBI'
arch=(any)
url='http://www.rubyforge.org/projects/ruby-dbi'
license=()
depends=(ruby ruby-deprecated-2)
options=(!emptydirs)
source=(https://rubygems.org/downloads/$_gemname-$pkgver.gem)
noextract=($_gemname-$pkgver.gem)
sha1sums=('4b56d97772c8e9cbcd0a10414a681c255089a5bc')

package() {
  local _gemdir="$(ruby -e'puts Gem.default_dir')"
  gem install --ignore-dependencies --no-user-install -i "$pkgdir/$_gemdir" -n "$pkgdir/usr/bin" $_gemname-$pkgver.gem
  rm "$pkgdir/$_gemdir/cache/$_gemname-$pkgver.gem"
  install -D -m644 "$pkgdir/$_gemdir/gems/$_gemname-$pkgver/LICENSE" "$pkgdir/usr/share/licenses/$pkgname/LICENSE"
}
