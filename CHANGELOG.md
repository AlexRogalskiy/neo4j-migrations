# 1.4.0

*No breaking changes*.  The version is bumped due to a couple of new features that required additional API, for example using only remote or locally discovered migrations.

A big "Thank you" goes out to @marianozunino, a long time Neo4j (and Spring Data Neo4j) user, who created his own refactor tooling dubbed [Morpheus](https://github.com/marianozunino/morpheus). We worked together so that this and his tooling use the same meta model. And afterwards, I took some inspiration from the features he had in Morpheus.

The feature I like the most in this release is the new and shiny integration with Quarkus dev-services, check it out: [Dev Services integration](https://michael-simons.github.io/neo4j-migrations/1.4.0/#devservicesintegration).

## 🚀 Features
- c8f29d4 Add unique constraint for migration nodes on Neo4j 4.4. (#428)
- ed04748 Write and read optional config file from CLI. (#427)
- ad644a5 Add `mode` option to `InfoCmd`.
- b9afdd8 Introduce a ChainBuilderMode to select local or remote chains only. (#425)
- d63629e Make `file:./neo4j/migrations` the default for `--location` in the CLI. (#424)
- f3ad97c Add Quarkus Dev-UI integration.
- 5814489 Provide `ConnectionDetails` without retrieving the whole chain of applied migrations.

## 🐛 Bug Fixes
- 085cb4f Fix JaCoCo configuration.

## 🔄️ Refactorings
- b476a79 Avoid unnessary accessors for Quarkus processors.
- 970c84c Use default location only if it exists.
- 16eca1e Avoid printing a full stack trace for expected exceptions in the CLI. (#423)
- 81048fa Reduce visibility of build items. (#412)
- 46263f2 Use Quarkus' built-in class indes and classpath resource utils.
- b5383f1 Improve test.

## 📝 Documentation
- 76e23ef Use correct language for Gradle snippet.
- c2bfe46 Add morpheus to README.
- 2e9594a Update local changelog.

## 🧹 Housekeeping
- ba4c60c Bump nexus-staging-maven-plugin from 1.6.11 to 1.6.12
- 1a152eb quarkus-neo4j extension from 1.0.3 to 1.0.4. (#431)
- 6f00824 Bump quarkus.version from 2.7.1.Final to 2.7.2.Final (#430)
- 2cc1184 Bump maven-compiler-plugin from 3.9.0 to 3.10.0 (#418)
- e47b2d3 Bump native-maven-plugin from 0.9.9 to 0.9.10 (#417)
- 1b828bb Bump maven-site-plugin from 3.10.0 to 3.11.0 (#416)
- 73963b4 Bump nexus-staging-maven-plugin from 1.6.8 to 1.6.11 (#415)

## 🛠 Build
- 2716106 Provide parameter names.
- a2ac68f Remove sysouts.


## Contributors
We'd like to thank the following people for their contributions:
- @michael-simons


# 1.3.3

*No breaking changes*.  Biggest change is the upgrade to Quarkus 2.7 inside the Quarkus extension. Thanks to @lukehutch for a new release of [ClassGraph](https://github.com/classgraph/classgraph) that improves compatibility with Quarkus' classloader.

## 📝 Documentation
- 09cabe1 Add a local changelog.

## 🧹 Housekeeping
- 125540c Revert "Bump nexus-staging-maven-plugin from 1.6.8 to 1.6.10 (#402)"
- a5a0c84 quarkus-neo4j extension from 1.0.2 to 1.0.3.
- 13fcae8 Bump nexus-staging-maven-plugin from 1.6.8 to 1.6.10 (#402)
- ca95751 Bump neo4j-harness from 4.4.3 to 4.4.4 (#403)
- 112f38c Bump picocli from 4.6.2 to 4.6.3 (#404)
- a75a0ef Bump slf4j.version from 1.7.35 to 1.7.36 (#406)
- a6b6452 Bump byte-buddy.version from 1.12.7 to 1.12.8 (#407)
- f5d8c32 Bump maven-javadoc-plugin from 3.3.1 to 3.3.2 (#408)
- 2f281a3 Bump quarkus.version from 2.6.3.Final to 2.7.1.Final (#401)
- fcebed4 Bump classgraph from 4.8.138 to 4.8.139 (#405)


## Contributors
We'd like to thank the following people for their contributions:
- @michael-simons


# 1.3.2

*No breaking changes*.  Mostly dependency upgrades.

Most notable is the fact that the native binaries are now build with **GraalVM 22.0** and benefit from the improvements in the SubstrateVM.

## 🐛 Bug Fixes
- d11401b Make version check more lenient during integration tests.

## 🧹 Housekeeping
- e976934 Bump graal-sdk from 21.3.0 to 22.0.0.2 (#391)
- 3613be7 Bump maven-project-info-reports-plugin from 3.1.2 to 3.2.1 (#400)
- 6eb3e3c Bump docker-maven-plugin from 0.38.1 to 0.39.0 (#399)
- aea9784 Bump quarkus.version from 2.6.2.Final to 2.6.3.Final
- 0db3094 Bump junit-jupiter-causal-cluster-testcontainer-extension from 2022.0.0 to 2022.0.1 and testcontainers.version from 1.16.2 to 1.16.3.
- d34fa93 Bump neo4j-java-driver from 4.4.2 to 4.4.3 (#398)
- 8e20a80 Bump checkstyle from 9.2.1 to 9.3 (#396)
- 83142e5 Bump japicmp-maven-plugin from 0.15.4 to 0.15.6 (#395)
- c10afa9 Bump asciidoctor-maven-plugin from 2.2.1 to 2.2.2 (#393)
- fd3f147 Bump mockito.version from 4.2.0 to 4.3.1 (#392)
- 87e8673 Bump slf4j.version from 1.7.33 to 1.7.35 (#390)
- 7425469 Bump spring-boot.version from 2.6.2 to 2.6.3 (#388)
- d653dac Bump maven-plugin-plugin from 3.6.2 to 3.6.4 (#387)
- b58a5e8 Bump maven-plugin-annotations from 3.6.2 to 3.6.4 (#385)
- 5100c54 Bump quarkus.version from 2.6.1.Final to 2.6.2.Final (#377)
- b41bd6d Bump byte-buddy.version from 1.12.6 to 1.12.7 (#376)
- 1b33ca3 Bump neo4j-harness from 4.4.2 to 4.4.3 (#378)
- d07182a Bump asciidoctorj from 2.5.2 to 2.5.3 (#379)
- 5fec62c Bump slf4j.version from 1.7.32 to 1.7.33 (#380)
- cff33f5 Bump maven-jar-plugin from 3.2.1 to 3.2.2 (#381)
- 34a7979 Bump maven-compiler-plugin from 3.8.1 to 3.9.0 (#382)
- f308d5f Revert "Bump maven-enforcer-plugin from 3.0.0-M3 to 3.0.0"
- 7ef3bff Bump maven-enforcer-plugin from 3.0.0-M3 to 3.0.0

## 🛠 Build
- aef5da1 Use GH usernames if available.
- 391d29f Introduce a 'fast' profile and mute javadoc plugin debug out.
- a8baea5 Simplify Testcontainers code. (#383)
- bcb7b14 Optimize release workflow.
- 18b1ab3 Enable debug information and use bytecode verification during tests.


## Contributors
We'd like to thank the following people for their contributions:
- @michael-simons
- @bsideup


# 1.3.1

## 🐛 Bug Fixes
- 81ea8e5 Check for non-empty classpath locations when in native image.

## 🧰 Tasks
- 24973fd Apply package name change in japicmp config.

## 🧹 Housekeeping
- fe713a9 Bump maven-jar-plugin from 3.2.0 to 3.2.1 (#373)

## 🛠 Build
- 5a74da1 Improve caching of Maven dependencies. (#375)
- 1360fd9 Use actions/cache@v2. (#374)
- dc37038 Add dedicated categories for chores and refactorings.


## Contributors
We'd like to thank the following people for their contributions:
- [Michael Simons](https://github.com/michael-simons)


# 1.3.0

Happy 2nd birthday, _neo4j-migrations_! 🥳 The first pre-release, 0.0.1 has been pushed out to central on January 9th, 2020. Since than, stuff has come a long way and I am super happy about it.

1.3.0 is a big release coming only 4 days after the last one [(1.2.3](https://github.com/michael-simons/neo4j-migrations/releases/tag/1.2.3)) and bumping the minor number. Why is that? 
The API hasn't changed in an incompatible way, but there are 2 changes in behavior

1. 2afaaa5 aligns the behavior of the `enabled` flag in the Spring Boot starter with the behavior in the Quarkus extension: A bean of type `Migrations` will be provided in the application context regardless of that setting. You are free to use it any way you want. You might want to make sure your application is on a valid database or not without us applying the migrations. Or you just want to use the `info` api to get the current version
2. c98d757 makes `locations-to-scan` and `packages-to-scan` [Build Time configuration](https://quarkus.io/guides/config-reference#build-time-configuration), meaning they are evaluated at built respectively augmentation time. This allows to finally complete the feature I had on my list since forever [("Add a Quarkus extension")](https://github.com/michael-simons/neo4j-migrations/issues/8) in full: Delivered with c10c4468 in 1.2.2 for the first time, it is now fully supported (and tested) in natively distributed Quarkus applications as well and with that, feature complete. If you want (or need) file based locations outside an augmented application, please use the new `external-locations`. It supports only file-based locations, does not become part of the image and is changeable without re-augmentation.

## 🚀 Features
- 20f27d3 Compress native CLI binaries. (#372)
- b67fcc0 Add `apply` alias for `migrate` to the CLI.
- c98d757 Support classpath scanning in Quarkus native image.
- 2afaaa5 Allow disabling of migrations in Spring Boot without removing the `Migrations` bean. (#361)

## 🔄️ Refactorings
- ccd6461 Fail early with `classpath://` locations passed to the CLI in native image. (#369)
- 62278f2 Make sure that all sessions handed out use the latest bookmarks known. (#370)
- 3923423 Use transaction functions for all interactions with Neo4j inside the core module. (#365)
- a3422a8 Replace `MigrationsInitializer` in Quarkus extension with ServiceStartBuildItem.
- 4ad5dd0 Use List.sort instead of Collections.

## 📝 Documentation
- 6a5ca16 Improve core JavaDocs.

## 🛠 Build
- 356fa46 Add end-to-end test for the native CLI. (#371)
- 5ffda5c Use official GraalVM action for releasing. (#366)
- 2c96895 Define a stable order for categories in the changelog.


## Contributors
We'd like to thank the following people for their contributions:
- [Michael Simons](https://github.com/michael-simons)
- [Gerrit Meier](https://github.com/meistermeier)


# 1.2.3

## 🚀 Features
- 4840904 Add Neo4j JBang catalog distribution.

## 📝 Documentation
- f80e684 Improve CONTRIBUTING document.

## 🧰 Tasks
- 4079810 Extend license header to 2022.

## 🧹 Housekeeping
- ffddee7 Bump jreleaser-maven-plugin from 0.9.1 to 0.10.0 (#360)
- 1d9da39 Bump native-maven-plugin from 0.9.8 to 0.9.9 (#351)
- fd82573 Bump maven-deploy-plugin from 3.0.0-M1 to 3.0.0-M2 (#358)
- 36cf426 Bump sortpom-maven-plugin from 3.0.0 to 3.0.1 (#359)
- bf76713 Bump system-lambda from 1.2.0 to 1.2.1 (#357)
- 4b144f3 Bump assertj-core from 3.21.0 to 3.22.0 (#356)
- 11b57ce Bump byte-buddy.version from 1.12.5 to 1.12.6 (#349)
- 9e06096 Bump spring-boot.version from 2.6.1 to 2.6.2 (#350)
- 0122f66 Bump quarkus.version from 2.6.0.Final to 2.6.1.Final (#352)
- 9f8a369 Bump maven-site-plugin from 3.9.1 to 3.10.0 (#353)
- e03eef0 Bump plexus-component-annotations from 2.1.0 to 2.1.1 (#354)
- cd829fa Bump checkstyle from 9.2 to 9.2.1 (#355)


## Contributors
We'd like to thank the following people for their contributions:
- [Michael Simons](https://github.com/michael-simons)
- [Gerrit Meier](https://github.com/meistermeier)


# 1.2.2

## 🚀 Features
- c10c446 Add Quarkus-Module. (#343)
- 209b1d6 Allow safe passwords in scripts. (#341)
- 06c7344 Add shell autocompletion for the CLI module.
- e5f017f Support lifecycle callbacks. (#336)

## 📝 Documentation
- 7b3decd Add Quarkus extension to README.
- 6776211 Add Quarkus extension to the list of modules.
- 2a1b096 Use the wording Quarkus extension.
- 8100163 Add instructions for running on the module-path.
- 54ba14d Correct spelling errors and unify wording across documentation and code. (#340)
- befea0e Create a dedicated manual instead of one overly long readme. (#339)

## 🧹 Housekeeping
- de51201 Bump docker-maven-plugin from 0.38.0 to 0.38.1 (#348)
- ad65f91 Bump byte-buddy.version from 1.12.3 to 1.12.5 (#347)
- 3df66f4 Bump quarkus-neo4j.version from 1.0.1 to 1.0.2 (#346)
- 812ef78 Bump mockito.version from 4.1.0 to 4.2.0 (#345)
- d76eadc Bump neo4j-harness from 4.4.0 to 4.4.2
- 9fc602c Bump classgraph from 4.8.137 to 4.8.138 (#338)
- 1fa0c55 Bump neo4j-java-driver from 4.4.1 to 4.4.2 (#337)

## 🛠  Build
- e4663c7 Generate zsh completion only for macos.
- 637412e Provide module-info for JDK 11 and higher instead of only for JDK 17+.
- f32e3ec Exlude JReleaser bits from Sortpom so that the emojis don't turn into cold XML-Entities.
- af91f0c Use one central script for creating the site.
- 1a53bc0 Polish build of docs.
- 318a889 Add zip file to distribution.
- 89e1e79 Reorder plugins so that the zip distribution isn't empty.


## Contributors
We'd like to thank the following people for their contributions:
- [Michael Simons](https://github.com/michael-simons)
- [Gerrit Meier](https://github.com/meistermeier)


# 1.2.1

## 🐛 Fixes
- 0378b27 Ignore files without extensions in filesystem resources.
- 118d078 Fix broken checkstyle config.
- 1e7cc51 Add MANIFEST.MF to native bundle and provide a central way to retrieve the product version. (#329)

## ♻️  Changes
- af1a790 Don't declare unchecked exception explicitly.
- ab7cccb Tidy up CLI. (#335)
- 08a4d0e Pre-filter Cypher scripts that cannot be parsed into a version. (#330)

## 🧹 Housekeeping
- a85bc05 Bump neo4j-harness from 4.3.7 to 4.4.0 (#332)
- f15f9a6 Bump byte-buddy.version from 1.12.2 to 1.12.3 (#333)
- ba09f1c Bump native-maven-plugin from 0.9.7.1 to 0.9.8 (#334)
- dcb531e Bump spring-boot.version from 2.6.0 to 2.6.1 (#331)

## 🛠  Build
- c31f9d1 Move all JReleaser templates into `etc/jreleaser`.
- 689dc17 Update JReleaser configuration with 0.9.1 changes. (#327)

## 📝 Documentation
- 73e279c Improve the structure of the readme.
- ab78aad Add information about  keyword.


## Contributors
We'd like to thank the following people for their contributions:
- [Michael Simons](https://github.com/michael-simons)
- [Andres Almiray](https://github.com/aalmiray)
- [Gerrit Meier](https://github.com/meistermeier)


# 1.2.0

## 🚀 Features
- 922b865 Add `validate` command. (#326)
- 4f3fe73 Add a Java Module system descriptor.

## 🐛 Bug Fixes
- cb2d614 Also catch `Neo.ClientError.Schema.ConstraintAlreadyExists` while locking. (#324)

## 📝 Documentation
- 839c1c2 Improve plain Java example in README.

## 🧹 Housekeeping
- e1a321d Bump checkstyle from 9.1 to 9.2 (#321)
- ea930f9 Bump maven-plugin-plugin from 3.6.1 to 3.6.2 (#322)
- 9655e3f Bump classgraph from 4.8.134 to 4.8.137 (#320)
- aad3209 Bump byte-buddy.version from 1.12.1 to 1.12.2 (#319)
- 14ea910 Bump maven-plugin-annotations from 3.6.1 to 3.6.2 (#318)
- 64f9c11 Bump junit-bom from 5.8.1 to 5.8.2 (#317)
- 2b2fd70 Bump version (needed due to added deprecations).

## 🧰 Build
- 2d3a29a Follow the Sonar manual for aggregating multi-module test-data. (#325)
- 1a1be95 Adapt JReleaser to changed dependabot commit messages.
- cb8c3fb Automate update of old (previous) version.

## Changes
- da5722b Separate integration tests from unittests. (#328)


## Contributors
We'd like to thank the following people for their contributions:
- [Michael Simons](https://github.com/michael-simons)


# 1.1.0

## 🚀 Features
- 08950cf Add `clean` command. (#315)
- 1efb2ba Add support for storing schema database independent from target database. (#303)

## 🐛 Bug Fixes
- 963d389 The match for versions in the default database was too fuzzy. (#311)
- a27e5a6 Fix flaky logging test. (#305)

## 🧰 Build
- 8b9c546 Automate update to README.adoc.
- 3a338e4 Enforce semantic versioning. (#304)
- 87ba6f1 Use testcontainers.cloud if available.

## 🧹 Housekeeping
- bc68f4f Bump spring-boot.version from 2.5.6 to 2.6.0 (#306)
- 2619ed9 Bump maven.version from 3.8.3 to 3.8.4 (#312)
- 61f0322 Bump classgraph from 4.8.133 to 4.8.134 (#314)
- 09475e8 Bump mockito.version from 4.0.0 to 4.1.0 (#313)
- 161e233 Bump classgraph from 4.8.132 to 4.8.133 (#307)
- 73d3b39 Bump neo4j-java-driver from 4.4.0 to 4.4.1 (#300)
- c25494c Bump byte-buddy.version from 1.11.19 to 1.12.1 (#299)
- 7bd06e7 Bump jna from 5.9.0 to 5.10.0 (#298)
- c52c6e4 Bump neo4j-harness from 4.3.6 to 4.3.7 (#297)
- 2bab394 Bump sonar-maven-plugin from 3.9.0.2155 to 3.9.1.2184 (#296)
- ab5b3e5 Bump docker-maven-plugin from 0.37.0 to 0.38.0 (#301)
- 0d13959 Bump classgraph from 4.8.129 to 4.8.132 (#302)

## Changes
- 375541d Provide a better example in the Maven integration test with single config. (#308)

## Tasks
- be63550 Make javadoc happy. (#309)
- 57e07be Rename `master` to `main`.
- 4c126ed Add a code of conduct.
- 74784c1 Rename license file in a generic way.


## Contributors
We'd like to thank the following people for their contributions:
- [Michael Simons](https://github.com/michael-simons)


# 1.0.0

## 🚀 Features
- d20c86d Add support for 4.4 user impersonation. (#292)

## 🐛 Bug Fixes
- 3a7bc1b Fix file mode.
- cd20925 Fix mutable defaults. (#285)
- a637c46 Fix name.
- 147e366 Fix typo.
- 4ace342 Fix low hanging smells. (#277)
- 6efe367 Add test for security hotspot fixes.
- 5bd1a9a Review and fix security hotspots. (#276)

## 📝 Documentation
- aa63ab4 Add simple contributing information.
- b65e2d0 Add homebrew instructions.
- 44f3402 Remove `$` to allow copy & paste via GH ui.
- 5f98717 Document how to add classes to the command line. (#26)

## 🧰 Build
- ffcd3de Use correct workflow name.
- b9e9623 Skip integration test aggregator signing on release.
- e1cc5f9 Use JReleaser for GH releases, uploading artifacts and Homebrew integration.

## 🧹 Housekeeping
- 3d7fa30 Bump neo4j-java-driver from 4.2.7 to 4.4.0 (#290)
- 368ff6c Bump picocli from 4.6.1 to 4.6.2 (#291)
- 4c596f3 Bump checkstyle from 9.0.1 to 9.1 (#289)
- 69103d4 Bump native-maven-plugin from 0.9.6 to 0.9.7.1 (#288)
- e97780d Bump classgraph from 4.8.128 to 4.8.129 (#287)
- acb89a9 Bump testcontainers.version from 1.16.0 to 1.16.2 (#278)
- 896e306 Bump spring-boot.version from 2.5.5 to 2.5.6 (#279)

---
- 1f53e7b Use singletonList. (#286)
- 1f6270d Remove unnecessary line break. (#283)
- 26ecff5 Simplify build steps.
- 81a88ee Analyze only on non-forked prs and no dependabot prs.
- 507ffd8 Aggregate coverage after integration test.
- 8e4b92b Remove superflous name from job.
- e6cb08a Improve Migrations api.
- f58c117 Improve DefaultChainElement.
- 69adb3e Remove remaining unmanaged version. (#29)
- b0e0d08 Improve exception handling.
- afff47b Add badges.
- 63b913e Improve AbstractConnectedMojo and tests.
- c466804 Add more tests.
- 51be13c Set expected coverage to a minimum now that there is at least one test
- 93c0233 Add JaCoCo and Sonar analysis to the build. (#275)


## Contributors
We'd like to thank the following people for their contributions:
- [Michael Simons](https://github.com/michael-simons)
- [Gerrit Meier](https://github.com/meistermeier)
- [Andres Almiray](https://github.com/aalmiray)


# 0.3.2

## 🧹 Housekeeping

* Tons of dependency updates thanks to @dependabot.


# 0.3.1

## 🚀 Features

- GH-238 - Add autocrlf option.

## 🐛 Bug Fixes

- Fix logging on native image.

## 🧹 Housekeeping

- GH-239 - Use transaction functions instead of auto commits where applicable.
- Don't print full stacktrace on auth error.
- Set pool size to 1 in CLI. [improvement]
 
Java and native binaries are now published with each GitHub-Release.


# 0.2.1

## 🚀 Features

* GH-237 - Add `validateOnMigrate` to skip validation of migration-checksums.

## 🐛 Bug Fixes

* GH-232 - Treat single `\r` as correct line endings.

## 🧹 Housekeeping

* Tons of dependency updates thanks to @dependabot.

Noteworthy: Upgraded the example using Neo4j Test-Harness to Neo4j *4.3.2*. Neo4j requires JDK 11, so this project requires now JDK 11 to **build** but **still targets JDK 8**, so that it can be used with Java 8. I do think that this change in the build justifies a minor version bump alone but we have also a new configuration option, hence the 0.2.1 version.

Thanks to @AndreasBoehme for his input on this release!


# 0.1.4

## 🧹 Housekeeping

* Tons of dependency updates thanks to @dependabot.

Noteworthy: Upgraded to Spring Boot 2.5.0.


# 0.1.3

## 🧹 Housekeeping

* Tons of dependency updates thanks to @dependabot.

Especially the upgrade to Classgraph 4.8.103 has to be mentioned, as that fixes a resource scanning issue.


# 0.1.2

## 🚀 Features

* GH-159 - Add support for more flexible version schemes in migration names (thanks to @katya-dovgalets)

## 🧹 Housekeeping

* Tons of dependency updates thanks to @dependabot


# 0.1.1

## 🧹 Housekeeping

* Tons of dependency updates thanks to @dependabot
* The Spring Boot Starter has been updated to Spring Boot 2.4 and thus doesn't require the custom Neo4j driver starter anymore!  🎉


# 0.0.13

## 🧹 Housekeeping

* Tons of dependency updates thanks to @dependabot
* In the Spring Boot starter: Configure the migrations after Neo4j Data, so that we indirectly run after the builtin driver starter from 2.4 on upwards.


# 0.0.12

## 🐛 Bug Fixes

* GH-89: Configure class scanner to handle Spring Boot packaged resources.

## 🧹 Housekeeping

* Tons of dependency updates thanks to @dependabot

Thanks to our contributor @corneil


# 0.0.11

## 🚀 Features

* Created a Maven plugin.

## 🐛 Bug Fixes

* Don't close `System.err` in the CLI (That happened accidentally as I inherited from `java.util.logging.ConsoleHandler`

## 🧹 Housekeeping

* Tons of dependency updates thanks to @dependabot


# 0.0.10

## 🐛 Bug Fixes

Neo4j-Migrations didn't work on instances with anonymous access due to the fact the user management procedures will be removed in such an instance.


# 0.0.9

## 🧹 Housekeeping

* Easier use of the starter: Starter for driver is a non-optional dependency for the starter and stays optional for the auto configuration itself, so that people have choice whether to include it or not.


# 0.0.8

## 🚀 Features

* Spring Boot starter added with instructions

## 🚨Api changes

* Renamed prefix `filesystem:` to `file:` to be consistent with most other tools out there. 

*NOTE:* There are 0.0.6 and 0.0.7 on central, but without the starter due to issues with Maven's release plugin, the Nexus plugin and submodules with a different parent. I'm sorry for that.


# 0.0.5

## 🚀 Features

* CLI Module added with instructions


# 0.0.4

## 🚀 Features

* Record execution time
* Full support for multiple databases in Neo4j 4.0
* Convenience methods `MigrationContext#getSession` and `MigrationContext#getSessionConfig` to for session or session config retrieval in Java based migrations
* Add `Migrations#info`, returning a `MigrationChain` containing the state of your database and all discoverable migrations

## 🚨Api changes

* Public Core API lives now under `ac.simons.neo4j.migrations.core`
* Datamodel change: Execution time is now stored as Neo4j `Duration`
* `MigrationType` is an enum now
* `MigrationState` added


# 0.0.3

## 🚀 Features

* Checksums for Cypher script based migrations (stored and validated)

## 🧹 Housekeeping

* Turned into multi module project
* Added Checkstyle to the build for making contributions easier
* Decoupled discovery of migrations from the actual migrations


# 0.0.2

## 🚀 Features

* Cypher based migrations
* More information stored on `__Neo4jMigration` nodes and `MIGRATED_TO` relations (description, type, database and system user, possible checksums)

## 🚨Api changes

* `ac.simons.neo4j.migrations.Migration#apply` takes in a `MigrationContext`, which contains the driver and the migrations configuration and allows for further changes without breaking that API again.


# 0.0.1

Preview release with basic functionality for use in JHipster.
