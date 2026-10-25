# Sonic Mania Wii - phone-friendly GitHub Actions build

This package combines the supplied Sonic Mania decompilation source with the supplied Mefiresu RSDKv5 Wii-port source.

## Build from a phone
1. Create an empty GitHub repository.
2. Upload the contents of this ZIP to the repository (the `.github` folder must be preserved).
3. Open **Actions** -> **Build Sonic Mania Wii** -> **Run workflow**.
4. When it finishes, open the run and download the **SonicMania-Wii** artifact.
5. Extract the artifact to get the `.dol`.

`Data.rsdk` is deliberately excluded. The Wii backend uses `BASE_PATH=/RSDKv5/`, so place your legally obtained `Data.rsdk` at `/RSDKv5/Data.rsdk` on the SD card.

The workflow uses the official `devkitpro/devkitppc:20260503` container and disables Plus/DLC in the distributed build.

This is an experimental community Wii port; a successful compile does not guarantee every Mania feature will run correctly on Wii hardware.
