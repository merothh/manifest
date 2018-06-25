Bootleggers ROM | 8.1 Sources
========

As always repo init, ser.

	repo init -u https://github.com/BootleggersROM/manifest.git -b oreo.1-gsi

And also sync, milord.

	repo sync -f --force-sync --no-clone-bundle -jx
        (the x on jx it's the amount of cores you have)

Since we're lazy people, we've done a buildscript named bootleg.sh (you'll find it after sync) to ease the build process.
Here's the usage help:

	"Usage: ./bootleg.sh <android-8.1> bootleg '# of jobs' 'version' "
	"*version examples"
	"*arm64-aonly"
	"*arm64-ab"

If you don't wanna use it, meh, you're on your own and we'll blame you for any derp. 
But if you do intersting stuff, PLOX, PR ser.


Help from other devices
-----------------------

Look, my device doesn't have flash, so i couldn't add and test the flash-required gestures and features. The same happens with Fingerprint stuff, so if you want to add tweaks, features or help me to optimize the ROM, you can make pull request and help me out, will be really appreciated.


Thanks section
--------------
Here's my thanks to people who made this possible:

* Shishu (For being there)
* Ground Zero ROMs Team
* AOSPExtended
* ABC ROMs
* NitrogenOS
* AICP
* DirtyUnicorns
* Lukas Koller (Camera Roll dev)
* fxckingdeathwish (for the amazing photos for wallpaper/headers)
* OmniROM
* CyanogenMod/LineageOS
* PixelExperience
* PureNexus
* merothh
* Resurrection Remix
* AOSiP
* CrDroid
* CypherOS
* PureKat
* theimpulson
* Dil3mm4

Help the GZOSP Guys
-------------------

They've done a really stable source but you can help them to get it better!
To do this, you will need an account setup with our gerrit server and a changeid hooks.
To add the changeid hook in a project, use the following commands:

	cd <project>
	scp -p -P 29418 <username>@review.gzospgzr.com:hooks/commit-msg ${gitdir}/hooks/

You can also install the hook globally in all local GZOSP projects

	repo forall -c 'gitdir=$(git rev-parse --git-dir); scp -p -P 29418 <username>@review.gzospgzr.com:hooks/commit-msg ${gitdir}/hooks/'

Go have a coffee while this runs

You can send patches by using these commands:

    cd <project>
    git add --all
    git commit
    git push ssh://<username>@review.gzospgzr.com:29418/GZOSP/<project> HEAD:refs/for/<branch>

This will commit your changes into a single commit.
Make sure your git has the changeid hooks added.
If you are going to make extra additions, just repeat steps, but instead of

	git commit

use

	git commit --amend

Gerrit will recognize it as a new patchset.

To view the status of your and others patches, visit [GZOSP Code Review](http://review.gzospgzr.com)
