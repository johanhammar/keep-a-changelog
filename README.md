# Keep-a-changelog plugin for release-it

This [release-it plugin](https://github.com/release-it/release-it/blob/master/docs/plugins.md) maintains your
CHANGELOG.md file according to the [Keep A Changelog](https://keepachangelog.com/) standards.

The idea and initial implementation comes [from @eMarek](https://github.com/release-it/release-it/issues/662).

```
npm install --save-dev @release-it/keep-a-changelog
```

In [release-it](https://github.com/release-it/release-it) config:

```json
"plugins": {
  "@release-it/keep-a-changelog": {
    "filename": "CHANGELOG.md"
  }
}
```

## Options

| option         | default value  | description                                                                                                                                      | command line option                                                                                                 |
| -------------- | -------------- | ------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------- |
| filename       | `CHANGELOG.md` | File with changelogs.                                                                                                                            | `--plugins.@release-it/keep-a-changelog.filename=OTHER.md`                                                            |
| strictLatest   | `true`         | Entry of latest version must be present in order to get correct changelog. Set this option to `false` if you expect latest version without logs. | `--plugins.@release-it/keep-a-changelog.strictLatest` or `--no-plugins.@release-it/keep-a-changelog.strictLatest`    |
| addUnreleased  | `false`        | It leaves "Unreleased" title row if set to `true`.                                                                                               | `--plugins.@release-it/keep-a-changelog.addUnreleased` or `--no-plugins.@release-it/keep-a-changelog.addUnreleased`  |
| keepUnreleased | `false`        | It leaves "Unreleased" title row unchanged if set to `true`.                                                                                     | `--plugins.@release-it/keep-a-changelog.keepUnreleased` or `--no-plugins.@release-it/keep-a-changelog.keepUnreleased`|
| addVersionUrl  | `false`        | Links the version to the according changeset.                                                                                                    | `--plugins.@release-it/keep-a-changelog.addVersionUrl` or `--no-plugins.@release-it/keep-a-changelog.addVersionUrl`  |
