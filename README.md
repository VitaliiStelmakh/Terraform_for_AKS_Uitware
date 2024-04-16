# Azure Kubernetes Service (AKS) Configuration with Terraform

This repository contains Terraform configurations for setting up an Azure Kubernetes Service (AKS) cluster along with an Azure Container Registry (ACR) within a designated resource group. It provides scalable Kubernetes services integrated with a private Docker container registry managed by Azure.

## Prerequisites

- **Terraform**: Version 1.3.0 or higher must be installed.
- **Azure CLI**: You should be logged into the Azure CLI and have appropriate permissions.
- **Azure Subscription**: An active subscription is required.

## Directory Structure

├── main.tf # Main Terraform configuration file.
├── provider.tf # Provider and backend configuration.
├── variables.tf # Variables declaration file.


## Configuration Details

### `main.tf`

This file defines the necessary Azure resources for the AKS cluster:

- **Resource Group**: Contains all related resources for the service.
- **ACR (Azure Container Registry)**: Manages Docker container images.
- **AKS (Azure Kubernetes Service)**: Manages the Kubernetes cluster setup.

### `provider.tf`

Sets up the Terraform provider and specifies the backend for remote state management:

- **Required Terraform Version**
- **AzureRM Provider**: Configuration including version and source.
- **Backend**: Azure storage configuration for Terraform state files.

### `variables.tf`

Includes all the variable declarations used across the configuration, allowing for customization of the resources.

## Usage

To deploy the AKS cluster:

1. **Initialize the Terraform environment**:
   ```bash
   terraform init

