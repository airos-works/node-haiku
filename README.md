# Node.js for Haiku (air/OS)

Haiku x86_64 builds of Node.js, one GitHub release per version, in the
nodejs.org download layout: each release (tagged like `v26.13.0`) holds
`node-vX.Y.Z-haiku-x64.tar.xz`, `.tar.gz` and `SHASUMS256.txt`, and the
release tagged `index` holds `index.tab` and `index.json`.

This is the default Haiku mirror of air/OS's nvm: on air/OS,

    nvm ls-remote
    nvm install 24

There is a build of the newest release of every major version from 10 to 26.

Each build is made from the unmodified nodejs.org source tarball with the
Haiku port in [airos-works/haiku](https://github.com/airos-works/haiku)
(`data/nvm/haiku/port`, applied by `port-haiku.py`) and
`tools/nodejs-haiku/build-node.sh`. OpenSSL, ICU, libuv, c-ares and the other
dependencies are bundled, so a build needs only Haiku's own libraries
(libroot, libbsd, libnetwork, gcc_syslibs).

To use another mirror in the same layout, set `NVM_HAIKU_MIRROR`
(`https://...` or `file:///path`).

Node.js is licensed under the MIT license; each archive carries its `LICENSE`.
Node.js is a trademark of the OpenJS Foundation; these builds are not
official Node.js releases.
