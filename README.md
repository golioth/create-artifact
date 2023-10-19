> :warning: This project is considered experimental and is not recommended for production use. Functionality may break at any time.

# create-artifact
Create an Artifact in the Golioth Cloud with GitHub Actions.

# ✨ Quickstart

To create an artifact using the latest version of the Golioth CLI:

```yaml
- name: Checkout
  uses: actions/checkout@v4

- name: Setup goliothctl
  uses: golioth/setup-goliothctl@main
  with:
    apiKey: ${{ secrets.APIKEY }}
    projectId: ${{ secrets.PROJECTID }}

- name: Create artifact
  uses: golioth/create-artifact@main
  with:
    file: app.bin
    artifactVersion: 1.0.0
```

`file` & `artifactVersion` are required inputs. `setup-goliothctl` requires a Golioth API Key and Project ID. See [golioth/setup-goliothctl](https://github.com/golioth/setup-goliothctl) for more details.

# Inputs

| Parameter | Description | Required |
| --- | --- | --- |
| file | File to use for artifact. | Yes |
| artifactVersion | Artifact semantic version. | Yes |