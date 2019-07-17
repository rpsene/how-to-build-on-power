## Do you want to build on POWER?

This FAQ answers common questions for those consideting adopting POWER (ppc64le) as a supported platform. It consolidates the several resources available to ease the journey to POWER. Welcome :)

## Where can I learn more about POWER?

To learn more about Power click [HERE](https://www.ibm.com/it-infrastructure/power). Do you want to become an expert on Power? [Get these BADGES](https://www.ibm.com/developerworks/community/wikis/home?lang=en#!/wiki/Business%20Partner%20Badges/page/IBM%20POWER%20System%20Badges).

## Where can I get access to POWER?

There are several public cloud offerings which provides access (some of that are FREE, yay!) to Power. Those offerings are very interesting for developers working with Open Source Communities which requires access to Power resources for testing, porting, etc.

* [Unicamp's Minicloud](http://openpower.ic.unicamp.br/minicloud/)
* [Power Development Cloud](https://www.ibm.com/partnerworld/wps/ent/pdp/web/MyProgramAccess)
* [Oregon State University](http://osuosl.org/services/powerdev/)
* [University of Texas](http://openfabric.org/)
* [Brno University of Technology](http://bit.ly/brnoPOWER8cloud)
* [SiteOX](https://www.siteox.com/cart.php?gid=22)

[Take a look at this map](http://developers.openpowerfoundation.org/explore) which depicts the location of those aforementioned clouds.

## Where can I find resources for development on POWER?

The [Developer Portal](https://developer.ibm.com/linuxonpower/) is your one-stop-shop for developer resources on Power. A set of great tools and technologies are available, [CHECK IT OUT!](https://developer.ibm.com/linuxonpower/tools-technologies/)

## How do I port amd64/x86_64 applications to POWER?

The definitive how-to guide can be find [HERE](https://developer.ibm.com/linuxonpower/porting-guide/).

## How do I run Linux on POWER?

All major Linux distributions are supported on Power:

* [Red Hat Enterprise Linux (RHEL)](https://access.redhat.com/solutions/1124983)
* [CentOS](http://isoredirect.centos.org/altarch/7/isos/ppc64le/)
* [Fedora](https://alt.fedoraproject.org/alt/)
* [Ubuntu](https://www.ubuntu.com/download/server/power)
* [Debian](https://cdimage.debian.org/debian-cd/current/ppc64el/iso-cd/)
* [SUSE Linux Enterprise Server (SLES)](https://www.suse.com/products/power/)
* [openSUSE](https://download.opensuse.org/ports/ppc/tumbleweed/iso/)

## How do I build on POWER using Travis?

[Travis CI](https://travis.ibm.com/auth) is a continuous integration service used to build and test software projects hosted on [GitHub](https://github.ibm.com/). To build on Power, just add **os: linux-ppc64le** as part of your **.travis.yaml** file.

This configuration builds on POWER and on x86_64:

```bash

language: bash

matrix: 
    include: 
        - os: linux-ppc64le
        - os: linux

script: 
    - uname -a

```

This configuration builds only on POWER:

```bash

language: bash

matrix: 
    include: 
        - os: linux-ppc64le

script: 
    - uname -a

```

**NOTE:** You can organize your builds by using build stages. Take a look at https://docs.travis-ci.com/user/build-stages/ and learn how to use this Travis feature.

## How can I check if an application or a package is available on POWER? 

There is an awesome tool called OSPAT (Open Source POWER Availability Tool) that provides you mechanisms to search for a specific package or application. [Try it NOW!](https://developer.ibm.com/linuxonpower/open-source-pkgs/)

## Under Development

### How to run Docker on POWER?

### How to build on POWER using GitLab?

### How to add POWER node in your Jenkins setup?

### How to create multi-arch Docker images?

## Support or Contact

Questions or concerns: rpsene@br.ibm.com.
