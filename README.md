# TrajectoryBot — GD 2.208 Android

This is an original Geode project skeleton for an offline/practice autoplay experiment.

## Important

The repository intentionally does **not** copy QOLMod or xdBot source. Their public projects can be studied for architecture, but code should only be reused when its license and attribution requirements permit it.

This project is split into:

- `RuntimeState`: collects the current player state.
- `Trajectory`: stores predicted points.
- `Predictor`: evaluates candidate input states.
- `AutoPlayer`: decides press/release.
- `Overlay`: draws debug information.
- `PlayLayer hook`: drives the controller once per game update.

## Current status

The project is a **buildable research foundation**, not a claim of perfect Geometry Dash botting. Exact 2.208 runtime behavior must be validated against the installed 2.208 Android bindings. A production-grade bot needs a complete object/trigger model for portals, pads, orbs, slopes, dual, wave, ship, UFO, spider, robot, swing and speed changes.

## Build

Install the matching Geode SDK and Android64 binaries, then:

```bash
geode sdk install-binaries -p android64
geode build -p android64
```

Do not mix a 2.208 mod target with 2.2081-only bindings or binary assumptions.

## Suggested test order

1. Launch with bot disabled.
2. Enable trajectory only.
3. Verify player state/trajectory.
4. Test candidate decision logging.
5. Enable bot in practice mode.
6. Only then test normal levels.

The controller is deliberately conservative: when confidence is low it does not press.
