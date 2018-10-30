# wazo-python-pyfcm-packaging

Debian packaging for [pyfcm](https://github.com/olucurious/PyFCM) used in Wazo.

## Upgrading

To upgrade pyfcm:

* Update the version number in the `VERSION` file
* Update the changelog using `dch -i` to the matching version
* Refresh patches
* Push the changes

## Building Locally

To build on a test environment before submitting a change to production the following procedure can be used.

```sh
make -f debian/rules get-orig-source
tar -xvf ../wazo-python-pyfcm-packaging_*.orig.tar.gz  --strip 1
dpkg-buildpackage -us -uc
```
The `.deb` will be located in the parent directory.
