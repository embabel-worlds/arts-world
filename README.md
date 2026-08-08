# Arts World

A preconfigured world template for the Embabel appliance, tuned for the arts:
new worlds created from it come with the **movie** and **impromptu** realms
already installed (plus **research** — Wikipedia and Wikidata are half of any
arts question).

## Use it

```bash
git clone https://github.com/embabel/appliance.git && cd appliance && ./me.py --world arts-world
```

The template applies when a world is **first created** — an existing world is
yours and is never reshaped by it.

## Shape

This is a world template in the same layout as
[default-world](https://github.com/embabel/default-world): `config/` holds the
world's declared surface (realms, types, views, behaviour…), `data/` its
starting content. The realm list lives in `config/realms.yml`.
