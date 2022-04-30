# Revanced CLI

Fork of the CLI version of the ReVanced Manager

If you don't know the first one, click [here](https://github.com/CriticalRange/revanced-patcher/blob/dev/README.md)

## Building

* Clone the repository as usual

`git clone https://github.com/RevancedTeam/revanced-cli`

* change directory to Revanced CLI

`cd revanced-cli`

* If you had put the [dependencies](https://github.com/CriticalRange/revanced-patches/blob/dev/README.md#putting-the-patcher-jar-file-into-gradle-dependencies) right, only thing left to do is to build via Gradle

`gradle build shadowJar`

And...

## Congratulations!🎉 

It should build the jar file (should be around 20mb)

Now to [patch the actually YouTube APK through Revanced CLI](https://github.com/CriticalRange/revanced-cli/wiki/Patching-YouTube-APK-using-ReVanced-CLI)