
# How to run this 3scale CI/CD example:

After creating an OpenShift namespace with deploying Jenkins in it, copy your local 3scale toolbox file: 3scalerc.yaml as a secret: 

```sh
oc create secret generic 3scale-toolbox --from-file=$HOME/.3scalerc.yaml
```
Create a new app, notice these hints:
  - API_BASE_SYSTEM_NAME: must be an unique identified in 3scale, it doesnt't be repeated even you delete the API in 3scale.
  - DEV_STAGING_PUBLIC_BASE_URL,DEV_PRODUCTION_PUBLIC_BASE_URL...: these URLs should be created upfront running the pipeline.
  - TARGET_INSTANCE_DEV, TARGET_INSTANCE_TEST: 3scale remote name which identifies the environment.
  - DEV_DEVELOPER_ACCOUNT_ID: 3scale account id which will create the test application (usually john identifier).

```sh
oc new-app -f cicd-demo-pipeline.yaml -p API_BASE_SYSTEM_NAME=stockAPI3 -p DEV_STAGING_PUBLIC_BASE_URL=https://stock-dev-staging.apps.my-cluster.ocp4.openshift.es -p DEV_PRODUCTION_PUBLIC_BASE_URL=https://stock-dev-production.apps.my-cluster.ocp4.openshift.es -p TEST_STAGING_PUBLIC_BASE_URL=https://stock-test-staging.apps.my-cluster.ocp4.openshift.es -p TEST_PRODUCTION_PUBLIC_BASE_URL=https://stock-test-production.apps.my-cluster.ocp4.openshift.es -p OPENAPI_SPECIFICATION_FILE=stock-spec-v1.0.json -p TARGET_INSTANCE_DEV=bispoc -p TARGET_INSTANCE_TEST=testenv -p DEV_DEVELOPER_ACCOUNT_ID=8
```
