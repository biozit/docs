!!! failure "OSG 3.5 end-of-life"
    The OSG 3.5 end-of-life date was May 1, 2022 per our
    [release policy](https://opensciencegrid.org/technology/policy/release-series/).
    We recommend
    [updating to OSG 3.6](../updating-to-osg-36.md)
    at your earliest convenience.

OSG Data Release 3.5.8-2
========================

**Release Date:** 2020-01-28    
**Supported OS Versions:** EL7

!!!tip "Want faster access to production-ready software?"
    OSG 3.5 and 3.4 offer a rolling release repository where packages are added as soon as they pass acceptance testing.
    To install packages from this repository, enable `[osg-rolling]` in `/etc/yum.repos.d/osg-rolling.repo`:

        [osg-rolling]
        ...
        enabled=1

    Or for one-time installations, append the following to your `yum` command:

        --enablerepo=osg-rolling

Summary of Changes
------------------

This release contains:

CA Certificates based on [IGTF 1.103](http://dist.eugridpma.info/distribution/igtf/current/CHANGES)

-   Updated contact addresses for DigiCert (US)
-   Regrafted InCommon IGTF Server CA onto self-signed Comodo RSA CA (US)
-   Discontinued superfluous AddTrust External CA Root (US)
-   Discontinued AustrianGrid CA (AT)

These
[JIRA tickets](https://jira.opensciencegrid.org/issues/?jql=project%20%3D%20SOFTWARE%20AND%20fixVersion%20%3D%203.5.8-2%20ORDER%20BY%20priority%20DESC%2C%20key%20DESC)
were addressed in this release.

Containers
----------

The [Worker node containers](../../worker-node/using-wn-containers.md) have been updated to this release.

Updating to the New Release
---------------------------

To update to the OSG 3.5 series, please consult the page on
[updating between release series](../updating-to-osg-35.md).

For sites using non-RPM worker node client installations, new [tarballs](../../worker-node/install-wn-tarball.md) and
[container images](../../worker-node/using-wn-containers.md) are available:

- Tarball: <https://repo.opensciencegrid.org/tarball-install/3.5/osg-wn-client-latest.el7.x86_64.tar.gz>
- Container Images: <https://hub.docker.com/r/opensciencegrid/osg-wn/>

Need Help?
----------

Do you need help with this release? [Contact us for help](../../common/help.md).

Detailed Changes in This Release
--------------------------------

### Packages

We added or updated the following packages to the production OSG yum repository.
Note that in some cases, there are multiple RPMs for each package.
You can click on any given package to see the set of RPMs or see the complete list [below](#rpms).

-   [igtf-ca-certs-1.103-1.osg35.el7](https://koji.chtc.wisc.edu/koji/search?match=glob&type=build&terms=igtf-ca-certs-1.103-1.osg35.el7)
-   [osg-ca-certs-1.85-1.osg35.el7](https://koji.chtc.wisc.edu/koji/search?match=glob&type=build&terms=osg-ca-certs-1.85-1.osg35.el7)

### RPMs

If you wish to manually update your system, you can run yum update against the following packages:

    igtf-ca-certs osg-ca-certs

If you wish to only update the RPMs that changed, the set of RPMs is:

``` file
igtf-ca-certs-1.103-1.osg35.el7
osg-ca-certs-1.85-1.osg35.el7
```
