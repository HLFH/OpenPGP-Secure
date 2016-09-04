# OpenPGP-Secure

For now, we are not able to appreciate PGP at its full potential.

Need OPENPGPKEY RR support ([see last related Internet-Draft](https://tools.ietf.org/html/draft-ietf-dane-openpgpkey-12)):
 - https://github.com/systemd/systemd/pull/2589 (now released in systemd 230 on 2016-05-21) 
 
   Verify your OPENPGPKEY RR: `systemd-resolve --openpgp email@example.com`
 - https://bitbucket.org/vinay.sajip/python-gnupg/issues/32/add-gpg-21-compability (fixed on 2016-06-06 master branch, will be released in python2-gnupg 0.3.9) 
 
   Generate your OPENPGPKEY RR: `openpgpkey --output rfc email@example.com`

Need ECC support: 
 - https://github.com/google/end-to-end/issues/319
 - https://github.com/RainLoop/rainloop-webmail/issues/1023
 - https://github.com/openpgpjs/openpgpjs/issues/428
 - https://github.com/openpgpjs/openpgpjs/issues/427
 - https://www.huque.com/bin/openpgpkey
 - https://github.com/open-keychain/open-keychain/issues/1533
 - https://github.com/open-keychain/open-keychain/issues/1627
 - https://github.com/keybase/keybase-issues/issues/2213
