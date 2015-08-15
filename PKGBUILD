# Maintainer: Saurabh Kumar <saurabhgeek92+aur AT gmail DOT com>
pkgname=fotonica
pkgver=20121203
pkgrel=2
pkgdesc="A first person game about jumping, sense of speed and discovery (Game package required)"
arch=('i686' 'x86_64')
if [[ $CARCH == 'x86_64' ]]; then
  depends=('glu' 'gcc-libs' 'alsa-lib' 'libxcursor')
else 
  depends=('lib32-glu' 'gcc-libs-multilib' 'lib32-alsa-lib' 'lib32-libxcursor')
fi
url="http://www.fotonica-game.com/"
license=('custom')
source=("hib://fotonica_linux.tar.gz")
md5sums=('610278f5367301db40b8e19cf0d8c1f9')

build (){
  true
}

package() {
  mkdir -p "$pkgdir/usr/bin"
  cd $srcdir
  install -d $pkgdir/opt/Fotonica_linux_uni
  tar -xvzf fotonica_linux.tar.gz
  cp -r $srcdir/Fotonica_linux_uni/* $pkgdir/opt/Fotonica_linux_uni
  if [[ $CARCH == 'x86_64' ]]; then
    ln -s /opt/Fotonica_linux_uni/fotonica.x86_64 $pkgdir/usr/bin/fotonica
  else
    ln -s /opt/Fotonica_linux_uni/fotonica.x86 $pkgdir/usr/bin/fotonica
  fi
}

