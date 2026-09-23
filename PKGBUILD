# Maintainer: KFERMercer <https://github.com/KFERMercer>

# shellcheck disable=2034,2148,2154

pkgname=comfykick
pkgver=1.9
pkgrel=1
pkgdesc="The Official ComfyUI Launch Process SUCKs🤮, this is better."
arch=(any)
url="https://github.com/KFERMercer/ComfyKick"
license=(GPL-3.0-only)
install=${pkgname}.install

depends=(python
         python-yaml
         uv)

optdepends=('cuda: CUDA support'
            'rocm-hip-sdk: ROCm support'
            'intel-compute-runtime: Intel XPU support')

source=(LICENSE
        comfykick.py
        comfykick.service
        comfykick.toml
        override.conf)

sha256sums=('3972dc9744f6499f0f9b2dbf76696f2ae7ad8af9b23dde66d6af86c9dfb36986'
            '59d6b15b130aff7023a5a69ca2e04ce9a5c6733f08dd3ba0df6c4f90f0440c88'
            '9456aac22fe356c8518c0787315fc0a4a18ca76f5202a6d6120321d60c609893'
            '775e4f5601d4af7c07a233ef4b0155ecb2fb3f56d1dbc5c81f3e96f817a2cff4'
            '4c993df4c0fa00334a9817adedcf2f2bcf8e60e071b378895b520cf0322782b2')

package() {
    install -Dm644 comfykick.py "${pkgdir}/usr/share/${pkgname}/comfykick.py"
    install -Dm644 comfykick.toml "${pkgdir}/usr/share/doc/${pkgname}/comfykick.toml"
    install -Dm644 comfykick.service "${pkgdir}/usr/lib/systemd/user/comfykick.service"
    install -Dm644 override.conf "${pkgdir}/usr/share/${pkgname}/override.conf"
    install -Dm644 LICENSE "${pkgdir}/usr/share/licenses/${pkgname}/LICENSE"
}
