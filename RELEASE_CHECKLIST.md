# RRR-CRM Stable Release Checklist

Use this checklist for every stable public release.

1. Private development build/tests are green.
2. RaceRoom end-to-end test completed.
3. Quest/VR release gate passed under comparable with/without Crew Manager conditions.
4. Build final installer as `RRR-CRM_Setup_<version>.exe`.
5. Calculate SHA-256 for the final installer bytes.
6. Create `RRR-CRM_Setup_<version>.exe.sha256` using that exact hash.
7. Create a GitHub Release with tag `v<version>`.
8. Ensure the release is published, not Draft, and not marked Pre-release.
9. Upload both installer and matching `.sha256` asset.
10. Add concise release notes and migration notes if required.
11. Verify `releases/latest` resolves to this stable release.
12. Test an update from the previous installed stable version and confirm sessions/settings are preserved.

Do not publish a stable release if the installer hash changed after the `.sha256` file was generated.
