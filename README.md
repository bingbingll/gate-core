# 做了一些汉化
1、执行 `mvn package` <br/>
2、将生成的jar包拷贝到你的GATE_Developer安装目录的lib文件夹中。 <br/>
3、将现有的gate-core-8.6.1.jar重命名为gate-core-8.6.1.jar.back，修改生成的gate-core-9.0.jar <br/>
# GATE Developer (including GATE Embedded)

[![Javadocs](https://javadoc.io/badge/uk.ac.gate/gate-core.svg?color=brightgreen&label=JavaDoc)](https://javadoc.io/doc/uk.ac.gate/gate-core)

Note that this is our current development code, if you are looking for stable releases please visit https://gate.ac.uk/download/

See the [user guide](http://gate.ac.uk/userguide) for more details

## Building and Running from the Source Code

Requirements:
* Java 8 or above
* Maven 3.6.0 or above

To build the development version of gate-core:
* clone this repository: `git clone https://github.com/GateNLP/gate-core.git` 
* change into the directory that has been created
* compile the library and install into your local Maven cache: `mvn install`

After this you can run the GUI from the `distro` directory as appropriate to your platform (`bin/gate.sh` on Linux, open `GATE.app` on Mac, or run `gate.exe` on Windows). When you update (`git pull`), it's the same procedure.

## Using Plugins

Plugins are no longer part of this `gate-core` repository - by default GATE will download its plugins from a Maven repository at runtime (the Central Repository for release versions of GATE, the [GATE Maven repository](https://repo.gate.ac.uk) for snapshots) so it is not necessary to build the plugins locally in order to use them. 

Each plugin by the GATE team is in its own repository on GitHub (search https://github.com/GateNLP for "gateplugin"), to make changes to a plugin simply clone its repository, make your changes, then `mvn install` - GATE will prefer your locally built version over one from a remote repository with the same (SNAPSHOT) version number.
