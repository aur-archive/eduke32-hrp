
pkgname=eduke32-hrp
pkgver=5.3.565
pkgrel=2
pkgdesc="High-resolution textures and 3D models for EDuke32"
arch=('any')
url="http://hrp.duke4.net/"
license=('HRP Art' 'CGTextures')
depends=('eduke32>=20081121')
conflicts=('eduke32-polymer-hrp')
source=("http://www.duke4.org/files/nightfright/hrp/duke3d_hrp.zip" \
	"CGTextures.license" )


md5sums=('e99c3607486adce92e08b30acac70ab7'
         '82167693ec2467aa5fa5c418a4a5f207')
         

package()
{
  mkdir -p "${pkgdir}"/usr/share/eduke32
  cp -rf *.def *.mhk highres/ highpal/ "${pkgdir}"/usr/share/eduke32/

  find "${pkgdir}" -type f -exec chmod 644 {} \;

  install -Dm644 hrp_art_license.txt "${pkgdir}"/usr/share/licenses/${pkgname}/hrp_art_license.txt
  install -m644 CGTextures.license "${pkgdir}"/usr/share/licenses/${pkgname}/


}


