# OpenShift Pipelines  / Tekton CICD project setup

## Description

This repository will create all the requires elements needed to use [Openshift Pipeline](https://www.openshift.com/learn/topics/ci-cd)) using [Tekton](https://tekton.dev/).


## Prerequisites

* Any Openshift cluster 4.3+ or CodeReady Container base on OCP 4.3+
* The Openshidt Pipeline Operator install and running inside the container.
* Openshift CLI install and connected to your cluster
* The [Tekton cli](https://github.com/tektoncd/cli) install

## Notes

This project uses [Kustomize] (https://kustomize.io/).

## Creating/using the project 
Connect as the cluster admin to run the following command to set up the project.


1. Create a cicd namespace that contains the different elements and configuration needed to run the pipelines, achieve this by using the f
following command:
* > $ oc apply -k infra 

2. Create the required service acount to be able to pull images from the cicd project, achieve this using the following command:
* > $ oc apply -k serviceAccounts

3. Create the different pipeline elements ( task, resources, pipeline, volume ...)  with the given command.
* > $ oc apply -k tekton



## Tekton
Usefull Tekton command that you can run on the project one running

Command | Description |
--------|-------------|
tkn taks ls | List the differents task in a projects
tkn resource ls | Lit the differents resources in the projects
tkn pipeline ls | List the differents pipeline in the projects and their status
tkn pipelie describe [PIPELINE NAME] | Give information on a given pipeline
tkn pipelinerun ls | List the different pipelinerun and their satus
