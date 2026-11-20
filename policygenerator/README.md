This directory contains a policy generator used to deploy OpenShift AI on an existing OpenShift cluster.

The current version deploys OpenShift AI with support with basic inference via KServe using a single deployment.

## Requirements

The pre-requisites for OpenShift AI deployment are detailed in the [official documentation](https://docs.redhat.com/en/documentation/red_hat_openshift_ai_self-managed/3.5/html/installing_and_uninstalling_openshift_ai_self-managed/installing-and-deploying-openshift-ai_install#component_requirements). Make sure all required operators are installed before deploying OpenShift AI.

## Disconnected environments

When deploying on a disconnected environment, you will need to mirror the operator images for OpenShift AI, as well as some additional images required during runtime. Use the [ImageSetConfiguration file](https://github.com/red-hat-data-services/rhoai-disconnected-install-helper/blob/main/rhoai-3.5.3-imagesetconfig.yaml) from the disconnected installer helper repository as a reference to build the mirroring configuration for your environment.

(add info about Kueue and JobSet operator)

## Usage

To deploy OpenShift AI following this guide, do the following:

(include details here)

Two different `PolicyGenerator` resources are provided, depending on the required use case:

- `rhoai-inferencing.yaml` for basic inferencing using KServe.
- `rhoai-workbench-pipelines.yaml` for pipelines or workbenches usage.
