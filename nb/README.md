# nb

A quick reference for managing notes with `nb`.

## Installation

macOS (Homebrew)

```bash
brew install nb
```

Linux

```bash
curl -L https://raw.githubusercontent.com/xwmx/nb/master/install.sh | bash
```

Verify installation

```bash
nb --version
```

## Notebooks

### List notebooks

```bash
nb notebooks
```

### Create a notebook

```bash
nb notebooks add rbkr
```

### Switch to a notebook

```bash
nb use rbkr
```

### Show current notebook

```bash
nb status
```

## Creating Notes

### Create a new note

```bash
nb add
```

This opens your default editor.

### Create a titled note

```bash
nb add -t "Architecture"
```

### Create a note with content

```bash
nb add \
  -t "AWS Accounts" \
  -c "Production Account: 123456789012"
```

### Create a Markdown note

```bash
nb add architecture.md
```

## Listing Notes

List all notes

```bash
nb ls
```

Long listing

```bash
nb list
```

## Viewing Notes

View by ID

```bash
nb show 12
```

View by title

```bash
nb show Architecture
```

## Editing Notes

Edit by ID

```bash
nb edit 12
```

Edit by title

```bash
nb edit Architecture
```

## Deleting Notes

Delete by ID

```bash
nb delete 12
```

Delete by title

```bash
nb delete Architecture
```

## Searching

Search all notes

```bash
nb search kafka
```

Search for an AWS account

```bash
nb search 123456789012
```

Search for production

```bash
nb search production
```

Search multiple words

```bash
nb search keycloak prod
```

## Tags

Create a tagged note

```bash
nb add \
  -t "Kafka" \
  --tags kafka,production
```

Search by tag

```bash
nb search production
```

## Attach Files

Add a PDF

```bash
nb add architecture.pdf
```

Add an image

```bash
nb add diagram.png
```

## Import Existing Markdown

```bash
nb import notes.md
```

## Export

Export a note

```bash
nb export 5
```

## Git Integration

Initialize Git

```bash
cd ~/.nb

git init
```

Commit changes

```bash
git add .
git commit -m "Updated architecture notes"
```

Push to GitHub

```bash
git push
```

## Useful Examples

### Store an AWS account

Title

```
AWS Accounts
```

Content

```text
Production
-----------
Account ID: 123456789012

QA
---
Account ID: 987654321012
```

### Store environment information

Title

```
Production Environment
```

Content

```text
AWS Account
123456789012

Region
af-south-1

VPC
10.0.0.0/16

EKS
prod-cluster

Jumpbox
10.0.5.12
```

### Store banking information

Title

```
Customer Banking
```

Content

```text
Customer: ABC Ltd

Bank: ZooBank

Branch: 012345

Account: 123456789
```

### Daily Workflow

```bash
# Switch notebook
nb use rbkr

# Add a note
nb add -t "Kafka"

# Search
nb search rebalance

# Edit
nb edit Kafka

# View
nb show Kafka

# List notes
nb ls
```

### Keyboard-Friendly Workflow

```bash
nb use rbkr

nb add -t "Terraform"

nb add -t "Kafka"

nb add -t "Keycloak"

nb search kafka

nb edit Kafka

nb show Kafka
```

### Help

Show help

```bash
nb help
```

Help for a command

```bash
nb help add
```

### Suggested Notebook Structure

```
rbkr
├── Architecture
├── AWS Accounts
├── Terraform
├── Kubernetes
├── Kafka
├── PostgreSQL
├── Keycloak
├── Banking
├── Runbooks
└── Useful Commands
```

