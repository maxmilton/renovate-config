[![CI status](https://badgen.net/github/checks/maxmilton/renovate-config?label=ci)](https://github.com/maxmilton/renovate-config/actions)
[![Licence](https://badgen.net/github/license/maxmilton/renovate-config)](./LICENSE)

# maxmilton/renovate-config

Renovate config preset. See:

- <https://renovatebot.com/docs/configuration-options/>
- <https://renovatebot.com/docs/config-presets/>

## Usage

Add `.github/renovate.json` (no schedule; updates at any time):

```json
{
  "$schema": "https://docs.renovatebot.com/renovate-schema.json",
  "extends": ["config:best-practices", "github>maxmilton/renovate-config"]
}
```

Or only update once a month (multiple PRs, per package)

```json
{
  "$schema": "https://docs.renovatebot.com/renovate-schema.json",
  "extends": ["config:best-practices", "github>maxmilton/renovate-config", "schedule:monthly"]
}
```

Or only update once a month (everything in one PR)

```json
{
  "$schema": "https://docs.renovatebot.com/renovate-schema.json",
  "extends": ["config:best-practices", "github>maxmilton/renovate-config", "config:semverAllMonthly"]
}
```

### Special case project presets

Enable automatic merging (of tooling and stable non-major packages):

```json
"github>maxmilton/renovate-config:auto",
```

TypeScript app:

```json
"config:js-app",
```

TypeScript lib:

```json
"config:js-lib",
```

## License

MIT; see [LICENSE](./LICENSE).

-----

© [Max Milton](https://maxmilton.com)
