
Lineage 18.1 for Cracklingx
=======================
I used this as a template: https://github.com/chil360/lineage_osprey


Build Instructions
------------------
Create a build directory

	mkdir lineage
	cd lineage

Initialize your local repository using the LineageOS trees, use a command like this:

    repo init -u git://github.com/LineageOS/android.git -b lineage-18.1

Now create a local_manifests directory

    mkdir .repo/local_manifests

Copy my local manifest 'cracklingx.xml' to the 'local_manifests' directory.

Then to sync up:

    repo sync -c --force-sync

OR, for those with limited bandwidth/storage:

    repo sync -c --no-clone-bundle --no-tags --force-sync --optimized-fetch --prune

Apply required repopicks:

    Copy the repopick.sh script from this repo to the root of your build folder. Then run the repopick.sh script to apply.	

Apply any required patches:

    Copy patch.sh and the .patch files from this repo to the root of your build folder. Then run the patch.sh script to apply.	


Now start the build...

```bash
# Go to the root of the source tree...
$
# ...and run to prepare our devices list
$ . build/envsetup.sh
# ... now run
$ brunch cracklingx
```

Please see the [LineageOS Wiki](https://wiki.lineageos.org/) for further information.
