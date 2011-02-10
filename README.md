Autoloader
=============

**Autoloader** is a component that provides a generic, PHP include_path aware autoloader for use in community-compliant PHP projects.

Installation
------------

You can install Autoloader in two ways:

Via pear:

    stuart@ubuntu:~$ sudo pear channel-discover pear.gradwell.com 
    Adding Channel "pear.gradwell.com" succeeded
    Discovery of channel "pear.gradwell.com" succeeded

    stuart@ubuntu:~$ sudo pear install Gradwell/Autoloader
    downloading Autoloader-0.0.3.tgz ...
    Starting to download Autoloader-0.0.3.tgz (1,973 bytes)
    ....done: 1,973 bytes
    install ok: channel://pear.gradwell.com/Autoloader-0.0.3

From source:

    git clone git@github.com:Gradwell/Autoloader.git
    cd Autoloader
    phing install-system

Both of these approaches will install the Autoloader code into your system's standard location (usually /usr/share/php).

Usage
-----

Simply include the autoloader, and it will automatically register itself with spl_autoload():

    <?php

    require_once 'gw.autoloader.php';

    ?>

After that, any classes that need autoloading, Autoloader will look for them along your PHP include_path.

Development
-----------

You will need the following dependencies installed first.

* phix
* phing
* PHPUnit
* xdebug
* pdepend
* phpDocumentor
* phpmd
* phpcpd
* phpcs
* phpcb

This component includes a build.xml file containing several options to make life a little easier.

    stuart@ubuntu:~/Devel/Gradwell/Autoloader$ phing
    Buildfile: /home/stuart/Devel/Gradwell/Autoloader/build.xml

    [property] Loading /home/stuarth/Dropbox/Devel/GWC/Autoloader/build.properties

     > help:

         [echo] Autoloader 1.0.0: build.xml targets:
         [echo] 
         [echo] lint
         [echo]   Check the PHP files for syntax errors
         [echo] test
         [echo]   Run the component's PHPUnit tests
         [echo] code-review
         [echo]   Run code quality tests (pdepend, phpmd, phpcpd, phpcs)
         [echo] build-vendor
         [echo]   Populate vendor/ with this package's dependencies
         [echo]   (used for running unit tests)
         [echo] pear-package
         [echo]   Create a PEAR-compatible package
         [echo] install.local
         [echo]   Install this component from source
         [echo]   You must be root to run this target!!
         [echo] publish
         [echo]   Publish the pear package onto the channel server
         [echo] hg-push
         [echo]   Push the changes back to the Mercurial master repo
         [echo] clean
         [echo]   Remove all temporary folders created by this build file

    BUILD FINISHED

    Total time: 0.1588 seconds

License
-------

**This component is released under the new-style BSD license.**

Copyright (c) 2010, Gradwell dot com Ltd
All rights reserved.

Redistribution and use in source and binary forms, with or without modification, are permitted provided that the following conditions are met:

* Redistributions of source code must retain the above copyright notice, this list of conditions and the following disclaimer.
* Redistributions in binary form must reproduce the above copyright notice, this list of conditions and the following disclaimer in the documentation and/or other materials provided with the distribution.
* Neither the name of the copyright holder nor the names of its contributors may be used to endorse or promote products derived from this software without specific prior written permission.

THIS SOFTWARE IS PROVIDED BY THE COPYRIGHT HOLDERS AND CONTRIBUTORS "AS IS" AND ANY EXPRESS OR IMPLIED WARRANTIES, INCLUDING, BUT NOT LIMITED TO, THE IMPLIED WARRANTIES OF MERCHANTABILITY AND FITNESS FOR A PARTICULAR PURPOSE ARE DISCLAIMED. IN NO EVENT SHALL THE COPYRIGHT HOLDER OR CONTRIBUTORS BE LIABLE FOR ANY DIRECT, INDIRECT, INCIDENTAL, SPECIAL, EXEMPLARY, OR CONSEQUENTIAL DAMAGES (INCLUDING, BUT NOT LIMITED TO, PROCUREMENT OF SUBSTITUTE GOODS OR SERVICES; LOSS OF USE, DATA, OR PROFITS; OR BUSINESS INTERRUPTION) HOWEVER CAUSED AND ON ANY THEORY OF LIABILITY, WHETHER IN CONTRACT, STRICT LIABILITY, OR TORT (INCLUDING NEGLIGENCE OR OTHERWISE) ARISING IN ANY WAY OUT OF THE USE OF THIS SOFTWARE, EVEN IF ADVISED OF THE POSSIBILITY OF SUCH DAMAGE.
