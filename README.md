# Ambient Light

A small DEX-free NativeActivity instrument displaying Android's actual light
reading in lux. Missing light hardware and failed activation are explicit
states; no accelerometer/proximity reading is substituted. The source was
absent before this SUN, so this establishes its first implementation rather
than claiming an existing app was upgraded.

The narrow Android adapter and packaging are shared with Gyroscope and
Magnetometer in the pinned utilities repository. Continuous 5×7 geometry and
8×8 coverage come only from `rough.framebuffer`. This repository owns its
manifest, label, package identity, dependency pins, build workflow and APK
acceptance. No renderer copy is embedded here.

Package: `com.isomorphisms.ambientlight`, versionCode 1.
Persistent public development certificate SHA-256:
`DE:9B:1D:47:C5:A6:5E:6D:46:A2:04:B7:9D:D9:EE:56:6B:9D:3C:98:32:BA:81:EB:C4:21:3D:33:92:E9:2F:F9`.

CI checks out pinned shared sources, qualifies ICK stages and builds ARMv7,
ARM64 and x86-64 APKs. ICK produces maintained C; NDK assembles/links and
provides upstream NativeActivity glue. The existing hosted signer performs
APK signing. No phone-side build is required.

APK inspection, same-candidate replacement, launch, posted frame, emulator
memory and APK sizes are separate configured checks until their run passes.
Physical MIRO A1/C67 readings, responsiveness, light response and typography
remain unverified. No calibration or photometric accuracy is claimed.
