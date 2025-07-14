# kpt

## Description
Package for creating and installing kernel modules from source and pushing the kernel module as a container to a registry.
NOTE: The create-setters.yaml file is used to parameterize the field values by adding setter comments by invoking the
`kpt fn eval --image gcr.io/kpt-fn/create-setters:v0.1.0 --fn-config ./create-setters.yaml`.
The command `kpt fn eval -i list-setters:v0.1.0` can be used to list the setter fields.
The `apply-setters.yaml` shows an example of providing values for setter fields for the gtp5g kernel module.

## Usage

### Fetch the package
`kpt pkg get REPO_URI[.git]/PKG_PATH[@VERSION] kpt`
Details: https://kpt.dev/reference/cli/pkg/get/

### View package content
`kpt pkg tree kpt`
Details: https://kpt.dev/reference/cli/pkg/tree/

### Apply the package
```
kpt live init kpt
kpt live apply kpt --reconcile-timeout=2m --output=table
```
Details: https://kpt.dev/reference/cli/live/