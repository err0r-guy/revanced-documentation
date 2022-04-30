# ReVanced Patches

Fork of the repository for all ReVanced patches ([original here](https://github.com/ReVancedTeam/revanced-cli))

Assuming you have built [patcher](https://github.com/CriticalRange/revanced-patcher)

If you didn't, go ahead and do it since it will be required to build this project

## Installation

* Clone the repository

`git clone https://github.com/RevancedTeam/revanced-patches`

* change directory to the project

`cd revanced-patches`

* Switch to `dalvik-patches` branch (again, if it's merged into mainline skip this part)

`git switch dalvik-patches`

* Build the project once, you should encounter errors (this is for creating the required files)

`./gradlew build`

### Fixing the errors

For `username must not be null` error:

1. Create a GitHub account (I hope you already have one)

2. Go to settings, swipe down and select "Developer Settings"

3. Go to Personal access tokens and click to "Generate new token"

4. Type "ReVanced" to note and tick the boxes (don't know which one is needed) and click to "Generate new token"

5. You should see a code starting with "ghp_", copy all of it

6. Now go back to cli and type `gradle build -Pgpr.user=username -Pgpr.key=token`

`username` = Your GitHub account name
`token` = the token you copied

Change accordingly

### Putting the Patcher jar file into Gradle dependencies

(It is recommended to use a file explorer for this part)

* Firstly, copy the jar file you built from `revanced-patcher/build/libs` using the guide of [patcher](https://github.com/CriticalRange/revanced-patcher)

* Secondly, go to your root destination and then `.gradle/caches/modules-2/files-2.1/app.revanced/revanced-patcher/1.0.0-dev8` 

* there should be 3 folders, one of them should have a jar file, replace it with the jar you copied

* You should be ready to build the project

`gradle build`

* Lastly, go to `build/libs` inside the project and copy the jar file and do the same as in [Putting the Patcher jar file into Gradle dependencies](https://github.com/CriticalRange/revanced-patches/edit/dev/README.md#putting-the-patcher-jar-file-into-gradle-dependencies) but for patches instead.

## Congratulations🎉!

* You have successfully built the jar file of ReVanced Patcher!

* If you had any problems doing this or have suggestions, open an [issue](https://github.com/CriticalRange/revanced-patches/issues)

* Next to build: [ReVanced CLI (Last Part)](https://github.com/CriticalRange/revanced-cli)
