# Terraform AWS EKS Karpenter with OpenTofu

This repository contains an example of how to set up an AWS EKS cluster with Karpenter using Terraform. This example is designed to work with OpenTofu for managing your infrastructure as code.

## Table of Contents
- [Prerequisites](#prerequisites)
- [Installation](#installation)
- [Usage](#usage)
- [Passing Variables](#passing-variables)
- [Contributing](#contributing)
- [License](#license)

## Prerequisites

Before you begin, ensure you have the following installed:

- [OpenTofu](https://github.com/OpenTofu/OpenTofu) - version 1.0 or higher
- [AWS CLI](https://aws.amazon.com/cli/) - configured with your AWS credentials

## Installation

Follow these steps to get started with the project:

1. **Clone this repository to your local machine**:

    ```bash
    git clone https://github.com/mohab58977/terraform-aws-eks-karpenter.git
    cd terraform-aws-eks-karpenter
    ```

2. **Configure your AWS credentials**:

    Ensure that your AWS credentials are set up for OpenTofu:

    ```bash
    aws configure
    ```

3. **Initialize OpenTofu**:

    Run the following command to initialize the OpenTofu configuration:

    ```bash
    opentofu init
    ```

    This will download the required Terraform modules and set up the backend for managing your AWS resources.

## Usage

Once the repository is cloned, and dependencies are initialized, follow the steps below to use OpenTofu for deploying the AWS EKS cluster with Karpenter.

### Step 1: Set up the `clustername` variable

You can specify the `clustername` variable:

####  Using `terraform.tfvars`

Create a `terraform.tfvars` file in your directory
```
opentofu plan -var "clustername=your-cluster-name"

opentofu apply -var "clustername=your-cluster-name"
```
## AFTER That ArgoCd will be available on your cluster You can deploy prometheus,alermanager,grafana,loki,thanos,promtail via Helmcharts
