# packetdrill
This is the official Google release of packetdrill.

The packetdrill scripting tool enables quick, precise tests for entire TCP/UDP/IPv4/IPv6 network stacks, from the system call layer down to the NIC hardware. packetdrill currently works on Linux, FreeBSD, OpenBSD, and NetBSD. It can test network stack behavior over physical NICs on a LAN, or on a single machine using a tun virtual network device.

The code is GPLv2. Currently the source for the testing tool and a number of test scripts is in the git repository. We will continue to post more tests from our team's Linux TCP test suite (described in our USENIX paper), as time permits.

Links:
* [the Google packetdrill git repository is now on github.com](https://github.com/google/packetdrill)
* [packetdrill USENIX ATC paper from June 2013](http://research.google.com/pubs/pub41316.html) describing the tool and our team's experiences
* [packetdrill USENIX ;login: article](http://research.google.com/pubs/pub41848.html) from October 2013
* [packetdrill mailing list](https://groups.google.com/forum/#!forum/packetdrill) for questions, discussions and patches
* [submitting patches for packetdrill](https://code.google.com/archive/p/packetdrill/wikis/SubmittingPatches.wiki)
* [packetdrill language syntax reference](https://code.google.com/archive/p/packetdrill/wikis/Syntax.wiki)

The USENIX 2013 paper describing the tool and our team's experiences using it may be found here:

    http://research.google.com/pubs/pub41316.html

building

To build packetdrill, first install flex and bison.

Then set up the Makefile for your platform:

```
./configure
```

Then build the tool:

```
make
```

running

Here's a quick example.

On FreeBSD, OpenBSD, and NetBSD, try:

```
./packetdrill tests/bsd/fast_retransmit/fr-4pkt-sack-bsd.pkt

```

On Linux try:

```
./packetdrill tests/linux/fast_retransmit/fr-4pkt-sack-linux.pkt

```

To run all the Linux tests: 

```
cd tests/linux/
./run_tests.sh
```

license

The packetdrill tool is released under version 2 of the GPL. See the COPYING file for full details.
discussion and contributions

If you have any questions, or code or patches to offer, please join the packetdrill e-mail list at:

    http://groups.google.com/group/packetdrill

Contributions of code or tests are both welcomed!

Enjoy!
