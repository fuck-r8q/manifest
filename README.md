repo init -u https://github.com/AOSPA/manifest -b calcite --git-lfs

git clone https://github.com/fuck-r8q/manifest.git -b calcite .repo/local_manifests

repo sync -c -j$(nproc --all) --force-sync --no-clone-bundle --no-tags

source build/envsetup.sh

lunch aospa_r8q-userdebug

m otapackage
