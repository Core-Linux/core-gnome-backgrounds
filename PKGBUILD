# Maintainer: m4teo.dev <Core Linux>

pkgname=core-gnome-backgrounds
pkgver=2.2
pkgrel=3
pkgdesc="Official GNOME wallpapers for Core Linux"
arch=('any')
url="https://github.com/Core-Linux/core-gnome-backgrounds"
license=('CC0')
makedepends=('git')
depends=()

source=("git+${url}.git")
sha256sums=('SKIP')

package() {
  cd "${srcdir}/${pkgname}"

  # Instalar fondos
  install -dm755 "${pkgdir}/usr/share/backgrounds/core"
  cp -rv backgrounds/* "${pkgdir}/usr/share/backgrounds/core/"

  # Instalar propiedades XML
  install -dm755 "${pkgdir}/usr/share/gnome-background-properties"
  cp -rv gnome-background-properties/* "${pkgdir}/usr/share/gnome-background-properties/"
}
