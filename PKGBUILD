

pkgname=crypt-post
pkgver=1.0
pkgrel=1
pkgdesc='Simple initcpio hook, prints /etc/crypt-post-issue after prompting for password.'
arch=('any')
license=('MIT')
depends=('mkinitcpio')
source=(
        'crypt-post.install'
        'crypt-post.hook'
        'crypt-post.txt'
        'README.md'
        'LICENSE'
        )
md5sums=(
        'SKIP'
        'SKIP'
        'SKIP'
        'SKIP'
        'SKIP'
        )

pkgver(){
  printf "%s.%s" "$(git rev-list --count HEAD)" "$(git rev-parse --short HEAD)"
}

package(){
  install -Dm644 "${srcdir}/crypt-post.install" \
      "${pkgdir}/usr/lib/initcpio/install/crypt-post"
  install -Dm644 "${srcdir}/crypt-post.hook" \
      "${pkgdir}/usr/lib/initcpio/hook/crypt-post"
  install -Dm644 "${srcdir}/crypt-post.txt" \
      "${pkgdir}/etc/crypt-post-issue"
  install -Dm644 "${srcdir}/README.md" \
      "${pkgdir}/usr/share/crypt-issue/README.md"
  install -Dm644 "${srcdir}/LICENSE" \
      "${pkgdir}/usr/share/crypt-issue/LICENSE"
}

