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
    # 1. Entramos a la carpeta que clonó Git
    cd "${srcdir}/${pkgname}"

    # 2. Según tu tree, los archivos están en la subcarpeta 'src' del repo
    # Estructura: core-gnome-backgrounds/src/core/
    local _repo_src="src"

    # 3. Instalar los Fondos
    install -d "${pkgdir}/usr/share/backgrounds/core"
    # Copiamos el contenido de la carpeta 'core' que está dentro de 'src'
    cp -r "${_repo_src}/core/"* "${pkgdir}/usr/share/backgrounds/core/"

    # 4. Instalar las Propiedades XML
    install -d "${pkgdir}/usr/share/gnome-background-properties"
    # Copiamos el contenido de gnome-background-properties que está dentro de 'src'
    cp -r "${_repo_src}/gnome-background-properties/"* "${pkgdir}/usr/share/gnome-background-properties/"
}
