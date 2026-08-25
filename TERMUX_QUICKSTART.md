# Quickstart: Android + Termux

```bash
termux-setup-storage
cd ~/TrajectoryBot-Termux-Android
chmod +x termux/*.sh
./termux/setup.sh
geode --version
./termux/build.sh
./termux/install-to-geode.sh
```

If `geode build -p android64` fails in Termux, use the included GitHub Actions workflow:
`.github/workflows/build-android64.yml`.

The workflow uses the official `geode-sdk/build-geode-mod` action and requests the `Android64` target.
