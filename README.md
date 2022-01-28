[![Create Release][release-badge]][release-url]
[![Import Labels][import-labels-badge]][import-labels-url]
[![Sync Labels][sync-labels-badge]][sync-labels-url]
[![PR AutoLabeler][autolabeler-badge]][autolabeler-url]
[![Assigner][assigner-badge]][assigner-url]


Composite Github Action the simply the setup steps of our workflow jobs by combining
steps into a single [Composite Action][Composite Action]

[Composite actions do not currently support the `if` conditional][if]

[Composite Action]: https://docs.github.com/en/actions/creating-actions/creating-a-composite-action
[if]: https://github.com/actions/runner/issues/646#issuecomment-901358313

### Inputs
#### `nodeVersion`
The version of node to install
Default: 12

#### `npmToken`
Token to be used for installing private NPM packages

#### `vulnerabilityToken`
Token used for vulnerability checking
If not set, vulnerabilities are not checked

#### `vulnerabilityLevel`
Override CRITICAL level for failure on vulnerability check.  HIGH, MODERATE or LOW.
Default: `Critical`

#### `vulnerabilityFail`
Override failure on found vulnerabilities
Default: `true`.  Set to `false` to not fail CI if Critical vulnerabilities found

#### `ref`
Checkout ref
Default: ''

#### `fetch-depth`
Checkout fetch-depth
Default: 1

#### `path`
Relative path under $GITHUB_WORKSPACE to place the repository
Default: ''

#### `clean`
Whether to execute `git clean -ffdx && git reset --hard HEAD` before fetching
Default: true

#### `setup_ruby`
Whether or not to execute ruby setup action
Default: false

#### `ruby_version`
Desired version of Ruby
Default (if enabled): 2.7

#### `ruby_bundler_cache`
Enable Ruby bundler-cache
Default (if enabled): false

### Example usage
```yaml
      - name: Setup job
        uses: CumulusDS/workflow-setup-action@master
        with:
          nodeVersion: 12
          npmToken: ${{ secrets.NODE_AUTH_TOKEN }}
          fetch-depth: 0
          vulnerabilityToken: ${{ secrets.SOME_TOKEN }
```


[release-badge]: https://github.com/CumulusDS/workflow-setup-action/actions/workflows/release.yml/badge.svg
[release-url]: https://github.com/CumulusDS/workflow-setup-action/actions/workflows/release.yml
[import-labels-badge]: https://github.com/CumulusDS/workflow-setup-action/actions/workflows/labels_import.yml/badge.svg
[import-labels-url]: https://github.com/CumulusDS/workflow-setup-action/actions/workflows/labels_import.yml
[sync-labels-badge]: https://github.com/CumulusDS/workflow-setup-action/actions/workflows/labels_sync.yml/badge.svg
[sync-labels-url]: https://github.com/CumulusDS/workflow-setup-action/actions/workflows/labels_sync.yml
[autolabeler-badge]: https://github.com/CumulusDS/workflow-setup-action/actions/workflows/autolabeler.yml/badge.svg
[autolabeler-url]: https://github.com/CumulusDS/workflow-setup-action/actions/workflows/autolabeler.yml
[assigner-badge]: https://github.com/CumulusDS/workflow-setup-action/actions/workflows/assign.yml/badge.svg
[assigner-url]: https://github.com/CumulusDS/workflow-setup-action/actions/workflows/assign.yml
