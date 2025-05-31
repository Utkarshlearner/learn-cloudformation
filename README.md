# Learn CloudFormation 📘

A beginner-friendly repository that walks you through AWS CloudFormation using modular, real-world YAML examples. Understand core concepts like Parameters, Mappings, Conditions, Resources, Outputs, and more.

---

## 🚀 What is AWS CloudFormation?

AWS CloudFormation is an **Infrastructure as Code (IaC)** service that enables you to define and provision AWS infrastructure using YAML or JSON templates. It allows you to manage resources like EC2, S3, IAM, VPC, and more in a repeatable and automated way.

---

## 🎯 Benefits of Using CloudFormation

- ✅ **Automation:** Deploy and manage resources without manual steps.
- 🔄 **Repeatability:** Use the same template to spin up identical environments.
- 📝 **Version Control:** Templates can be tracked in Git.
- 🧩 **Modularity:** Supports nested stacks and reusable components.
- 🔍 **Change Tracking:** Built-in change sets and rollback options.
- ☁️ **Native to AWS:** Full integration with AWS services and management tools.

---

## 📐 CloudFormation Template Structure

| Section                    | Purpose                                                                 |
|----------------------------|-------------------------------------------------------------------------|
| `AWSTemplateFormatVersion`| (Optional) Version of the template format (e.g., '2010-09-09')           |
| `Description`              | Description of the template's purpose                                   |
| `Parameters`               | Input values to customize template behavior                             |
| `Mappings`                 | Key-value lookups based on region or environment                        |
| `Conditions`               | Define logic to conditionally create resources                          |
| `Resources`                | **Required** section that defines the AWS resources to be created       |
| `Outputs`                  | Export useful values (e.g., instance IDs, bucket names)                 |

---

## 📁 What's Inside

This repo includes modular examples for:

- ✅ AWSTemplateFormatVersion
- ✅ Description
- ✅ Parameters
- ✅ Mappings
- ✅ Conditions
- ✅ Resources
- ✅ Outputs

Each template is standalone and deployable using the AWS CLI or Console.

---

## 📌 How to Deploy

### ✅ 1. Validate Template
```
aws cloudformation validate-template \
  --template-body file://your-template.yaml
```

### 🚀 2. Deploy the Stack
```
aws cloudformation create-stack \
  --template-file your-template.yaml \
  --stack-name YourStackName \
  --capabilities CAPABILITY_NAMED_IAM
```

### 🧹 4. Delete the Stack
```
aws cloudformation delete-stack \
  --stack-name YourStackName
```


## 🔐 What is `--capabilities`?

The `--capabilities` flag is required when your CloudFormation template **creates or modifies IAM resources**, such as roles or policies.

### ✅ Supported Types:

| Capability               | Description                                                             |
|--------------------------|-------------------------------------------------------------------------|
| `CAPABILITY_IAM`         | Acknowledge that the template creates/modifies IAM users, roles, or policies |
| `CAPABILITY_NAMED_IAM`   | Same as above, but allows explicitly naming IAM resources               |
| `CAPABILITY_AUTO_EXPAND` | Required when using AWS CloudFormation macros                           |

👉 Most common usage:
```
--capabilities CAPABILITY_NAMED_IAM
```


## 🧑‍💻 About Me

Utkarsh Rastogi — Cloud Specialist | AWS Community Builder  
📍 Based in India  

🌐 Blog: [https://awslearner.hashnode.dev](https://awslearner.hashnode.dev)  

🚀 Passionate about building serverless, AI-powered, cloud-native solutions.

---

## 📬 Contributions

Feel free to open issues or submit PRs if you'd like to contribute additional examples!