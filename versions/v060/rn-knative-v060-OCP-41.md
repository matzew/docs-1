<!--please copy and paste this template into your vXXX folder for the current release and modify there. Do NOT edit this template)-->

![Release Notes](https://github.com/openshift-knative/docs/blob/master/images/release-notes-banner.png)

# Knative v0.6.0 on OpenShift  

**Release Date:** 17th June 2019

This document describes the latest changes, enhancements, bug fixes and known issues for Knative on OpenShift. It incorporates changes to Knative’s Serving and Eventing components, and may be adopted for consistency and compatibility on OpenShift.

>**NOTE:** The functionality introduced by Knative on an OpenShift cluster is preview only. Red Hat support is not provided, and this release should not be used in a production environment. Features are still under development and are not fully supported under Red Hat Subscription Level Agreements.

>**NOTE:** The features outlined in this document reflect the selected contributions of the Red Hat team. For complete details of Knative releases, refer to the **Resources and Links** section of this document.
-------------

## General Information

### Release components
The following components have been tested on the OpenShift 4.1 cluster in this release:


|Component|Version|
|---------|-------|
| Knative Serving | 0.6.0 |
| Knative Eventing | 0.6.0 |

----------------

## What's New
### Serving
- **Knative Serving Operator now available.** An Operator that installs the Knative Serving component on OpenShift 4.1 is now available through the embedded OperatorHub in the  OpenShift console. This replaces the previous installation script available in Knative on OpenShift v0.5.0. ([#139](https://github.com/openshift/knative-serving/pull/139), [#405](https://github.com/operator-framework/community-operators/pull/405))

- **Operator automatically installs the Maistra Operator and ControlPlane.** The operator will attempt to discover Istio. If not found, it will install the Maistra Operator and a minimal Maistra ControlPlane. ([#12](https://github.com/openshift-knative/knative-serving-operator/pull/12))

- **Operator automatically installs the Knative OpenShift Ingress Operator.** After installing Knative Serving, the operator now ensures that the Knative OpenShift Ingress Operator is deployed so that OpenShift Routes get created automatically for every Knative Route. ([#14](https://github.com/openshift-knative/knative-serving-operator/pull/14))

- **Knative Build component has been removed.** The Knative Build component is likely to be discontinued in the Knative upstream project, so it will no longer be present in Knative on OpenShift releases from v0.6.0 onwards.

### Eventing

- **Knative Eventing Operator now available.** An Operator that installs the Knative Eventing component on OpenShift 4.1 is now available through the embedded OperatorHub in the  OpenShift console. This replaces the previous installation script available in Knative on OpenShift v0.5.0. ([#407](https://github.com/operator-framework/community-operators/pull/407))

-------------

## Fixed Issues

### Serving
- See the [Knative core Serving release notes](https://github.com/knative/serving/releases).

### Eventing
- See the [Knative core Eventing release notes](https://github.com/knative/eventing/releases).

-------------

## Known Issues
- **Camel and Kafka optional eventing sources have been removed.** The Camel and Kafka sources that were previously available by installing the Knative Eventing Operator have been removed. These will become standalone Knative Kafka and Knative Camel Operators in a future release of Knative on OpenShift. See *Resources and Links* below for more information. ([#34](https://github.com/openshift-knative/knative-eventing-operator/pull/34), [#1](https://github.com/openshift-knative/knative-kafka-operator/pull/1))

-------------

## Resources and Links

- https://github.com/knative/docs/releases
- https://github.com/knative/serving/releases
- https://github.com/knative/eventing/releases
- https://github.com/tektoncd/pipeline/releases
