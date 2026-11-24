# Vantablack External Mod Mirror

Patched or pinned third-party Fabric mods served to the Vantablack serverpack
build via packwiz. Each release documents its upstream source and the exact
modification. Upstream licenses ship unmodified inside every jar.

| Release | Upstream | Patch |
| --- | --- | --- |
| `fantasy-0.8.0+26.1.2-vb.1` | [NucleoidMC Fantasy 0.8.0+26.1.2](https://maven.nucleoid.xyz/xyz/nucleoid/fantasy/0.8.0+26.1.2/) (LGPLv3) | `fantasy.mixins.json`: `injectors.defaultRequire` 1 → 0 so Fantasy's cosmetic rain-packet `@Redirect` skips gracefully when another dimension library (arcade-dimensions) owns the same injection point instead of hard-failing the server boot. No class files changed. |
| `everyslab-4.0.0+26.1.2-vb.1` | [Boxadactle EverySlab 4.0.0](https://github.com/Boxadactle/EverySlab/tree/4.0.0) (GPLv3), built from upstream commit `c7239c0` | Startup speed-up: wall and fence block states that resolve to the same shape share one cached `VoxelShape`, and face-support checks are memoized per shape (`ShapeCache` plus `BlockStateCacheMixin`, `CrossCollisionBlockMixin`, `WallBlockMixin`). Version set to `4.0.0+26.1.2-vb.1`. Assets and data are byte-identical to the CurseForge 4.0.0 jar. Full source and patch are attached to the release. |
