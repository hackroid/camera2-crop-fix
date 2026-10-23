## 0.4.0-beta.2

Support the official OnePlus 15T (PLZ110) LineageOS builds `24.0-20261011-NIGHTLY-fairlady`, `24.0-20261014-NIGHTLY-fairlady`, `24.0-20261015-NIGHTLY-fairlady` and `24.0-20261022-NIGHTLY-fairlady` in one package. The native patch source and its exact camera-service and camera-library hash checks are unchanged, so a listed build with different camera files is still rejected at install and activation.

- 20261011: device-tested profile.
- 20261022: camera service and the three checked camera libraries are byte-identical to the 20261011 profile (official OTA); device validation follows the update.
- 20261014, 20261015: listed by exact version; their camera files were not extracted, so the on-device hash checks decide.

## 0.4.0-beta.1

Initial public pre-release for OnePlus 15T (PLZ110), LineageOS `24.0-20261011-NIGHTLY-fairlady` only.

- Correct repeated crop metadata scaling for independently opened physical rear cameras 2 and 3, including quantized 10× and CUSTOM still requests.
- Toggle with Magisk Action; retain the requested state across reboot.
- Validate exact firmware/library identities and disable correction on a detected fault.
- Construct the patched image from the verified installed original; no complete system image is distributed.

Logical-camera automatic lens selection and application post-processing are outside this patch. Install this beta manually; automatic updates start with stable releases.
