# Cakely API Ops
> EKS cluster, ECR repository, and Flux management for `cakely/api`

## About

This repository contains a GitHub Actions workflow ([`setup.yaml`](.github/workflows/setup.yml)) that creates an EKS cluster and ECR repository upon `workflow_dispatch`. Self hosted runner "ECR Create" is used in this workflow to communicate to a pre-configured instance of Vault using an AppRole with the `ecr-create` policy. See [`cakely/vault-runner-setup`](https://github.com/cakely/vault-runner-setup) for details.

The EKS cluster infrastructure definition is in [`cluster.yaml`](cluster.yaml).

## Context

This repo is the technical complement to a webinar entitled Secure GitOps Workflows with GitHub Actions and HashiCorp Vault, delivered on August 25<sup>th</sup> 2020, which can be viewed online [**here**](https://www.hashicorp.com/resources/secure-gitops-workflows-with-github-actions-and-hashicorp-vault).

The work here represents the final state of the demos and workflows that were presented as a part of that webinar. It is recommended to view this repo in the context of that webinar.

You are here 🍰:
* [`cakely/api`](https://github.com/cakely/api)
* **🍰 [`cakely/api-ops`](https://github.com/cakely/api-ops) 🍰 - AWS EKS cluster for cakely/api**
* [`cakely/vault-runner-setup`](https://github.com/cakely/vault-runner-setup)

For more goodness related to cake, GitHub, and Terraform, kindly view the previous webinar entitled [Unlocking the Cloud Operating Model with GitHub Actions](https://www.hashicorp.com/resources/unlocking-the-cloud-operating-model-with-github-actions/).

## Pre-requisites

- AWS account
- [HashiCorp Vault](https://vaultproject.io/) downloaded and configured according to guidance in [`cakely/vault-runner-setup`](https://github.com/cakely/vault-runner-setup)

## License

[MIT](LICENSE)

## Credits

* [eksctl GitOps Quickstart](https://eksctl.io/gitops-quickstart/) tutorial
