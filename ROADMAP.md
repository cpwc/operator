# Roadmap

## Towards seamless upgrades

Support seamless upgrades from a version to another. This mean being
able to update some object pre-reconcile (upgrade) if need be (in case
of deprecated fields, …).

## Driving adoption

- Add more docs, and have it publish as part of the tekton.dev/docs
  website.
- Highlight the benefit of using the operator, and mainly what pain it
  solves

An acceptance criteria for this would be to use the operator in our
own CI (aka dogfooding).

## Pipeline

### Support feature flags

Support setting feature flags, such as:

- Affinity Assistant
- Custom Tasks
- API feature flag (stable, …)

### Support configuration options

Support configuration options of `tektoncd/pipeline`, such as:

- Support managing the content of pipeline's configmap (default, …)
- Enabling/configuring High availability

## Triggers

- Ship and configure custom interceptors (built-in, from experimental,
  …)
- Multi-tenant eventlistener support

## New Component integration

As of today, the operator is capable of installing Pipeline, Triggers
and the dasbhoard. We may want to support shipping more components

### Components

- results
- chains
- self-hosted hub

### Experimental projects

- custom tasks
- other projects

## Add Catalog ClusterTask to all targets

Today, we are shipping ClusterTask only for the OpenShift target. We
should aim towards shipping this for all targets (k8s, …)

## More targets

We are currently targeting and releasing only two target:
- Vanilla k8s
- OpenShift

We should aim to support more, starting with GKE. GKE is a easy target
as we could use this in dogfooding. An idea of what could be specific
for GKE is around the ingress configuration, …

## Releases

- Automated relases
- Automated publication on OperatorHub
- More often (monthly)
- Better management of the payloads (releases yamls)
  Today, we do some manual changes in order to release, we should aim
  towards taking the upstream releases yamls as is and *fix* anything
  programmatically (if need be).

## Metrics

Enable metrics on the operator, to be able to gather information on
the health of managed components from the operator.
