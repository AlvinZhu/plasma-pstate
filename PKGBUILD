 
# Maintainer: Alvin Zhu <alvin.zhuge@gmail.com>
pkgname=plasma5-applets-plasma-pstate
pkgver=1.0.7
pkgrel=1
pkgdesc="Intel P-state and CPUFreq Manager Widget"
arch=('any')
url="https://github.com/AlvinZhu/plasma-pstate"
license=('GPL2')
groups=('aur-alvin')
depends=('plasma-workspace' 'polkit')
optdepends=("libsmbios: Dell's Thermal Management Feature"
            "x86_energy_perf_policy: If your processor doesn't support EPP i.e. older generations without HWP")

package() {
  mkdir -p "$pkgdir/usr/share/polkit-1/actions"
  cp ../org.pkexec.set_prefs.policy "$pkgdir/usr/share/polkit-1/actions/"
  mkdir -p "$pkgdir/usr/lib/systemd/system"
  cp ../set_perfsd.service "$pkgdir/usr/lib/systemd/system"
  mkdir -p "$pkgdir/usr/share/plasma/plasmoids"
  cp -r ../gr.ictpro.jsalatas.plasma.pstate "$pkgdir/usr/share/plasma/plasmoids"
  chmod 755 "$pkgdir/usr/share/plasma/plasmoids/gr.ictpro.jsalatas.plasma.pstate/contents/code/set_prefs.sh"
}