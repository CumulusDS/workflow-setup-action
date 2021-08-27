[![Create Release][release-badge]][release-url]
[![Import Labels][import-labels-badge]][import-labels-url]
[![Sync Labels][sync-labels-badge]][sync-labels-url]
[![PR AutoLabeler][autolabeler-badge]][autolabeler-url]
[![Assigner][assigner-badge]][assigner-url]

Description

### Inputs
#### `nodeVersion`
The version of node to install

#### `npmToken`
Token to be used for installing private NPM packages

### Example usage
```yaml
      - name: Setup job
        uses: CumulusDS/workflow-setup-action@master
        with:
          nodeVersion: 12
          npmToken: ${{ secrets.NODE_AUTH_TOKEN }}
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
