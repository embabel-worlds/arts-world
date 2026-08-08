# Arts World

A world template for the Embabel appliance, tuned for the arts: worlds created
from it start with the **movie** and **impromptu** realms installed (plus
**research** — Wikipedia and Wikidata are half of any arts question, arriving through the default-world tier below).

## Use it

```bash
git clone https://github.com/embabel/appliance.git && cd appliance && ./me.py --world arts-world
```

Applies when a world is **first created**; an existing world is never reshaped.

## Why this repo is so small

It is a **delta, not a copy**. Every world resolves through the appliance's
four-tier overlay — this world's own config, then the installation's, then the
shared [default-world](https://github.com/embabel/default-world), then the
product's baked-in defaults — first hit wins, and anything absent here falls
through. So this repo declares only what makes the arts world *itself*: its
realm list. Types, apps, behaviour, prompts and the rest are inherited live
from the tiers below, and improvements to default-world reach arts worlds
without this repo changing.

Even `config/realms.yml` is a delta: realm manifests merge across the cascade
tiers (user-first), so this file declares only movie and impromptu, and the
default world's realms arrive through their own tier.

This template also works as a PARENT — a world (or another template) can declare

```yaml
extends:
  - arts-world
```

in its `config/world.yml` and inherit all of this live as a cascade tier.
