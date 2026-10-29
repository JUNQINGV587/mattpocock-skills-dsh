---
"mattpocock-skills-dsh": patch
---

Widen the `@deepseek-ai/dsh-skill-filesystem` peer range to `>=0.1.0-rc.6 <0.3.0`.

dsh 0.2.x renamed nothing the bundle relies on: `apply(ctx, config)` still accepts
`providerName`, `includeDefaultRoots`, `bundledSkillDir`, and `watch`. The old
`^0.1.0-rc.6` range made the harness deny the profile bundle at startup
("Plugin mattpocock-skills-dsh@… is incompatible with dsh 0.2.2-alpha.2"), even
though the bundle loads all 25 skills through the host provider.
