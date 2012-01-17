---
layout: default
title: download
tagline: up and running in moments.
description: 'The [SBT Launcher](http://github.com/sbt/sbt-launcher) project contains a set of native packages for use in your operating system. <br/>&nbsp;<br/>
[msi](#windows) | [yum](#rpm) | [apt-get](#deb) | [homebrew](#mac) | [by hand](#manual)
'
toplinks:
       - name: 'Windows MSI downloads'
         url: '#windows'
       - name: 'Yum Repository'
         url: '#rpm'
       - name: 'Apt Repository'
         url: '#deb'
       - name: 'Homebrew'
         url: '#mac'
       - name: 'Macports'
         url: '#mac'
       - name: 'Manual Installation'
         url: '#manual'
---

---------
<a id="windows" label="windows"></a>

#### Windows Releases ####

[Click here](http://typesafe.artifactoryonline.com/typesafe/windows-releases/org/scalasbt/sbt/0.11.2/sbt.msi) for the latest windows MSI.

*Note: This MSI is still in BETA.  While it has been tested it may fail in obscure situations, please make sure to report any issues you may find [here](https://github.com/sbt/sbt-launcher-package/issues).*

---------
<a id="rpm" label="rpm"></a>

#### Yum Repositories ####

Coming Soon...

---------

<a id="deb" label="deb"></a>

#### APT Repositories ####

Coming Soon...

---------

<a id="mac" label="mac"></a>

#### Hombrew/Macports ####

Use either MacPorts:

    $ sudo port install sbt

Or HomeBrew:

    $ brew install sbt

---------

<a id="manual" label="manual"></a>

#### By Hand installation ####

First, download the [launcher jar](http://typesafe.artifactoryonline.com/typesafe/ivy-releases/org.scala-tools.sbt/sbt-launch/0.11.2/sbt-launch.jar) and place it somewhere useful.

THEN, create a script in that same directory.

##### Windows #####

Create a `sbt.bat` file next to the launch jar.

    set SCRIPT_DIR=%~dp0
    java -Xmx512M -jar "%SCRIPT_DIR%sbt-launch.jar" %*

Add the directory containing `sbt.bat` to the windows path.

##### Unix-Like #####

Create a `sbt` script (a good place is `~/bin/sbt`

    java -Xmx512M -jar `dirname $0`/sbt-launch.jar "$@"

then make the script executable:

    $ chmod u+x ~/bin/sbt

