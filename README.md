## Do you want to build on POWER?

This FAQ answers common questions for those consideting adopting POWER (ppc64le) as a supported platform. It consolidates the several resources available to ease the journey to POWER. Welcome :)

## Table of Contents<a name="top"></a>
1. [Where can I learn more about POWER?](#learn-more)
2. [Where can I get access to POWER?](#access-power)
3. [Where can I find resources for development on POWER?](#resources-power)
4. [How can I get familiar with POWER Instruction Set Architecture (ISA)?](#isa-power)
5. [How do I port amd64/x86_64 applications to POWER?](#app-power)
6. [How do I run Linux on POWER?](#linux-power)
7. [How do I build on POWER using Travis?](#travis-power)
8. [How can I check if an application or a package is available on POWER?](#pkg-power)
9. [Under Development](#dev)

## Where can I learn more about POWER?<a name="learn-more"></a>

To learn more about Power click [HERE](https://www.ibm.com/it-infrastructure/power). Do you want to become an expert on Power? [Get these BADGES](https://www.ibm.com/developerworks/community/wikis/home?lang=en#!/wiki/Business%20Partner%20Badges/page/IBM%20POWER%20System%20Badges).

[back to top](#top)

## Where can I get access to POWER?<a name="access-power"></a>

There are several public cloud offerings which provides access (some of that are FREE, yay!) to Power. Those offerings are very interesting for developers working with Open Source Communities which requires access to Power resources for testing, porting, etc.

* [Unicamp's Minicloud](http://openpower.ic.unicamp.br/minicloud/)
* [Power Development Cloud](https://www.ibm.com/partnerworld/wps/ent/pdp/web/MyProgramAccess)
* [Oregon State University](http://osuosl.org/services/powerdev/)
* [University of Texas](http://openfabric.org/)
* [Brno University of Technology](http://bit.ly/brnoPOWER8cloud)
* [SiteOX](https://www.siteox.com/cart.php?gid=22)

[Take a look at this map](http://developers.openpowerfoundation.org/explore) which depicts the location of those aforementioned clouds.

[back to top](#top)

## Where can I find resources for development on POWER?<a name="resources-power"></a>

The [Developer Portal](https://developer.ibm.com/linuxonpower/) is your one-stop-shop for developer resources on Power. A set of great tools and technologies are available, [CHECK IT OUT!](https://developer.ibm.com/linuxonpower/tools-technologies/)

[back to top](#top)

## How can I get familiar with POWER Instruction Set Architecture (ISA)?<a name="isa-power"></a>

Power [ISA Version 2.07B](https://ibm.ent.box.com/s/jd5w15gz301s5b5dt375mshpq9c3lh4u) consists of five books and a set of appendices. It is intended for use with IBM® POWER8® with NVIDIA® NVLink™ Technology, IBM® POWER8®, and prior IBM Power Architecture® processors.

* Book I, Power ISA User Instruction Set Architecture, covers the base instruction set and related facilities available to the application programmer.
* Book II, Power ISA Virtual Environment Architecture, defines the storage model and related instructions and facilities available to the application programmer.
* Book III-S, Power ISA Operating Environment Architecture - Server Environment, defines the supervisor instructions and related facilities used for general purpose implementations.
* Book III-E, Power ISA Operating Environment Architecture - Embedded Environment, defines the supervisor instructions.
* Book VLE, Power ISA Operating Environment Architecture - Variable Length Encoding (VLE) Instructions Architecture, defines alternative instruction encoding and definitions intended to increase instruction density for very low end implementations.

Power [ISA Version 3.0B](https://ibm.ent.box.com/s/1hzcwkwf8rbju5h9iyf44wm94amnlcrv) consists of three books and a set of appendices. It is intended for use with the IBM POWER9 processor.

* Book I, Power ISA User Instruction Set Architecture, covers the base instruction set and related facilities available to the application programmer.
* Book II, Power ISA Virtual Environment Architecture, defines the storage model and related instructions and facilities available to the application programmer.
* Book III, Power ISA Operating Environment Architecture, defines the supervisor instructions and related facilities.

[back to top](#top)

## How do I port amd64/x86_64 applications to POWER?<a name="app-power"></a>

The definitive how-to guide can be find [HERE](https://developer.ibm.com/linuxonpower/porting-guide/).

[back to top](#top)

## How do I run Linux on POWER?<a name="linux-power"></a>

All major Linux distributions are supported on Power:

* [Red Hat Enterprise Linux (RHEL)](https://access.redhat.com/solutions/1124983)
* [CentOS](http://isoredirect.centos.org/altarch/7/isos/ppc64le/)
* [Fedora](https://alt.fedoraproject.org/alt/)
* [Ubuntu](https://www.ubuntu.com/download/server/power)
* [Debian](https://cdimage.debian.org/debian-cd/current/ppc64el/iso-cd/)
* [SUSE Linux Enterprise Server (SLES)](https://www.suse.com/products/power/)
* [openSUSE](https://download.opensuse.org/ports/ppc/tumbleweed/iso/)

[back to top](#top)

## How do I build on POWER using Travis?<a name="travis-power"></a>

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

[back to top](#top)

## How can I check if an application or a package is available on POWER?<a name="pkg-power"></a>

There is an awesome tool called OSPAT (Open Source POWER Availability Tool) that provides you mechanisms to search for a specific package or application. [Try it NOW!](https://developer.ibm.com/linuxonpower/open-source-pkgs/)

[back to top](#top)

## Under Development<a name="dev"></a>

### How to run Docker on POWER?

### How to build on POWER using GitLab?

### How to add POWER node in your Jenkins setup?

### How to create multi-arch Docker images?

The step-by-step [can be found here](https://rpsene.wordpress.com/2019/03/19/docker-creating-multi-arch-images/). Ensure you have a DockerHub account when trying it :)

[back to top](#top)

## Support or Contact

Questions or concerns: rpsene@br.ibm.com.

[back to top](#top)
