# Rècupè - Automated Backup and Disaster Recovery Solution

This project implements an automated backup and disaster recovery solution for a critical application using Bacula, Velero, AWS, and Terraform.

## Components

- Bacula for file-level backups
- Velero for Kubernetes cluster backups
- Terraform scripts for DR infrastructure
- Automated testing of backup integrity and recovery processes

## Prerequisites

- Docker
- Minikube
- kubectl
- Terraform
- Bacula
- Velero

- ## Setup

1. Clone this repository:
git clone https://github.com/ambekadeshmukh/backup-dr-solution.git
cd backup-dr-solution

3. Set up the development environment:
Follow the instructions in `docs/dev-environment-setup.md`.

4. Deploy the sample application:
Follow the instructions in `docs/sample-app-deployment.md`.

5. Set up Bacula:
Follow the instructions in `docs/bacula-setup.md`.

6. Set up Velero:
Follow the instructions in `docs/velero-setup.md`.

7. Apply Terraform scripts:
Follow the instructions in `docs/terraform-usage.md`.

8. Run automated tests:
./test_backup_recovery.sh

## Usage

- To perform a manual Bacula backup:
sudo bconsole
run job=BackupJob


- To create a Velero backup:
velero backup create my-backup --include-namespaces=note-taking-app
  
- To restore from a Velero backup:
velero restore create --from-backup my-backup

## Contributing

Please read `CONTRIBUTING.md` for details on our code of conduct and the process for submitting pull requests.

## License

This project is licensed under the MIT License - see the `LICENSE.md` file for details.

