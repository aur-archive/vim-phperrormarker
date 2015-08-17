# Maintainer : Jacek Roszkowski <j.roszk@gmail.com>
# Maintainer : Hexcles Ma <bob1211 (at) gmail (dot) com>

pkgname=vim-phperrormarker
pkgver=0.0.6
_scriptid=19225
pkgrel=2
pkgdesc="Mark syntax errors in php file"
arch=(any)
url="http://www.vim.org/scripts/script.php?script_id=2794"
license=('GPL')
depends=(vim)
groups=('vim-plugins')
install=vimdoc.install
source=(phpErrorMarker.vmb::http://www.vim.org/scripts/download_script.php?src_id=${_scriptid})
md5sums=('2f1c8a6b3eb632992e17f8e65e1f9502')

build() {
  cd $srcdir
  installdir=${srcdir}/vim-phperrormarker
  vim -c "UseVimball ${installdir}" -c "q" phpErrorMarker.vmb

  cd ${installdir}
  install -D -m644 autoload/phpErrorMarker.vim ${pkgdir}/usr/share/vim/vimfiles/autoload/phpErrorMarker.vim
  install -D -m644 ftplugin/php/phpErrorMarker.vim ${pkgdir}/usr/share/vim/vimfiles/ftplugin/php/phpErrorMarker.vim
}
