# Optional modules

AzerothCore modules are C++ compiled into the core, so "new modules" arrive as
new package variants in the package feed (see `packages/`), shipped disabled by
default via their `.conf.dist`. A `catalog.json` listing those variants will
live here once the package CI builds them.
