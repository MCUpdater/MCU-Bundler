# MCU-Bundler

This is a set of scripts and tools for wrapping the MCUpdater bootstrap jar up
as a Windows EXE or an OSX App file for easier use by players.

## OSX

The OSX app is bundled via the java.net Java Application Bundler project, which
itself is GPL2 licensed. A copy of the compiled appbundler jar is included in
this repository. For more information, see:
* https://java.net/projects/appbundler
* https://java.net/downloads/appbundler/appbundler.html
* http://docs.oracle.com/javase/7/docs/technotes/guides/jweb/packagingAppsForMac.html

## Windows

There is no windows bundler configured yet.

# Usage

The bundler is implemented as an ant build script, so in addition to cloning
this repository, one also needs:
* Apache Ant (http://ant.apache.org/), installed to your cli path.
* A compiled "MCUpdater.jar" file, placed at the root directory of this repo.

At that point, building the app is as simple as typing:
    ant

The default behavior is to package all configured bundlers. If you are only
interested in building an individual target, you can run:
    ant build-osx
or
    ant build-win

The resultant artifact(s) will be placed in the `out/` directory.
