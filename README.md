# azure-philly-aks

Examples for the Azure Meetups about AKS Fundamentals

## Introduction

This is a set of files for demonstrating the internals of AKS.  The files assume that you have already provisioned at least two AKS clusters, one with the Azure AD authentication configured and another with Virtual Kubelet, VMSS, Node Pools, and Availability Zones enabled.  Consult the Microsoft Docs on how to create each cluster.  The presentation is roughly broken up into four areas:

 - Identity
 - Compute
 - Storage
 - Network

Each area has files to create resources in the AKS cluster that can be investigated via the portal.

## Identity

The `azure-ad-authentication.yaml` file will create the necessary `ClusterRole` binding for an Azure AD user.  Replace the last entry with either the user's `UserPrincipalName` or `ObjectId`.  In `commands-you-wont-remember.txt` (by you I mean me) are the commands to check out the service principal that is created when an AKS cluster is provisioned.  You can also see the Azure AD config section of the cluster and perform the login for the cluster using Azure AD config.


