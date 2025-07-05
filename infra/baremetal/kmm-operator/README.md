# kmm-operator

## Description
kernel module management operator package

## Usage

### Fetch the package
`kpt pkg get REPO_URI[.git]/PKG_PATH[@VERSION] kmm-operator`
Details: https://kpt.dev/reference/cli/pkg/get/

### View package content
`kpt pkg tree kmm-operator`
Details: https://kpt.dev/reference/cli/pkg/tree/

### Apply the package
```
kpt live init kmm-operator
kpt live apply kmm-operator --reconcile-timeout=2m --output=table
```
Details: https://kpt.dev/reference/cli/live/

### References
To get the latest tags for the below container images, refer the release section at https://github.com/kubernetes-sigs/kernel-module-management/releases
- gcr.io/k8s-staging-kmm/kernel-module-management-webhook-server
- gcr.io/k8s-staging-kmm/kernel-module-management-operator
- gcr.io/k8s-staging-kmm/kernel-module-management-signimage
- gcr.io/k8s-staging-kmm/kernel-module-management-worker

To get the latest tag for the below container image, refer the release section at https://github.com/GoogleContainerTools/kaniko/releases
- gcr.io/kaniko-project/executor