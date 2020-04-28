Papercut ![Java CI](https://github.com/Minevictus/Papercut/workflows/Java%20CI/badge.svg)
==

Fork of [Paper](https://github.com/PaperMC/Paper) for Minevictus.

## How To (Server Admins)
Papercut uses the same paperclip jar system that Paper uses.

You can [build it yourself](https://github.com/Minevictus/Papercut#building)

## How To (Plugin developers)
In order to use Papercut as a dependency you must [build it yourself](https://github.com/Minevictus/Papercut#building).
Each time you want to update your dependency you must re-build Papercut.

Papercut-API maven dependency:
```xml
<dependency>
    <groupId>us.minevict.papercut</groupId>
    <artifactId>papercut-api</artifactId>
    <version>1.15.2-R0.1-SNAPSHOT</version>
    <scope>provided</scope>
 </dependency>
 ```

Papercut-Server maven dependency:
```xml
<dependency>
    <groupId>us.minevict.papercut</groupId>
    <artifactId>papercut</artifactId>
    <version>1.15.2-R0.1-SNAPSHOT</version>
    <scope>provided</scope>
</dependency>
```

There is no repository required since the artifacts should be locally installed
via building Papercut.

## Building

Requirements:
- You need `git` installed, with a configured user name and email. 
  On Windows you need to run from git bash.
- You need `maven` installed
- You need `jdk` 8+ installed to compile (and `jre` 8+ to run)
- Anything else that `paper` requires to build

If all you want is a paperclip server jar, just run `./papercut jar`.

Otherwise, to setup the `Papercut-API` and `Papercut-Server` repo, just run the following command
in your project root `./papercut patch` additionally, after you run `./papercut patch` you can run `./papercut build` to build the 
respective api and server jars.

`./papercut patch` should initialize the repo such that you can now start modifying and creating
patches. The folder `Papercut-API` is the api repo and the `Papercut-Server` folder
is the server repo and will contain the source files you will modify.

#### Creating a patch
Patches are effectively just commits in either `Papercut-API` or `Papercut-Server`.
To create one, just add a commit to either repo and run `./papercut rb`, and a
patch will be placed in the patches folder. Modifying commits will also modify its
corresponding patch file.

## License
The PATCHES-LICENSE file describes the license for api & server patches,
found in `./patches` and its subdirectories except when noted otherwise.

Everything else is licensed under the MIT license, except when noted otherwise.
See https://github.com/starlis/empirecraft and https://github.com/electronicboy/byof
for the license of material used/modified by this project.

### Note

The fork this is based off of is based off of aikar's EMC framework found [here](https://github.com/starlis/empirecraft).
This fork is based off of Tuinity with its patches and whatnot removed.
