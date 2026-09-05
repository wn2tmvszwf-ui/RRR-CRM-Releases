# RRR-CRM Stable Release Checklist

Use this checklist for every stable public release.

1. Private development build/tests are green.
2. RaceRoom end-to-end test completed.
3. Quest/VR release gate passed under comparable with/without Crew Manager conditions.
4. Build the final installer from the private development repository with `packaging/Build-StableRelease.ps1 -Version <version> -FrozenV1DistributionDirectory <path>`; this must produce `RRR-CRM_Setup_<version>.exe` and the matching `.sha256` file from the final installer bytes.
5. Verify the generated SHA-256 file matches the final installer.
6. Create a GitHub Release with tag `v<version>`.
7. Ensure the release is published, not Draft, and not marked Pre-release.
8. Upload both installer and matching `.sha256` asset.
9. Add concise release notes and migration notes if required.
10. Verify `releases/latest` resolves to this stable release.
11. Test an update from the previous installed stable version and confirm sessions/settings are preserved.

Do not publish a stable release if the installer hash changed after the `.sha256` file was generated.
