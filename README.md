# Vantablack External Mod Mirror

Patched or pinned third-party Fabric mods served to the Vantablack serverpack
build via packwiz. Each release documents its upstream source and the exact
modification. Upstream licenses ship unmodified inside every jar.

| Release | Upstream | Patch |
| --- | --- | --- |
| `fantasy-0.8.0+26.1.2-vb.1` | [NucleoidMC Fantasy 0.8.0+26.1.2](https://maven.nucleoid.xyz/xyz/nucleoid/fantasy/0.8.0+26.1.2/) (LGPLv3) | `fantasy.mixins.json`: `injectors.defaultRequire` 1 → 0 so Fantasy's cosmetic rain-packet `@Redirect` skips gracefully when another dimension library (arcade-dimensions) owns the same injection point instead of hard-failing the server boot. No class files changed. |
