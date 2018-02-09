# OpenPGP-Secure

For now, we are not able to appreciate PGP at its full potential.

Need OPENPGPKEY RR support ([see related RFC](https://tools.ietf.org/html/rfc7929) and [the Bortzmeyer analysis](http://www.bortzmeyer.org/7929.html)):
 - The `systemd` package supports [resolving of OPENPGPKEY RR since `systemd` 230 released on 2016-05-22](https://github.com/systemd/systemd/pull/2589)  
   **Verify your OPENPGPKEY RR:** `systemd-resolve --openpgp email@example.com`

 - The `python2-gnupg` dependency of `hash-slinger` [has been fixed on 2016-06-06 master branch](https://bitbucket.org/vinay.sajip/python-gnupg/issues/32/add-gpg-21-compability) and the 0.3.9 version with the patch has been released on 2016-09-10.  
   **Generate your OPENPGPKEY RR:** `openpgpkey --output rfc email@example.com`  

 - The `python2-unbound` dependency of `hash-slinger` is really heavy because it depends also of the [`unbound`](https://www.archlinux.org/packages/community/x86_64/unbound/) recursive DNS server package which, on `Arch Linux`, contains also the `libunbound2`/`unbound-libs` library. On the contrary, on `Ubuntu` or on `Fedora`, the main `unbound` package and `libunbound2`/`unbound-libs` library are splitted. An `unbound-libs` AUR package should be created to remplace the `unbound` dependency of `python2-unbound`. Nevertheless, it is not the [`Arch Linux` philosophy](https://wiki.archlinux.org/index.php/Arch_Linux#Simplicity) :
 > Packages are only split when **compelling** advantages exist.
 
 - **For now, it's better [to generate your OPENPGPKEY RR with `gpg`](https://tools.ietf.org/html/rfc7929#appendix-A)**.

Need ECC support: 
 - https://github.com/mailvelope/mailvelope/issues/547 MAIN ISSUE
 - ~https://github.com/google/end-to-end/issues/319~ STALLED
 - ~~https://github.com/RainLoop/rainloop-webmail/issues/1023~~ CLOSED
 - ~https://github.com/RainLoop/rainloop-webmail/issues/1618~ STALLED
  - ~~https://github.com/openpgpjs/openpgpjs/issues/427~~ DONE
 - ~~https://github.com/openpgpjs/openpgpjs/issues/428~~ DONE
 - ~~https://www.huque.com/bin/openpgpkey~~ DONE
 - ~~https://github.com/open-keychain/open-keychain/issues/1533~~ CLOSED
 - ~~https://github.com/open-keychain/open-keychain/issues/1627~~ CLOSED
 - ~https://github.com/open-keychain/open-keychain/issues/2178~ STALLED
 - Keybase [1](https://github.com/keybase/keybase-issues/issues/1738) & [2](https://github.com/keybase/keybase-issues/issues/2213) are being solved by the [`kbpgp` fork](https://github.com/zapu/kbpgp/tree/curve25519)
