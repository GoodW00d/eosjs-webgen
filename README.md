# EOS Wallet Key Generator

# Usage

* Download `eosjs-keygen.html` from [releases](https://github.com/jcalfee/eosjs-keygen/releases)
* Perform desired level of security
  * Verify the code and build/release hash
  * Use from cold storage

# Cold Storage

Here is one version of Cold Storage which I think is relatively simple given the tools available.

* Get a USB with a read-only switch
* Install a bootable OS like Ubuntu onto the USB
* Remove the hard-drive (any storage device) and wireless card from an old laptop or desktop
* Put the USB in read-only mode and boot
* Connect to the Internet if desired, load any software or tools needed
* Unplug the Internet (ethernet cable) and work with your software and private keys
* Use a second writable USB for a backup
* Power off

Never re-connect the Internet after working with private keys.

# Todo

Password encrypted wallet file.

# Build

I'll make a post at Steemit.com with each release hash.

Additionally you can verify that the build hash matches the human source code:

* Node
* sha256sum

```bash
git checkout tags/v1.0.0
npm install
npm run build
```

The build script runs `sha256sum eosjs-keygen.html`

You should see a sha256 hash and a eosjs-keygen.html file.  For example, v1.0.0 should hash too:

```bash
3d87f79639fa3aceaadd217b40c9e07bd0ecedc889de64cd4334eac26f66076f  eosjs-keygen.html
```

This should match the release hash at github and the hash on Steemit.
