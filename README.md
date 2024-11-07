# OpenShift Virtualization - CentOS Stream 9 VM Deployment using Ansible

This project demonstrates a proof of concept (PoC) for deploying a CentOS Stream 9 virtual machine (VM) on OpenShift Virtualization using GitLab CI/CD and Ansible. The deployment utilizes the certified Kubernetes collection for Ansible from Ansible Galaxy.

---

## Prerequisites
Ensure the following prerequisites are met before running the project:

- OpenShift Platform 4.14 or higher
- OpenShift Virtualization
- OpenShift Storage Provider
- GitLab / GitLab Runner
- Ansible
- Kubernetes Collection from Ansible Galaxy

## Security Considerations

> **Warning**: The `install-httpd-centos-vm.yml.j2` template contains VM credentials in plain text. This setup is intended for a proof of concept and is not secure for production environments. Use a secrets management solution to handle sensitive information securely.

## Usage Instructions

1. **Set Up GitLab Variables**:
   - Configure `OPENSHIFT_SERVER` and `OPENSHIFT_TOKEN` as variables in your GitLab project settings to authenticate with OpenShift.

2. **Run the CI/CD Pipeline**:
   - When the pipeline is triggered, it will execute the `CreateVM` job to deploy the CentOS Stream 9 VM and install HTTPD.

3. **Verify the Deployment**:
   - Check the OpenShift Virtualization console or use `oc` commands to ensure the VM is created and HTTPD is running.

