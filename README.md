# Google Cloud Deployment Manager Guide

This guide provides an overview of using the Google Cloud Deployment Manager with the `gcloud` command-line tool.

## Setting Your Project

Before you start using Deployment Manager, make sure you're working with the correct project:

```sh
gcloud config set project YOUR_PROJECT_ID
```

Replace `YOUR_PROJECT_ID` with your actual Google Cloud project ID.

## Creating a New Deployment

To create a new deployment from your YAML or Python template file:

```sh
gcloud deployment-manager deployments create DEPLOYMENT_NAME --config CONFIG_FILE
```

- `DEPLOYMENT_NAME` is the name you want to give your deployment.
- `CONFIG_FILE` is the path to your configuration file.

## Viewing Existing Deployments

To list all your current deployments:

```sh
gcloud deployment-manager deployments list
```

## Getting Information About a Specific Deployment

To describe a specific deployment:

```sh
gcloud deployment-manager deployments describe DEPLOYMENT_NAME
```

## Updating an Existing Deployment

When you need to update your resources:

```sh
gcloud deployment-manager deployments update DEPLOYMENT_NAME --config CONFIG_FILE
```

Use `--preview` to see what changes would occur without applying them.

## Deleting a Deployment

To delete a deployment and all associated resources:

```sh
gcloud deployment-manager deployments delete DEPLOYMENT_NAME
```

## Learn More

For more detailed instructions and best practices, check out my [blog post on Google Cloud Deployment Manager](https://dev.to/gdgcloudlahore_org).
