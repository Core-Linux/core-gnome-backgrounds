# Maintainer: m4teo.dev <Core Linux>

pkgname=core-gnome-backgrounds
pkgver=2.2
pkgrel=3
pkgdesc="Official Gnome backgrounds for Core Linux"
arch=('any')
url="https://github.com/Core-Linux/core-gnome-backgrounds"

makedepends=('git')
depends=('gtk-update-icon-cache')

source=("git+${url}.git")
sha256sums=('SKIP')

package() {
  # 1. Entramos a la carpeta que makepkg creó para el clon de git
  # $srcdir es donde makepkg descomprime todo.
  # ${pkgname} es 'core-gnome-backgrounds'.
  cd "${srcdir}/${pkgname}"

  # 2. Instalamos los fondos
  # Usamos -d para crear toda la ruta de una vez
  install -d "${pkgdir}/usr/share/backgrounds/core"

  # Copiamos el contenido de la carpeta src/core que está DENTRO del repo
  # Usamos ./src/core/ para asegurarnos de que sea relativo a la carpeta del repo
  cp -r ./src/core/* "${pkgdir}/usr/share/backgrounds/core/"

  # 3. Instalamos las propiedades XML
  install -d "${pkgdir}/usr/share/gnome-background-properties"
  cp -r ./src/gnome-background-properties/* "${pkgdir}/usr/share/gnome-background-properties/"
}
