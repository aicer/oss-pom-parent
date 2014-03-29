### Releasing Artifacts to Maven Central ###

The following steps outline how to publish Maven artifacts via Sonatype

Detailed instructions are available here

https://docs.sonatype.org/display/Repository/Sonatype+OSS+Maven+Repository+Usage+Guide


Run the following command to deploy a SNAPSHOT

```shell
$ mvn clean deploy
```

The following steps allow us to prepare the release

```shell
$ mvn release:clean && mvn release:prepare
```

The following step allows us to stage the release on sonatype

```shell
$ mvn release:perform
```

You can also run the following step to prepare and perform the release

```shell
$ mvn release:clean && mvn release:prepare && mvn release:perform
```

To release your artifacts, open your favorite browser and go to https://oss.sonatype.org/

Login and then select your artifacts and close them

Then the next step is to select the item and release it from the UI.

The artifacts will be synced to the central repository in approximately 2 hours.

If you are having issues with the artifacts you can drop them from the UI as well.

