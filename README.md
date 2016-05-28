Language Utils
=================

[![Gitter](https://badges.gitter.im/Join%20Chat.svg)](https://gitter.im/MascusJeoraly/LanguageUtils?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge)

A Bukkit/Spigot API offering the ability to get the name of **vanilla** items, entities, enchantments, and enchantment levels. 

The major version of this API supports 1.9.4. If you are using 1.7.10 or 1.8.9, please download versions with the suffix `-1.7.10` or `-1.8.9` accordingly.

Loading language files may cost 100-300 ms, but it should be fine to wait.

Also, if you want to know how to add customized language entries, just read the `README.txt` inside `lang/` folder.

You can get the latest build [here](https://drone.io/github.com/MeowInnovation/LanguageUtils/files "here").

You CAN install this plugin on Cauldron/KCauldron servers if you are using 1.2.0.1-1.7.10+ version of this plugin. Again, the API only supports **vanilla** language entries. It will just return the auto-generated material name of an item in mods.

Status: [![Build Status](https://snap-ci.com/MeowInnovation/LanguageUtils/branch/master/build_image)](https://snap-ci.com/MeowInnovation/LanguageUtils/branch/master) [![Build Status](https://drone.io/github.com/MeowInnovation/LanguageUtils/status.png)](https://drone.io/github.com/MeowInnovation/LanguageUtils/latest)


----------

Planned to have a refactoring and add mod support.

----------

## Use Language Utils

You can also see this [Example](https://github.com/MascusJeoraly/LangUtilsExample "Example") for detailed usage.

### Plugin dependency

First, you need to add LangUtils as a dependency in your `plugin.yml` file:

	depend: [LangUtils]

If you have multiple dependencies, add `,` between each of them:

	depend: [LangUtils, Vault]

Instead of adding LangUtils as a dependency, you can just add it as a soft dependency:

	softdepend: [LangUtils]

### Build Path

Just add this library to your build path.

### Maven/Gradle dependency

This plugin is hosting on [Github](https://github.com/MascusJeoraly/LanguageUtils/tree/mvn-repo "Github") cause I don't have a server.

If you are using Gradle, add the following to you `build.gradle`:

	repositories {
	    maven {
	        url 'https://raw.github.com/MascusJeoraly/LanguageUtils/mvn-repo/'
	    }
	}
	dependencies {
		compile group: 'com.meowj', name: 'LangUtils', version: '1.5.0' // Please check the latest version
	}

If you are using Maven, add the following to your `pom.xml`:

	<repositories>
	  <repository>
	    <id>lang-utils-repo</id>
	    <url>https://raw.github.com/MascusJeoraly/LanguageUtils/mvn-repo/</url>
	  </repository>
	</repository>
	
	<dependencies>
	  <dependency>
	    <groupId>com.meowj</groupId>
	    <artifactId>LangUtils</artifactId>
		<!--Please check the latest version -->  
	    <version>1.5.0</version>
	  </dependency>
	</dependencies>

### Usage

For further information, see the [Example](https://github.com/MascusJeoraly/LangUtilsExample "Example") plugin or `LanguageHelper` and `LocaleHelper`.

----------


## Contribute to this Project

If you don't have [Gradle](http://gradle.org/ "Gradle") installed, you can download one or use `gradlew`(Windows) / `./gradlew`(Linux) instead of `gradle` in the commands.

If you don't have permission when using `./gradlew`, run `chmod +x gradlew` and run the command again.

### Build

	[Navigate to the project directory]
	$ gradle build

You can find the output in the `build/libs` folder.

### Run Bukkit/Spigot Test Server

Before you run the command, you need to build Bukkit/Spigot server using [BuildTools](https://hub.spigotmc.org/jenkins/job/BuildTools/ "BuildTools") or download it [here](http://www.spigotdl.com/ "here"). (Powered by [spigotdl.com](spigotdl.com))

You should get something like `spigot-1.9.4-R0.1-SNAPSHOT.jar`. Rename it to `Server.jar`, and put it in the `run/` folder.(if not existed, create one in the project directory)

Then:

	[Navigate to the project directory]
	$ gradle run

### Test

	[Navigate to the project directory]
	$ gradle test
If there are some problems, see `build\reports\tests\index.html` for more info.

### Setup Dev Environment

If you are using IntelliJ IDEA(recommended):

	[Navigate to the project directory]
	$ gradle idea

If you just want to create a Module instead of a Project, run `gradle ideaModule` instead.

If you are using Eclipse(not tested)

	[Navigate to the project directory]
	$ gradle eclipse

### Pull Request

If you find any problems or want to improve the efficiency, please send me PR or issues.
