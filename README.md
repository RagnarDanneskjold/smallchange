Koindashian integration/staging tree
================================

http://www.koindashian.com

Copyright (c) 2009-2013 Bitcoin Developers
Copyright (c) 2013-2275 Koindashian Developers

###
Koindashian [KOIN, ¤]
http://koindashian.com/

What is Koindashian?
Koindashian is like Bitcoin, but based on Litecoin, and much prettier. 

License - pretty license
Koindashian is released under the terms of the MIT license. See COPYING for more information or see http://opensource.org/licenses/MIT.

Development and contributions -
Developers work in their own trees, then submit pull requests when they think their feature or bug fix is ready.

Frequently Asked Questions:

How much Koindashian can exist?
333,333,333,333 koins

Block Target Every 0.333… Minutes

3.3333.. Hour Difficulty Readjustments

Initial block reward: 333,333

Block reward adjustment rate[-1/3 or *.666..]: 333,333

How to get Koindashian?

Scrypt Proof of Work

make koindashiand

sudo apt-get install build-essential \
                     libssl-dev \
                     libdb5.1++-dev \
                     libboost-all-dev \
                     libqrencode-dev \
                     libminiupnpc-dev

cd src/
make -f makefile.unix...
###
########
########

License
-------

Koindashian is released under the terms of the MIT license. See `COPYING` for more
information or see http://opensource.org/licenses/MIT.

Development process
-------------------

Developers work in their own trees, then submit pull requests when they think
their feature or bug fix is ready.

If it is a simple/trivial/non-controversial change, then one of the Koindashian
development team members simply pulls it.

If it is a *more complicated or potentially controversial* change, then the patch
submitter will be asked to start a discussion (if they haven't already) on the
[mailing list](http://sourceforge.net/mailarchive/forum.php?forum_name=bitcoin-development).

The patch will be accepted if there is broad consensus that it is a good thing.
Developers should expect to rework and resubmit patches if the code doesn't
match the project's coding conventions (see `doc/coding.txt`) or are
controversial.

The `master` branch is regularly built and tested, but is not guaranteed to be
completely stable. [Tags](https://github.com/bitcoin/bitcoin/tags) are created
regularly to indicate new official, stable release versions of Koindashian.

Testing
-------

Testing and code review is the bottleneck for development; we get more pull
requests than we can review and test. Please be patient and help out, and
remember this is a security-critical project where any mistake might cost people
lots of money.

### Automated Testing

Developers are strongly encouraged to write unit tests for new code, and to
submit new unit tests for old code.

Unit tests for the core code are in `src/test/`. To compile and run them:

    cd src; make -f makefile.unix test

Unit tests for the GUI code are in `src/qt/test/`. To compile and run them:

    qmake koindashian-qt_test=1 -o Makefile.test koindashian-qt.pro
    make -f Makefile.test
    ./koindashian-qt_test

